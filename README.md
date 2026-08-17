# Plugins-for-agent

[Cyrene-Agent](https://github.com/ahwhshen/Cyrene-Agent) 的插件仓库。
每个顶层目录就是一个完整的插件包，拷进应用即可使用。

---

## 📦 插件目录

| 插件 | 说明 | 版本 |
| --- | --- | --- |
| [currency-wars](./currency-wars) | 《崩坏：星穹铁道》货币战争自动运行：窗口定位截图 + OCR/VLM 识别，按词条规则自动选祝福与投资 | 1.0.0 |

---

## 🚀 安装方法

1. 下载（或 clone 本仓库后复制）目标插件目录，例如 `currency-wars/`。
2. 把整个目录放进 Cyrene 的用户插件目录：

   ```
   %APPDATA%\live2d-cyrene\plugins\
   ```

   即最终路径形如 `%APPDATA%\live2d-cyrene\plugins\currency-wars\plugin.json`。
3. 重启应用（或在 设置 → 插件 栏重新扫描），打开对应插件的开关即可。

> 用户插件与内置插件同 id 时会覆盖内置版本，方便自行修改与修复。

---

## 🧩 自己写一个插件

插件包 = 一个目录：`plugin.json`（清单）+ `index.js`（逻辑），
可选图标与自带窗口。完整开发契约见 Cyrene-Agent 仓库的
[插件 API 调用规范](https://github.com/ahwhshen/Cyrene-Agent/blob/main/docs/cyrene-plugin-api-spec.md)。

最小结构：

```
my-plugin/
├── plugin.json    # id / name / version / entry / defaultEnabled
├── index.js       # module.exports 插件对象（registerTools 等钩子均可选）
└── icon.png       # 推荐
```

欢迎提交 PR 分享你的插件（请附清单校验通过的说明与截图）。

---

## 📄 许可证

各插件许可证见其目录内声明；未单独声明的默认遵循仓库根目录 [LICENSE](./LICENSE)。
