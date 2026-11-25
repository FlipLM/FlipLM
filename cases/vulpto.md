<div align="center">

# 🏎️ Vulpto — SaaS Multi-tenant para Estética Automotiva & Detailing

**Vistoria 3D interativa, Kanban de pátio ao vivo, preços por porte veicular, DRE gerencial real e CRM de retenção.**

<p>
  <img src="https://img.shields.io/badge/Next.js-14_App_Router-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" alt="Next.js 14" />
  <img src="https://img.shields.io/badge/TypeScript-5.6-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Three.js-Vistoria_3D-049EF4?style=for-the-badge&logo=threedotjs&logoColor=white" alt="Three.js" />
  <img src="https://img.shields.io/badge/PostgreSQL_%2B_Prisma-Multi--tenant-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/Redis-Cache-DC382D?style=for-the-badge&logo=redis&logoColor=white" alt="Redis" />
</p>

<p>
  <img src="https://img.shields.io/badge/M%C3%B3dulos-19_Integrados-10b981?style=flat-square" alt="19 Módulos" />
  <img src="https://img.shields.io/badge/Seguran%C3%A7a-RBAC_ADMIN_%7C_OPERATOR-6366f1?style=flat-square" alt="RBAC" />
  <img src="https://img.shields.io/badge/QA_E2E-43%2F43_Asser%C3%A7%C3%B5es-f59e0b?style=flat-square" alt="43/43" />
  <img src="https://img.shields.io/badge/Produ%C3%A7%C3%A3o-vulpto.duckdns.org-000000?style=flat-square" alt="Produção" />
</p>

