# Guia de Estudo TVE — Resolução do Exame Exemplo

**Exame:** Época de Recurso TVE 2011/12 (10 Jul 2012, 1h15, 8 valores) — Prof. Paulo Pereirinha
**Cotações:** Q1–1,3 | Q2–1,4 | Q3–1,4 | Q4–1,3 | Q5–1,3 | Q6–1,3

> Nota: já existem fichas mais detalhadas no projeto "Estudar TVE" (Ficha 1 — História; Ficha 2 — Componentes). Este guia resolve o exame completo e serve de resumo transversal.

---

## Q1 — Evolução histórica dos VEs vs. motores de combustão interna (1,3 v)

### Resolução

Os VEs **não são uma ideia nova** — antecederam e chegaram a dominar o automóvel a combustão:

- **1830s–1880s:** primeiros protótipos de veículos elétricos (Anderson ~1835; Trouvé 1881). A bateria de chumbo-ácido (Planté, 1859) torna-os viáveis.
- **~1900:** os VEs **dominavam o mercado** urbano (EUA: ~38% elétricos, ~40% vapor, ~22% gasolina). Eram silenciosos, limpos e sem manivela de arranque. Em 1899, o **"La Jamais Contente"** (elétrico, Camille Jenatzy) foi o primeiro veículo a ultrapassar os **100 km/h**.
- **1908–1930:** declínio dos VEs. Causas: **Ford Model T** (produção em série, preço baixo), **arranque elétrico** do motor a gasolina (Kettering, 1912), petróleo barato e abundante, rede de estradas (maior necessidade de autonomia) vs. **baixa densidade energética das baterias**.
- **1930–1990:** quase desaparecimento. Renasceres pontuais em crises do petróleo (1973, 1979).
- **1990s:** retoma — preocupações ambientais e regulamentação (CARB/ZEV na Califórnia; GM EV1, 1996).
- **2000s–presente:** híbridos (Toyota Prius, 1997) como ponte; baterias de **iões de lítio** mudam o paradigma; Tesla Roadster (2008), Nissan Leaf (2010); crescimento exponencial desde então, apoiado por políticas públicas e descida do custo das baterias.

**Síntese a dar na resposta:** o VE nasceu antes do automóvel a gasolina e dominou ~1900; perdeu pela limitação das baterias face ao baixo custo e autonomia da gasolina; regressou ~100 anos depois quando as baterias (Li-ião) e as preocupações ambientais/energéticas inverteram a balança.

---

## Q2 — Componentes principais de um VE a baterias + obstáculos (1,4 v)

### Resolução

**Componentes principais (BEV):**

1. **Bateria de tração** (RESS) — armazena a energia (Li-ião, LFP/NMC)
2. **BMS** — monitoriza/equilibra células (tensão, temperatura, SoC, SoH)
3. **Conversor eletrónico de potência / Inversor** (DC→AC, tipicamente com IGBT/SiC) — alimenta e controla o motor
4. **Motor elétrico de tração** (indução ou síncrono de ímanes permanentes)
5. **Transmissão** (redutor de relação fixa, normalmente sem caixa de velocidades)
6. **Carregador** (on-board AC; carregamento rápido DC externo)
7. **Conversor DC/DC** auxiliar (rede de bordo 12 V) e **auxiliares** (climatização, direção)
8. **Sistema de controlo do veículo** (VCU) — gere pedal, travagem regenerativa, gestão de energia

**Esboço da interligação:**

```
Carregador AC ──┐
                ▼
Rede ──► [BATERIA + BMS] ──► [INVERSOR DC/AC] ──► [MOTOR] ──► [TRANSMISSÃO] ──► Rodas
                │                    ▲   (travagem regenerativa: fluxo inverso)
                ├──► [DC/DC 12V] ──► auxiliares
                ▼
        Carreg. rápido DC
```

**Maior obstáculo: a BATERIA.** Porquê:

- **Densidade energética** baixa face aos combustíveis (~0,1–0,25 kWh/kg vs. ~12 kWh/kg da gasolina) → autonomia limitada e peso elevado
- **Custo** elevado (fração dominante do preço do VE)
- **Tempo de carregamento** vs. minutos a abastecer
- **Vida útil/degradação** e dependência de matérias-primas (Li, Co, Ni)
- Associado: **infraestrutura de carregamento** insuficiente ("range anxiety")

