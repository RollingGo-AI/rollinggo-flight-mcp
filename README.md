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

- Powered by the world’s 3rd largest travel B2B firm with global reach: partnered with over 500 airlines, covering 200+ countries and regions and more than 1,000 destinations worldwide.
- Diverse flight options: millions of flight combinations to cater to varied travel needs, supporting direct flights, connecting flights and other itinerary types.
- Competitive pricing: aggregated premium global airfare resources to deliver real-time fares with market advantages.
- Reliable customer support: professional team providing round-the-clock 7×24 customer service.

## Who is this for?
Individual users requiring flight price tracking, hotel search and hotel price comparison
Individuals and development teams building AI Agents
Developers looking to integrate flight booking capabilities into MCP Clients
Developers creating intelligent agents for travel planning, corporate travel management, OTA platforms and lifestyle services
Product teams aiming to verify the end-to-end commercial transaction loop for AI Agents


##  Quick Start 🚀

> 💡 In summary, you only need to do two things: apply for an API Key and configure it in your AI assistant. **No coding required** – any MCP-compliant AI assistant gains hotel search capabilities in 5 minutes with your first tool call.

### Step 1: Get Your API Key

1. [Visit the Application Page](https://mcp.agentichotel.cn/apply)
2. Fill in basic information – automatic approval within 1-3 minutes. You'll receive an email containing:
   - API Key
   - Partner Center account (login + initial password) to configure markups, view orders, and check earnings
3. ⚠️ Check your email (including spam folder) for the API Key
4. **Limited-Time Offer**: All developers who complete their first tool call within 3 days of receiving the API Key unlock **permanent unlimited free access**. We prioritize developers with real needs and execution speed, offering zero-cost access to complete hotel MCP capabilities.

> The email includes both hotel and flight MCP endpoints – 1 key for both.

### Step 2: Setup & Running
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

---

## Support💬 

Join our WeChat technical support group for assistance. Don't worry about any issues during integration – our core development team will be online throughout to help you with environment configuration, API debugging, and completing your first successful flight search query.

You'll get:
- Integration configuration guidance
- API / MCP call troubleshooting
- Flight search, pricing, and inventory query workflow support
- Integration suggestions tailored to your use case

![Support WeChat](https://raw.githubusercontent.com/RollingGo-AI/rollinggo-hotel-mcp/main/support-wehcat%20group.png)
