# valstry.net 信源看板

只读静态站：本机 Pi `run-daily` 产出 digest 后同步至此，经 Cloudflare Pages 发布。

- 不暴露 `localhost:1200` / raw 全库
- 不依赖 Grok Bot 额度
- 聊天早报按需，另走「早间新闻」

## 发布约定

| 文件 | 含义 |
|------|------|
| `index.html` | 当日 `report.html`（覆盖） |
| `latest.md` | `最新摘要.md`（覆盖） |
| `archive/YYYY-MM-DD/` | 可选历史 |

同步：git push 本仓，或 `wrangler pages deploy`。
