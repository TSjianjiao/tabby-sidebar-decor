# tabby-sidebar-addition

继承自 [tabby-better-sidebar](https://github.com/TooMuhtsh/tabby-better-sidebar) 的 Tabby 侧边栏增强插件，npm 包名为 `tabby-sidebar-addition`，在 Tabby 插件市场中显示为 `sidebar-addition`。

本包是独立发布的衍生版本，不是上游官方发布。

## 本次新增

### 单击聚焦，双击新建

| 操作 | 该配置已有打开的终端 | 该配置没有打开的终端 |
|---|---|---|
| 单击 | 聚焦已有终端标签，不新建 | 不启动终端 |
| 双击 | 新建一个终端标签 | 新建一个终端标签 |

配置树和“最近启动”列表使用同一套行为：

- 单击只回到已经打开的终端；没有打开终端时不会启动新的会话。行选中和多选的原有逻辑保留。
- 双击始终新建一个终端，不受是否已有终端影响。
- 同一配置打开多个终端时，优先聚焦当前已经聚焦的标签，其次是在线会话，最后才是已断开的标签。
- `Ctrl`/`Shift` 单击仍用于多选，不会把焦点切到终端。
- 行尾的播放按钮和右键菜单里的启动项仍是显式启动，单击会新建终端。

## 安装

在 Tabby 的插件目录中安装：

Windows：

```powershell
Set-Location "$env:APPDATA\tabby\plugins"
npm install tabby-sidebar-addition
```

macOS / Linux：

```bash
cd ~/.config/tabby/plugins
npm install tabby-sidebar-addition
```

然后完全退出并重新启动 Tabby。只重载窗口不够，Tabby 需要重新加载插件。

也可以在 **Settings → Plugins** 中搜索 `sidebar-addition` 或 `tabby-sidebar-addition` 安装；如果搜索尚未收录，使用上面的 npm 命令。

安装前请先卸载上游包 `tabby-better-sidebar`，两个包会注册同一个侧边栏设置页，不能同时启用。

## 配置

设置仍在 **Settings → Better Sidebar**（同时安装 `tabby-better-vault` 时，在 **Better Tabby → 📁 Sidebar**）。其余功能、配置项和快捷键继承上游，见 [上游 README](https://github.com/TooMuhtsh/tabby-better-sidebar#readme)。

## 来源与许可

- 上游项目：[TooMuhtsh/tabby-better-sidebar](https://github.com/TooMuhtsh/tabby-better-sidebar)
- 许可证：MIT，见 [LICENSE](LICENSE)
- 第三方组件与图标声明：[THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md)
