# trading_bot
# Binance Futures Testnet Trading Bot

A Python-based command-line trading bot that places **Market** and **Limit** orders on the **Binance USDT-M Futures Testnet** using the Binance API.

## Features

- Place **Market** orders
- Place **Limit** orders
- Supports **BUY** and **SELL**
- Command-line interface (CLI)
- Input validation
- Logging of API requests, responses, and errors
- Exception handling for API and network errors
- Modular project structure for easy maintenance

## Project Structure

```
trading_bot/
│
├── bot/
│   ├── client.py
│   ├── orders.py
│   ├── validators.py
│   ├── logging_config.py
│   └── __init__.py
│
├── logs/
│   └── trading.log
│
├── cli.py
├── requirements.txt
├── README.md
├── .env.example
└── .gitignore
```

## Requirements

- Python 3.10+
- Binance Futures Testnet Account
- Binance Testnet API Key and Secret

## Installation

1. Clone the repository:

```bash
git clone https://github.com/your-username/trading_bot.git
cd trading_bot
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Create a `.env` file:

```env
API_KEY=YOUR_BINANCE_TESTNET_API_KEY
API_SECRET=YOUR_BINANCE_TESTNET_API_SECRET
```

## Running the Application

### Market Order

```bash
python cli.py --symbol BTCUSDT --side BUY --type MARKET --quantity 0.001
```

### Limit Order

```bash
python cli.py --symbol BTCUSDT --side SELL --type LIMIT --quantity 0.001 --price 65000
```

## Example Output

```
========== Order Summary ==========
Symbol : BTCUSDT
Side   : BUY
Type   : MARKET
Quantity : 0.001

Order Successfully Placed

Order ID      : 123456789
Status        : FILLED
Executed Qty  : 0.001
Average Price : 60500.50
```

## Logging

All API requests, responses, and errors are logged in:

```
logs/trading.log
```

## Error Handling

The application handles:

- Invalid user input
- Invalid trading symbols
- Missing limit price
- Binance API errors
- Authentication failures
- Network failures
- Unexpected exceptions

## Assumptions

- The user has a Binance Futures Testnet account.
- API credentials are valid.
- Internet connectivity is available.
- The account has sufficient testnet balance.

## Technologies Used

- Python 3
- python-binance
- argparse
- python-dotenv
- logging

## License

This project was created as part of a Python Developer technical assessment.
