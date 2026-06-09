# Ficha 2 — Componentes e Arquiteturas do VE 🔧

> Tema da Q2 do exame exemplo. Fonte: T1, slides A-62 a A-64 (Componentes de um VE; ISO/TR 8713) + Doc. B, cap. 1.

## 1. Nomenclatura (T1, A-62)

| Sigla PT | Sigla EN | Significado |
|---|---|---|
| **VEB** | BEV | VE a baterias |
| **VEPC** | FCEV | VE com células de combustível |
| **VEH** | HEV | VE híbrido |
| **VEH plug-in** | PHEV | híbrido "ligável" |
| **VMCI/VCI** | ICEV | veículo com motor de combustão interna |
| **SAER** | RESS | sistema de armazenamento de energia recarregável |

## 2. Componentes principais de um BEV (resposta à Q2)

1. **Bateria de tração (RESS)** — armazena a energia (Li-ião: LFP/NMC)
2. **BMS** — monitoriza e equilibra as células (tensão, temperatura, SoC, SoH) → ver [Ficha 3](ficha3_baterias.md)
3. **Inversor / conversor de potência** (DC→AC, IGBT/SiC) — alimenta e controla o motor
4. **Motor elétrico de tração** (MIA ou PMSM) → ver [Ficha 5](ficha5_motores.md)
5. **Transmissão** — redutor de relação fixa (sem caixa de velocidades)
6. **Carregador on-board** (AC) + tomada de **carregamento rápido DC**
7. **Conversor DC/DC** (rede de bordo 12 V) e **auxiliares** (climatização, direção)
8. **VCU** — unidade de controlo (pedal, travagem regenerativa, gestão de energia)

```
Carregador AC ──┐
                ▼
Rede ──► [BATERIA + BMS] ──► [INVERSOR DC/AC] ──► [MOTOR] ──► [TRANSMISSÃO] ──► Rodas
                │                    ▲   (travagem regenerativa: fluxo inverso)
                ├──► [DC/DC 12V] ──► auxiliares
                ▼
        Carreg. rápido DC
```

## 3. Arquiteturas (BEV / híbridos / FCEV)

- **BEV:** bateria → inversor → motor (cadeia única, simples e eficiente)
- **Híbrido série:** MCI move só um **gerador**; a tração é 100% elétrica (ex.: trens range-extender; é também a estrutura do FCEV, com a pilha no lugar do MCI)
- **Híbrido paralelo:** MCI **e** motor elétrico podem ambos mover as rodas (acoplamento mecânico)
- **Híbrido misto/série-paralelo:** combina os dois (Toyota Prius — engrenagem planetária)
- Classificação por grau de hibridização: micro < mild < full hybrid < PHEV
- **FCEV:** pilha de combustível + bateria tampão → ver [Ficha 4](ficha4_pilhas_combustivel.md)

## 4. O maior obstáculo: a bateria

- **Densidade energética** ~0,1–0,25 kWh/kg vs. ~12 kWh/kg da gasolina → autonomia/peso
- **Custo** (fração dominante do preço) e dependência de matérias-primas (Li, Co, Ni)
- **Tempo de carregamento** vs. minutos a abastecer; infraestrutura ("range anxiety")
- **Degradação** (ciclos, temperatura) — vida útil

## 5. Escolhas de projeto (slide A-64: "escolhas a efectuar")

Tensão do barramento DC (400 V vs. 800 V), química e dimensionamento da bateria (kWh vs. massa/custo), tipo de motor (MIA vs. PMSM — custo vs. rendimento), 1 motor + diferencial vs. motores por eixo/roda, potência de carregamento AC/DC.

## 6. Exercícios de treino

**E1.** Para que serve o conversor DC/DC num BEV?
<details><summary>Solução</summary>
Alimenta a rede de bordo de 12 V (luzes, infotainment, ECUs) a partir da bateria de tração de alta tensão — substitui o alternador do VMCI.
</details>

**E2.** Distingue híbrido série de paralelo numa frase cada.
<details><summary>Solução</summary>
Série: o MCI só gera eletricidade, a tração é sempre elétrica. Paralelo: MCI e motor elétrico podem ambos acionar mecanicamente as rodas.
</details>

**E3.** Porque é que a maioria dos BEVs não tem caixa de velocidades?
<details><summary>Solução</summary>
O motor elétrico dá binário máximo desde 0 rpm e funciona numa gama larga de velocidades (com enfraquecimento de campo) — basta um redutor fixo.
</details>

## Erros a evitar no exame

- Esquecer o **BMS** ou o **conversor DC/DC** na lista de componentes
- Não desenhar o **esboço da interligação** (a pergunta costuma pedi-lo)
- Apontar o motor como obstáculo principal — é a **bateria** (justificar com números)
- Confundir **carregador on-board (AC)** com o carregamento **rápido DC** (externo)
