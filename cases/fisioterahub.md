<div align="center">

# 🩺 FisioTeraHub — SaaS Multi-tenant para Clínicas de Fisioterapia

**Do agendamento ao prontuário imutável (COFFITO/LGPD), convênios ANS TISS 4.01 e 57.064 RPS em 1 vCPU.**

<p>
  <img src="https://img.shields.io/badge/Node.js-20-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node.js 20" />
  <img src="https://img.shields.io/badge/TypeScript-5.8-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/React-18_%2B_Vite-149ECA?style=for-the-badge&logo=react&logoColor=white" alt="React 18" />
  <img src="https://img.shields.io/badge/PostgreSQL-16_%2B_Prisma-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL 16" />
  <img src="https://img.shields.io/badge/Cloudflare-57.064_RPS-F38020?style=for-the-badge&logo=cloudflare&logoColor=white" alt="57.064 RPS" />
</p>

<p>
  <img src="https://img.shields.io/badge/M%C3%B3dulos_Backend-22-0d9488?style=flat-square" alt="22 Módulos" />
  <img src="https://img.shields.io/badge/Modelos_Prisma-38-6366f1?style=flat-square" alt="38 Modelos" />
  <img src="https://img.shields.io/badge/Conformidade-COFFITO_%7C_LGPD_%7C_ANS_TISS_4.01-10b981?style=flat-square" alt="Conformidade" />
  <img src="https://img.shields.io/badge/Produ%C3%A7%C3%A3o-fisioterahub.com-000000?style=flat-square" alt="Produção" />
</p>

