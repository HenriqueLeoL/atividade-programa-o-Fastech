dados = []
continuar = 'S'

while continuar == "S":

    while True:
        elevador = input("Qual elevador mais utilizado? A/B/C: ").capitalize()
        if elevador in ["A", "B", "C"]:
            break
        else:
            print('Caractere inválido, tente novamente!')

    while True:
        período = input("Qual período? (M/V/N): ").capitalize()
        if período in ["M", "V", "N"]:
            break
        else:
            print('Caractere inválido, tente novamente!')

    dados.append((elevador, período))

    while True:
        continuar = input("Deseja adicionar mais? (S/N): ").capitalize()
        if continuar in ["S", "N"]:
            break
        else:
            print("Digite S ou N!")

print(f"\nDados coletados: {dados}\n")

contElevadorA = 0
contElevadorB = 0
contElevadorC = 0

for elevador, período in dados:
    if elevador == "A":
        contElevadorA += 1
    elif elevador == "B":
        contElevadorB += 1
    elif elevador == "C":
        contElevadorC += 1

if contElevadorA > contElevadorB and contElevadorA > contElevadorC:
    elevador_mais = "A"
    freq_elev = contElevadorA
elif contElevadorB > contElevadorA and contElevadorB > contElevadorC:
    elevador_mais = "B"
    freq_elev = contElevadorB
else:
    elevador_mais = "C"
    freq_elev = contElevadorC

#Periodos

contPeríodoM = 0
contPeríodoV = 0
contPeríodoN = 0

for elevador, período in dados:
    if período == "M":
        contPeríodoM += 1
    elif período == "V":
        contPeríodoV += 1
    elif período == "N":
        contPeríodoN += 1

#P mais usado
if contPeríodoM >= contPeríodoV and contPeríodoM >= contPeríodoN:
    período_mais = "M"
    freq_mais = contPeríodoM
elif contPeríodoV >= contPeríodoM and contPeríodoV >= contPeríodoN:
    período_mais = "V"
    freq_mais = contPeríodoV
else:
    período_mais = "N"
    freq_mais = contPeríodoN

#P menos usado
if contPeríodoM <= contPeríodoV and contPeríodoM <= contPeríodoN:
    período_menos = "M"
    freq_menos = contPeríodoM
elif contPeríodoV <= contPeríodoM and contPeríodoV <= contPeríodoN:
    período_menos = "V"
    freq_menos = contPeríodoV
else:
    período_menos = "N"
    freq_menos = contPeríodoN

#Mat

if freq_menos == 0:
    diferenca = 0
else:
    diferenca = ((freq_mais - freq_menos) / freq_menos) * 100

#Exibir

print("=" * 60)
print("RESULTADOS DA PESQUISA")
print("=" * 60)

print(f"\n ELEVADOR MAIS UTILIZADO: {elevador_mais}")
print(f"   Elevador A: {contElevadorA}")
print(f"   Elevador B: {contElevadorB}")
print(f"   Elevador C: {contElevadorC}")

nomes_período = {"M": "Matutino", "V": "Vespertino", "N": "Noturno"}

print(f"\n PERÍODO MAIS UTILIZADO: {nomes_período[período_mais]}")
print(f"   Matutino: {contPeríodoM}")
print(f"   Vespertino: {contPeríodoV}")
print(f"   Noturno: {contPeríodoN}")

print(f"\n DIFERENÇA PERCENTUAL:")
print(f"   Mais usado: {nomes_período[período_mais]} ({freq_mais})")
print(f"   Menos usado: {nomes_período[período_menos]} ({freq_menos})")
print(f"   Diferença: {diferenca:.2f}%")

print("\n" + "=" * 60)
