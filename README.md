# Quantumult X 分流规则集合 | Quantumult X Filter Rules Collection

[中文](#中文) | [English](#english)

---

## 中文

### 📖 项目介绍

这是一个专为 **Quantumult X** 优化的分流规则库，包含国外AI网站、代理服务等分流规则。所有规则均经过测试和优化，可直接订阅使用。

**主要特性：**
- ✅ 包含100+个国外AI网站
- ✅ 自动更新机制（24小时更新一次）
- ✅ 轻量级规则，不占用过多资源
- ✅ 持续维护和优化

---

### 🚀 快速开始

#### 前置要求
- 已安装 **Quantumult X** 应用（iOS）
- 已配置代理策略
- 仓库中已有对应的节点配置

#### 最快上手 (3步)

1. **复制订阅链接**
   ```
   https://raw.githubusercontent.com/1240264383/quantumult-X/main/ai-worldwide.list
   ```

2. **打开 Quantumult X** → 进入 **配置文件** → 点击 **编辑**

3. **在配置文件中添加规则**
   ```
   [filter_remote]
   https://raw.githubusercontent.com/1240264383/quantumult-X/main/ai-worldwide.list, tag=AI Website Global, force-policy=proxy, update-interval=86400, opt-parser=true, enabled=true
   ```

4. **保存配置** → **重启应用** ✨

---

### 📋 详细的规则说明

#### 规则文件列表

| 规则文件 | 文件名 | 规则数量 | 更新频率 | 说明 |
|--------|------|--------|--------|------|
| AI网站全球版 | `ai-worldwide.list` | 100+ | 24小时 | 包含ChatGPT、Claude、Gemini等国外主流AI网站 |

#### 📌 ai-worldwide.list 规则详解

**覆盖的AI服务分类：**

1. **聊天AI** 
   - OpenAI (ChatGPT)
   - Anthropic (Claude)
   - Google (Gemini/Bard)
   - Perplexity AI
   - Microsoft Copilot

2. **图像生成AI**
   - DALL-E (OpenAI)
   - Midjourney
   - Stable Diffusion
   - Craiyon
   - Dream by WOMBO

3. **语音/视频AI**
   - ElevenLabs (文本转语音)
   - Deepgram (语音识别)
   - AssemblyAI (音频处理)
   - Descript (音视频编辑)
   - Synthesia (AI视频生成)

4. **开发者工具**
   - GitHub
   - Hugging Face
   - Kaggle
   - Replicate
   - LangChain
   - Pinecone

5. **其他AI服务**
   - Mistral AI
   - Cohere
   - Together AI
   - Groq
   - Modal
   - RapidAPI

---

### 📱 订阅方法教程

#### 方法一：通过配置文件订阅（推荐）

**步骤：**

1. 打开 **Quantumult X**
2. 点击底部菜单栏 → **配置文件**
3. 找到你当前使用的配置文件 → 点击 **编辑**
4. 找到 `[filter_remote]` 部分（如果没有则新建）
5. 在该部分添加以下内容：

```ini
[filter_remote]
https://raw.githubusercontent.com/1240264383/quantumult-X/main/ai-worldwide.list, tag=AI Website Global, force-policy=proxy, update-interval=86400, opt-parser=true, enabled=true
```

**参数说明：**
- `tag=AI Website Global` - 规则标签名称（显示在Quantumult X界面）
- `force-policy=proxy` - 强制使用 "proxy" 策略（需确保已配置该策略）
- `update-interval=86400` - 更新间隔（86400秒 = 24小时）
- `opt-parser=true` - 优化解析器
- `enabled=true` - 启用此规则

6. 点击 **保存** → 返回主界面
7. 完全退出后重启 Quantumult X

#### 方法二：通过URL方案订阅

直接在浏览器中打开以下链接（需已安装Quantumult X）：

```
quantumult-x:///add-filter?remote-resource=https://raw.githubusercontent.com/1240264383/quantumult-X/main/ai-worldwide.list
```

> ⚠️ 此方法需要配置文件中已有相同的策略名称

#### 方法三：手动导入

1. 复制 `ai-worldwide.list` 文件的内容
2. 在 Quantumult X 中创建新的本地规则
3. 粘贴内容后保存

---

### ⚙️ 配置建议

#### 完整配置示例

如果你的配置文件中还没有 `[policy]` 部分，建议先添加代理策略：

```ini
[policy]
static=proxy, server-tag-name, img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/Proxy.png

[filter_remote]
https://raw.githubusercontent.com/1240264383/quantumult-X/main/ai-worldwide.list, tag=AI Website Global, force-policy=proxy, update-interval=86400, opt-parser=true, enabled=true
```

#### 推荐政策设置

- **proxy** - 用于国外AI网站（通过代理访问）
- **domestic** - 用于国内网站（直连）
- **reject** - 用于广告/追踪（拒绝访问）

---

### 🔄 自动更新说明

- **更新频率**：24小时自动检查更新
- **手动更新**：在 Quantumult X 中向下滑动可手动刷新规则
- **更新内容**：
  - 添加新的AI网站
  - 移除失效域名
  - 修复规则错误

---

### ❓ 常见问题

**Q: 为什么添加了规则还是无法访问某些网站？**
- A: 请检查：
  1. 是否启用了该规则（enabled=true）
  2. 是否已正确配置代理策略
  3. 代理策略中的节点是否有效

**Q: 规则是否会影响应用性能？**
- A: 不会。规则文件很小（<4KB），对性能几乎没有影响。

**Q: 如何禁用某个规则？**
- A: 在配置文件中找到该规则，改为 `enabled=false`，然后保存重启。

**Q: 可以同时使用多个规则吗？**
- A: 可以。在 `[filter_remote]` 中添加多条规则即可，Quantumult X会自动合并。

**Q: 规则中的域名是最新的吗？**
- A: 是的。规则每24小时自动更新，包含最新的AI网站域名。

---

### 📧 反馈和建议

如有任何建议或发现规则错误，欢迎：
- 提交 Issue
- 发起 Pull Request
- 直接联系维护者

---

### 📄 许可证

本项目采用 MIT License，详见 LICENSE 文件。

---

## English

### 📖 Project Introduction

This is a **Quantumult X** optimized filter rules library containing proxy rules for overseas AI websites and services. All rules are tested and optimized for direct subscription.

**Main Features:**
- ✅ 100+ overseas AI websites
- ✅ Automatic update mechanism (updates every 24 hours)
- ✅ Lightweight rules with minimal resource usage
- ✅ Continuous maintenance and optimization

---

### 🚀 Quick Start

#### Prerequisites
- **Quantumult X** app installed (iOS)
- Proxy policy configured
- Corresponding node configuration in repository

#### Get Started in 3 Steps

1. **Copy Subscription Link**
   ```
   https://raw.githubusercontent.com/1240264383/quantumult-X/main/ai-worldwide.list
   ```

2. **Open Quantumult X** → Go to **Settings** → **Configuration File** → **Edit**

3. **Add Rule to Configuration**
   ```
   [filter_remote]
   https://raw.githubusercontent.com/1240264383/quantumult-X/main/ai-worldwide.list, tag=AI Website Global, force-policy=proxy, update-interval=86400, opt-parser=true, enabled=true
   ```

4. **Save Configuration** → **Restart App** ✨

---

### 📋 Detailed Rule Explanation

#### Rule File List

| Rule File | Filename | Rules Count | Update Frequency | Description |
|-----------|----------|-------------|------------------|-------------|
| AI Websites Global | `ai-worldwide.list` | 100+ | Every 24 hours | Includes mainstream overseas AI websites like ChatGPT, Claude, Gemini, etc. |

#### 📌 ai-worldwide.list Rule Details

**Covered AI Service Categories:**

1. **Chat AI**
   - OpenAI (ChatGPT)
   - Anthropic (Claude)
   - Google (Gemini/Bard)
   - Perplexity AI
   - Microsoft Copilot

2. **Image Generation AI**
   - DALL-E (OpenAI)
   - Midjourney
   - Stable Diffusion
   - Craiyon
   - Dream by WOMBO

3. **Voice/Video AI**
   - ElevenLabs (Text-to-Speech)
   - Deepgram (Speech Recognition)
   - AssemblyAI (Audio Processing)
   - Descript (Audio/Video Editing)
   - Synthesia (AI Video Generation)

4. **Developer Tools**
   - GitHub
   - Hugging Face
   - Kaggle
   - Replicate
   - LangChain
   - Pinecone

5. **Other AI Services**
   - Mistral AI
   - Cohere
   - Together AI
   - Groq
   - Modal
   - RapidAPI

---

### 📱 Subscription Tutorial

#### Method 1: Subscribe via Configuration File (Recommended)

**Steps:**

1. Open **Quantumult X**
2. Tap the menu bar at the bottom → **Settings**
3. Find your current configuration file → Tap **Edit**
4. Find the `[filter_remote]` section (create if not exists)
5. Add the following:

```ini
[filter_remote]
https://raw.githubusercontent.com/1240264383/quantumult-X/main/ai-worldwide.list, tag=AI Website Global, force-policy=proxy, update-interval=86400, opt-parser=true, enabled=true
```

**Parameter Explanation:**
- `tag=AI Website Global` - Rule label name (displayed in Quantumult X)
- `force-policy=proxy` - Force using "proxy" policy (ensure policy is configured)
- `update-interval=86400` - Update interval (86400 seconds = 24 hours)
- `opt-parser=true` - Enable optimized parser
- `enabled=true` - Enable this rule

6. Tap **Save** → Return to main screen
7. Completely exit and restart Quantumult X

#### Method 2: Subscribe via URL Scheme

Open the following link directly in browser (requires Quantumult X installed):

```
quantumult-x:///add-filter?remote-resource=https://raw.githubusercontent.com/1240264383/quantumult-X/main/ai-worldwide.list
```

> ⚠️ This method requires the same policy name already configured in your configuration file

#### Method 3: Manual Import

1. Copy the content of `ai-worldwide.list` file
2. Create a new local rule in Quantumult X
3. Paste content and save

---

### ⚙️ Configuration Recommendations

#### Complete Configuration Example

If your configuration file doesn't have a `[policy]` section, add proxy policy first:

```ini
[policy]
static=proxy, server-tag-name, img-url=https://raw.githubusercontent.com/Koolson/Qure/master/IconSet/Proxy.png

[filter_remote]
https://raw.githubusercontent.com/1240264383/quantumult-X/main/ai-worldwide.list, tag=AI Website Global, force-policy=proxy, update-interval=86400, opt-parser=true, enabled=true
```

#### Recommended Policy Settings

- **proxy** - For overseas AI websites (via proxy)
- **domestic** - For domestic websites (direct connection)
- **reject** - For ads/tracking (reject access)

---

### 🔄 Automatic Update Information

- **Update Frequency**: Automatic check every 24 hours
- **Manual Update**: Swipe down in Quantumult X to manually refresh rules
- **Update Content**:
  - Add new AI websites
  - Remove invalid domains
  - Fix rule errors

---

### ❓ FAQ

**Q: Why can't I access certain websites after adding the rules?**
- A: Please check:
  1. Whether the rule is enabled (enabled=true)
  2. Whether the proxy policy is configured correctly
  3. Whether the nodes in the proxy policy are valid

**Q: Will the rules affect app performance?**
- A: No. The rule file is very small (<4KB) with almost no performance impact.

**Q: How do I disable a specific rule?**
- A: Find the rule in the configuration file, change to `enabled=false`, then save and restart.

**Q: Can I use multiple rules at the same time?**
- A: Yes. Add multiple rules in the `[filter_remote]` section, Quantumult X will automatically merge them.

**Q: Are the domains in the rules up-to-date?**
- A: Yes. Rules are automatically updated every 24 hours with the latest AI website domains.

---

### 📧 Feedback and Suggestions

If you have any suggestions or find errors in the rules, welcome to:
- Submit an Issue
- Create a Pull Request
- Contact the maintainer directly

---

### 📄 License

This project is licensed under the MIT License. See LICENSE file for details.

---

**Last Updated: 2026-06-21**

⭐ If you find this useful, please give this repository a star!