[← Voltar ao Portfólio Principal](../README.md) • [🌐 Acessar Plataforma](https://vulpto.duckdns.org/) • [📸 Tour pelos Módulos](#-tour-pelos-módulos-prints-reais) • [🧠 Arquitetura](#-arquitetura-multi-tenant--rbac)

</div>

> **Nota de confidencialidade:** produto comercial de código privado. Todos os prints foram capturados em ambiente real de demonstração sem exposição de dados de clientes.

---

## 💡 O Desafio

Estúdios de detailing e lava-jatos especializados costumam perder margem em três frentes: **risco jurídico na recepção** (sem prova fotográfica de riscos prévios), **pátio caótico** sem controle de boxes/comissões e **cegueira financeira** sobre o lucro líquido real depois de insumos químicos, descontos e despesas fixas. O **Vulpto** resolve a operação de ponta a ponta em **19 módulos integrados**.

---

## 📸 Tour pelos Módulos (Prints Reais)

### 1. Landing Page SaaS & Dashboard Executivo
Apresentação comercial com simulador interativo de vistoria 3D e painel gerencial ao vivo exibindo ocupação do pátio, faturamento, ticket médio, despesas e lucro líquido real.

<table>
  <tr>
    <td align="center" width="50%">
      <img src="../assets/vulpto-home.png" alt="Vulpto — Página Inicial Pública" width="100%" /><br/>
      <strong>Landing Page SaaS</strong><br/>
      <sub><code>https://vulpto.duckdns.org/</code></sub>
    </td>
    <td align="center" width="50%">
      <img src="../assets/vulpto-dashboard.png" alt="Vulpto — Dashboard Executivo" width="100%" /><br/>
      <strong>Visão Geral da Estética</strong><br/>
      <sub>Ocupação de boxes, faturamento e margem líquida</sub>
    </td>
  </tr>
</table>

---

### 2. Operação de Pátio: Vistoria 360º, Kanban ao Vivo & Ordens de Serviço
Fluxo completo de entrada do veículo: checklist fotográfico com mapeamento de avarias, quadro **Kanban Drag & Drop** por etapa ou box físico e controle rigoroso de Ordens de Serviço.

<table>
  <tr>
    <td align="center" width="50%">
      <img src="../assets/vulpto-vistoria.png" alt="Vulpto — Recepção e Vistoria Digital 360º" width="100%" /><br/>
      <strong>Recepção &amp; Vistoria Digital 360º</strong><br/>
      <sub>Checklist de entrada, fotos e registro de avarias</sub>
    </td>
    <td align="center" width="50%">
      <img src="../assets/vulpto-patio.png" alt="Vulpto — Kanban do Pátio ao Vivo" width="100%" /><br/>
      <strong>Kanban do Pátio ao Vivo</strong><br/>
      <sub>Para Fazer → Em Serviço → Concluídos → Pagos</sub>
    </td>
  </tr>
  <tr>
    <td align="center" width="50%">
      <img src="../assets/vulpto-os.png" alt="Vulpto — Ordens de Serviço" width="100%" /><br/>
      <strong>Ordens de Serviço</strong><br/>
      <sub>Congelamento histórico de preços e PDF vetorial</sub>
    </td>
    <td align="center" width="50%">
      <img src="../assets/vulpto-servicos.png" alt="Vulpto — Catálogo e Matriz de Preços por Porte" width="100%" /><br/>
      <strong>Catálogo &amp; Preços por Porte</strong><br/>
      <sub>Hatch, Sedan, SUV/Picape, Moto e Utilitário</sub>
    </td>
  </tr>
</table>

---

### 3. Gestão Estratégica: DRE em Tempo Real, Estoque Químico & CRM de Retenção
Visibilidade contábil real (Receita Bruta → Custos Variáveis → Despesas Fixas → **Lucro Líquido**), controle de químicos com custo médio ponderado e CRM inteligente (dias de chuva, alerta de churn 45d+ e Curva ABC).

<table>
  <tr>
    <td align="center" width="33%">
      <img src="../assets/vulpto-financeiro.png" alt="Vulpto — Financeiro e DRE" width="100%" /><br/>
      <strong>Financeiro &amp; DRE Real</strong><br/>
      <sub>Margem líquida e contas a pagar</sub>
    </td>
    <td align="center" width="33%">
      <img src="../assets/vulpto-estoque.png" alt="Vulpto — Estoque Químico" width="100%" /><br/>
      <strong>Estoque Químico</strong><br/>
      <sub>Custo médio e alerta de mínimo</sub>
    </td>
    <td align="center" width="33%">
      <img src="../assets/vulpto-crm.png" alt="Vulpto — CRM e Retenção" width="100%" /><br/>
      <strong>CRM &amp; Retenção Ativa</strong><br/>
      <sub>Curva ABC, dias de chuva e churn 45d+</sub>
    </td>
  </tr>
</table>

---

### 📱 Experiência Mobile (Pátio, Dashboard & Vistoria 3D no Celular)

<table>
  <tr>
    <td align="center" width="25%">
      <img src="../assets/vulpto-mobile-home.png" alt="Vulpto Mobile — Home" width="100%" /><br/>
      <strong>Home Mobile</strong>
    </td>
    <td align="center" width="25%">
      <img src="../assets/vulpto-mobile-showcase.png" alt="Vulpto Mobile — Vistoria 3D Interativa" width="100%" /><br/>
      <strong>Vistoria 3D no Celular</strong>
    </td>
    <td align="center" width="25%">
      <img src="../assets/vulpto-mobile-dashboard.png" alt="Vulpto Mobile — Dashboard" width="100%" /><br/>
      <strong>Dashboard Mobile</strong>
    </td>
    <td align="center" width="25%">
      <img src="../assets/vulpto-mobile-patio.png" alt="Vulpto Mobile — Kanban do Pátio" width="100%" /><br/>
      <strong>Kanban Mobile</strong>
    </td>
  </tr>
</table>

---

## 🧠 Arquitetura Multi-tenant & RBAC

```mermaid
flowchart LR
    Users["Navegador / Tablet no Pátio\n(ADMIN vs OPERATOR)"]
    MW["Next.js 14 Middleware\nJWT HttpOnly + Deny-by-Default\n+ RBAC Server-Side"]
    UI["19 Módulos Operacionais\nVistoria 3D • Kanban • DRE • CRM"]
    API["Route Handlers + Zod\nPDF Vetorial • Comissões • Estoque"]
    PG[("PostgreSQL (Prisma)\nIsolamento por tenantId")]
    RD[("Redis Cache")]

    Users --> MW --> UI --> API --> PG
    API --> RD
```

<details>
<summary><strong>🛠️ Stack Completa & Validação de Qualidade</strong></summary>

- **Frontend:** Next.js 14 (App Router), React 18, TypeScript 5.6, Tailwind CSS, Framer Motion, Three.js (`@react-three/fiber` + `@react-three/drei`) e Lucide React.
- **Backend & Segurança:** Next.js Route Handlers, Zod, JWT (`jose`) em Cookies `HttpOnly`, Google OAuth2 PKCE, `timingSafeEqual`, `jsPDF` + `jspdf-autotable` e Nodemailer.
- **Qualidade:** suíte automatizada cobrindo autenticação, RBAC (`ADMIN` vs `OPERATOR`), vistorias, OS, financeiro e auditoria mobile (**43/43 asserções aprovadas**).

</details>

---

<div align="center">
  <a href="https://vulpto.duckdns.org/"><strong>🌐 Acessar Vulpto em Produção</strong></a> &nbsp;•&nbsp; <a href="../README.md"><strong>← Voltar ao Portfólio Principal</strong></a>
</div>
