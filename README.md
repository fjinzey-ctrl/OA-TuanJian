# OA 团建服务平台

OA 团建服务平台面向多个团支部提供信息发布、活动回顾、团费协作、规范资料、成员管理、通知、备份和平台治理。不同支部数据相互隔离，成员只能访问与本人身份和所属支部相符的内容。

2.1 已于 2026-07-15 完成内测修复并正式发布。本仓库仅用于介绍完整功能、提供使用指南和收集反馈，不提供源代码、部署材料或内部技术文档。

2026-07-14 内测跟进已同步：适应页宽的连续 PDF、发布标题与中英文字体规则、详细功能帮助、手机表单布局，以及文件上传和团费归档撤销的可操作错误说明。

最新跟进补充通知跳转自动收起、团费深链回跳、归档后默认重置、清晰的改密规则、编辑空间统计，以及文本、表格、Word 和图片等更多附件预览。历史 TXT 类型现已兼容；无法可靠预览的音频等附件只显示下载。访问量接近每日免费额度时，平台会暂时展示静态高峰提示并在额度重置后恢复。

静态高峰提示页使用与正式站点一致的小旗标识，不会读取账号、内容、团费或附件数据。

平台每 10 分钟检查一次账号级免费请求额度；达到 80% 保护阈值后启用静态高峰提示，额度重置后自动恢复。

2026-07-17 的 2.1 完善 Preview 增加正文图片高度、团建指定封面、平台用户批量冻结、五类通知存档，以及默认/图床/本地文件三种头像来源。外链头像通过本站安全检查后复制保存；短时大量下载、多网络来源登录和反复危险链接会形成只面向系统管理员的“安全提醒”，不记录原始 IP、完整链接或附件正文。

## 主要能力

- 登录与反馈：页面加载后开始安全检测，验证前不可提交；访客可直接申请支部入驻或反馈登录问题。
- 支部协作：首页、公示、团建、团费和规范资料覆盖日常团务，支持富文本、图片、附件、修改记录和明确空状态。
- 内容管理：编辑与管理员可拖入、粘贴或选择文件，发布者责任固定，编辑仅修改本人内容。
- 成员与账号：普通账号全平台唯一且最多属于一个支部；移出支部不删除账号、密码、头像或历史责任记录。
- 通知中心：自动接收平台升级、设置与内容变化、身份调整、备份和管理决定，并展示操作人、时间与变更详情。
- 支部治理：系统管理员维护支部、容量、备份、删除审批、公共资料和平台用户；支部唯一管理员受到保护。
- 账号安全：系统管理员可冻结或批量管理平台账号；安全提醒使用哈希和计数发现明显异常，不展示用户原始网络地址或外链内容。
- 多端体验：桌面侧栏与手机专用五项底部导航分别适配；每个主要模块提供功能概览，窄屏长文字保持可读，通知在手机端以易关闭的面板展示。

## 文档

- [完整功能总览（中文）](docs/功能总览.md)
- [Complete Feature Overview (English)](docs/Feature-Overview.md)
- [成员使用指南](docs/成员使用指南.md)
- [编辑与管理员指南](docs/编辑与管理员指南.md)
- [系统管理员指南](docs/系统管理员指南.md)
- [通知、备份与支部删除说明](docs/通知备份与删除说明.md)
- [隐私与安全使用须知](docs/隐私与安全使用须知.md)
- [问题反馈指南](docs/问题反馈指南.md)

## 角色

| 身份       | 主要权限                                                                     |
| ---------- | ---------------------------------------------------------------------------- |
| 成员       | 查阅本支部内容、确认团费状态、使用规范资料、管理本人头像和密码               |
| 编辑       | 拥有成员能力，可发布、修改自己负责的内容并查看本支部空间统计                 |
| 管理员     | 管理本支部内容、成员、团费、资料和空间；可移出非管理员但不能永久删除平台账号 |
| 系统管理员 | 管理平台通知、公共资料、支部目录、容量、备份、支部管理员和平台用户账号       |

