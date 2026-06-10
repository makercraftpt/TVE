# Exame 2020/21 (Época de Recurso) — Resolvido 📝

**Exame:** TVE 2020/21, Época de Recurso, 20/07/2021, 18:30 — 1h30 — Prof. Paulo Pereirinha
**Cotação (12 valores):** Q1–1,5 | Q2–1,3 | Q3–1,8 | Q4–1,8 | Q5–1,5 | Q6–1,4 | Q7–1,4 | Q8–1,3

> Instruções do enunciado: "Identifique todas as grandezas e símbolos que utilizar. Responda de forma direta e concisa."

---

## Q1 — Poluentes dos VMCI, efeito na saúde; poço-à-roda vs. ciclo de vida (1,5 v)

**Principais poluentes dos motores de combustão interna e efeitos na saúde:**

| Poluente | Efeito na saúde humana |
|---|---|
| **NOx** (óxidos de azoto) | irritação respiratória, asma; precursor do ozono troposférico e das chuvas ácidas |
| **Partículas (PM10/PM2,5)** | penetram nos pulmões e corrente sanguínea — doenças cardiovasculares e respiratórias, cancro |
| **CO** (monóxido de carbono) | liga-se à hemoglobina (carboxihemoglobina) — reduz transporte de O₂; letal em concentração |
| **HC / COV** (hidrocarbonetos não queimados) | cancerígenos (benzeno); precursores de smog fotoquímico |
| **CO₂** | não é tóxico, mas é o principal gás com efeito de estufa (alterações climáticas) |

**Como os VEs reduzem estes problemas:** têm **zero emissões locais** (TTW) — retiram os poluentes das cidades, onde está a densidade populacional. As emissões que existirem ficam concentradas nas centrais elétricas (fora das zonas urbanas, com filtragem controlada) e diminuem com a descarbonização do mix. Além disso, o rendimento do VE é muito superior (ver [Ficha 8](ficha8_well_to_wheel.md)) e a travagem regenerativa recupera energia.

**Poço-à-roda (WTW) vs. ciclo de vida (LCA):**

- **WTW** analisa apenas a cadeia **energética** da utilização: obtenção/transporte da energia (WTT) + conversão no veículo (TTW).
- **LCA** (análise de ciclo de vida) vai mais longe: inclui também o **fabrico** do veículo e componentes (baterias!), materiais, transporte, manutenção e **fim de vida** (reciclagem). Cf. ferramenta GREET (ANL).
- Ou seja: WTW ⊂ LCA. Um BEV pode ter mais emissões **de fabrico** que um VMCI (bateria), compensadas durante a utilização.

---

## Q2 — Porque venceram os VMCI a partir dos anos 20; que razões persistem (1,3 v)

(= Q1 do exame 2011/12 com um acrescento — ver [Ficha 1](ficha1_historia.md))

**Razões da vitória dos VMCI (~década de 1920):**

1. **Baixa densidade energética das baterias** (Pb-ácido ~30 Wh/kg vs. ~12 000 Wh/kg da gasolina) → autonomia muito limitada
2. **Ford Model T** — produção em série, preço acessível
3. **Arranque elétrico** (Kettering, 1912) — eliminou a manivela, principal incómodo do MCI
4. **Petróleo barato e abundante**; abastecimento em minutos
5. Expansão da **rede de estradas** → necessidade de autonomia que o VE não dava

**Quais persistem como obstáculo (e porquê):**

- **Densidade energética da bateria** — ainda hoje (Li-ião ~150–250 Wh/kg) é ~50× inferior à gasolina: autonomia menor e peso elevado. É o obstáculo de fundo.
- **Tempo de "abastecimento"** — carregar demora dezenas de minutos vs. minutos a atestar; exige infraestrutura de carregamento densa.
- **Custo** associado à bateria (embora em queda acentuada).
- Já **não** persistem: o arranque (irrelevante), o preço do petróleo (volátil e taxado), e a produção em série (os VEs já a têm).

---

## Q3 — VE numa rampa: forças, dependências, atuação dos fabricantes (1,8 v)

(ver [Ficha 7](ficha7_potencia_tracao.md))

**Esboço** — VE numa rampa de ângulo α, com as forças aplicadas:

```
            ↗ v (movimento)
           ╱
     ┌────╱───┐   F_t (tração, no sentido do movimento)
     │ VE ╱   │ → F_DA (aerodinâmica, contra o movimento)
     └───╱────┘ → F_RR (rolamento, contra o movimento)
        ╱ α      ↘ m·g·sin α (componente do peso na rampa)
   ────╱──────── ↓ m·g (peso)   ↑ N (reação normal = m·g·cos α)
```

**Componentes da força total de resistência: F_R = F_RR + F_DA + F_I (+ F_a):**

