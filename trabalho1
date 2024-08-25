# Função para validar a temperatura
def validar_temperatura(temperatura):
    while True:
        try:
            temperatura = float(temperatura)
            if -60 <= temperatura <= 50:
                return temperatura
            else:
                print("Temperatura inválida. Por favor, informe uma temperatura entre -60 e 50 graus Celsius.")
                temperatura = input("Temperatura máxima do mês (Celsius): ")
        except ValueError:
            print("Temperatura inválida. Por favor, informe um número válido.")
            temperatura = input("Temperatura máxima do mês (Celsius): ")

# Função para obter o nome do mês em português
def obter_nome_mes(mes):
    meses = ["Janeiro", "Fevereiro", "Março", "Abril", "Maio", "Junho", 
             "Julho", "Agosto", "Setembro", "Outubro", "Novembro", "Dezembro"]
    return meses[mes - 1]

# Função para encontrar o mês mais quente
def obter_mes_mais_quente(temperaturas_mes):
    temperatura_maxima = max(temperaturas_mes)
    mes_mais_quente = temperaturas_mes.index(temperatura_maxima) + 1
    return obter_nome_mes(mes_mais_quente)

# Função para encontrar o mês menos quente
def obter_mes_menos_quente(temperaturas_mes):
    temperatura_minima = min(temperaturas_mes)
    mes_menos_quente = temperaturas_mes.index(temperatura_minima) + 1
    return obter_nome_mes(mes_menos_quente)

# Função principal para análise meteorológica
def analise_meteorologica():
    temperaturas = []
    meses_escaldantes = 0

    for mes in range(1, 13):
        print(f"Mês: {obter_nome_mes(mes)}")
        temperatura = validar_temperatura(input("Temperatura máxima do mês (Celsius): "))
        temperaturas.append(temperatura)

        if temperatura > 33:
            meses_escaldantes += 1

    temperatura_media = sum(temperaturas) / len(temperaturas)
    mes_mais_quente = obter_mes_mais_quente(temperaturas)
    mes_menos_quente = obter_mes_menos_quente(temperaturas)

    print(f"\nTemperatura média2 anual: {temperatura_media:.2f} graus Celsius")
    print(f"Quantidade de meses escaldantes: {meses_escaldantes}")
    print(f"Mês mais escaldante do ano: {mes_mais_quente}")
    print(f"Mês menos quente do ano: {mes_menos_quente}")

# Executar a função principal
analise_meteorologica()
