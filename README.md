# OA 团建服务平台

OA 团建服务平台面向多个团支部提供内容发布、活动回顾、团费协作、公开资料、成员管理、通知、备份和平台治理。不同支部的数据相互隔离，用户只能访问与本人身份、所属支部和内容可见范围相符的信息。

当前正式版本为 **v2.1.11**，于 **2026-08-24** 发布。

- 正式站点：<https://oa-tuanjian.pages.dev>
- 问题反馈：[GitHub Issues](https://github.com/fjinzey-ctrl/OA-TuanJian/issues)
- 仓库用途：公开产品能力、使用指南和反馈渠道；不提供源代码、部署材料或内部技术文档。

## v2.1.11 更新重点

- 附件区支持带放置位置提示的拖动排序；上传后由编辑者逐个决定是否及在何处插入正文。
- 只对 PDF、图片、文本等浏览器可靠预览的格式显示预览入口；Office 等不支持格式保留下载。
- 有编辑权限的用户可从正式内容页点击“点击编辑”直达已获取最新数据的编辑器；修改记录同步覆盖附件变更。
- 系统管理员可调整公开资料顺序和单文件上传上限；关键管理页面补齐刷新操作，进入主要子页时静默获取最新数据。
- 修复设备重命名，优化行为审计详情排版和支部删除流程图；扩展过期水印衍生缓存的安全清理兼容，源文件不受影响。
- 版本号统一为 **2.1.11**，完整技术与发布记录在项目内部留档。

## v2.1.10 更新重点

- 强化通知事件、富文本清理、匿名公开资料核验、支部空间信息脱敏和设备会话语义，保持既有权限与数据边界。
- 富文本编辑器提前准备并修复初始化等待；正文优先使用设备中的国标字体，本站字体作为后备，内容无需等待字体后才显示。
- 修复头像大图关闭误跳转、团费正文显示 HTML 标签等问题，并同步更新全站功能帮助和开发者邮箱复制入口。
- 超过 30 天的水印衍生缓存由独立维护任务清理，下次授权打开时从仍受保护的源文件重新生成；源文件不受该清理规则影响。
- 版本号统一为 **2.1.10**，完整技术与发布记录在项目内部留档。

## v2.1.9 更新重点

- 平台用户管理恢复为信息更完整的多维表格，便于系统管理员集中查看账号、身份、支部和状态。
- 支部删除改为严格的最终版备份与全体管理员一致同意流程；备份失效或任何管理员不同意时，流程必须重新开始。
- 自动通知改为后台异步处理，业务操作完成后由通知中心校验并发送，减少通知延迟对操作结果的影响。
- 新增通俗、紧凑的行为审计页面，以“谁在什么时间对什么对象做了什么”为主线呈现重要操作。
- 原资料入口统一为“公开资料”，按“团务资料、现行规定、学习资料”分类；匿名访客只能查看前两类中的公开内容。
- 匿名访客进入公开资料后，安全检测在后台完成，不阻塞首屏；异常或疑似机器行为会被阻止继续停留。
- 团费支付区域进入重构准备阶段：暂不允许团费正文图片和附件，但缴费确认、统计和归档仍正常使用；没有当期团费时隐藏无效操作区。
- 管理概览空间占用与空间统计统一使用实际存储口径；富文本编辑器按需加载，并支持逐段决定是否首行缩进。
- 站内各入口开始显示完整版本号 **2.1.9**；管理概览提供简洁的“刷新”按钮。

## 主要能力

### 成员使用

- 查看本支部公示、团建回顾和团费内容。
- 确认本人团费状态，查看缴费进度和历史归档。
- 阅读平台公开资料和平台内学习资料。
- 管理头像、密码、登录设备、Cookie 与隐私选择。
- 接收平台更新、内容异动、身份调整和安全提醒。

### 内容与支部管理

- 编辑和管理员可创建富文本内容，管理附件、发布状态、置顶状态和修改记录。
- 首次发布者永久保留；发布者可把编辑权限开放给本支部指定管理员或编辑。
- 管理员可维护成员、团费状态、单条或批量缴费备注、支部设置和空间使用情况。
- 支部业务数据与其他支部隔离；移出支部不会删除平台账号、密码、头像或历史责任记录。

### 系统管理

- 维护平台用户、支部目录、容量、公开资料和全平台通知。
- 查看经过字段清理的行为审计，快速定位重要操作的主体、对象、时间和结果。
- 管理最终版备份与支部删除流程；最终删除前再次核验下载凭证、备份有效性和全体管理员意见。
- 查看平台与支部空间统计，处理账号冻结、角色调整和安全提醒。

## 角色与权限

| 身份 | 主要权限 |
| --- | --- |
| 成员 | 查阅获授权内容、确认本人团费状态、使用资料、管理本人账号与设备 |
| 编辑 | 拥有成员能力，并可发布和修改本人负责或获授权协作的内容 |
| 管理员 | 管理本支部内容、成员、团费、设置和空间；不能永久删除平台账号 |
| 系统管理员 | 管理平台用户、支部、公开资料、通知、审计、容量、备份和删除流程 |

## 使用文档

- [完整功能总览（中文）](docs/功能总览.md)
- [Complete Feature Overview (English)](docs/Feature-Overview.md)
- [成员使用指南](docs/成员使用指南.md)
- [编辑与管理员指南](docs/编辑与管理员指南.md)
- [系统管理员指南](docs/系统管理员指南.md)
- [通知、备份与支部删除说明](docs/通知备份与删除说明.md)
- [隐私与安全使用须知](docs/隐私与安全使用须知.md)
- [问题反馈指南](docs/问题反馈指南.md)

## 安全与反馈边界

反馈问题时，请提供脱敏后的操作步骤、页面、浏览器、设备类型和 `GMT+8:00` 时间。请勿在公开 Issue 中提交密码、Cookie、会话值、成员名单、缴费材料、内部附件或其他敏感信息。

---

# OA Youth League Service Platform

The OA Youth League Service Platform supports multiple Youth League branches with content publishing, activity reviews, fee coordination, public resources, member administration, notifications, backups, and platform governance. Data is isolated between branches, and users can access only information permitted by their role, branch affiliation, and content visibility.

The current production release is **v2.1.11**, published on **August 24, 2026**.

- Production: <https://oa-tuanjian.pages.dev>
- Feedback: [GitHub Issues](https://github.com/fjinzey-ctrl/OA-TuanJian/issues)
- Repository scope: public product capabilities, user guides, and feedback channels only; no source code, deployment material, or internal technical documentation is provided.

## v2.1.11 Highlights

- Attachments can be reordered with a visible drop-position cue. Editors decide per file whether and where it is inserted into the body.
- Preview actions appear only for formats the browser can reliably render, such as PDFs, images, and text. Unsupported Office formats remain download-only.
- Authorized collaborators can select “Edit” from a published content page and enter an editor that fetches the latest saved data; revision records now cover attachment changes.
- System administrators can reorder Public Resources and configure the per-file upload limit. Key management pages have dedicated refresh actions, while primary subpages silently refresh their data on entry.
- Device renaming, audit-detail layout, the branch-deletion flow diagram, and safe legacy watermark-derivative cleanup were refined without changing source files.
- Product surfaces now show the full version number **2.1.11**.

## v2.1.10 Highlights

- Notification events, rich-text sanitization, anonymous public-resource verification, branch-storage redaction, and device-session semantics were hardened without widening permissions.
- The rich-text editor is prepared earlier and no longer waits on a circular initialization state. Content uses locally installed standard document fonts first, with first-party web fonts as a fallback.
- Closing an avatar preview no longer redirects to Profile, fee content no longer exposes HTML tags, and help/copy controls were refreshed.
- Watermark derivatives older than 30 days are removed by an isolated maintenance task and regenerated from protected source files on the next authorized access. Source files are not covered by this cleanup.
- Product surfaces now show the full version number **2.1.10**.

## v2.1.9 Highlights

- Platform users are presented in a richer multidimensional table for faster account, role, branch, and status review.
- Branch deletion now requires a valid final backup, download evidence from both sides, and unanimous approval from all branch administrators. An expired backup or any rejection restarts the workflow.
- Automatic notifications are processed asynchronously by a validation and delivery center after the business operation succeeds.
- A compact behavior-audit page explains who acted, what was changed, which object was affected, and when it happened.
- Resources are unified under “Public Resources” and grouped into League Affairs, Current Rules, and Learning Resources. Anonymous visitors can access only public items in the first two categories.
- Anonymous security verification runs in the background after the resource page appears. Failed or suspicious checks prevent the visitor from remaining on the page.
- The fee payment area is prepared for a later redesign: fee-body images and attachments are temporarily unavailable, while confirmation, statistics, and archiving remain available.
- Dashboard storage totals now use the same actual-storage calculation as the storage page. The rich-text editor loads on demand and supports paragraph-level first-line indentation.
- Product surfaces now show the full version number **2.1.9**, and the management dashboard uses a concise Refresh action.

## Main Capabilities

### Member Experience

- Read authorized branch notices, activity reviews, and fee content.
- Confirm personal fee status and review progress and archive history.
- Use public resources and platform-only learning resources.
- Manage avatar, password, signed-in devices, and privacy choices.
- Receive platform releases, content updates, role changes, and security alerts.

### Content and Branch Administration

- Editors and administrators can create rich content and manage files, publication state, pinning, and revision history.
- The first publisher is permanently retained. The publisher may grant editing access to selected administrators or editors in the same branch.
- Administrators can maintain members, fee status, single or batch fee notes, branch settings, and storage usage.
- Branch data remains isolated. Removing a member from a branch does not delete the platform account, password, avatar, or historical responsibility records.

### System Administration

- Maintain platform users, branches, capacity, public resources, and platform-wide notifications.
- Review sanitized behavior audits with clear actors, targets, times, and outcomes.
- Manage final backups and branch-deletion workflows, with a final verification of download evidence, backup validity, and unanimous approval.
- Review platform and branch storage, account restrictions, roles, and security alerts.

## Roles

| Role | Main permissions |
| --- | --- |
| Member | Read authorized content, confirm personal fee status, use resources, and manage the member account and devices |
| Editor | All member abilities, plus publishing and editing responsible or explicitly shared content |
| Administrator | Manage branch content, members, fees, settings, and storage without permanently deleting platform accounts |
| System administrator | Manage platform users, branches, public resources, notifications, audits, capacity, backups, and deletion workflows |

## Documentation

- [Complete Feature Overview (English)](docs/Feature-Overview.md)
- [完整功能总览（中文）](docs/功能总览.md)
- [Member Guide](docs/成员使用指南.md)
- [Editor and Administrator Guide](docs/编辑与管理员指南.md)
- [System Administrator Guide](docs/系统管理员指南.md)
- [Notifications, Backups, and Branch Deletion](docs/通知备份与删除说明.md)
- [Privacy and Safe-Use Notice](docs/隐私与安全使用须知.md)
- [Feedback Guide](docs/问题反馈指南.md)

## Security and Feedback Boundary

When reporting a problem, provide sanitized steps, page names, browser and device type, and the relevant `GMT+8:00` time. Never post passwords, cookies, session values, member lists, fee materials, internal attachments, or other sensitive information in a public Issue.
