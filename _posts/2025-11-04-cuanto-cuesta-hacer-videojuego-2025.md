---
title: Cuánto Cuesta Hacer un Videojuego en 2025
date: 2025-11-04
categories:
- datos-industria
- development-costs
- budget-analysis
tags:
- game-budgets
- indie-costs
- aaa-spending
- publisher-impact
- engine-costs
- multiplayer-budgets
slug: cuanto-cuesta-hacer-videojuego-2025
descripcion: 'HushCrasher analizó 100K games con ML model: Kei median $65K, Midi 14x
  más, AA 33x Midi, AAA 10x AA. Publisher aumenta budget 3-4x, 3D 16x vs 2D'
fuente: https://hushcrasher.substack.com/p/how-much-does-it-cost-to-make-a-video
excerpt: 'HushCrasher analizó 100K games con ML model: Kei median $65K, Midi 14x más,
  AA 33x Midi, AAA 10x AA. Publisher aumenta budget 3-4x, 3D 16x vs 2D'
---

En una creative industry, cash es lo que keeps the lights on. Game budgets son key para tracking market dynamics, pero este es uno de los hardest data to get. Todos están quick para hablar de sales, pero los budgets necesarios para hacer esos games a menudo permanecen como greatest unknown. No hay budgets database, y muy pocos public announcements. Solo rumors y whimsical estimates.

HushCrasher usó data science para predecir el budget de todos los games en Steam. Aquí están los resultados.

## El modelo: 100,000 games analizados

HushCrasher pasó semanas scavenging web archives, news articles, data leaks, post-mortems y forums. También consultaron industry contacts que generously agreed to share su financial data confidentially.

Pero no era suficiente. El dataset era nowhere big enough para draw direct conclusions sobre industry-wide trends. La good news: el dataset era big enough para train un machine learning model que generaría budget estimates para every single game available en Steam.

Para hacer resultados lo más precise posible, alimentaron el model con predictors de costs: credit length, publisher's y studio's experience, variety de distinct job titles, supported languages, y dozens de otras variables.

El model achieves high level de accuracy, prediciendo el actual budget dentro de 10% margin, en average. Terminaron con budget estimates para alrededor de 100,000 games. Este análisis presenta resultados para 2022-2025, excluyendo games con fewer que 10 reviews, dejando 19,634 games.

## Scope determina spending: La escalada exponencial

**Kei games (pequeño scope):** Median cost $65K  
Developers claramente know how need to keep costs low. Esto mainly reflects developers' cost de living y location. Braid, por ejemplo, costó $200K porque su developer Jonathan Blow "didn't want to live in a shack somewhere." Meanwhile, Eldritch, el 2013 Lovecraft inspired FPS costó total de $22K.

**Midi games:** Median 14x más expensive que Kei  
El budget box might look like they're chilling con el Kei one, pero el overlap solo concerns los data points outside del 75th percentile. Los medians muestran real story: making un Midi game es actually 14 veces más pricey.

Cost está doomed to increase con larger team y proper company structure. Thimbleweed Park, un 2017 point-and-click, terminó costando no less que $1M según Ron Gilbert.

**AA games:** Median 33x Midi games  
**AAA games:** Median 10x AA games

La escalada es exponencial. Black Ops Cold War costó $700M, casi 9 veces los $82M ya required para Spider-Man: Miles Morales. AAA games ahora fully rival los biggest US cinema blockbusters. Es fair to say ahora van far beyond it.

## Engine Wars: Godot vs Goliath

Es stunning que Godot es uno de Unity's biggest challengers para small-scope (<$100K) games. Es David, el open-source tool, contra Goliath, el billion-dollar financed software.

Godot got un booster en 2023 cuando Unity changed su pricing model. Mientras fue fully reversed apenas un año después, el trust was broken, dando lasting bonus a Godot, ahora on the edge para overcome GameMaker.

Para Unreal, el cliché de que es mainly para large projects still holds true. Kei successes como Manor Lords might convince otros. Currently, Unreal leads el high-budget game market, holding más de half de su share.

El true challenger a Unity y Unreal reside en la categoría "Other." Para projects con small budgets, es diverse array de open-source solutions y custom engines. Conversely, en high end, "Other" mainly defines proprietary, in-house engines: Rockstar's RAGE, Bethesda's Creation Engine, o el impressive Decima Engine de Guerrilla Games.

