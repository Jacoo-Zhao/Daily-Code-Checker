

# 🧠 Daily Code Commit Reminder

[![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/Jacoo-Zhao/daily-code-checker/reminder.yml?branch=main)](https://github.com/Jacoo-Zhao/Daily-Code-Checker/actions)
[![License](https://img.shields.io/github/license/Jacoo-Zhao/daily-code-checker)](https://github.com/Jacoo-Zhao/daily-code-checker/blob/main/LICENSE)
[![Last Commit](https://img.shields.io/github/last-commit/Jacoo-Zhao/daily-code-checker)](https://github.com/Jacoo-Zhao/daily-code-checker/commits)
[![Stars](https://img.shields.io/github/stars/Jacoo-Zhao/daily-code-checker?style=social)](https://github.com/Jacoo-Zhao/daily-code-checker/stargazers)

GitHub Actions 自动提醒你每天写代码！  
每天澳洲时间 18:00，如果当天还没有 GitHub 提交记录，将通过 **邮件 + 微信（Server酱）** 同时提醒你打卡写代码 ✅

---

## 🚀 功能特点

- ⏰ 每天定时检查 GitHub 是否有提交；
- 💌 如果没有：通过 **邮件提醒**；
- 📱 同时推送到 **微信 Server酱提醒**；
- 🔒 支持私有部署，低打扰，自定义灵活。

---

## ⚙️ 使用方法

### 1️⃣ Fork / Clone 本仓库

你可以直接 fork 本项目，或复制 `.github/workflows/daily-reminder.yml` 到你的其他仓库中。

---

### 2️⃣ 添加 Secrets

前往仓库 `Settings` → `Secrets and variables` → `Actions`，添加以下内容：

| 名称              | 用途                                                       |
| ----------------- | ---------------------------------------------------------- |
| `EMAIL_USERNAME`  | 用于发送提醒邮件的 Gmail 地址（如 xxx@gmail.com）          |
| `EMAIL_PASSWORD`  | Gmail 应用专用密码（非登录密码）                           |
| `SERVER_CHAN_KEY` | Server酱 SendKey（微信提醒） [官网](https://sct.ftqq.com/) |
| `GH_TOKEN`        | GitHub Token（默认可用）                                   |

> 📌 获取 Gmail 应用密码：[生成教程（需开启两步验证）](https://myaccount.google.com/apppasswords)

---

### 3️⃣ 修改你的 GitHub 用户名

编辑 `.github/workflows/daily-reminder.yml` 中这部分，将 `GH_USERNAME` 改为你的用户名：

```yaml
env:
  GH_USERNAME: your-github-username
```

---

## 📬 效果展示

- 💌 邮件提醒内容：

  ```
  🧠 提醒你：今天还没有在 GitHub 上 commit 任何代码哦！
  
  快去敲点代码，养成写代码的好习惯吧～
  ```

- 📱 微信 Server酱提醒内容：

  ```
  😴 今天还没写代码！
  GitHub 没有任何提交，快去写点代码打卡吧！🔥
  ```

---

## 🧪 手动测试方法

你可以进入 GitHub → Actions → 选择工作流 `Daily GitHub Commit Reminder` → 点击右上角 “Run workflow” 来手动触发测试。

---

## 📈 进阶玩法（可选）

- 🗓 自动生成打卡 Markdown 日志；
- 📊 GitHub 打卡热力图 / 日历图；
- 📅 团队打卡排行榜；
- 📥 改为 Telegram / Discord / 钉钉 等提醒。

有需求可以提 Issue 或联系作者。

---

## 🧑‍💻 作者

由 [@Jacoo-Zhao](https://github.com/Jacoo-Zhao) 构建。  

---

## 📄 License

MIT License. 自由使用，欢迎改造 & 二次开发 🙌