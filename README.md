# projeto-em-python_finance
import yfinance as yf
import matplotlib.pyplot as plt

def baixa_dados(acao="PETR4.SA"):
  dados = yf.download(acao, start="2023-01-01", end="2024-01-01")
  return dados["Close"]

precos = baixa_dados()
plt.plot(precos)
plt.title("preço de fechamento -PETR4")
plt.xlabel("Data")
plt.ylabel("Preço")
plt.show()