## Publisher partnership: 3-4x budget increase

Partnering con publisher es rarer de lo que might think: solo 23% de developers lo hacen. Cuando lo hacen, es más que just shifting costs de self-funding a external finance. Ultimately, resulta en higher development budget, 3x a 4x en average.

Este increase podría significar varias cosas:

**Principal-agent problem:** Publisher money might be invested less efficiently que developers' own capital. O podría ser inevitable added cost de professional relationship (meetings, reporting, having to justify por qué este step está late on top de already being late).

**Necessary investment:** Este extra money podría ser necessary investment para achieve successful game. ¿Lo es? Habrá que cross-check esto contra commercial success metrics.

## 2D vs 3D: 16x cost difference

Making 3D games might have been impossible para small teams en el pasado, pero ya no es el case. Ahora vemos 3D games de all budgets, desde PSX stylized horror Kei hasta ultra realistic AAA.

La large average difference en cost (3D games son 16 veces costlier) es mainly porque 2D games rarely get past over $1M budgets. Pero el floor para 3D dropped significantly. Small teams ahora pueden tackle 3D con budgets que antes eran 2D-only territory.

## Multiplayer: Multi-million dollar business

Multiplayer games son more likely para break el million-dollar mark. Mientras account solo por 16% de all games, make up half del market para budgets above $10M.

Este gap highlights cómo single player games son relatively scarce para big studios. El infrastructure, server costs, ongoing maintenance, y complexity de networking features all contribute a este premium.

## Implicaciones para developers en diferentes stages

**Para Kei developers ($65K median):**
- Location arbitrage es real factor en costs
- Living expenses son primary cost driver
- Open-source tools como Godot son viable para keep costs down
- $22K (Eldritch) a $200K (Braid) range muestra flexibility

**Para Midi developers (14x Kei = ~$900K median):**
- Proper company structure adds significant overhead
- Team scaling no es linear en costs
- Decision sobre 2D vs 3D tiene major budget implications
- Publisher consideration starts becoming relevant

**Para AA developers (33x Midi = ~$30M median):**
- Casi todos necesitan publisher backing
- 3D es default, 2D es rare
- Engine choice matters menos (budget allows cualquier engine)
- Multiplayer features common y expensive

**Para AAA developers (10x AA = ~$300M median):**
- In-house engines o Unreal dominan
- Marketing puede double el budget
- Multiplayer es significant portion de market
- Comparable a biggest cinema blockbusters

## Preguntas sin responder y future research

HushCrasher identifica varios topics para future investigation:

**Budget evolution over time:** ¿Han game budgets realmente skyrocketed over years como everyone says? ¿Concernió all games o specific category?

**Causal impact analysis:** Más allá de correlations, ¿cuánto exactly aumenta budget cuando making it 3D vs 2D? ¿Cuánto más cada new team member really cost in the end? ¿Es marginal cost de team member stable mientras game size increase?

**Geographic differences:** Budgets pueden differ greatly between countries. Sería insightful mirar back a esos figures knowing donde están based las people detrás de esos games.

## La realidad del budget landscape

Este snapshot de today's budget revela varias truths críticas:

1. **Exponential scaling es real:** Cada scope jump no solo doubles costs, los multiplica exponentially
2. **Publisher money no es free money:** Viene con 3-4x budget increase y loss de creative control
3. **Engine choice importa para small budgets:** Godot challenging Unity en <$100K space
4. **Multiplayer es premium feature:** Heavily concentrated en high-budget games
5. **Geographic arbitrage es advantage:** Living expenses son major cost driver para Kei/Midi

Para developers planning su next project, understanding estos benchmarks es critical para realistic budgeting, fundraising conversations, y scope decisions.

---

¿Estás planning tu game budget, considering publisher partnerships, o evaluating scope decisions? Como consultor especializado en marketing de videojuegos, ayudo a developers a understand budget implications de creative decisions, assess funding options, y create realistic financial projections. Si quieres discutir tu budget strategy, contáctame.

**Fuente:** https://hushcrasher.substack.com/p/how-much-does-it-cost-to-make-a-video
