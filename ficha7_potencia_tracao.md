# Ficha 7 — Cálculo da Potência de Tração ⚙️

> Fonte: T1, slides A-96 a A-105 (Vehicle Dynamics, Road Load Forces and Power) + Tparte3 Doc L/J (ferroviário).

## 1. Forças de resistência ao movimento (road load)

A força total que se opõe ao movimento:

**F_R = F_RR + F_DA + F_I = μ_RR·m·g + ½·ρ·C_D·A_F·v² + m·g·sin α**

### a) Resistência ao rolamento

**F_RR = μ_RR · m · g**

- μ_RR: coeficiente de resistência ao rolamento — **0,015** pneus convencionais; **0,005** pneus para VEs (Larminie)
- Domina a **baixas velocidades**
- Mede-se puxando o veículo a velocidade constante muito baixa

### b) Resistência aerodinâmica

**F_DA = ½ · ρ · C_D · A_F · v²**

- ρ: densidade do ar (≈1,2 kg/m³, depende de pressão e temperatura); C_D: coeficiente de arrasto; A_F: área frontal; v: velocidade **relativa ao vento**
- Domina a **altas velocidades**
- Potência correspondente cresce com o **cubo**: P_DA = F_DA·v ∝ v³

### c) Inclinação da estrada (rampa)

**F_I = m · g · sin α**

- Independente da velocidade; positiva a subir, negativa a descer
- Declive em % ⇒ sin α ≈ tan α = declive/100 (para ângulos pequenos)

### d) Aceleração (força de inércia)

**F_a = m · a** (rigorosamente, com massa equivalente k_m·m, k_m ≈ 1,04–1,1, pelas inércias rotativas)

## 2. Potência e energia

**P = F_total · v** [W]  (com F em N e v em m/s)

**Consumo [Wh/km] = P[W] / v[km/h]** (à roda; dividir pelo rendimento da cadeia para obter consumo à bateria)

**Forma alternativa (coast-down EPA):** F_r = A + B·v + C·v² ⇒ **P = A·v + B·v² + C·v³**
(A ↔ rolamento; B ↔ perdas rotacionais; C ↔ aerodinâmica)

## 3. Do movimento ao motor

- Binário na roda: **T_roda = r · F_R** (r = raio da roda)
- Binário visto do motor: **T_R = (r/i) · F_R** (i = razão de transmissão)
- Dinâmica: **T_m − T_r = J_T · dω_m/dt**, com J_T = J_m + J_r + J_v e **J_v = m·(r/i)²**
- Velocidade: ω_roda = v/r; ω_motor = i·ω_roda

## 4. Como reduzir a potência necessária

Atuar em: **μ_RR** (pneus), **m** (massa), **C_D** e **A_F** (aerodinâmica), **v** (velocidade). É aqui que os fabricantes trabalham (ex.: Mercedes EQXX ~1200 km; Tesla Semi mais eficiente que uma carrinha por tonelada).

## 5. Exemplo resolvido

VE: m = 1500 kg, μ_RR = 0,01, C_D = 0,30, A_F = 2,2 m², ρ = 1,2 kg/m³, a 100 km/h (27,8 m/s) em estrada plana:

1. F_RR = 0,01 × 1500 × 9,81 = **147 N**
2. F_DA = ½ × 1,2 × 0,30 × 2,2 × 27,8² = **306 N**
3. F_R = 147 + 306 = **453 N**
4. **P = 453 × 27,8 ≈ 12,6 kW** (à roda)
5. Consumo à roda: 12 600/100 = **126 Wh/km**; com η = 85% da cadeia: ≈ **148 Wh/km** à bateria

Com rampa de 5% à mesma velocidade: F_I = 1500 × 9,81 × 0,05 = 736 N ⇒ F_total = 1189 N ⇒ **P ≈ 33 kW** — a rampa quase triplica a potência!

## 6. Nota ferroviária (Tparte3, Doc L/J)

No comboio o princípio é o mesmo, com termos próprios: resistência ao avanço (fórmula tipo Davis, a + b·v + c·v²), **força devida às curvas** e **aos túneis**, aderência roda-carril (aço-aço, μ ≈ 0,1–0,3, muito menor que pneu-asfalto — limita a força de tração máxima: F_max = μ·P_aderente), e transmissão elástica motor-eixo no bogie.

## 7. Exercício de treino

Calcula a potência para o mesmo VE a 120 km/h (33,3 m/s), plano.
<details><summary>Solução</summary>
F_RR = 147 N; F_DA = ½×1,2×0,3×2,2×33,3² = 439 N; F_R = 586 N; P = 586×33,3 ≈ 19,5 kW.
De 100→120 km/h (+20%) a potência sobe ~55% — eis o v³.
</details>

## Erros a evitar

- Usar v em **km/h** nas fórmulas (tem de ser **m/s**: km/h ÷ 3,6)
- Esquecer que F_DA usa a velocidade **relativa ao vento**
- Confundir potência **à roda** com potência **à bateria** (dividir pelo rendimento)
- No ferroviário, esquecer o limite de **aderência** roda-carril
