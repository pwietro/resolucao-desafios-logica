<div align="center">

<br>

⋆˙⟡ ·˚ ⋆ ·˚ ⟡˙⋆ ·˚ ⋆ ·˚ ⟡˙⋆

<br>

# resolucao-desafios-logica

*exercícios de lógica de programação resolvidos no BeeCrowd*

<br>

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![BeeCrowd](https://img.shields.io/badge/BeeCrowd-30BF56?style=flat-square&logo=codeforces&logoColor=white)

<br>

</div>

---

### ⟡ sobre

Repositório dedicado à prática constante de lógica de programação.
Todos os exercícios são resolvidos em **Python** e organizados por dificuldade.

---

### ˚✦ estrutura de pastas

```
resolucao-desafios-logica/
└── python/
    ├── facil/
    │   └── ...
    ├── medio/
    │   └── ...
    └── dificil/
        └── ...
```

---

### ⟡ exercícios — 3ª maratona beecrowd

#### ˚ python / médio

| # | nome | descrição |
|---|------|-----------|
| 01 | Quadrante | Dado um ponto (x, y), identifica se está na origem, em um dos eixos ou em qual quadrante do plano cartesiano |
| 02 | Display de LEDs | Calcula quantos segmentos de LED são necessários para exibir os dígitos de um número |
| 03 | Jogo de Palavras | Analisa palavras de um jogador e determina a pontuação com base em combinações de letras |
| 04 | Moeda Deslizante | Simula movimentos de uma moeda entre três posições (A, B, C) e retorna a posição final |

---

### ˚✦ soluções

<details>
<summary>⋆ 01 · Quadrante</summary>

```python
x, y = map(float, input().split())
if x == 0 and y == 0:
    print("Origem")
elif x == 0:
    print("Eixo Y")
elif y == 0:
    print("Eixo X")
elif x > 0 and y > 0:
    print("Q1")
elif x < 0 and y > 0:
    print("Q2")
elif x < 0 and y < 0:
    print("Q3")
else:
    print("Q4")
```

</details>

<details>
<summary>⋆ 02 · Display de LEDs</summary>

```python
n = int(input())
leds = {
    '0': 6, '1': 2, '2': 5, '3': 5, '4': 4,
    '5': 5, '6': 6, '7': 3, '8': 7, '9': 6
}
for _ in range(n):
    numero = input().strip()
    total = 0
    for digito in numero:
        total += leds[digito]
    print(f"{total} leds")
```

</details>

<details>
<summary>⋆ 03 · Jogo de Palavras</summary>

```python
n = int(input())
for _ in range(n):
    palavra = input().strip()
    if len(palavra) == 5:
        print(3)
    else:
        if (
            (palavra[0] == 'o' and palavra[1] == 'n') or
            (palavra[0] == 'o' and palavra[2] == 'e') or
            (palavra[1] == 'n' and palavra[2] == 'e')
        ):
            print(1)
        else:
            print(2)
```

</details>

<details>
<summary>⋆ 04 · Moeda Deslizante</summary>

```python
n = int(input())
moeda = input().strip()
for _ in range(n):
    movimento = int(input())
    if movimento == 1:
        if moeda == "A":
            moeda = "B"
        elif moeda == "B":
            moeda = "A"
    elif movimento == 2:
        if moeda == "B":
            moeda = "C"
        elif moeda == "C":
            moeda = "B"
    elif movimento == 3:
        if moeda == "A":
            moeda = "C"
        elif moeda == "C":
            moeda = "A"
print(moeda)
```

</details>

---

<div align="center">

⋆˙⟡ ·˚ ⋆ ·˚ ⟡˙⋆ ·˚ ⋆ ·˚ ⟡˙⋆

*resolvendo um problema por vez ˚*

</div>
