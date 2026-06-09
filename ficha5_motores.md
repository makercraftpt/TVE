# Ficha 5 — Motores para VEs e Variação de Velocidade 🔄

> Tema da Q5 do exame exemplo. Fonte: Tparte2, slides A-181 a A-183 (Motores e Drives para VE) + Doc. B (cap. 5–8), Doc. C4/C5/C7.

## 1. Classificação (árvore do slide A-182)

```
                 Máquinas elétricas para VE/VEH
                    │
        ┌───────────┴───────────┐
        AC                      DC (coletor + escovas)
   ┌────┴─────┐                 ├─ excitação série
Assíncrono  Síncrono            ├─ excitação separada
   │          ├─ Relutância:    └─ ímanes permanentes
Indução (MIA, │   SRM, SynRM,
gaiola, 3~)   │   PMaSynRM
              ├─ Ímanes permanentes:
              │   BLDC, PMSM (BLAC), IPM, SPM
              └─ Rotor bobinado
```

## 2. Comparação dos motores (tabela-resposta da Q5)

| Motor | Vantagens | Desvantagens | Variação de velocidade |
|---|---|---|---|
| **DC série** (clássico) | controlo simples, binário de arranque alto (tração histórica) | escovas/coletor = manutenção, volume, menor rendimento → **desuso** (kits de conversão) | tensão de armadura (**chopper** DC/DC); enfraquecimento de campo |
| **Indução MIA** (gaiola) | robusto, barato, **sem ímanes**, tecnologia madura | rendimento e densidade de binário inferiores ao PMSM; precisa de magnetização | **inversor**: V/f ou **controlo vetorial (FOC)**; acima da velocidade base, enfraquecimento de fluxo |
| **PMSM / BLDC** (ímanes) | **maior rendimento e densidade de potência** — o mais usado | ímanes de terras-raras (custo, cadeia de abastecimento); desmagnetização | inversor com **FOC** (frequência sincronizada com o rotor); enfraquecimento por corrente d negativa |
| **SRM / SynRM** | sem ímanes, robusto, barato, suporta alta temperatura | binário pulsante, ruído, conversor dedicado | comutação sequencial das fases em função da **posição do rotor** |

**Tendência atual:** soluções híbridas **IPM-SynRM** (ímanes interiores + relutância — Tesla Model 3, BYD), motores de **fluxo axial** (YASA, ~59 kW/kg pico), motores **sem terras-raras** (MIA, SynRM, rotor bobinado — Renault/Horse ~98% rendimento).

## 3. Como se varia a velocidade (ideia-chave)

Nos motores AC, a velocidade é imposta pela **frequência**:

**n_s = 60·f/p [rpm]** (f = frequência; p = pares de polos)

- **MIA:** roda a n = n_s·(1−s), com escorregamento s de poucos %
- **Síncronos:** rodam exatamente a n_s (o inversor segue a posição do rotor)

A variação faz-se com **eletrónica de potência (inversor DC→AC)**, controlando **amplitude e frequência** da tensão:

| Zona | Estratégia | Resultado |
|---|---|---|
| 0 → velocidade base | fluxo nominal, V e f crescem juntos (V/f ≈ const.) | **binário constante** |
| acima da velocidade base | V no máximo, f continua a subir ⇒ **enfraquecimento de campo** | **potência constante** (binário ∝ 1/n) |

Métodos de controlo: escalar **V/f** (simples) < **FOC** (controlo vetorial — desacopla fluxo e binário, padrão atual) < DTC.

## 4. Caso de estudo rápido (para enriquecer a resposta)

- **Tesla:** Model S original — MIA (Curtis/AC Propulsion heritage); Model 3/Y — **IPM-SynRM** atrás (+ MIA à frente nas versões AWD)
- **Nissan Leaf, Hyundai/Kia, maioria dos europeus:** PMSM
- **Renault Zoe / Mégane E-Tech:** síncrono de **rotor bobinado** (sem terras-raras)
- **Metro/elétricos:** tradicionalmente **MIA** (robustez), a migrar para PMSM (ver trabalho Metros Ligeiros)

## 5. Exercícios de treino

**E1.** Motor síncrono de 4 polos (p = 2) alimentado a 100 Hz. Velocidade?
<details><summary>Solução</summary>
n = 60×100/2 = 3000 rpm
</details>

**E2.** MIA de 4 polos, 50 Hz, escorregamento 3%. Velocidade do rotor?
<details><summary>Solução</summary>
n_s = 60×50/2 = 1500 rpm; n = 1500×0,97 = 1455 rpm
</details>

**E3.** Porque se usa enfraquecimento de campo acima da velocidade base?
<details><summary>Solução</summary>
A tensão do inversor atinge o máximo (limitada pelo barramento DC); para continuar a subir a velocidade reduz-se o fluxo (no PMSM: corrente d negativa) — mantém-se a potência constante à custa do binário.
</details>

## Erros a evitar no exame

- Esquecer a fórmula **n = 60·f/p** (é a chave da variação de velocidade AC)
- Dizer que o MIA roda à velocidade síncrona (há **escorregamento**)
- Não referir o **inversor/eletrónica de potência** — sem ele não há variação de velocidade
- Confundir zona de **binário constante** (até à velocidade base) com a de **potência constante** (acima)