*(Nota: em 2012 o custo rondava 600–800 $/kWh; hoje <150 $/kWh — referir a evolução valoriza a resposta.)*

---

## Q3 — Cálculo: 12 baterias em série (1,4 v)

**Dados (tabela do exame):** bateria de **12 V**, **20 Ah**, C-rate 3~5C, ESR ≤ 60 mΩ.

### Resolução

**Tensão do conjunto** (série soma tensões, capacidade mantém-se):

U = 12 × 12 V = **144 V**  (capacidade: 20 Ah)

**Energia disponível:**

E = U × C = 144 V × 20 Ah = **2880 Wh ≈ 2,9 kWh**

**Autonomia esperada** (consumo médio 60 Wh/km):

d = 2880 / 60 = **48 km**

**Influência da velocidade:**

- A potência aerodinâmica cresce com o **cubo** da velocidade (P ∝ v³), logo a energia gasta **por km** cresce com o **quadrado** (E/km ∝ v²) → a alta velocidade a autonomia cai fortemente.
- **Efeito Peukert / C-rate:** descargas a corrente elevada reduzem a capacidade efetiva da bateria e aumentam as perdas internas (ESR: P_perdas = R·I²) → menos energia útil. (Aqui, 3C = 60 A de descarga contínua.)
- A velocidade **muito baixa** também penaliza: os consumos auxiliares (climatização, eletrónica) são ~constantes no tempo, pesando mais por km.
- Conclusão: existe uma **velocidade ótima moderada** que maximiza os km percorridos; os 48 km só se obtêm ao consumo médio indicado.

---

## Q4 — Pilhas de combustível (1,3 v)

### Resolução

**O que é:** dispositivo **eletroquímico** que converte diretamente a energia química de um combustível (tipicamente **hidrogénio**) em **energia elétrica**, sem combustão, enquanto for alimentado. Na PEMFC (membrana de troca protónica, a usada em automóveis):

- Ânodo: H₂ → 2H⁺ + 2e⁻
- Cátodo: ½O₂ + 2H⁺ + 2e⁻ → H₂O
- Produtos: **eletricidade + água + calor**. Cada célula dá ~0,6–0,8 V; associam-se em série numa **pilha (stack)**.

**Concordo com a expectativa?** Resposta equilibrada, justificada — vantagens: abastecimento rápido (~5 min), boa autonomia, zero emissões locais. Mas há obstáculos fortes:

- **Eficiência global (well-to-wheel) baixa:** eletricidade → eletrólise → compressão/transporte → pilha → motor dá ~25–35%, contra ~70–80% do BEV
- **Hidrogénio verde caro** e maioritariamente ainda produzido a partir de gás natural (reformação — com emissões de CO₂)
- **Infraestrutura** de produção/distribuição/armazenamento de H₂ praticamente inexistente e cara; armazenamento a 350–700 bar
- **Custo** da pilha (catalisadores de platina) e durabilidade

**Conclusão defensável:** não substituirão os BEVs na mobilidade ligeira; fazem sentido em **nichos** — pesados de longo curso, autocarros, comboios em linhas não eletrificadas, marítimo — onde o peso das baterias é proibitivo.

---

## Q5 — Motores para VEs e variação de velocidade (1,3 v)

### Resolução

**Motores utilizáveis em VEs:**

| Motor | Características | Variação de velocidade |
|---|---|---|
| **DC (escovas)** | Simples controlo, histórico (tração clássica); manutenção das escovas, menor rendimento | Variação da **tensão de armadura** (chopper DC/DC) e **enfraquecimento de campo** para altas velocidades |
| **Indução (assíncrono, MIA)** | Robusto, barato, sem ímanes; rendimento ligeiramente inferior | **Inversor** com variação de **tensão e frequência** (V/f, ou melhor, **controlo vetorial/FOC**); acima da velocidade base, enfraquecimento de fluxo |
| **Síncrono de ímanes permanentes (PMSM/BLDC)** | Maior rendimento e densidade de potência/binário — o mais usado atualmente; ímanes de terras-raras (custo) | **Inversor** com controlo vetorial (FOC) sincronizando a frequência com o rotor; enfraquecimento de campo por injeção de corrente d negativa |
| **Relutância comutada (SRM) / relutância síncrona (SynRM)** | Sem ímanes, robusto e barato; binário pulsante e ruído | Conversor eletrónico dedicado com comutação sequencial das fases em função da posição do rotor |

