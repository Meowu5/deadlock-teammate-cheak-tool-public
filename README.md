# Deadlock 玩家记录器

面向 Windows x64 的本地玩家记录工具，用来查看已采集的同局记录、管理玩家备注，并按明确选择的范围补充可获取的历史资料。

本仓库提供下载包、使用说明和版本校验信息。本工具非商业、免费，无付费功能或广告。它是独立社区工具，与 Valve、Steam、QoL Lock、Statlocker 或 Microsoft 无官方隶属或背书关系。

## 下载与开始使用

**[下载 Windows x64 单文件 EXE](https://github.com/Meowu5/deadlock-teammate-cheak-tool-public/releases/latest/download/Deadlock-Recorder-Windows-x64.exe)**

当前正式版 **v0.1.1**，主文件为 `Deadlock-Recorder-Windows-x64.exe`。[查看版本说明](https://github.com/Meowu5/deadlock-teammate-cheak-tool-public/releases/latest)；[下载 SHA256SUMS.txt](https://github.com/Meowu5/deadlock-teammate-cheak-tool-public/releases/latest/download/SHA256SUMS.txt) 核对文件。

v0.1.1 修复历史补抓连续寻找候选、缺失时间影响近期对局排序、旧终止回执恢复入口及关闭竞态。本批最多寻找 50 个候选，不保证外部索引覆盖全部历史；本版不包含托盘后台运行。

1. 按 [启动与更新](docs/INSTALL.md) 核对 EXE 的 SHA-256。
2. 双击下载的 EXE，统一启动界面和采集功能。首次使用按界面选择资料目录和游戏日志来源；已有资料先关闭旧程序并备份完整资料目录。
3. 查看来源状态。只有拿到有效采集数据才会出现本局名单；“桥接兼容”“已加载”或“等待数据”都不代表已采集完成。

本版关闭窗口会退出程序及其拥有的采集进程；尚未提供关闭到托盘功能。

EXE 内含应用组件，首次运行校验后将组件准备到当前用户的私有运行缓存。图形界面依赖 Windows 上已有的 Microsoft Edge WebView2 Runtime；本包不附带或自动安装该浏览器运行时。Release 中的技术 ZIP 供应用自动更新使用，普通使用从主 EXE 开始。

## 数据来源与当前范围

- **主要采集来源**：本机游戏日志中的有效 QoL 桥接记录。本版本正式支持的精确适配目标为 **QoL Lock 4.0.5 hotfix**，对应 [GameBanana 更新 461898](https://gamebanana.com/updates/461898)。普通 QoL 安装、版本号相同或兼容检测成功，都不能单独证明名单已经产生。
- **桥接设置**：只读检查。本版本不提供 QoL 桥接的安装、修复、卸载或回退；不会替你生成或安装派生模组。没有可用桥接记录时，可继续查询和编辑本地资料，按需使用历史补充入口。
- **历史资料**：在明确选择账号、范围并确认后，查询界面注明的外部来源。服务未收录、缺项或无法访问时保留真实状态；“已补充”不等于获得全部游戏历史。
- **Steam 备用**：实验功能，默认 **关闭**。真实 Steam/DLL 版本组合及实战名单尚未完成验收；即使取得候选，也不是完整本局名单，须按提示人工确认。
- **Statlocker 自动补抓**：真实 API 尚未接通。等待任务或网页跳转不代表自动补抓成功。

请先阅读 [数据获取、原因与注意事项](docs/DATA-SOURCES.md) 和 [已知限制](docs/KNOWN-LIMITATIONS.md)。本工具不提供零封禁风险承诺。

## 资料与反馈

个人记录、备注和配置保存在你选择的资料目录。软件目录与资料目录可以不同；移动或更新程序不会自动搬迁资料。反馈时可在 [Issues](https://github.com/Meowu5/deadlock-teammate-cheak-tool-public/issues) 描述版本、操作和错误提示；请勿公开完整玩家日志、数据库、账号凭据或个人路径。

第三方组件声明及完整许可随软件提供，见 [第三方说明](docs/THIRD-PARTY.md)。
