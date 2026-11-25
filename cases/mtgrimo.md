<div align="center">

# 🧙‍♂️ MTGrimo — Motor Autoral de Busca de Cartas & NLP Determinístico PT-BR

**Pesquise em 118.000+ cartas de Magic: The Gathering falando português natural — sem alucinação de LLM, sem custo por token e com cotações em reais.**

<p>
  <img src="https://img.shields.io/badge/Rust-Axum_%2B_Tokio-000000?style=for-the-badge&logo=rust&logoColor=white" alt="Rust Axum" />
  <img src="https://img.shields.io/badge/PostgreSQL-16_pg__trgm_%2B_GIN-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL 16" />
  <img src="https://img.shields.io/badge/Redis-7_Cache-DC382D?style=for-the-badge&logo=redis&logoColor=white" alt="Redis 7" />
  <img src="https://img.shields.io/badge/React-19_%2B_Vite_8-149ECA?style=for-the-badge&logo=react&logoColor=white" alt="React 19" />
  <img src="https://img.shields.io/badge/Expo-React_Native_SQLite-000020?style=for-the-badge&logo=expo&logoColor=white" alt="Expo" />
</p>

<p>
  <img src="https://img.shields.io/badge/Cat%C3%A1logo-118k%2B_Cartas_%7C_123k%2B_Faces-f97316?style=flat-square" alt="118k Cartas" />
  <img src="https://img.shields.io/badge/Parser-NLP_PT--BR_100%25_Determin%C3%ADstico-10b981?style=flat-square" alt="NLP Determinístico" />
  <img src="https://img.shields.io/badge/APIs-Scryfall_%7C_EDHREC_%7C_LigaMagic_BRL-6366f1?style=flat-square" alt="APIs" />
  <img src="https://img.shields.io/badge/Produ%C3%A7%C3%A3o-mtgrimo.com-000000?style=flat-square" alt="Produção" />
</p>

[← Voltar ao Portfólio Principal](../README.md) • [🌐 Acessar MTGrimo](https://mtgrimo.com/) • [📸 Prints em Produção](#-prints-reais-em-produção) • [🧠 Pipeline NLP](#-pipeline-do-motor-de-busca-determinístico)

</div>

> **Nota de autoria e confidencialidade:** o **MTGrimo** é um projeto colaborativo de código privado. Este estudo de caso documenta minha atuação específica no **mecanismo autoral de busca de cartas, integrações com APIs de bases de dados e conversor determinístico de linguagem natural PT-BR → AST → SQL**.

---

## 💡 O Desafio

Jogadores brasileiros de *Magic: The Gathering* (especialmente *Commander*) esbarravam em duas barreiras: memorizar sintaxes obscuras em inglês (`t:creature id<=bg o:"add"`) ou depender de LLMs caros, lentos e sujeitos a alucinações. A solução foi criar um **parser semântico PT-BR 100% determinístico** em Rust, conectado ao PostgreSQL (`pg_trgm` + `GIN`), Redis e APIs externas (**Scryfall**, **EDHREC** e **LigaMagic BRL**).

---

## 📸 Prints Reais em Produção

### 💻 Versão Desktop (`https://mtgrimo.com/`)

<table>
  <tr>
    <td align="center" width="50%">
      <img src="../assets/mtgrimo-home.png" alt="MTGrimo — Interface Principal" width="100%" /><br/>
      <strong>Grimório &amp; Catálogo Principal</strong><br/>
      <sub>Busca instantânea em português sobre 118k+ cartas</sub>
    </td>
    <td align="center" width="50%">
      <img src="../assets/mtgrimo-busca.png" alt="MTGrimo — Busca NLP PT-BR em Ação" width="100%" /><br/>
      <strong>NLP PT-BR em Ação</strong><br/>
      <sub><em>"criatura verde que gera mana"</em> &rarr; <strong>Entendi 3 filtros</strong> + preços em BRL</sub>
    </td>
  </tr>
</table>

### Decks da Comunidade (Top 10, Brackets & Arquétipos)
![MTGrimo — Decks da Comunidade](../assets/mtgrimo-comunidade.png)

---

### 📱 Versão Mobile (Responsivo)

<table>
  <tr>
    <td align="center" width="50%">
      <img src="../assets/mtgrimo-mobile-home.png" alt="MTGrimo Mobile — Busca NLP PT-BR" width="290" /><br/>
      <strong>Busca Semântica Mobile</strong><br/>
      <sub>Filtros em português, cotações em R$ e rolagem infinita</sub>
    </td>
    <td align="center" width="50%">
      <img src="../assets/mtgrimo-mobile-comunidade.png" alt="MTGrimo Mobile — Comunidade" width="290" /><br/>
      <strong>Decks da Comunidade Mobile</strong><br/>
      <sub>Ranking, votação e navegação por abas</sub>
    </td>
  </tr>
</table>

---

## 🧠 Pipeline do Motor de Busca Determinístico

```mermaid
flowchart LR
    Q["Consulta em Português\n'criatura verde que gera mana'"] --> Lex["Normalização & Léxico PT-BR"]
    Lex --> Map["Mapeamento de Regras / Oracle"]
    Map --> AST["Parser & Árvore Sintática (AST)"]
    AST --> SQL["SQL Query Builder (Rust / Axum)"]
    SQL --> PG[("PostgreSQL 16\npg_trgm + FTS + GIN\n118k+ cartas")]
    SQL --> RD[("Redis 7 Cache\nScryfall • EDHREC • LigaMagic BRL")]
```

<details>
<summary><strong>🛠️ Stack & Resultados Comprováveis</strong></summary>

- **Motor & Backend:** Rust (Axum, Tokio), parser estruturado PT-BR → AST → SQL determinístico (zero custo por token e resultados 100% reproduzíveis).
- **Dados & APIs:** PostgreSQL 16 (`pg_trgm` + índices GIN), Redis 7, Scryfall (118k+ cartas / 123k+ faces), EDHREC (sinergias Commander) e LigaMagic (cotações BRL).
- **Clientes:** Web PWA em React 19 + Vite 8 e Mobile em React Native + Expo SDK 57 com persistência offline SQLite.

</details>

---

<div align="center">
  <a href="https://mtgrimo.com/"><strong>🌐 Acessar MTGrimo em Produção</strong></a> &nbsp;•&nbsp; <a href="../README.md"><strong>← Voltar ao Portfólio Principal</strong></a>
</div>
