# Ficha 8 — Análise do Poço-à-Roda (Well-to-Wheel) 🛢️➡️🛞

> Fonte: T1, slides A-72 a A-74 (Perspetivas de análise: consumos, emissões e consumos WTW) — tabela de Pereirinha, P.G. (2023), *Electric Vehicles*, Encyclopedia of Electrical and Electronic Power Engineering, Elsevier.

## 1. As três perspetivas de análise

| Análise | O que inclui | Sigla |
|---|---|---|
| **Tank-to-Wheel** | emissões/consumo **no veículo** (do tanque/bateria à roda) | TTW |
| **Well-to-Tank** | obtenção da energia: extração, processamento, **transporte e distribuição** até ao tanque | WTT |
| **Well-to-Wheel** | a cadeia completa: **WTT + TTW = WTW** | WTW |

Também chamada "Fonte-à-Utilização" (Source-to-Service). A análise de **ciclo de vida (LCA)** vai mais longe: inclui fabrico, materiais e fim de vida do veículo (cf. GREET Model).

⚠️ Ponto-chave: "zero emissões" do BEV é uma afirmação **TTW**. A comparação justa entre tecnologias é **WTW** (ou LCA).

## 2. A tabela das aulas (rendimentos, valores aproximados)

| Etapa | ICEV diesel | ICEV gasolina | BEV (renováveis) | BEV (central boa, gás CC) | BEV (central média) |
|---|---|---|---|---|---|
| Extração/refinação | 90% | 90% | — | 97% | 95% |
| Transporte/distribuição | 97% | 97% | 94% | 94% | 92% |
| Geração de eletricidade | — | — | 100% | 55% | 33% |
| Carregador | — | — | 92% | 90% | 85% |
| Bateria | — | — | 95% | 95% | 90% |
| Conversor/inversor | — | — | 94% | 90% | 85% |
| Motor (térmico/elétrico) | 20% | 17% | 90% | 90% | 85% |
| Transmissão | 97% | 97% | 97% | 97% | 96% |
| **WTT** | **87%** | **87%** | **86%** | **45%** | **25%** |
| **TTW** | **19%** | **16%** | **78%** | **75%** | **62%** |
| **WTW** | **17%** | **14%** | **67%** | **34%** | **15%** |
| **WTW c/ regeneração (+10%)** | 17% | 14% | **74%** | 37% | 17% |

## 3. Leitura da tabela (o que dizer no exame)

- O motor de combustão é o **elo fraco** do ICEV: rendimento ~17–20% deita tudo a perder (WTW 14–17%), apesar de o WTT do gasóleo/gasolina ser alto (87%).
- O BEV inverte a situação: TTW altíssimo (62–78%) e **travagem regenerativa** (+10%) que o ICEV não tem.
- O WTW do BEV **depende do mix elétrico**: com renováveis ~**67–74%**; com centrais térmicas médias cai para ~15–17% — comparável ao ICEV **em energia**, mas as emissões concentram-se na central (controláveis, fora da cidade) e o mix melhora todos os anos.
- **FCEV (hidrogénio):** eletrólise (~70%) × compressão/transporte × pilha (~50–60%) × motor ⇒ WTW ~**25–35%** — entre o ICEV e o BEV (ver [Ficha 4](ficha4_pilhas_combustivel.md)).

## 4. Ordem de mérito (memorizar)

**BEV renovável (≈70%) > FCEV H₂ verde (≈30%) > ICEV diesel (≈17%) > ICEV gasolina (≈14%)**

E em emissões locais (cidade): BEV = FCEV = 0; ICEV ≠ 0 — argumento adicional independente do WTW.

## 5. Exercícios de treino

**E1.** Calcula o WTW de um BEV com: geração 55%, transporte 94%, carregador 90%, bateria 95%, inversor 90%, motor 90%, transmissão 97%.
<details><summary>Solução</summary>
0,55×0,94×0,90×0,95×0,90×0,90×0,97 ≈ 0,35 → ~35% (com regeneração +10% ≈ 38%)
</details>

**E2.** Porque é que o BEV "zero emissões" pode não o ser numa análise WTW?
<details><summary>Solução</summary>
Se a eletricidade vier de centrais fósseis, as emissões existem — mas a montante (WTT), não no veículo (TTW). A vantagem mantém-se nas emissões locais e cresce com a descarbonização do mix.
</details>

**E3.** Um ICEV gasolina consome 7 L/100 km (~61 kWh/100 km em energia química). Quanta energia chega às rodas com TTW = 16%? Compara com um BEV de 15 kWh/100 km e TTW = 78%.
<details><summary>Solução</summary>
ICEV: 61×0,16 ≈ 9,8 kWh às rodas. BEV: 15×0,78 ≈ 11,7 kWh — energia útil semelhante, mas o BEV partiu de 4× menos energia.
</details>

## Erros a evitar no exame

- Confundir **TTW** com **WTW** (o "zero emissões" é só TTW)
- Esquecer que **WTT + TTW = WTW** (rendimentos **multiplicam-se**, não somam)
- Comparar BEV e ICEV sem indicar o **mix de geração** assumido
- Esquecer a **travagem regenerativa** (+10%) — exclusiva dos elétricos
