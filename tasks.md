```bash
curl --location --request POST 'https://api.myshell.fun/v1/tg2app/miniapp/get_bot_list' \
--header 'authority: staging-api-v2.myshell.ai' \
--header 'myshell-service-name: organics-api' \
--header 'pragma: no-cache' \
--header 'Accept-Language: zh' \
--header 'Sec-Ch-Ua-Mobile: ?1' \
--header 'X-Telegram-Init-Data: auth_date=1754919224&hash=32930bbf751755f0cdca72647de20b2a53fcaf7dc5b1569e781806be5dc6cf2c&user=%7B%22first_name%22%3A%22Test%22%2C%22id%22%3A123456789%2C%22language_code%22%3A%22en%22%2C%22last_name%22%3A%22User%22%2C%22username%22%3A%22testuser%22%7D' \
--header 'content-type: application/json' \
--data-raw '{}'
```

bot 列表

```json
{
  "bots": [
    {
      "id": "1",
      "name": "My First Bot",
      "selected": true
    },
    {
      "id": "2",
      "name": "News Update Bot",
      "selected": false
    }
  ]
}
```

```js
  // 方式1：直接获取 initData 字符串
  const initData = window.Telegram.WebApp.initData;
  
  // 设置 Bot Token
  async function setBotToken(botToken) {
    const response = await fetch('/v1/tg2app/miniapp/set_bot_token', {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json',
        'X-Telegram-Init-Data': window.Telegram.WebApp.initData
      },
      body: JSON.stringify({
        bot_token: botToken
      })
    });

    if (!response.ok) {
      throw new Error('Failed to set bot token');
    }
  }
```

> chat: 根据文档讲 bot list 换成接口