**Ideia-chave para a resposta:** nos motores AC a velocidade é ditada pela frequência (n ≈ 60f/p, menos o escorregamento no MIA); a variação de velocidade faz-se com **inversores (eletrónica de potência)** que controlam amplitude e frequência da tensão; abaixo da velocidade base trabalha-se a **binário constante** (fluxo nominal), acima a **potência constante** (enfraquecimento de campo).

---

## Q6 — Normas UIC de designação do material circulante (1,3 v)

### Resolução

**Norma UIC (disposição dos rodados):**

- **Letras** = eixos **motores** consecutivos num bogie/grupo: A=1, B=2, C=3, D=4
- **Algarismos** = eixos **não motores** (livres): 1, 2, …
- **Apóstrofo (')** = os eixos desse grupo estão montados num **bogie** (chassis orientável independente)
- **"o"** (índice) = eixos com **motores individuais** (ex.: Bo'Bo')

**Designações pedidas:**

- **Co'Co' (COCO):** 2 bogies, cada um com **3 eixos motores** → 6 eixos motores no total. Típico de locomotivas pesadas de mercadorias.

```
  ●●●     ●●●     (● = eixo motor)
 [bogie] [bogie]
```

- **Bo'Bo' (BOBO):** 2 bogies, cada um com **2 eixos motores** individuais → 4 eixos motores. A configuração mais comum em locomotivas elétricas modernas e unidades múltiplas.

```
  ●●      ●●
 [bogie] [bogie]
```

- **(A1A)(A1A):** 2 bogies de 3 eixos em que o eixo **central é livre**: motor–livre–motor → 4 eixos motores + 2 livres. Usado para reduzir a carga por eixo.

```
  ●○●     ●○●    (○ = eixo livre)
 [bogie] [bogie]
```

**Outras normas (desatualizadas):**

- **Notação Whyte** (contagem de **rodas**, não eixos: à frente–motoras–atrás), usada no vapor: Co'Co' ≈ **0-6-6-0**; Bo'Bo' ≈ **0-4-4-0**; (A1A)(A1A) ≈ 0-6-6-0 (não distingue eixos livres interiores — limitação da norma).
- **Classificação francesa** (eixos em vez de rodas): equivalentes 030+030, 020+020, etc.

---

## Para estudar — mapa das matérias

| Tema do exame | Onde estudar | Ficha (projeto "Estudar TVE") |
|---|---|---|
| 1. História dos VEs | T1 (Doc A) | ✅ Ficha 1 (feita) |
| 2. Componentes do BEV | T1 (arquitetura VEB/VEH/FCEV) | ✅ Ficha 2 (feita) |
| 3. Cálculo de baterias | Tparte2 (baterias, C-rate, autonomia) | ⏳ Ficha 3 (pendente) |
| 4. Pilhas de combustível | Tparte2 (FC, PEMFC, H₂) | ⏳ Ficha 4 (pendente) |
| 5. Motores e variação velocidade | Tparte2 (MIA, PMSM, SRM, inversores) | ⏳ Ficha 5 (pendente) |
| 6. Normas UIC / ferroviário | Tparte3 (Doc I, L, J — tecnologias ferroviárias) | ⏳ Ficha 6 (pendente) |

**Fórmulas a saber de cor:**

- Série: U_total = n·U_célula; C mantém | Paralelo: C_total = n·C; U mantém
- E [Wh] = U [V] × C [Ah] | Autonomia [km] = E [Wh] / consumo [Wh/km]
- C-rate: I = k·C (ex.: 3C de 20 Ah = 60 A) | Perdas ESR: P = R·I²
- Potência aerodinâmica ∝ v³ → consumo por km ∝ v²
- Velocidade síncrona: n = 60·f/p [rpm]