| Força | Expressão | Depende de |
|---|---|---|
| **Rolamento** | F_RR = μ_RR·m·g·cos α | tipo de pneus (μ_RR ≈ 0,015 convencional; 0,005 p/ VE), massa, piso |
| **Aerodinâmica** | F_DA = ½·ρ·C_D·A_F·v² | densidade do ar, coef. de arrasto C_D, área frontal A_F, **quadrado** da velocidade relativa ao vento |
| **Rampa** | F_I = m·g·sin α | massa e inclinação (positiva a subir, recuperável a descer) |
| **Inércia** (se acelera) | F_a = k_m·m·a | massa (com k_m ≈ 1,04–1,1 pelas inércias rotativas) e aceleração |

**Onde atuam os fabricantes para baixar o consumo:**

- **Aerodinâmica:** reduzir C_D (formas, puxadores embutidos, fundo plano) e A_F
- **Pneus** de baixa resistência ao rolamento (μ_RR)
- **Massa:** materiais leves (alumínio, compósitos), integração estrutural da bateria
- **Cadeia de tração:** rendimento do motor/inversor (SiC), travagem regenerativa
- Auxiliares eficientes (bomba de calor) — ex.: Mercedes EQXX (>1000 km de autonomia)

---

## Q4 — Célula LiFePO₄: parâmetros e energia extraível ao longo da vida (1,8 v)

**Significado dos parâmetros da tabela:**

| Parâmetro | Valor | Significado |
|---|---|---|
| Nominal Capacity | **50 Ah** | carga que a célula fornece numa descarga completa (C = I·t) |
| Impedance | **< 0,8 mΩ** | resistência interna (ESR) — perdas P = R·I², aquecimento, queda de tensão |
| Specific Energy | **98 Wh/kg** | energia por unidade de **massa** |
| Volumetric Specific Energy | **146 Wh/L** | energia por unidade de **volume** |
| Weight | **1,8 kg** | massa da célula |
| Nominal Voltage | **3,2 V** | tensão média de descarga (típica do LFP) |
| Charge Voltage (CC-CV) | **3,65 V** | tensão final de carga na fase CV |
| Discharge Cut-off | **2,8 V** | tensão mínima admissível — abaixo danifica a célula |
| Max. Charge / Discharge Current | **3C** (= 150 A) | correntes máximas contínuas (3 × 50 Ah) |
| Max. Pulse Discharge | **10C** (= 500 A) | corrente de pico admissível (curta duração) |
| Charge Method CC-CV, Standard 0,3C | 15 A | carga a corrente constante até 3,65 V, depois tensão constante; rápida: 50% em 10 min |
| Operating Temperature | 0–45 °C carga; −20–60 °C descarga | janelas de temperatura (carregar abaixo de 0 °C degrada — lithium plating) |
| Cycle Life | **80% DOD ≥ 2000 ciclos; 70% DOD ≥ 3500** | n.º de ciclos até a capacidade cair ao limite (SoH); menor DOD ⇒ mais ciclos |
| Self Discharge | ≤ 3%/mês | perda de carga em repouso |

**Energia total extraível ao longo da vida:**

Energia nominal da célula: E = U × C = 3,2 V × 50 Ah = **160 Wh**

- **80% DOD:** por ciclo extrai 0,8 × 160 = 128 Wh → E_vida = 128 × 2000 = **256 kWh**
- **70% DOD:** por ciclo extrai 0,7 × 160 = 112 Wh → E_vida = 112 × 3500 = **392 kWh**

**Conclusão:** usando 70% DOD extrai-se **~53% mais energia ao longo da vida** (392 vs. 256 kWh) — descargas menos profundas prolongam a vida útil mais do que proporcionalmente. (Valores "≥" ⇒ são mínimos garantidos.)

---

## Q5 — Veículo elétrico a hidrogénio: funcionamento, desafios, campos promissores (1,5 v)

(= Q4 do exame 2011/12 — ver [Ficha 4](ficha4_pilhas_combustivel.md))

**Funcionamento:** tanques de H₂ a 350–700 bar → **pilha de combustível PEMFC** (ânodo: H₂ → 2H⁺ + 2e⁻; cátodo: ½O₂ + 2H⁺ + 2e⁻ → H₂O) produz eletricidade + água + calor → conversor DC/DC → inversor → motor elétrico, com **bateria tampão** para transitórios e travagem regenerativa (estrutura de híbrido série).

**Principais desafios:** apesar de o H₂ ser o elemento mais abundante do universo, **não existe livre** — é um *vetor* energético, não uma fonte: (1) produção — eletrólise verde cara, reformação de gás natural emite CO₂; (2) rendimento WTW baixo (~25–35% vs. ~70% BEV); (3) armazenamento/transporte — péssima energia/volume, compressão dispendiosa; (4) infraestrutura quase inexistente; (5) custo e durabilidade da pilha (platina).

**Campos promissores:** onde o peso das baterias é proibitivo e o abastecimento é centralizado — **pesados de longo curso, autocarros** (CaetanoBus H2.City Gold), **comboios em linhas não eletrificadas, marítimo**, empilhadores/indústria.

---

## Q6 — Motores para VEs: características e aplicações (1,4 v)

