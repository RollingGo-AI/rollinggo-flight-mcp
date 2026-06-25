# RollingGo Flight MCP Server全球机票查询MCP

[**中文**](#中文版本) | [**English**](README.en.md)

[![Version](https://img.shields.io/badge/Version-1.0.0-blue.svg)](https://github.com/RollingGo-AI/rollinggo-flight-mcp/releases)
[![ModelScope](https://img.shields.io/badge/ModelScope-Rank%237-brightgreen.svg)](https://modelscope.cn/)
[![Calls](https://img.shields.io/badge/Calls-847.3k-orange.svg)](https://github.com/RollingGo-AI/rollinggo-flight-mcp)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)

🏠 [官网](https://rollinggo.store/) · 🚀 [快速开始](#快速开始) · 🔧 [工具](#tools) · 💬 [技术支持](#技术支持) 📚 [接入教程-视频版(0基础0代码可实操)](https://www.xiaohongshu.com/discovery/item/6a22affe0000000017029504?app_platform=ios&app_version=9.33.4&share_from_user_hidden=true&xsec_source=app_share&type=video&xsec_token=CBwWFsJ1iLP0QLjYWHV4RatLComUk4vekr3adma28ssMU=&author_share=1&xhsshare=CopyLink&shareRedId=NzxGN0RLSTo-O0pGTEwzOTszTkBGSUlM&apptime=1782376771&share_id=09ec1dc114174939916826fc8471d07a&code=051iMqFa1D1hXL08HNGa1Eq5Jb3iMqF7&state=wx_oauth)
📚 [接入教程-文档版](https://rollinggo.store/docs/mcp-docs/quick-start)


| 服务 | 端点 | 已上线 Tool | 认证 |
|------|------|------------|------|
| 酒店 MCP | `https://mcp.rollinggo.cn/mcp` | searchHotels, getHotelDetail, getHotelSearchTags | `Authorization: Bearer <YOUR_API_KEY>` |
| 机票 MCP | `https://mcp.rollinggo.cn/mcp/flight` | searchAirports, searchFlights | `Authorization: Bearer <YOUR_API_KEY>` |


## MCP亮点
- ✅ **实时库存价确** - 库存直连+实时价格确认能力，信息零延迟
- ✅ **成熟供应链保障** - 全球第三大酒旅B2B官方数据源，14年旅行产品供应链积累，全链路API直连
- ✅ **全球航线覆盖** - 500+ 合作航司，覆盖全球 200+ 国家和地区、1000+ 全球目的地
- ✅ **航线丰富**：千万级航线组合，满足多样化出行需求，支持直飞、中转等多种行程类型
- ✅ **差异化价格优势** - 锚定OTA上游供应，航线价格优势显著
- ✅ **兼容性** - 支持 Cursor、Claude Code、Codex、Windsurf、Copilot 等 40 多种主流大模型代理，针对ClawHub/扣子/Qclaw等Agent 平台，还提供[Rollinggo全能订机票酒店Skill](https://rollinggo.store/solutions/skills)。

## 适用人群
- 正在开发 AI Agent 的团队或个人开发者
- 想在 MCP Client 中接入机票预订能力的开发者
- 正在构建旅行规划、差旅管理、OTA、生活服务类智能体的开发者
- 希望验证 AI Agent 商业交易闭环的产品团队
- 有机票监控、比价、低价提醒需求的个人用户

## 应用场景
- **通用 AI Agent**：让你的大模型 Agent 直接拥有原生机票预订能力，用户在自然对话中即可完成从需求理解、智能推荐、比价筛选到订单创建的全流程
- **AI 旅行助手**：根据用户出发地、目的地、出行日期、预算和个性化偏好精准推荐航班，支持多维度需求匹配
- **行程规划工具**：把机票搜索和预订能力无缝嵌入对话式行程规划流程，实现 "规划即预订" 的一体化体验
- **MCP / Agent Demo**：快速验证 "AI Agent 直接完成机票交易" 的产品能力，打造可演示的完整闭环

## 核心功能
- 支持城市名称、机场代码、航空公司名称、航班号等多种关键字精准搜索机场和航班信息
- 提供灵活的出发/返程日期设置、舱等选择（经济舱/超级经济舱/商务舱/头等舱）、乘客人数配置、直飞/中转筛选、航空公司偏好等专业筛选功能
- 基于用户个人偏好提供个性化推荐，生成高性价比、最快到达、最少中转、热门航司等多维度专业榜单
- 全程自然语言交互，智能完成从地点解析、航班查询、比价筛选、个性化推荐到订单生成的完整闭环
- 价格和库存实时同步供应商数据，确保查询结果准确可订

## 你可以让 Agent 完成以下机票相关任务
- 根据出发地、目的地、出行日期和乘客人数搜索航班
- 查询航班价格、舱位信息和实时库存
- 判断航班或舱位是否可订
- 构建航班推荐、比价、行程规划等 AI 工作流
---
## 效果演示
> "帮我设置机票价格监控"

<table>
  <tr>
    <td><img height="400" alt="image" src="https://github.com/user-attachments/assets/39564221-304a-4afd-b468-f6dc6f5cac0c" /></td>
    <td><img height="400" alt="image" src="https://github.com/user-attachments/assets/032d5e0f-2695-4db8-9825-f4d26bcbb82e" /></td>
  </tr>
</table>

> Agent成功监测机票降价

<img width="600" alt="image" src="https://github.com/user-attachments/assets/e542e285-3d51-4ee6-a7e5-8b597d18bc77" />


## 🚀快速开始
> 💡 总结来说，你只需要做两件事：申请API Key+ 在AI助手中一键配置，**无需编写代码**，就能让任何支持MCP的AI助手具备酒店搜索能力，5 分钟内完成第一次 MCP Tool 调用，

### 第一步：获取API密钥
1. [点击进入申请地址](https://mcp.agentichotel.cn/apply)
2. 填写基本信息，0等待，申领即得API Key
3. 为什么需要填写信息申请 KEY？机票价格、库存涉及真实交易链路，因此我们需要为每个开发者开通专属的独立KEY。申请 KEY 时仅需填写少量信息，这样做主要是为了减少无效配置成本，保护接口稳定性，避免恶意调用或异常流量，在测试订单、价格查询、库存校验等问题上能及时联系到你。

### 第二步：在AI助手中配置
> 推荐 Claude CLI、Codex、Cursor 三个客户端。其他支持 MCP 的客户端（如 Kiro、豆包等）配置方式类似。

### Claude CLI

在项目根目录创建 `.mcp.json`：

```json
{
  "mcpServers": {
    "RollingGo-Hotel": {
      "url": "https://mcp.rollinggo.cn/mcp",
      "type": "http",
      "headers": {
        "Authorization": "Bearer YOUR_API_KEY"
      }
    },
    "RollingGo-Flight": {
      "url": "https://mcp.rollinggo.cn/mcp/flight",
      "type": "http",
      "headers": {
        "Authorization": "Bearer YOUR_API_KEY"
      }
    }
  }
}
```

也可以通过命令行直接添加：

```bash
claude mcp add \
  --transport http \
  --header "Authorization: Bearer YOUR_API_KEY" \
  RollingGo-Hotel \
  https://mcp.rollinggo.cn/mcp

claude mcp add \
  --transport http \
  --header "Authorization: Bearer YOUR_API_KEY" \
  RollingGo-Flight \
  https://mcp.rollinggo.cn/mcp/flight
```

### Codex

配置文件位置：项目根目录 `.codex/config.json` 或全局 `~/.codex/config.json`

```json
{
  "mcpServers": {
    "RollingGo-Hotel": {
      "url": "https://mcp.rollinggo.cn/mcp",
      "type": "streamable-http",
      "headers": {
        "Authorization": "Bearer YOUR_API_KEY"
      }
    },
    "RollingGo-Flight": {
      "url": "https://mcp.rollinggo.cn/mcp/flight",
      "type": "streamable-http",
      "headers": {
        "Authorization": "Bearer YOUR_API_KEY"
      }
    }
  }
}
```

### Cursor

配置文件位置：项目根目录 `.cursor/mcp.json` 或全局 `~/.cursor/mcp.json`

```json
{
  "mcpServers": {
    "RollingGo-Hotel": {
      "url": "https://mcp.rollinggo.cn/mcp",
      "type": "streamable-http",
      "headers": {
        "Authorization": "Bearer YOUR_API_KEY"
      }
    },
    "RollingGo-Flight": {
      "url": "https://mcp.rollinggo.cn/mcp/flight",
      "type": "streamable-http",
      "headers": {
        "Authorization": "Bearer YOUR_API_KEY"
      }
    }
  }
}
```

> 将 `YOUR_API_KEY` 替换为你收到的实际 API Key。酒店和机票使用相同的认证方式，区别仅在于 URL（`/mcp` vs `/mcp/flight`）。

### cURL 直接测试

> **注意**：cURL 必须带 `-H "Accept: application/json, text/event-stream"` 头，否则服务端返回 400。

```bash
curl -X POST https://mcp.rollinggo.cn/mcp \
  -H "Content-Type: application/json" \
  -H "Accept: application/json, text/event-stream" \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -d '{
    "jsonrpc": "2.0",
    "method": "tools/call",
    "params": {
      "name": "searchHotels",
      "arguments": {
        "originQuery": "上海外滩五星酒店",
        "place": "上海外滩",
        "placeType": "景点",
        "checkInParam": {
          "checkInDate": "2026-06-01",
          "stayNights": 2
        },
        "filterOptions": {
          "starRatings": [5.0]
        },
        "size": 3
      }
    },
    "id": 1
  }'
```

---

## 第四步：第一次 MCP 调用

配置完成后，对你的 AI 助手说：

> "帮我搜一下杭州到北京的机票"。AI 会自动调用Tool，返回机票列表。

### 机票查询示例（两步）

**Step 1**：搜索机场，获取城市代码

```json
{
  "jsonrpc": "2.0",
  "method": "tools/call",
  "params": {
    "name": "searchAirports",
    "arguments": { "keyword": "杭州" }
  },
  "id": 1
}
```

**Step 2**：用城市代码查询航班

```json
{
  "jsonrpc": "2.0",
  "method": "tools/call",
  "params": {
    "name": "searchFlights",
    "arguments": {
      "adultNumber": 1,
      "childNumber": 0,
      "cabinGrade": "ECONOMY",
      "tripType": "ONE_WAY",
      "fromCity": "HGH",
      "toCity": "CTU",
      "fromDate": "2026-06-01"
    }
  },
  "id": 1
}
```

---

## 第五步：查看结果，展示案例

### 机票查询结果（实测数据）

> 杭州→成都，单程，经济舱，共返回 **95 条航班**：

| 航班号 | 航线 | 时间 | 价格 |
|--------|------|------|------|
| CA1741 | 杭州萧山 → 成都天府 | 07:40 - 10:40 | ¥2,869 |
| CZ6198 | 杭州萧山 → 武汉 | 13:10 - 15:00 | ¥4,631 |
| CA3338 | 杭州萧山 → 深圳 | 12:55 - 15:15 | ¥5,341 |
---

## 附录

[mcp tool参考文档](https://rollinggo.store/docs/mcp-docs/mcp-tool-reference)

### 推荐调用流程
**机票查询**
```
1. 用户说"帮我查机票"
2. 调用 searchAirports → 获取城市代码
3. 调用 searchFlights → 返回航班列表
4. 展示给用户（⚠️ 价格和库存实时变化）
```

### 常见问题

**Q1: 配置后客户端看不到 Tool**
1. 检查 JSON 配置格式是否正确
2. 确认 `url` 和 `type` 是否正确
3. 确认 `Authorization` header 中的 API Key 是否正确
4. 重启客户端（修改配置后需要重启才能生效）

**Q2: 返回 401 Unauthorized**
API Key 无效或格式错误：
1. API Key 应以 `mcp_` 开头
2. `Authorization: Bearer YOUR_API_KEY` 中 Bearer 后有一个空格
3. API Key 是否有多余的空格或换行

**Q3: 返回 400 Bad Request**
cURL 直接调用时常见，检查是否带了 Accept 头：
```bash
-H "Accept: application/json, text/event-stream"
```

**Q4: searchHotels 返回空结果**
1. 检查 `place` 和 `placeType` 是否匹配（如"上海外滩"应配"景点"）
2. 放宽筛选条件（去掉星级/标签限制）
3. 确认 `checkInDate` 不是过去的时间

**Q5: searchFlights 报错**
1. 确认先调用了 `searchAirports` 获取正确的城市代码
2. 确认 `fromDate` 不是过去的时间
3. 往返行程必须传 `retDate`

**Q6: 价格和实际不一致**
搜索结果中的价格是参考价，实时价格可能有变动。当前仅支持查询，暂不支持在线下单。

**Q7: 如何获取 API Key？**
前往 [https://rollinggo.store/apply](https://rollinggo.store/apply) 提交申请，1-3 分钟内审核通过，免费无限制。

### 接入门槛与限制

| 项目 | 说明 |
|------|------|
| 是否需要注册 | 是，需要在开发者平台提交申请 |
| 是否需要 API Key | 是，所有请求需要 `Authorization: Bearer <API_KEY>` |
| 调用量限制 | 无限制 |
| 费用 | 完全免费 |
| 审核周期 | 1-3 分钟自动通过 |
| 支持的地区/币种 | 全球酒店和机票，国内用 CNY，海外用 USD |
| 下单能力 | 当前仅支持查询，不支持在线下单（规划中） |

### 技术支持

加入微信群，获取技术支持
接入路上有任何问题都别担心！欢迎加入我们的微信技术支持群，我们的核心开发团队会全程在线，手把手帮你搞定环境配置、接口调试，陪你跑通第一个成功的机票查询调用，让你零障碍快速上线。

你可以在群内获得：
- 接入配置指导
- API / MCP 调用问题排查
- 机票搜索、价格、库存查询流程说明
- 适合你业务场景的集成建议

![Support WeChat](https://raw.githubusercontent.com/RollingGo-AI/rollinggo-hotel-mcp/main/support-wehcat%20group.png)

| 其他类型 | 方式 |
|------|------|
| API Key 申请 | [https://rollinggo.store/apply](https://rollinggo.store/apply) |
| 商务合作 | contact@rollinggo.cn |
| 伙伴中心 | [https://travelportal-partner-center.dida.com](https://travelportal-partner-center.dida.com) |
| Skill Hub | [https://rollinggo.store/solutions/skills](https://rollinggo.store/solutions/skills) |
| GitHub | [https://github.com/RollingGo-AI/rollinggo-readme](https://github.com/RollingGo-AI/rollinggo-readme) |

---

*文档版本：v1.0*

## English Version

See [README.md](README.en.md) for the English version.
