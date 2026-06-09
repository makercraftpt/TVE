# Ficha 6 — Normas UIC: Disposição dos Eixos e Rodados 🚂

> Tema da Q6 do exame exemplo. Fonte: Tparte3 (Tecnologias Ferroviárias — Doc. J e L, secção 2 "Disposição dos eixos e designação dos eixos motores").

## 1. A norma UIC (a que está em vigor)

Designa a disposição dos rodados de uma locomotiva/unidade motora:

| Símbolo | Significado |
|---|---|
| **Letra** (A, B, C, D…) | n.º de eixos **motores** consecutivos: A=1, B=2, C=3, D=4 |
| **Algarismo** (1, 2…) | n.º de eixos **livres** (não motores) |
| **' (apóstrofo)** | o grupo está montado num **bogie** (chassis orientável independente da caixa) |
| **o** (índice) | eixos com **motores individuais** (um motor por eixo) |
| **( )** | agrupa eixos no mesmo bogie quando há mistura (ex.: (A1A)) |

## 2. As três designações do exame

**Co'Co'** — 2 bogies, cada um com **3 eixos motores** (6 no total). Locomotivas pesadas (mercadorias): grande força de tração, peso aderente distribuído.

```
  ●●●     ●●●      ● = eixo motor
 [bogie] [bogie]
```

**Bo'Bo'** — 2 bogies, cada um com **2 eixos motores individuais** (4 no total). A configuração **mais comum** nas locomotivas elétricas modernas e UMEs.

```
  ●●       ●●
 [bogie] [bogie]
```

**(A1A)(A1A)** — 2 bogies de 3 eixos com o **central livre**: motor–livre–motor (4 motores + 2 livres). Serve para **reduzir a carga por eixo** (linhas com limite de peso) mantendo o comprimento do bogie.

```
  ●○●     ●○●      ○ = eixo livre
 [bogie] [bogie]
```

**Exemplos reais:** CP 5600 — Bo'Bo'; locomotivas de mercadorias pesadas (ex.: Euro 6000) — Co'Co'; ALCO FA / nohab antigas — (A1A)(A1A).

## 3. Normas antigas (referir como "desatualizadas")

**Notação Whyte** (era do vapor) — conta **rodas** (não eixos), em três grupos: dianteiras–motoras–traseiras. Ex.: 4-6-2 "Pacific" = 4 rodas livres à frente + 6 motoras + 2 livres atrás. Aplicada às elétricas: Bo'Bo' ≈ 0-4-4-0; Co'Co' ≈ 0-6-6-0. **Limitação:** não distingue bogies, motores individuais nem eixos livres interiores.

**Classificação francesa** — como a Whyte mas conta **eixos**: 0-3-3-0 ≡ Co'Co'; 0-2-2-0 ≡ Bo'Bo'.

## 4. Porque importa a disposição dos eixos

- **Força de tração máxima** limitada pela aderência: F_max = μ·P_aderente (μ aço-aço ≈ 0,1–0,3) — só conta o peso sobre os **eixos motores** → ver [Ficha 7](ficha7_potencia_tracao.md)
- **Carga por eixo** limitada pela via (ex.: 22,5 t/eixo) → mais eixos para distribuir o peso
- **Bogies** orientáveis → inscrição em curva, conforto, menor desgaste roda-carril
- Motores individuais ("o") com transmissão elástica motor-eixo → menos massas não suspensas

## 5. Exercícios de treino

**E1.** O que significa B'B'?
<details><summary>Solução</summary>
2 bogies, cada um com 2 eixos motores acoplados mecanicamente (acionados pelo mesmo motor — sem o índice "o" não são motores individuais).
</details>

**E2.** Uma locomotiva de 120 t, Co'Co', todos os eixos motores. Carga por eixo? E se fosse (A1A)(A1A) com o mesmo peso?
<details><summary>Solução</summary>
Co'Co': 120/6 = 20 t/eixo, todo o peso é aderente. (A1A)(A1A): também 20 t/eixo, mas só 4×20 = 80 t são peso aderente → menos força de tração disponível.
</details>

**E3.** Escreve a designação UIC de uma automotora com 2 bogies: o da frente com 2 eixos motores individuais, o de trás com 2 eixos livres.
<details><summary>Solução</summary>
Bo'2'
</details>

## Erros a evitar no exame

- Trocar letras (motores) com algarismos (livres)
- Esquecer o significado do **apóstrofo** (bogie) e do **"o"** (motores individuais)
- Na Whyte, contar **eixos** em vez de **rodas** (é ao contrário da francesa)
- Esquecer que em (A1A) o peso do eixo central **não é aderente**
