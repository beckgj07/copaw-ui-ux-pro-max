---
name: ui-ux-pro-max
description: "专业的 UI/UX 设计智能助手。支持多平台（Web/iOS/Android/React Native/Flutter）设计系统生成、组件设计、设计规范检查。包含配色、字体、布局、动效、交互动效等完整设计知识库。"
emoji: "🎨"
metadata:
  {
    "builtin_skill_version": "1.0",
    "copaw": { "emoji": "🎨", "requires": {} }
  }
---

# 🎨 UI/UX Pro Max

专业的 UI/UX 设计智能助手。源自 [nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill)（⭐ 56.7k）。

---

## 核心能力

| 能力 | 说明 |
|------|------|
| **设计系统生成** | 根据产品类型/行业生成完整设计系统（配色、字体、布局、动效） |
| **多平台支持** | Web / iOS / Android / React Native / Flutter / SwiftUI / Jetpack Compose |
| **组件设计** | 按钮、卡片、表单、弹窗、导航、图表等 |
| **设计规范检查** | 无障碍、可访问性、性能、响应式、动效规范 |
| **设计知识库** | 涵盖 4 大类 10 个优先级规则 + 100+ Quick Reference 关键词 |

---

## 工作流程

### Step 1: 分析需求

从用户需求中提取关键信息：
- **产品类型**：娱乐社交 / 工具类 / 生产力 / 混合
- **目标用户**：C端用户，考虑年龄、使用场景
- **风格关键词**：playful / minimal / dark mode / immersive 等
- **技术栈**：React / Vue / React Native / Flutter / SwiftUI 等

### Step 2: 生成设计系统（推荐）

使用 Python 脚本生成完整设计系统：

```bash
python skills/ui-ux-pro-max/scripts/search.py "<产品类型> <行业> <关键词>" --design-system
```

**示例：**
```bash
python skills/ui-ux-pro-max/scripts/search.py "fintech crypto modern minimal" --design-system -f markdown
```

**输出内容：**
- Pattern（页面结构模式）
- Style（视觉风格）
- Colors（配色方案）
- Typography（字体系统）
- Effects（动效/光影）
- Anti-patterns（避免的反模式）

### Step 3: 补充详细搜索（按需）

```bash
# 风格搜索
python skills/ui-ux-pro-max/scripts/search.py "<关键词>" --domain style

# 配色搜索
python skills/ui-ux-pro-max/scripts/search.py "<关键词>" --domain color

# 字体搜索
python skills/ui-ux-pro-max/scripts/search.py "<关键词>" --domain typography

# UX 规范
python skills/ui-ux-pro-max/scripts/search.py "<关键词>" --domain ux

# 图表推荐
python skills/ui-ux-pro-max/scripts/search.py "<关键词>" --domain chart

# 技术栈最佳实践
python skills/ui-ux-pro-max/scripts/search.py "<关键词>" --stack <stack-name>
```

### Step 4: 设计交付检查

使用 Quick Reference 进行交付前检查（详见下方规则列表）。

---

## 支持的搜索域

| 域 | 用途 | 示例关键词 |
|----|------|-----------|
| `product` | 产品类型推荐 | SaaS, e-commerce, portfolio, healthcare, beauty |
| `style` | UI 风格、颜色、效果 | glassmorphism, minimalism, dark mode, brutalism |
| `typography` | 字体搭配、Google Fonts | elegant, playful, professional, modern |
| `color` | 配色方案 | saas, ecommerce, healthcare, beauty, fintech |
| `landing` | 页面结构、CTA 策略 | hero, hero-centric, testimonial, pricing |
| `chart` | 图表类型、库推荐 | trend, comparison, timeline, funnel, pie |
| `ux` | 最佳实践、反模式 | animation, accessibility, z-index, loading |
| `react` | React/Next.js 性能 | waterfall, bundle, suspense, memo |
| `web` | App 界面规范 | accessibilityLabel, touch targets, safe areas |
| `prompt` | AI 提示词、CSS 关键词 | (style name) |

---

## 支持的技术栈

| 栈 | 专注点 |
|----|--------|
| `react-native` | 组件、导航、列表性能 |
| `react` | React 性能优化 |
| `nextjs` | Next.js SSR/SSG |
| `vue` | Vue 3 组合式 API |
| `flutter` | Flutter 组件 |
| `swiftui` | SwiftUI 原生 |
| `jetpack-compose` | Jetpack Compose |
| `html-tailwind` | HTML + Tailwind CSS |
| `shadcn` | shadcn/ui 组件 |

