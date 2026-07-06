<div align="center">

  # Serv00_CT8_Auto_Login

</div>

### 将代码fork到你的仓库并运行的操作步骤

#### 1. Fork 仓库

1. **访问原始仓库页面**：
    - 打开你想要 fork 的 GitHub 仓库页面。

2. **Fork 仓库**：
    - 点击页面右上角的 "Fork" 按钮，将仓库 fork 到你的 GitHub 账户下。

#### 2. 设置 GitHub Secrets

1. **创建 Telegram Bot**
    - 在 Telegram 中找到 `@BotFather`，创建一个新 Bot，并获取 API Token。
    
2. **配置 GitHub Secrets**
    - 转到你 fork 的仓库页面。
    - 点击 `Settings`，然后在左侧菜单中选择 `Secrets`。
    - 添加以下 Secrets：
        - `ACCOUNTS_JSON`: 包含账号信息的 JSON 数据。例如：
        - 
          ```json
           [
            {"username": "serv00的账号", "password": "serv00的密码", "panel": "panel11.serv00.com"},
            {"username": "ct8的账号", "password": "ct8的密码", "panel": "panel.ct8.pl"},
            {"username": "ct8的账号", "password": "ct8的密码", "panel": "panel.ct8.pl"}
           ]
          ```
        - `TELEGRAM_BOT_TOKEN`: 你的 Telegram Bot 的 API Token。
        - `TELEGRAM_CHAT_ID`: 你的 Telegram Chat ID。
        
    - **获取方法**：
        - 在 Telegram 中创建 Bot，并获取 API Token 和 Chat ID。
        - 在 GitHub 仓库的 Secrets 页面添加这些值，确保它们安全且不被泄露。

#### 3. 启动 GitHub Actions

1. **配置 GitHub Actions**
    - 在你的 fork 仓库中，进入 `Actions` 页面。
    - 如果 Actions 没有自动启用，点击 `Enable GitHub Actions` 按钮以激活它。

2. **运行工作流**
    - GitHub Actions 将会根据你设置的定时任务（例如每三天一次）自动运行脚本。
    - 如果需要手动触发，可以在 Actions 页面手动运行工作流。

#### 示例 Secrets 和获取方法总结

- **TELEGRAM_BOT_TOKEN**
    - 示例值: `1234567890:ABCDEFghijklmnopQRSTuvwxyZ`
    - 获取方法: 在 Telegram 中使用 `@BotFather` 创建 Bot 并获取 API Token。

- **TELEGRAM_CHAT_ID**
    - 示例值: `1234567890`
    - 获取方法: 发送一条消息给你的 Bot，然后访问 `https://api.telegram.org/bot<your_bot_token>/getUpdates` 获取 Chat ID。

- **ACCOUNTS_JSON**
    - 示例值:
      ```json
      [
            {"username": "serv00的账号", "password": "serv00的密码", "panel": "panel11.serv00.com"},
            {"username": "ct8的账号", "password": "ct8的密码", "panel": "panel.ct8.pl"},
            {"username": "ct8的账号", "password": "ct8的密码", "panel": "panel.ct8.pl"}
      ]
      ```
    - 获取方法: 创建一个包含serv00账号信息的 JSON 文件，并将其内容添加到 GitHub 仓库的 Secrets 中。

#### 通知示例

成功运行后，您将收到如下格式的Telegram通知：

````markdown
📨 Serv00 & CT8 保号脚本运行报告
━━━━━━━━━━━━━━━━━━━━
🕘 北京时间: 2025-02-01 12:34:56
🌐 UTC时间: 2025-02-01 04:34:56
━━━━━━━━━━━━━━━━━━━━

📊 登录状态报告

🔹 服务商: CT8
👤 账号: user123
🕒 时间: 2025-02-01 12:34:56
✅ 状态: 登录成功
────────────────────
🔹 服务商: Serv00
👤 账号: example_user
🕒 时间: 2025-02-01 12:35:02
❌ 状态: 登录失败
────────────────────

🏁 所有账号操作已完成
````

> 通知包含以下关键信息：
> - 📅 双时区时间显示
> - ✅/❌ 状态图标
> - 🔍 详细账户登录结果
> - 📊 可视化分隔线

### 注意事项

- **保密性**: Secrets 是敏感信息，请确保不要将它们泄露到公共代码库或未授权的人员。
- **更新和删除**: 如果需要更新或删除 Secrets，可以通过仓库的 Secrets 页面进行管理。

通过以上步骤，你就可以成功将代码 fork 到你的仓库下并运行它了。如果需要进一步的帮助或有其他问题，请随时告知！