(= Q5 do exame 2011/12 — ver [Ficha 5](ficha5_motores.md))

| Motor | Características | Onde se usa |
|---|---|---|
| **DC com escovas** | controlo simples, binário de arranque; manutenção, volume | tração clássica, kits de conversão — **desuso** |
| **Indução (MIA)** | robusto, barato, sem ímanes; rendimento um pouco menor | Tesla Model S original, metros/elétricos, 2.º eixo de AWD |
| **PMSM/BLDC** | melhor rendimento e densidade de potência; terras-raras | a maioria dos BEVs atuais (Leaf, Hyundai/Kia, e-bikes) |
| **IPM-SynRM** | ímanes interiores + relutância — rendimento alto com menos ímanes | Tesla Model 3/Y, BYD |
| **SRM/SynRM** | sem ímanes, barato, robusto; ruído/binário pulsante | aplicações industriais; interesse crescente p/ VEs low-cost |
| **Rotor bobinado** | excitação controlável, sem terras-raras | Renault Zoe/Mégane |

Variação de velocidade: **inversor** (V/f ou FOC), n = 60·f/p; binário constante até à velocidade base, potência constante acima (enfraquecimento de campo).

---

## Q7 — Bitolas; locomotiva Co'Co' para a Linha do Norte (1,4 v)

**Bitolas (distância entre faces interiores dos carris):**

| Rede | Bitola |
|---|---|
| **Portugal** | **1668 mm** (bitola ibérica) |
| **Espanha** | **1668 mm** (ibérica; alta velocidade: 1435) |
| **França** | **1435 mm** (bitola europeia/standard/UIC) |

**Linha do Norte (Lisboa–Porto): eletrificação em 25 kV, 50 Hz, AC monofásica** (catenária), retorno pelo carril.

**Esquema de uma locomotiva moderna Co'Co' (componentes do sistema de alimentação):**

```
        catenária 25 kV / 50 Hz
   ───────────────────────────────
          │ pantógrafo
          ▼
   [disjuntor principal]
          ▼
   [transformador principal] (abaixa 25 kV → centenas de V)
          ▼
   [retificador 4Q / conversor AC-DC]
          ▼
   [barramento DC] ──► [filtro]
          ▼
   [inversores DC-AC] ──► [motores de tração ×6] (um por eixo, "o")
          ▼
   ●●●        ●●●     2 bogies × 3 eixos motores = Co'Co'
  [bogie]    [bogie]
   └─ retorno da corrente pelas rodas/carril ─┘
```

(ver [Ficha 6](ficha6_uic.md) para a norma UIC; exemplo real: locomotivas de mercadorias pesadas. As CP 5600 da Linha do Norte são Bo'Bo' — a pergunta pede explicitamente COCO, típica de mercadorias.)

---

## Q8 — Propulsão elétrica vs. MCI em pequenas embarcações de águas interiores (1,3 v)

**Vantagens da propulsão elétrica pura:**

- **Zero emissões locais** — crítico em rios, lagos e albufeiras (água potável!); em muitos lagos europeus o MCI está **proibido** e só barcos elétricos podem navegar
- **Silêncio** — sem ruído nem vibração (fauna, conforto, pesca, turismo)
- **Sem derrames** de combustível/óleo na água
- **Rendimento elevado** e binário imediato; manutenção mínima (sem óleo, filtros, refrigeração complexa)
- Possibilidade de **carregamento solar** (barcos-casa, ferries fluviais)

**Desvantagens:**

- **Autonomia limitada** (densidade energética da bateria) — mas em águas interiores as distâncias e velocidades são baixas, o que atenua o problema
- **Tempo de carregamento** e necessidade de pontos de carga nas marinas
- **Custo inicial** superior; peso das baterias
- Na água a resistência cresce muito com a velocidade (casco) — a velocidade elevada esgota a bateria rapidamente

**Conclusão:** em pequenas embarcações de águas interiores (velocidades baixas, percursos curtos, zonas ambientalmente sensíveis) a propulsão elétrica é **francamente vantajosa** — é dos nichos onde o elétrico já hoje domina o MCI.

---

## Mapa: este exame vs. fichas

| Questão | Ficha de apoio |
|---|---|
| Q1 Poluentes + WTW/LCA | [Ficha 8](ficha8_well_to_wheel.md) |
| Q2 História/obstáculos | [Ficha 1](ficha1_historia.md) + [Ficha 2](ficha2_componentes.md) |
| Q3 Forças/rampa | [Ficha 7](ficha7_potencia_tracao.md) |
| Q4 Parâmetros de células | [Ficha 3](ficha3_baterias.md) |
| Q5 Hidrogénio | [Ficha 4](ficha4_pilhas_combustivel.md) |
| Q6 Motores | [Ficha 5](ficha5_motores.md) |
| Q7 Bitolas/locomotiva | [Ficha 6](ficha6_uic.md) |
| Q8 Barcos elétricos | (nova matéria — resumo acima) |
