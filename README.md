# Price Watcher Bot

Telegram-бот, который следит за ценой товара/криптовалюты и присылает алерт, когда цена опускается до заданного порога.

## Быстрый старт (Docker)

```bash
docker build -t price-watcher:dev .
docker run -d \
  -e TG_TOKEN=<YOUR_TELEGRAM_BOT_TOKEN> \
  -e CFG_FILE=config.yaml \
  -v $(pwd)/app/config.example.yaml:/app/app/config.yaml \
  price-watcher:dev


sites:
  - url: "https://www.coingecko.com/en/coins/bitcoin"
    selector: "span.tw-text-gray-900"
    target_price: 60000
    chat_id: "123456789"
    interval_sec: 300
**Команда 2** – фиксируем файл:

```bash
git add README.md
git commit -m "Add README draft"
git push
