# Better Region
## v1.0.0

---

<div style="text-align: center; margin: 20px 0;">
  <a href="https://marketplace.visualstudio.com/items?itemName=IgerNolan.BetterRegion" target="_blank">
    <img src="https://img.shields.io/badge/vscode-marketplace-blue.svg?logo=visualstudiocode" alt="VS Code Marketplace">
  </a>
  <a href="https://github.com/IgerNolan/better-region" target="_blank">
    <img src="https://img.shields.io/badge/GitHub-better--region-181717?logo=github&logoColor=white" alt="GitHub Repository">
  </a>
  <a href="https://www.gnu.org/licenses/gpl-3.0.html" target="_blank">
    <img src="https://img.shields.io/badge/license-GPLv3-green.svg" alt="License: GPL v3">
  </a>
</div>

---

该扩展为 Visual Studio Code 添加了自定义代码区域折叠和高亮，支持任意文件类型。  
This extension adds custom code region folding and highlighting for Visual Studio Code in any file type.

---

## ✨ 新功能

✅ 全面使用 `#pragma region` 格式  
所有注释模板升级为可折叠 region

✅ 内置匹配检查（绿色箭头 ▸◂ 表示匹配，红色表示错误）  
*Green ▸◂ arrows for matches, red for errors*

✅ 智能折叠（左侧行号栏显示折叠标记 ▶，支持嵌套）  
*Smart folding with ▶ markers on gutter, supports nesting*

✅ 自定义高亮（默认绿色）  
*Configurable highlighting for region markers (default: green)*

---

## 📖 使用方法

在代码中添加区域标记：
```cpp
// region MySection
// ... code ...
// endregion
```

点击左侧 ▶ 折叠，或使用快捷键：

- **折叠**：Ctrl+Shift+[ / ⌘+Option+[  
- **展开**：Ctrl+Shift+] / ⌘+Option+]  
- **折叠所有**：Ctrl+K Ctrl+0  
- **展开所有**：Ctrl+K Ctrl+J  

命令面板中可运行：**Region Fold: Fold Up Region**

---

## 🎨 Region 匹配效果
```cpp
✅ ▸ #pragma region include ← 绿色向右 | Green right arrow (matched)
✅ ◂ #pragma endregion include ← 绿色向左 | Green left arrow (matched)
✅ ▸ #pragma region include::header ← 嵌套匹配 | Nested match
✅ ◂ #pragma endregion include::header
❌ ▸ #pragma region test ← 红色（不匹配） | Red (mismatch)
❌ ◂ #pragma endregion wrong ← 红色（名称错误） | Red (name error)
```

绿色 = 完美匹配，点击左侧 ▶ 折叠！

---

## 💡 示例

### 1. 基本区域 | Basic Region
```cpp
▸ #pragma region MySection
// ... code ...
◂ #pragma endregion MySection
```

### 2. 嵌套区域 | Nested Region
```cpp
▸ #pragma region Outer
▸ #pragma region Inner
// ... code ...
◂ #pragma endregion Inner
◂ #pragma endregion Outer
```

---

## ⚙️ 配置设置

可在 **设置 (Ctrl+, / ⌘+,)** → **Extensions → Better Region Fold** 下配置：

| 设置项 | 类型 | 默认值 | 描述 |
|--------|------|--------|----------------------------------|
| `regionFold.markerColor` | string | `green` | 区域标记高亮的 CSS 颜色 |

---

## 📦 安装步骤

1. 打开 **Extensions** 面板（Ctrl+Shift+X / ⌘+Shift+X）  
2. 搜索 **"Better Region Fold"** 并点击 **Install**  
或使用命令行手动安装：

```bash
npm install -g vsce
vsce package
code --install-extension better-region-fold-0.0.3.vsix
```

---

## 📧 反馈与支持

欢迎提交 Issue 或邮件反馈  
Welcome to submit Issues or email feedback  

📧 [2481036245@qq.com](mailto:2481036245@qq.com)

---
