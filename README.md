# planilha
import pandas as pd

# Ler o arquivo Excel
nome_arquivo = 'compra_venda_avancado.xlsx'
df = pd.read_excel(nome_arquivo, sheet_name='Sheet1')

# Mostrar os dados lidos
print("Dados de Compra, Venda, Troca e Devolução:")
print(df)

# Calcular o total de compras, vendas, trocas e devoluções
total_compras = df['Compra'].sum()
total_vendas = df['Venda'].sum()
total_trocas = df['Troca'].sum()
total_devolucoes = df['Devolução'].sum()

# Mostrar o total de compras, vendas, trocas e devoluções
print(f"\nTotal de Compras: {total_compras}")
print(f"Total de Vendas: {total_vendas}")
print(f"Total de Trocas: {total_trocas}")
print(f"Total de Devoluções: {total_devolucoes}")

# Calcular o lucro (vendas - compras + trocas - devoluções)
lucro = total_vendas - total_compras + total_trocas - total_devolucoes
print(f"\nLucro Total: {lucro}")
