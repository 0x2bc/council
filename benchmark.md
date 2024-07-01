# Description
This script fetches historical cryptocurrency data from CoinGecko and current market data from CoinMarketCap for a predefined list of tokens. The script calculates the average price for a specific date and prints the data in CSV format. The script includes API requests to CoinGecko for historical prices and to CoinMarketCap for market cap information, handling API keys and request delays to avoid rate limits.

# Usage
Add your CoinGecko and CoinMarketCap API keys in place of the placeholders.
Run the script to fetch data and print it in CSV format.

# Script

``` import requests
from datetime import datetime, timedelta
import time

# Your API keys
cg_api_key = 'YOUR_COINGECKO_API_KEY'
cmc_api_key = 'YOUR_COINMARKETCAP_API_KEY'

# List of tokens with their CoinGecko API IDs and CoinMarketCap details
tokens = {
    'Friend.tech': {'cg_id': 'friend-tech', 'ticker': 'FRIEND', 'cmc_id': 31056},
    'Theta Network': {'cg_id': 'theta-token', 'ticker': 'THETA', 'cmc_id': 2416},
    'Chiliz': {'cg_id': 'chiliz', 'ticker': 'CHZ', 'cmc_id': 4066},
    'Joystream': {'cg_id': 'joystream', 'ticker': 'JOY', 'cmc_id': 6827},
    'Cyber': {'cg_id': 'cyberconnect', 'ticker': 'CYBER', 'cmc_id': 24781},
    'LimeWire': {'cg_id': 'limewire-token', 'ticker': 'LMWR', 'cmc_id': 24476},
    'Decentralized Social': {'cg_id': 'deso', 'ticker': 'DESO', 'cmc_id': 10442},
    'Rally': {'cg_id': 'rally-2', 'ticker': 'RLY', 'cmc_id': 8075},
    'XCAD Network': {'cg_id': 'xcad-network', 'ticker': 'XCAD', 'cmc_id': 9868},
    'Hive': {'cg_id': 'hive', 'ticker': 'HIVE', 'cmc_id': 5370},
    'Steem': {'cg_id': 'steem', 'ticker': 'STEEM', 'cmc_id': 1230},
    'MovieBloc': {'cg_id': 'moviebloc', 'ticker': 'MBL', 'cmc_id': 4038},
    'Contentos': {'cg_id': 'contentos', 'ticker': 'COS', 'cmc_id': 4036},
    'Torum': {'cg_id': 'torum', 'ticker': 'XTM', 'cmc_id': 10421},
    'Only1': {'cg_id': 'only1', 'ticker': 'LIKE', 'cmc_id': 10891},
    'WeWay': {'cg_id': 'weway', 'ticker': 'WWY', 'cmc_id': 17047},
    'Gifto': {'cg_id': 'gifto', 'ticker': 'GFT', 'cmc_id': 2289},
    'Audius': {'cg_id': 'audius', 'ticker': 'AUDIO', 'cmc_id': 7455},
    'Beoble': {'cg_id': 'beoble', 'ticker': 'BBL', 'cmc_id': 28823},
    'Inspect': {'cg_id': 'inspect', 'ticker': 'INSP', 'cmc_id': 28610},
    'LBRY Credits': {'cg_id': 'lbry-credits', 'ticker': 'LBC', 'cmc_id': 1298},
    'Livepeer': {'cg_id': 'livepeer', 'ticker': 'LPT', 'cmc_id': 3640}
}

# Function to fetch historical data from CoinGecko
def fetch_historical_data_cg(token_id, date):
    url = f"https://api.coingecko.com/api/v3/coins/{token_id}/history"
    parameters = {
        'date': date,
        'localization': 'false',
        'x_cg_demo_api_key': cg_api_key
    }
    response = requests.get(url, params=parameters)
    if response.status_code == 200:
        return response.json()
    else:
        print(f"Error fetching data from CoinGecko for token {token_id} on {date}: {response.status_code} - {response.text}")
        return None

# Function to fetch data from CoinMarketCap
def fetch_data_cmc(cmc_id):
    url = f"https://pro-api.coinmarketcap.com/v1/cryptocurrency/quotes/latest"
    parameters = {
        'id': cmc_id,
        'convert': 'USD'
    }
    headers = {
        'X-CMC_PRO_API_KEY': cmc_api_key
    }
    response = requests.get(url, headers=headers, params=parameters)
    if response.status_code == 200:
        return response.json()
    else:
        print(f"Error fetching data from CoinMarketCap for id {cmc_id}: {response.status_code} - {response.text}")
        return None

# Date for July 1, 2024
date = '01-07-2024'

# Current date for comparison
current_date = datetime.now()

# Fetch data and store in a dictionary
data = {token_name: {} for token_name in tokens}
cmc_data = {token_name: {} for token_name in tokens}

for token_name, details in tokens.items():
    print(f"Fetching data for {token_name} ({details['cg_id']}):")
    date_obj = datetime.strptime(date, '%d-%m-%Y')
    if date_obj <= current_date:
        print(f"  Fetching price for {date}...")
        historical_data = fetch_historical_data_cg(details['cg_id'], date)
        if historical_data:
            market_data = historical_data.get('market_data', {})
            current_price = market_data.get('current_price', {}).get('usd', 'N/A')
            if current_price == 0:
                current_price = 'N/A'
        else:
            current_price = 'N/A'
        data[token_name][date] = current_price
        time.sleep(5)  # Add a delay of 5 seconds between requests
    
    # Fetching CoinMarketCap data
    print(f"  Fetching market cap data for {details['ticker']} from CoinMarketCap...")
    cmc_info = fetch_data_cmc(details['cmc_id'])
    if cmc_info and str(details['cmc_id']) in cmc_info['data']:
        cmc_info = cmc_info['data'][str(details['cmc_id'])]
        cmc_data[token_name] = {
            'fully_diluted_mcap': cmc_info['quote']['USD'].get('fully_diluted_market_cap', 'N/A') / 1_000_000,
            'current_circulation_mcap': cmc_info['quote']['USD'].get('market_cap', 'N/A') / 1_000_000
        }
    else:
        cmc_data[token_name] = {
            'fully_diluted_mcap': 'N/A',
            'current_circulation_mcap': 'N/A'
        }
    time.sleep(5)  # Add a delay of 5 seconds between requests

# Calculate averages
averages = {date: []}
for token_name, prices in data.items():
    price = prices.get(date, 'N/A')
    if price != 'N/A':
        try:
            averages[date].append(float(price))
        except ValueError:
            pass

# Print data in CSV format
header = ["Token Name", "Ticker", "Fully Diluted Mcap (M)", "Current Circulation Mcap (M)", date]
print(",".join(header))

for token_name, prices in data.items():
    row = [
        token_name,
        tokens[token_name]['ticker'],
        f"{cmc_data[token_name]['fully_diluted_mcap']:.2f}" if cmc_data[token_name]['fully_diluted_mcap'] != 'N/A' else 'N/A',
        f"{cmc_data[token_name]['current_circulation_mcap']:.2f}" if cmc_data[token_name]['current_circulation_mcap'] != 'N/A' else 'N/A',
        str(prices.get(date, 'N/A'))
    ]
    print(",".join(row))

# Print averages
average_row = ["Average", "", "", ""]
if averages[date]:
    average_value = sum(averages[date]) / len(averages[date])
    average_row.append(f"{average_value:.6f}")
else:
    average_row.append("N/A")
print(",".join(average_row))
```
