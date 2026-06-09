# Ficha 4 — Pilhas de Combustível ⚡💧

> Tema da Q4 do exame exemplo. Fonte: Tparte2, slides A-154 a A-161 (Células e Pilhas de Combustível) + Doc. D e Doc. E.

## 1. O que é uma célula de combustível

Dispositivo **eletroquímico** que converte **diretamente** a energia química de um combustível (tipicamente **hidrogénio**) em **energia elétrica**, sem combustão e sem ciclo térmico, enquanto for alimentado (ao contrário da bateria, não armazena — converte).

**PEMFC** (Proton Exchange Membrane FC — a usada em automóveis):

- **Ânodo:** H₂ → 2H⁺ + 2e⁻ (o catalisador de platina separa o hidrogénio)
- **Membrana:** deixa passar os protões H⁺; os eletrões vão pelo circuito externo (= corrente elétrica)
- **Cátodo:** ½O₂ + 2H⁺ + 2e⁻ → H₂O
- **Produtos: eletricidade + água + calor** (zero emissões locais)

Cada célula dá ~**0,6–0,8 V** ⇒ associam-se **em série** numa **pilha (stack)** para obter tensões úteis.

## 2. Tipos de pilhas de combustível

| Tipo | Eletrólito | Temp. | Aplicação típica |
|---|---|---|---|
| **PEMFC** | membrana polimérica | 60–80 °C | **automóveis, autocarros** (arranque rápido) |
| **DMFC** | membrana (metanol direto) | 60–130 °C | portáteis |
| **AFC** | alcalino (KOH) | 60–250 °C | espacial (Apollo) |
| **PAFC** | ácido fosfórico | ~200 °C | estacionário |
| **MCFC** | carbonatos fundidos | ~650 °C | estacionário/cogeração |
| **SOFC** | óxido sólido cerâmico | 600–1000 °C | estacionário; rendimento alto |

(Comparação: energy.gov/eere/fuelcells/comparison-fuel-cell-technologies)

## 3. Veículo a célula de combustível (VCC / FCEV)

Arquitetura: **tanques de H₂ (350–700 bar) → pilha → conversor DC/DC → barramento DC → inversor → motor**, com **bateria tampão** (a pilha responde mal a transitórios; a bateria absorve picos e travagem regenerativa) — é de facto um **híbrido série**.

**Caso Toyota Mirai** (slides A-159/160) — simplificações face ao FCHV-adv: sistema **sem humidificador externo**, novo compressor de ar, consolidação das válvulas (corte de entrada/saída da pilha, desvio de fluxo, regulação de pressão), eliminação do diluente de hidrogénio, redução de **4 para 2 tanques** de H₂.

## 4. Problemas / obstáculos (a parte crítica da resposta)

- **Rendimento well-to-wheel baixo:** eletricidade → eletrólise → compressão/transporte → pilha → motor ≈ **25–35%**, contra ~70–80% (WTW c/ renováveis) do BEV → ver [Ficha 8](ficha8_well_to_wheel.md)
- **Origem do H₂:** maioritariamente **reformação de gás natural** (com CO₂); H₂ "verde" (eletrólise renovável) ainda caro
- **Transporte/armazenamento:** péssima relação **energia/volume** do H₂ (slide A-158); compressão a 350–700 bar consome energia; infraestrutura quase inexistente
- **Custo e durabilidade da pilha:** catalisadores de **platina**, gestão de água/temperatura
- Rede de abastecimento: poucos postos (exemplos dos slides desapareceram — sinal do estado do setor)

**Vantagens** a contrapor: abastecimento rápido (~5 min), autonomia, zero emissões locais, menos peso que baterias para grandes autonomias.

## 5. Resposta-tipo à Q4 ("concorda com a expectativa de que substituirão as baterias?")

Estrutura: (1) explicar o princípio (reações, stack); (2) reconhecer as vantagens; (3) confrontar com os obstáculos (rendimento WTW, custo do H₂ verde, infraestrutura); (4) concluir de forma equilibrada: **não substituem os BEVs nos ligeiros**; fazem sentido em **nichos** — pesados de longo curso, autocarros (CaetanoBus H2.City Gold!), comboios em linhas não eletrificadas, marítimo.

## 6. Exercícios de treino

**E1.** Uma pilha PEMFC tem 330 células em série a 0,65 V/célula. Tensão do stack?
<details><summary>Solução</summary>
U = 330 × 0,65 ≈ 215 V (ordem de grandeza do stack do Mirai)
</details>

**E2.** Porque é que um FCEV precisa de bateria além da pilha?
<details><summary>Solução</summary>
A pilha tem resposta dinâmica lenta e não absorve energia — a bateria cobre os transitórios (acelerações) e recebe a travagem regenerativa; a pilha trabalha perto do ponto ótimo.
</details>

**E3.** Indica duas razões para o rendimento WTW do hidrogénio ser inferior ao do BEV.
<details><summary>Solução</summary>
Perdas na eletrólise (~70-80% de rendimento) e na compressão/transporte; mais a conversão na própria pilha (~50-60%) — multiplicando, sobra ~25-35%, enquanto o BEV evita estas conversões intermédias.
</details>

## Erros a evitar no exame

- Dizer que a pilha **armazena** energia (converte; quem armazena são os tanques de H₂)
- Esquecer as **reações** de ânodo/cátodo ou trocar os eletrodos
- Resposta de opinião sem **justificação técnica** (a pergunta pede argumentos)
- Ignorar que o H₂ atual vem sobretudo de **gás natural** (não é automaticamente "limpo")
