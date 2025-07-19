# PteroCord

PteroCord 是一個整合 Discord 與 Pterodactyl 面板的機器人，提供用戶註冊、伺服器查詢與控制、以及強大的管理員功能（如伺服器停權、用戶管理等）。

## 功能特色

- **用戶註冊申請**：透過 Discord Modal 表單，讓用戶申請註冊，管理員審核後自動創建 Pterodactyl 帳號。
- **伺服器查詢與控制**：使用 `/server <伺服器UUID>`，自動查詢伺服器資訊，顯示狀態、擁有者，並提供一鍵控制按鈕（啟動、關閉、重啟、強制停止）。
- **管理員專用指令**：管理員可透過指令停權伺服器、刪除用戶、管理伺服器與用戶。

## 目錄結構

```
pterocord/
│ config.json
│ main.py
│ requirements.txt
│ README.md
│ .gitignore
└─ cogs/
   │ __init__.py
   │ register.py
   │ server.py
   │ admin.py
```

## 快速開始

1. **安裝依賴**
    ```bash
    pip install -r requirements.txt
    ```
2. **設定 config.json**  
   - 填入 Discord Token、Pterodactyl API URL 及 Key、管理員頻道 ID 等參數

3. **啟動機器人**
    ```bash
    python main.py
    ```

## 依賴套件

- [discord.py](https://pypi.org/project/discord.py/)
- [pteropy](https://pypi.org/project/pteropy/) (或其他 Pterodactyl API library)

## 設定檔 config.json 範例

```json
{
    "DISCORD_TOKEN": "YOUR_DISCORD_BOT_TOKEN",
    "PTERODACTYL_URL": "https://panel.example.com",
    "PTERODACTYL_API_KEY": "YOUR_PTERODACTYL_API_KEY",
    "ADMIN_CHANNEL_ID": 123456789012345678
}
```

## 授權

MIT License
