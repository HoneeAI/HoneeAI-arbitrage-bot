## Overview

This project is designed to run on a Raspberry Pi 24/7, scraping news data and enabling continuous arbitrage execution. The front-end dashboard, which can be started with `gatsby develop`, provides a visual interface for monitoring the bot's arbitrage performance and system activity.

---

## Quick Start with Docker

To quickly start the project using Docker, follow these steps from the root directory of the project:

### Clone the Repository

```bash
git clone https://github.com/roblen001/Crypto-Bot.git
cd Crypto-Bot
```

### Build Docker Image

```bash
docker build --no-cache -t gatsby-flask-app .
```

### Run Docker Container

```bash
docker run -p 5000:5000 -p 8000:8000 gatsby-flask-app
```

Head to `http://localhost:8000/` in your favorite browser.

---

## Project Structure

* **flask-api/**: Contains the backend Flask API for scraping news and running the arbitrage bot.
* **front-end/**: Contains the Gatsby-based front-end for the arbitrage dashboard.
* **strategy_testing/**: Contains data and scripts for testing various arbitrage strategies.

---

## Modifying the Flask App

The Flask app is located in the `flask-api/src/app/` directory.

### Key Components

* **app.py**: The main application file where the Flask app is initialized and routes are defined.
* **run_all_news_scraper.py**: Script to scrape all news data.
* **run_top_news_scraper.py**: Script to scrape top news data.
* **run_arbitrage_bot.py**: Script to run the arbitrage bot.
* **config.py**: Configuration file for the Flask app.

### How to Modify

* **Add New Routes**: Edit `app.py` and define new Flask routes as needed.
* **Update Scraping Logic**: Modify `run_all_news_scraper.py` or `run_top_news_scraper.py` to adjust how news data is scraped.
* **Adjust Arbitrage Logic**: Update `run_arbitrage_bot.py` to alter the bot’s arbitrage behavior, exchange connections, or spread detection mechanisms.

---

## Modifying the UI Arbitrage Dashboard

The front-end dashboard is located in the `front-end/` directory and uses Gatsby to create a dynamic web interface.

### Key Components

* **src/pages/**: Contains the main pages of the dashboard.
* **src/components/**: Contains React components used throughout the dashboard.
* **gatsby-config.js**: Configuration file for the Gatsby site.
* **gatsby-node.js**: Custom Node.js scripts for Gatsby.

### How to Modify

* **Update UI Components**: Edit files in `src/components/` to change the look and feel of dashboard components.
* **Add New Pages**: Create new pages in `src/pages/` to add new sections, such as arbitrage spread monitoring or exchange comparison views.
* **Modify Configuration**: Update `gatsby-config.js` and `gatsby-node.js` to change site settings or add custom Node.js functionality.

---

## Modifying and Running Individual Components of the Project

Developers are encouraged to explore and enhance the app and its arbitrage strategies. You can integrate trained reinforcement learning models from the existing agent to optimize arbitrage detection and execution, making it production-ready while efficiently managing capital allocation and risk exposure.

---

## Prerequisites

* Python 3.x
* Node.js and npm
* Gatsby CLI
* Docker

---

## Installation

### Clone the Repository

```bash
git clone https://github.com/roblen001/Crypto-Bot.git
```

### Set Up Flask API

```bash
cd flask-api
pip install -r requirements.txt
```

### Set Up Front-End

```bash
cd ../front-end
npm install
```

---

## Running the Project without Docker

### Start Flask API

```bash
cd flask-api/src/app
python app.py
```

### Start Front-End

```bash
cd front-end
gatsby develop
```

---

## Contributing

Contributions are welcome. Please fork the repository and submit a pull request with your improvements or arbitrage strategy enhancements.