如需反馈，请前往仓库 Issues 并遵循[问题反馈指南](docs/问题反馈指南.md)。请勿公开密码、成员名单、缴费材料、内部附件或其他敏感信息。

---

# OA Youth League Service Platform

The OA Youth League Service Platform provides multiple Youth League branches with information publishing, activity reviews, fee coordination, official resources, member administration, notifications, backups, and platform governance. Branch data is isolated, and members can access only content permitted by their role and branch affiliation.

Version 2.1 completed its beta-fix cycle and was formally released on July 15, 2026. This repository presents complete product capabilities, user guides, and feedback channels only. It does not provide source code, deployment materials, or internal technical documentation.

The latest update fixes previewing for historical TXT metadata, hides preview controls for unsupported files such as anthem audio, and temporarily switches to a static peak-traffic notice when daily service usage approaches the free allowance. Full access resumes after the allowance resets.

The platform checks the account-level free request allowance every 10 minutes. At the 80% protection threshold, it enables the static peak-traffic notice and restores full access after the allowance resets.

The July 17 Preview adds resizable body images, explicit activity covers, batch account freezing, five archive categories, and default/URL/local avatar sources. Remote avatars are validated and copied into platform storage. Security alerts use counts and irreversible hashes rather than raw IP addresses, full URLs, or attachment contents.

## Main Capabilities

- Sign-in and feedback: security checks begin when the page loads, submission is unavailable before verification, and visitors can request branch onboarding or report sign-in problems directly.
- Branch collaboration: home, notices, activities, fees, and official resources support daily work, rich text, images, attachments, revision records, and clear empty states.
- Content management: editors and administrators can drag, paste, or select files. Publisher responsibility is fixed, and editors can modify only their own content.
- Members and accounts: each ordinary account is unique across the platform and belongs to at most one branch. Removal from a branch preserves the account, password, avatar, and historical responsibility records.
- Notification center: automatically receive platform releases, settings and content changes, role updates, backups, and administrative decisions with the operator, time, and detailed changes.
- Branch governance: system administrators maintain branches, capacity, backups, deletion approval, public resources, and platform users. Every branch's sole administrator is protected.
- Multi-device experience: desktop side navigation and a phone-specific five-item bottom navigation are provided. Each main module includes a quick feature overview, long text remains readable on narrow screens, and notifications open in an easy-to-close mobile panel.

## Documentation

- [Complete Feature Overview (English)](docs/Feature-Overview.md)
- [完整功能总览（中文）](docs/功能总览.md)
- [Member Guide](docs/成员使用指南.md)
- [Editor and Administrator Guide](docs/编辑与管理员指南.md)
- [System Administrator Guide](docs/系统管理员指南.md)
- [Notifications, Backups, and Branch Deletion](docs/通知备份与删除说明.md)
- [Privacy and Safe-Use Notice](docs/隐私与安全使用须知.md)
- [Feedback Guide](docs/问题反馈指南.md)

## Roles

| Role                 | Main permissions                                                                                                                            |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| Member               | Read branch content, confirm fee status, use official resources, and manage the member's avatar and password                                |
| Editor               | All member capabilities, plus publishing and editing content for which the editor is responsible                                            |
| Administrator        | Manage branch content, members, fees, details, and storage; remove non-administrators without permanently deleting platform accounts        |
| System administrator | Manage platform notifications, public resources, the branch directory, capacity, backups, branch administrators, and platform user accounts |

To provide feedback, open a repository Issue and follow the [Feedback Guide](docs/问题反馈指南.md). Do not publicly share passwords, member lists, fee materials, internal attachments, or other sensitive information.
# 2026-07-17 · 2.1 使用说明更新

通知和内容编辑现支持在光标位置插入居中图片，并分别控制正文与附件区显示；已发布内容保存后会自动进入成员端页面。空间统计包含源文件、水印衍生文件与头像，支部默认空间为 1.5 GiB。透明背景头像现在会保留透明区域。
