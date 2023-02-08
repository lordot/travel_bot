Travel Currency Bot
=====

Travel Currency Bot is a telegram bot that allows you to convert the currency of any country into dollars and rubles on the fly. Currency conversion works out of the box: IDR, GEL and THB




## Installation

This repository can be run on the Heroku cloud platform or any other PaaS such as Dokku.

For correct operation, you need to forward any port for Webhook telegram messages. Requires an SSL certificate configured on the web server.




## Environment Variables

To run this project, you will need to add the following environment variables to your .env file

`TOKEN = <YOUR_TELEGRAM_BOT_TOKEN>`

`PORT = <YOUR_EXTERNAL_PORT_FOR_WEBHOOK>(Default 8443)`

`APP_DOMAIN = <YOUR_SERVER_DOMAIN_NAME>`
## FAQ

#### How to add your own currency?

You can edit the file database/Create_database.py. This method requires deleting the old database and restarting the bot:
    
    # edit Create_database.py:

    def _load_data(session: Session):
    <ANY> = Currency(name='<CURRENCY_NAME>', rate=<RATE>, api_url='<API_URL_FOR_RATE_UPDATES>')

Or you can edit the 'currencies' table of the database.
## Roadmap

- Automatic exchange rate update via API


## Demo

https://t.me/travel_cur_bot