[← Voltar ao Portfólio Principal](../README.md) • [🌐 Acessar Plataforma](https://fisioterahub.com) • [📸 Tour pelos Módulos](#-tour-pelos-módulos-prints-reais) • [⚡ Benchmark 57k RPS](#-benchmark-real-de-carga-57064-rps-em-1-vcpu)

</div>

> **Nota de confidencialidade:** produto comercial de código privado. Todas as capturas abaixo foram registradas em ambiente demonstrativo com dados fictícios (`Clínica OrthoVita`), sem expor código proprietário ou dados reais de pacientes.

---

## 💡 O Desafio

Clínicas de fisioterapia e Pilates frequentemente operam no improviso: agenda no WhatsApp, prontuários em papel sem rastreabilidade (**COFFITO / LGPD**), faturamento manual de guias **ANS TISS / TUSS** e planilhas financeiras desconectadas. O **FisioTeraHub** unifica toda a clínica em um SaaS multi-tenant seguro, auditável e absurdamente rápido mesmo rodando em uma VPS enxuta de **1 vCPU / 2 GB RAM**.

---

## 📸 Tour pelos Módulos (Prints Reais)

### 1. Página Pública & Dashboard Executivo
Entrada comercial focada em conversão e painel gerencial com indicadores em tempo real, ações rápidas do dia, status dos módulos contratados e auditoria de acessos recentes.

<table>
  <tr>
    <td align="center" width="50%">
      <img src="../assets/fisio-home.png" alt="FisioTeraHub — Landing Page Pública" width="100%" /><br/>
      <strong>Landing Page Pública</strong><br/>
      <sub><code>https://fisioterahub.com</code></sub>
    </td>
    <td align="center" width="50%">
      <img src="../assets/fisio-dashboard.png" alt="FisioTeraHub — Dashboard Executivo" width="100%" /><br/>
      <strong>Painel de Gestão Clínica</strong><br/>
      <sub>KPIs do dia, ações rápidas e status multi-filial</sub>
    </td>
  </tr>
</table>

---

### 2. Agenda Clínica, Pacientes & Turmas de Pilates
Controle visual de horários por profissional e sala, gestão completa de prontuários longitudinais imutáveis e organização de turmas/grupos recorrentes.

<table>
  <tr>
    <td align="center" width="50%">
      <img src="../assets/fisio-agenda.png" alt="FisioTeraHub — Agenda Clínica" width="100%" /><br/>
      <strong>Agenda Clínica Inteligente</strong><br/>
      <sub>Visão por status, profissional e sala</sub>
    </td>
    <td align="center" width="50%">
      <img src="../assets/fisio-pacientes.png" alt="FisioTeraHub — Gestão de Pacientes" width="100%" /><br/>
      <strong>Gestão de Pacientes &amp; Prontuários</strong><br/>
      <sub>Evolução imutável alinhada ao COFFITO e LGPD</sub>
    </td>
  </tr>
  <tr>
    <td align="center" width="50%">
      <img src="../assets/fisio-turmas.png" alt="FisioTeraHub — Turmas e Grupos" width="100%" /><br/>
      <strong>Turmas &amp; Grupos (Pilates / Reabilitação)</strong><br/>
      <sub>Controle de vagas, horários e frequência</sub>
    </td>
    <td align="center" width="50%">
      <img src="../assets/fisio-exercicios.png" alt="FisioTeraHub — Banco de Exercícios Domiciliares" width="100%" /><br/>
      <strong>Banco de Exercícios Domiciliares</strong><br/>
      <sub>Biblioteca com vídeos do YouTube e prescrição ao paciente</sub>
    </td>
  </tr>
</table>

---

### 3. Financeiro, Convênios ANS TISS 4.01 & Comunicação WhatsApp
Faturamento completo com Pix/boletos (Asaas), importação OFX, tabela TUSS + geração de lotes XML TISS e régua automática de lembretes no WhatsApp (Evolution API) e e-mail (Resend).

<table>
  <tr>
    <td align="center" width="33%">
      <img src="../assets/fisio-financeiro.png" alt="FisioTeraHub — Financeiro" width="100%" /><br/>
      <strong>Financeiro &amp; Cobranças</strong><br/>
      <sub>Contas, Pix, boletos FEBRABAN e OFX</sub>
    </td>
    <td align="center" width="33%">
      <img src="../assets/fisio-convenios.png" alt="FisioTeraHub — Convênios e TISS" width="100%" /><br/>
      <strong>Convênios &amp; ANS TISS 4.01</strong><br/>
      <sub>Operadoras, códigos TUSS e lotes XML</sub>
    </td>
    <td align="center" width="33%">
      <img src="../assets/fisio-comunicacao.png" alt="FisioTeraHub — Comunicação e WhatsApp" width="100%" /><br/>
      <strong>Comunicação &amp; WhatsApp</strong><br/>
      <sub>Lembretes automáticos anti-faltas</sub>
    </td>
  </tr>
</table>

---

### 📱 Experiência Mobile (Celular & Tablet)

<table>
  <tr>
    <td align="center" width="25%">
      <img src="../assets/fisio-mobile-home.png" alt="FisioTeraHub Mobile — Home" width="100%" /><br/>
      <strong>Landing Mobile</strong>
    </td>
    <td align="center" width="25%">
      <img src="../assets/fisio-mobile-features.png" alt="FisioTeraHub Mobile — Recursos" width="100%" /><br/>
      <strong>COFFITO &amp; TISS</strong>
    </td>
    <td align="center" width="25%">
      <img src="../assets/fisio-mobile-dashboard.png" alt="FisioTeraHub Mobile — Dashboard" width="100%" /><br/>
      <strong>Dashboard Mobile</strong>
    </td>
    <td align="center" width="25%">
      <img src="../assets/fisio-mobile-agenda.png" alt="FisioTeraHub Mobile — Agenda" width="100%" /><br/>
      <strong>Agenda Mobile</strong>
    </td>
  </tr>
</table>

---

## 🧠 Arquitetura & Edge Microcaching

```mermaid
flowchart LR
    Client["Navegador / Mobile / Portal do Paciente"]
    CF["Cloudflare Edge\nOrigin Shielding + RFC 9111\n(99,997% Cache Hit)"]
    Nginx["Nginx Proxy Reverso\n(VPS 1 vCPU / 2 GB RAM)"]
    API["API Express Modular\n22 Módulos + RBAC + OWASP JWT"]
    DB[("PostgreSQL 16\n38 Modelos Prisma Multi-tenant")]
    EXT["Asaas • Resend • Evolution WhatsApp"]

    Client --> CF --> Nginx --> API --> DB
    API --> EXT
```

---

## ⚡ Benchmark Real de Carga (57.064 RPS em 1 vCPU)

Testes reais de estresse executados no **Loader.io** com **10.000 clientes simultâneos contínuos** sobre uma VPS de **1 vCPU / 2 GB RAM**:

| Métrica | Sem Edge Cache | Com Edge Microcaching (RFC 9111) | Ganho Real |
| :--- | :---: | :---: | :---: |
| **Vazão Média (RPS)** | ~2.508 RPS | **~57.064 RPS** | **+2.175%** |
| **Requisições em 1 min** | 150.527 | **3.423.876** | +3,27 milhões |
| **Latência Média** | 4.549 ms | **68 ms** *(mín. 5 ms)* | **-98,5%** |
| **Timeouts / Erros** | 14,4% (5.802) | **0,0% (Zero erros)** | 100% estável |
| **CPU da VPS sob Pico** | 100% saturada | **~10% (repouso)** | Origem protegida |

<details>
<summary><strong>🛠️ Stack Completa & Salvaguardas de Engenharia</strong></summary>

- **Backend:** Node.js 20, TypeScript 5.8, Express 4, Prisma ORM 6, Zod, JWT em memória + Refresh Token rotacionado em Cookie `HttpOnly, Secure, SameSite=Strict`, Helmet, Rate-Limit e PDFKit.
- **Frontend:** React 18, Vite 6, Tailwind CSS, TanStack Query v5, React Hook Form e React Router v7.
- **Banco & Performance:** PostgreSQL 16 com `tenantId` obrigatório, Nested Writes atômicos, eliminação de N+1 (`findMany` em lote), projeções `select` cirúrgicas e `Cache-Control: private, no-store` em todas as rotas LGPD.
- **Integrações:** Asaas (Pix, boletos e assinaturas), Resend (e-mail transacional) e Evolution API (WhatsApp).

</details>

---

<div align="center">
  <a href="https://fisioterahub.com"><strong>🌐 Acessar FisioTeraHub em Produção</strong></a> &nbsp;•&nbsp; <a href="../README.md"><strong>← Voltar ao Portfólio Principal</strong></a>
</div>
