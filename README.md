## Features
- Low latency replies (it usually takes about 3-5 seconds)
- No request limits
- Message streaming (watch demo)
- GPT-4 support
- Voice message recognition
- Code highlighting
- Special chat modes: 👩🏼‍🎓 Assistant, 👩🏼‍💻 Code Assistant, 📝 Text Improver and 🎬 Movie Expert. You can easily create your own chat modes by editing `config/chat_modes.yml`
- Support of [ChatGPT API](https://platform.openai.com/docs/guides/chat/introduction)
- List of allowed Telegram users
- Track $ balance spent on OpenAI API

<p align="center">
  <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExYmM2ZWVjY2M4NWQ3ZThkYmQ3MDhmMTEzZGUwOGFmOThlMDIzZGM4YiZjdD1n/unx907h7GSiLAugzVX/giphy.gif" />
</p>

---

## 🤑 Payments
[My bot](https://t.me/chatgpt_karfly_bot) supports many payments providers:
- 💎 Crypto
- [Stripe](https://stripe.com)
- [Smart Glocal](https://smart-glocal.com)
- [Unlimint](https://www.unlimint.com)
- [ЮMoney](https://yoomoney.ru)
- and [many-many other](https://core.telegram.org/bots/payments#supported-payment-providers)

If you want to add payments to your bot – write me on Telegram ([@karfly](https://t.me/karfly)).

## News
- *24 Mar 2023*: GPT-4 support. Run `/settings` command to choose model
- *15 Mar 2023*: Added message streaming. Now you don't have to wait until the whole message is ready, it's streamed to Telegram part-by-part (watch demo)
- *9 Mar 2023*: Now you can easily create your own Chat Modes by editing `config/chat_modes.yml`
- *8 Mar 2023*: Added voice message recognition with [OpenAI Whisper API](https://openai.com/blog/introducing-chatgpt-and-whisper-apis). Record a voice message and ChatGPT will answer you!
- *2 Mar 2023*: Added support of [ChatGPT API](https://platform.openai.com/docs/guides/chat/introduction). It's enabled by default and can be disabled with `use_chatgpt_api` option in config. Don't forget to **rebuild** you docker image (`--build`).

## Bot commands
- `/retry` – Regenerate last bot answer
- `/new` – Start new dialog
- `/mode` – Select chat mode
- `/balance` – Show balance
- `/settings` – Show settings
- `/help` – Show help

## Setup
1. Get your [OpenAI API](https://openai.com/api/) key

2. Get your Telegram bot token from [@BotFather](https://t.me/BotFather)

3. Edit `config/config.example.yml` to set your tokens and run 2 commands below (*if you're advanced user, you can also edit* `config/config.example.env`):
    ```bash
    mv config/config.example.yml config/config.yml
    mv config/config.example.env config/config.env
    ```

4. 🔥 And now **run**:
    ```bash
    docker-compose --env-file config/config.env up --build
    ```

## ❤️ Top donations
You can be in this list: <a href="https://github.com/karfly/chatgpt_telegram_bot/blob/main/static/donate/donate.md#%EF%B8%8F-donate" alt="Donate shield"><img src="https://img.shields.io/badge/-Donate-red?logo=undertale" /></a>

1. [Ilias Ism](https://twitter.com/illyism). Donation: **69$**

    *Message:* I wanted to thank you for your amazing code! It helped me start my own Telegram ChatGPT bot and add a bunch of cool features. I really appreciate your hard work on this project. For anyone interested in trying my bot, feel free to check it out here: [magicbuddy.chat](https://magicbuddy.chat) 🤖 Thanks again! 😊

2. [Alexander Zimin](https://t.me/azimin). Donation: **50$**

3. [Hans Blinken](https://t.me/hblink). Donation: **10$**

## References
1. [*Build ChatGPT from GPT-3*](https://learnprompting.org/docs/applied_prompting/build_chatgpt)