---

## Quick Reference 规则清单

### CRITICAL（必须）

#### 1. 无障碍访问 ⭐⭐⭐
- `color-contrast` - 文本对比度 ≥ 4.5:1
- `focus-states` - 交互元素有可见焦点环
- `alt-text` - 重要图片有描述性 alt 文字
- `aria-labels` - 图标按钮有 aria-label
- `keyboard-nav` - Tab 顺序与视觉顺序一致
- `reduced-motion` - 支持 prefers-reduced-motion

#### 2. 触控交互 ⭐⭐⭐
- `touch-target-size` - 最小触控区域 44×44pt
- `touch-spacing` - 触控目标间 ≥ 8px 间隔
- `loading-buttons` - 异步操作时禁用按钮并显示加载状态
- `haptic-feedback` - 重要操作提供触觉反馈
- `press-feedback` - 按压有视觉反馈（ripple/highlight）

#### 3. 性能 ⭐⭐
- `image-optimization` - 使用 WebP/AVIF + 懒加载
- `virtualize-lists` - 50+ 条目的列表使用虚拟化
- `main-thread-budget` - 单帧工作保持在 ~16ms 内
- `progressive-loading` - 使用骨架屏而非长时间 loading

### HIGH（重要）

#### 4. 风格选择 ⭐⭐
- `style-match` - 风格匹配产品类型
- `consistency` - 全站风格一致
- `no-emoji-icons` - 使用 SVG 图标，不用 Emoji
- `dark-mode-pairing` - 浅色/深色变体一起设计

#### 5. 布局与响应式 ⭐⭐
- `mobile-first` - 移动优先设计
- `breakpoint-consistency` - 使用系统性断点
- `no-horizontal-scroll` - 移动端无横向滚动
- `spacing-scale` - 使用 4pt/8dp 间距系统

#### 6. 导航模式 ⭐⭐
- `bottom-nav-limit` - 底部导航最多 5 项
- `back-behavior` - 返回导航可预测
- `deep-linking` - 关键页面支持深链接

### MEDIUM（建议）

#### 7. 排版与配色 ⭐
- `line-height` - 正文行高 1.5–1.75
- `color-semantic` - 使用语义化颜色 token
- `font-scale` - 一致的字体大小等级

#### 8. 动效 ⭐
- `duration-timing` - 微交互 150–300ms
- `easing` - ease-out 进入，ease-in 退出
- `exit-faster-than-enter` - 退出动画短于进入

#### 9. 表单与反馈 ⭐
- `input-labels` - 每个输入框有可见标签
- `error-placement` - 错误显示在相关字段下方
- `inline-validation` - 失焦时验证（非按键验证）

#### 10. 图表 ⭐
- `chart-type` - 图表类型匹配数据
- `color-guidance` - 使用无障碍配色
- `legend-visible` - 图例始终可见

---

## 常见问题解决

| 问题 | 解决方案 |
|------|----------|
| 风格/配色拿不定主意 | 重新运行 `--design-system`，换关键词组合 |
| 深色模式对比度问题 | Quick Reference §6：`color-dark-mode` + `color-accessible-pairs` |
| 动画感觉不自然 | Quick Reference §7：`spring-physics` + `easing` + `exit-faster-than-enter` |
| 表单体验差 | Quick Reference §8：`inline-validation` + `error-clarity` |
| 导航让人困惑 | Quick Reference §9：`nav-hierarchy` + `bottom-nav-limit` |
| 小屏幕布局破坏 | Quick Reference §5：`mobile-first` + `breakpoint-consistency` |
| 性能卡顿 | Quick Reference §3：`virtualize-lists` + `main-thread-budget` |

---

## 输出格式

支持两种输出格式：

```bash
# ASCII box（默认）- 终端显示效果最佳
python skills/ui-ux-pro-max/scripts/search.py "fintech crypto" --design-system

# Markdown - 文档化最佳
python skills/ui-ux-pro-max/scripts/search.py "fintech crypto" --design-system -f markdown
```

---

## 前置条件

确保 Python 已安装：

```bash
python --version
```

**Windows 未安装？**
```powershell
winget install Python.Python.3.12
```

---

## 输出格式

```bash
