# Ficha 3 — Cálculo de Baterias 🔋

> Tema da Q3 do exame exemplo. Fonte: Tparte2 (Doc D/E — baterias), slides A-111 a A-134.

## 1. Definições essenciais

| Grandeza | Definição | Unidade |
|---|---|---|
| **Capacidade C** | Carga que a bateria fornece: C = I × t | Ah |
| **Energia E** | E = U × C (tensão × capacidade) | Wh |
| **Taxa de descarga (C-rate)** | I = k·C → "2C" numa bateria de 20 Ah = 40 A | — |
| **SoC** (State of Charge) | % de carga disponível | % |
| **DoD** (Depth of Discharge) | % descarregada (DoD = 100% − SoC) | % |
| **SoH** (State of Health) | Capacidade atual / capacidade nominal | % |
| **Energia específica** | Wh/kg (massa) | Wh/kg |
| **Densidade de energia** | Wh/dm³ (volume) | Wh/L |
| **ESR** | Resistência interna equivalente | mΩ |

**Notação C/x:** descarga completa em x horas. Ex.: bateria de 200 Ah a C/10 → 200/10 = **20 A durante 10 h**.

## 2. Associação de baterias

- **Série:** U soma, C mantém → U_t = n·U; C_t = C
- **Paralelo:** C soma, U mantém → U_t = U; C_t = n·C
- Em ambos os casos: **E_t = n·U·C** (a energia soma sempre)

⚠️ **Equalização:** células em série divergem (autodescarga e fabrico diferentes). Sem equalização, a célula mais fraca esgota primeiro e limita todo o conjunto (bateria "flat" — a célula vira resistência e a tensão colapsa). É uma das funções do **BMS**.

## 3. Capacidade depende da taxa de descarga (efeito Peukert)

A capacidade nominal das baterias de chumbo é definida para descarga lenta (**C/20**). Descargas mais rápidas ⇒ **capacidade efetiva menor** (perdas internas R·I², limitações da difusão química).

Lei de Peukert: **C_efetiva = C_nominal · (I_nominal / I)^(k−1)**, com k ≈ 1,1–1,3 (Pb-ácido); Li-ião é muito menos sensível (k ≈ 1,05).

Exemplo das aulas: bateria 42 Ah (definida a C/20). Descarregar a 2C₂₀ (84 A) ⇒ capacidade real **bem inferior** a 42 Ah. Para tração usar valores a C/5, C/3 ou 1C — confirmar com o fabricante.

## 4. Autonomia

**d [km] = E_disponível [Wh] / consumo [Wh/km]**

Na prática, E_disponível < E_nominal: limites de DoD (proteger ciclo de vida), temperatura, idade (SoH), taxa de descarga.

## 5. Exemplo resolvido (= Q3 do exame)

12 baterias **em série**, cada uma 12 V / 20 Ah (3~5C, ESR ≤ 60 mΩ):

1. **Tensão:** U = 12 × 12 = **144 V**
2. **Energia:** E = 144 V × 20 Ah = **2880 Wh ≈ 2,9 kWh**
3. **Autonomia** a 60 Wh/km: d = 2880/60 = **48 km**
4. **Influência da velocidade:**
   - Alta velocidade: P_aero ∝ v³ ⇒ consumo por km ∝ v² ⇒ autonomia cai muito
   - Corrente elevada (C-rate alto): Peukert + perdas ESR (P = R·I²) ⇒ menos energia útil
   - Velocidade muito baixa: auxiliares (≈ constantes no tempo) pesam mais por km
   - ⇒ existe uma **velocidade ótima moderada**

## 6. DOD e energia ao longo da vida (saiu no exame 2020/21!)

O ciclo de vida depende da profundidade de descarga: **menor DOD ⇒ mais ciclos**, e o ganho é mais do que proporcional.

**E_vida = DOD × E_célula × n.º de ciclos**

Exemplo (célula LFP 3,2 V / 50 Ah = 160 Wh; 80% DOD ≥ 2000 ciclos; 70% DOD ≥ 3500 ciclos):

- 80% DOD: 0,8×160×2000 = **256 kWh**
- 70% DOD: 0,7×160×3500 = **392 kWh** → +53%! Por isso os BEVs limitam a janela de SoC.

## 7. Exercícios de treino

**E1.** 8 baterias de 12 V/55 Ah em série. U? E? Autonomia a 150 Wh/km?
<details><summary>Solução</summary>
U = 96 V; E = 96 × 55 = 5280 Wh; d = 5280/150 = 35,2 km
</details>

**E2.** Para 96 V com células de 3,2 V (LFP, 100 Ah), quantas em série? E se quiser 19,2 kWh, quantos ramos em paralelo?
<details><summary>Solução</summary>
Série: 96/3,2 = 30 células. Um ramo: 96 V × 100 Ah = 9,6 kWh → 2 ramos em paralelo (30s2p = 60 células).
</details>

**E3.** Bateria de 20 Ah a 3C: que corrente? Quanto tempo dura (ideal)?
<details><summary>Solução</summary>
I = 3 × 20 = 60 A; t = 20/60 h = 20 min (na prática menos, por Peukert/perdas).
</details>

## Erros a evitar no exame

- Confundir **Ah com Wh** (capacidade ≠ energia)
- Somar capacidades em **série** (não soma! só em paralelo)
- Esquecer que a autonomia calculada é **ideal** — referir sempre os fatores que a reduzem
- Não identificar grandezas e unidades (o enunciado pede explicitamente)
