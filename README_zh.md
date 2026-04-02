# CoPaw UI/UX Pro Max

🎨 专业级 UI/UX 设计智能助手，专为 CoPaw Agent 构建。

## 简介

这是 [nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill)（⭐ 56.7k）的 CoPaw 适配版本。

一款全面的设计智能技能，提供：
- **设计系统生成** - 根据产品类型生成完整设计系统
- **多平台支持** - Web / iOS / Android / React Native / Flutter
- **组件设计指导** - 按钮、卡片、表单、导航等
- **UX/UI 最佳实践** - 100+ 规范清单
- **设计知识库** - 涵盖 15+ 技术栈

## 功能一览

| 功能 | 说明 |
|------|------|
| 设计系统生成器 | 一键生成配色、字体、布局、动效完整方案 |
| 多平台覆盖 | Web、iOS、Android、React Native、Flutter、SwiftUI |
| 10 级优先级规则 | CRITICAL → HIGH → MEDIUM → LOW |
| 100+ 快速参考 | 即查即用的设计模式和反模式 |
| 15+ 技术栈指南 | React、Vue、Next.js、Flutter、SwiftUI 等 |

## 快速开始

### 环境要求

```bash
python --version
```

**Windows 未安装？**
```powershell
winget install Python.Python.3.12
```

### 生成设计系统

```bash
# 生成完整设计系统
python skills/ui-ux-pro-max/scripts/search.py "金融 科技 现代" --design-system

# 搜索特定风格
python skills/ui-ux-pro-max/scripts/search.py "玻璃拟态 暗色" --domain style

# 获取 UX 最佳实践
python skills/ui-ux-pro-max/scripts/search.py "动效 无障碍" --domain ux

# 搜索配色方案
python skills/ui-ux-pro-max/scripts/search.py "SaaS 金融" --domain color

# 字体搭配
python skills/ui-ux-pro-max/scripts/search.py "现代 专业" --domain typography
```

### 输出格式

```bash
# ASCII 盒子（默认）- 终端显示效果最佳
python skills/ui-ux-pro-max/scripts/search.py "金融 加密" --design-system

# Markdown - 便于文档化
python skills/ui-ux-pro-max/scripts/search.py "金融 加密" --design-system -f markdown
```

## 可搜索的领域

| 领域 | 用途 | 示例关键词 |
|------|------|-----------|
| `product` | 产品类型推荐 | SaaS、电商、医疗、美妆 |
| `style` | UI 风格、颜色、效果 | 玻璃拟态、极简主义、暗色模式 |
| `typography` | 字体搭配、Google Fonts | 优雅、趣味、专业、现代 |
| `color` | 按产品类型的配色 | SaaS、电商、金融、科技 |
| `landing` | 页面结构、CTA 策略 | 首屏、推荐、定价 |
| `chart` | 图表类型、库推荐 | 趋势、对比、时间线、漏斗 |
| `ux` | 最佳实践、反模式 | 动效、无障碍、加载 |
| `react` | React/Next.js 性能 | 瀑布流、记忆化、重渲染 |
| `web` | App 界面规范 | 无障碍标签、触控区域、安全区域 |
| `prompt` | AI 提示词、CSS 关键词 | （风格名称） |

## 支持的技术栈

| 技术栈 | 专注领域 |
|--------|--------|
| `react-native` | 组件、导航、列表性能 |
| `react` | React 性能优化 |
| `nextjs` | Next.js SSR/SSG |
| `vue` | Vue 3 组合式 API |
| `flutter` | Flutter 组件 |
| `swiftui` | SwiftUI 原生开发 |
| `jetpack-compose` | Jetpack Compose |
| `html-tailwind` | HTML + Tailwind CSS |
| `shadcn` | shadcn/ui 组件库 |

## 优先级规则

### CRITICAL（关键）

- **无障碍访问**：对比度 4.5:1、焦点状态、Alt 文字、ARIA 标签
- **触控交互**：最小 44×44pt、8px 间距、加载反馈
- **性能**：WebP/AVIF、懒加载、列表虚拟化

### HIGH（重要）

- **风格选择**：匹配产品类型、保持一致、SVG 图标（不用 Emoji）
- **布局与响应式**：移动优先、断点一致、无横向滚动
- **导航**：底部导航 ≤5 项、可预测的返回、深链接

### MEDIUM（建议）

- **排版与配色**：行高 1.5、语义化 Token、字体等级
- **动效**：150–300ms、ease-out/ease-in、退出快于进入
- **表单**：可见标签、错误位置、失焦验证

### LOW（可选）

- **图表**：图表类型匹配数据、无障碍配色、图例可见

## 目录结构

```
ui-ux-pro-max/
├── SKILL.md                  # CoPaw 技能文档
├── README.md                 # 英文版说明
├── README_zh.md             # 中文版说明（本文件）
├── data/                     # 设计知识库
│   ├── colors.csv            # 配色方案
│   ├── styles.csv            # 视觉风格
│   ├── typography.csv        # 字体系统
│   ├── ux-guidelines.csv     # UX 最佳实践
│   └── stacks/               # 技术栈指南
│       ├── react.csv
│       ├── vue.csv
│       └── ...（15+ 技术栈）
├── scripts/
│   ├── search.py             # 主搜索脚本
│   ├── core.py               # 核心函数
│   └── design_system.py      # 设计系统生成器
└── templates/
    ├── base/                 # 基础模板
    └── platforms/            # 其他平台配置参考
```

## 开源协议

基于 [nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill)，采用 MIT 协议。

详见 [LICENSE](./LICENSE)。

## 贡献

欢迎提交 Issue 和 Pull Request！欢迎改进或适配到其他 Agent 平台。
