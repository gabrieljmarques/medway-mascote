# Mascote Universitário — Instagram Analytics Dashboard

Painel interativo de métricas do Instagram do Mascote Universitário, filtrado por dias de evento em parceria com a **Medway**. Desenvolvido para apresentação de resultados de presença digital em competições e eventos da medicina esportiva universitária.

**Acesse:** `https://SEU_USUARIO.github.io/medway-dashboard`

---

## O que o painel mostra

Dados diários do Instagram Insights extraídos para cada evento Medway realizado entre **março de 2025 e abril de 2026**, com as seguintes métricas:

| Métrica | Cobertura |
|---|---|
| Alcance (Reach) | Todos os eventos |
| Visitas ao Perfil | Todos os eventos |
| Views | A partir de 22/08/2025 |
| Interações | A partir de 22/08/2025 |
| Seguidores Ganhos | A partir de 26/04/2025 |

Eventos com múltiplos dias de cobertura (Copa Medway, FUF, Intermed SP, JUMED, Intermed MG, Pré Intermed) têm as métricas **somadas** e aparecem como uma entrada única.

---

## Funcionalidades

- **Filtro por evento** — caixa recolhível com checkbox individual para cada evento
- **Seletor de categoria** — alterna entre *Todos*, *Inters* (Intermed SP, JUMED, Intermed MG, Pré Intermed) e *Eventos Mensais*
- **KPIs dinâmicos** — Eventos, Dias trabalhados, Alcance, Visitas, Views, Interações e Seguidores Ganhos, todos recalculados ao vivo conforme a seleção
- **5 gráficos de barras** em ordem cronológica crescente, com tooltip mostrando o nome do evento ao passar o mouse
- **Tabela detalhada** com mini-barras de proporção relativa e separadores por ano (2025 / 2026)
- **Modo dark** ativável pelo botão no canto superior direito

---

## Eventos cobertos

### 2025
| Data | Evento | Dias |
|---|---|---|
| 22/03 | Copa Urso | 1 |
| 26–27/04 | Copa Medway | 2 |
| 01/06 | Copa Amstel / Tuna | 1 |
| 07/06 | Gestão Med Unicamp | 1 |
| 15/06 | Pentagonal Tênis de Mesa | 1 |
| 25/07 | Atl Med ABC | 1 |
| 06/08 | Atl Med Einstein | 1 |
| 07/08 | VM Med ABC | 1 |
| 12/08 | VF Med Unicid | 1 |
| 22/08 | Festa Med9 | 1 |
| 06/09 | Inter São Camilo | 1 |
| 07–13/09 | Intermed SP ⚡ | 3 |
| 08–09/09 | JUMED ⚡ | 2 |
| 13–14/10 | Intermed MG ⚡ | 2 |
| 11/11 | Judô Med9 | 1 |
| 13/11 | Campo Med Anhembi | 1 |
| 22/11 | JIMESP | 1 |
| 23/11 | CRM | 1 |
| 24/11 | Gestão Med Santos | 1 |
| 02/12 | Natação Med 9 | 1 |
| 05/12 | Gestão São Camilo | 1 |

### 2026
| Data | Evento | Dias |
|---|---|---|
| 21–22/02 | FUF | 2 |
| 01/03 | Copa Águia | 1 |
| 02/03 | Running Med | 1 |
| 07/03 | Medswim | 1 |
| 08/03 | Torneio de Atletismo | 1 |
| 15/03 | TUNA | 1 |
| 21/03 | Copa Urso | 1 |
| 29/03–04/04 | Pré Intermed ⚡ | 2 |

> ⚡ Categoria **Inters** — eventos intercolegiais de grande porte.

**Total: 29 eventos · 35 dias de cobertura**

---

## Fonte dos dados

Exportações do **Instagram Insights** em formato CSV (UTF-16), geradas diretamente pelo Meta Business Suite:

- `Reach.csv` — alcance diário
- `Visits.csv` — visitas ao perfil
- `Views.csv` — visualizações de conteúdo
- `Interactions.csv` — interações com conteúdo
- `Follows.csv` — novos seguidores
- `Link clicks.csv` — cliques no link da bio

Os CSVs foram processados via Python para extração, agregação por evento e embutimento direto no HTML.

---

## Tecnologia

Arquivo único `index.html` — sem backend, sem build, sem dependências locais.

- **Chart.js 4.4** via CDN para os gráficos
- CSS custom properties para tema claro/escuro
- JavaScript vanilla para filtros, KPIs e renderização dinâmica
