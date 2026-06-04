# RollingGo Flight MCP Server

[**中文**](README.中文.md) | [**English**](#english-version)

[![Version](https://img.shields.io/badge/Version-1.0.0-blue.svg)](https://github.com/RollingGo-AI/rollinggo-flight-mcp/releases)
[![ModelScope](https://img.shields.io/badge/ModelScope-Rank%237-brightgreen.svg)](https://modelscope.cn/)
[![Calls](https://img.shields.io/badge/Calls-847.3k-orange.svg)](https://github.com/RollingGo-AI/rollinggo-flight-mcp)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)

🏠 [Homepage](https://global.rollinggo.store/) · 🚀 [Quick Start](#quick-start) · 🔧 [Tools](#tools) · 💬 [Support](#support)

## Overview

RollingGo Flight Search MCP Server. Provides airport search and flight query capabilities for AI Agents and MCP clients via FastMCP.

## Tools

Currently exposes 2 tools:

- `searchAirports` — Search airport/city info by English city name, English airport name, or IATA code.
- `searchFlights` — Query flight options by date, route, passenger count, and cabin class.

`checkFlightSeats` and `checkBaggageAllowance` are not yet implemented.

## Installation

```bash
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
```

## Configuration

Default upstream API address:

```text
https://mcp.rollinggo.cn
```

Override via environment variable:

```bash
set ROLLINGGO_API_BASE_URL=https://mcp.rollinggo.cn
```

The HTTP server reads the API Key from request headers. Pass one of the following:

```http
Authorization: Bearer <your_api_key>
```

or:

```http
X-Secret-Key: <your_api_key>
```

## 🚀 Quick Start

```bash
python server.py
```

Default endpoint:

```text
http://127.0.0.1:8000/mcp
```

## MCP Client Configuration

```json
{
  "mcpServers": {
    "RollingGo-Flight-MCP": {
      "url": "http://127.0.0.1:8000/mcp",
      "type": "streamable_http",
      "headers": {
        "Authorization": "Bearer YOUR_API_KEY"
      }
    }
  }
}
```

## searchAirports

For the `keyword` parameter, prefer English city names, English airport names, or IATA codes (e.g. `Hangzhou`, `Chengdu`, `HGH`, `CTU`). Chinese city names are not recommended as primary input.

Input:

```json
{
  "keyword": "Hangzhou"
}
```

Upstream endpoint:

```text
POST /api/mcp/airportsearch
```

## searchFlights

Input:

```json
{
  "adultNumber": 1,
  "childNumber": 0,
  "cabinGrade": "ECONOMY",
  "fromCity": "HGH",
  "toCity": "CTU",
  "fromDate": "2026-05-01",
  "tripType": "ONE_WAY"
}
```

Upstream endpoint:

```text
POST /api/mcp/flightsearch
```

Field descriptions follow `rollinggo-readme/FLIGHT-README.md`.

---

## 💬 Support

Join our WeChat technical support group for assistance. Don't worry about any issues during integration – our core development team will be online throughout to help you with environment configuration, API debugging, and completing your first successful flight search query.

You'll get:
- Integration configuration guidance
- API / MCP call troubleshooting
- Flight search, pricing, and inventory query workflow support
- Integration suggestions tailored to your use case

![Support WeChat](https://raw.githubusercontent.com/RollingGo-AI/rollinggo-hotel-mcp/main/support-wehcat%20group.png)
