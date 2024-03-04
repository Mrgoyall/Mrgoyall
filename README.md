- 👋 Hi, I’m @Mrgoyall
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Mrgoyall/Mrgoyall is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
```python
"""
Crypto Portfolio Tracker
Author: Mr. Goyall
Description: This program tracks the values of various cryptocurrencies in a portfolio.
"""

class CryptoPortfolio:
    def __init__(self, name):
        self.name = name
        self.portfolio = {}

    def add_coin(self, coin, amount):
        if coin in self.portfolio:
            self.portfolio[coin] += amount
        else:
            self.portfolio[coin] = amount

    def remove_coin(self, coin, amount):
        if coin in self.portfolio:
            if self.portfolio[coin] >= amount:
                self.portfolio[coin] -= amount
            else:
                print("Error: Not enough {} to remove.".format(coin))
        else:
            print("Error: {} not found in portfolio.".format(coin))

    def print_portfolio(self):
        print("Crypto Portfolio for", self.name)
        for coin, amount in self.portfolio.items():
            print(coin, ":", amount)

# Sample Usage
if __name__ == "__main__":
    portfolio = CryptoPortfolio("Mr. Goyall")
    portfolio.add_coin("BTC", 5)
    portfolio.add_coin("ETH", 10)
    portfolio.add_coin("BNB", 20)
    portfolio.add_coin("NFT", 50)

    portfolio.print_portfolio()
```
