# SAD Alvorada — Sistema de Apoio à Decisão Data-Driven

> **SAD Alvorada** é uma plataforma **B2B SaaS** analítica, preditiva e prescritiva projetada para superar a miopia financeira em Pequenas e Médias Empresas (PMEs). O sistema combina motores de **KDD (Knowledge Discovery in Databases)**, um **Cockpit de Valor com Simulação What-If (Modelo Damodaran)** e um **Comitê Multiagente de Inteligência Artificial (CrewAI / Groq LLaMA-3.3-70B)**.

🌐 **Acesse o Portfólio Executivo do Desenvolvedor:** https://portfolio-executivo-app.web.app/

---

## 📽️ Apresentação Executiva / Pitch Deck (10 Slides)

### 📊 Slide 1: O Problema da Miopia Financeira nas PMEs
* **Estatística Crítica:** Mais de 90% das PMEs tomam decisões de preço, estoque e investimentos baseadas puramente em intuição ou em réplicas concorrenciais.
* **O Retrovisor Contábil:** ERPs tradicionais apenas registram o passado, sem projetar o impacto financeiro futuro.
* **Risco de Caixa:** Falta de ferramentas de teste de estresse (What-If) resulta em corrosão de margens e alta taxa de mortalidade empresarial.

### 💡 Slide 2: A Solução — SAD Alvorada
* **Plataforma B2B SaaS:** Aplicação analítica preditiva e prescritiva em Progressive Web App (PWA).
* **Entrada de Dados Simplificada:** Ingestão e higienização automática de planilhas de PDV e caixa (CSV, XLSX, SQL).
* **Decisão Orientada por Dados:** Tradução de números brutos em alavancas práticas de geração de valor corporativo.

### 🤖 Slide 3: Motor KDD & Machine Learning
* **Execução Paralela de 5 Algoritmos:**
  1. **K-Means:** Clusterização e segmentação RFM (Recência, Frequência e Valor) de clientes.
  2. **DBSCAN:** Filtro estatístico para detecção e remoção de anomalias/outliers no faturamento.
  3. **Apriori / FP-Growth:** Engenharia de vendas casadas e combos promocionais para giro de estoque.
  4. **LightGBM + SHAP:** Classificação de risco de insolvência com transparência e explicabilidade causal.
  5. **Regressão Quadrática:** Elasticidade-preço e cálculo do ponto de equilíbrio ótimo (Break-Even).

### 🎛️ Slide 4: Cockpit de Valor & Simulação What-If
* **Fundamentação Acadêmica:** Baseado nas metodologias de avaliação de valor de Aswath Damodaran e Tom Copeland.
* **Sliders Interativos:** Teste de cenários em tempo real para Preço, Volume, Custos Fixos/Variáveis e Prazos.
* **Métricas em Tempo Real:** Recálculo instantâneo do EVA (Economic Value Added), ROIC, NCG e Ponto de Equilíbrio.

### 👥 Slide 5: Comitê Multiagente de IA (CrewAI)
* **Orquestração de 4 Subagentes Especialistas:**
  * Estrategista: Analisa tendências de longo prazo e cenários macroeconômicos.
  * Vendedor: Sugere combos e estratégias de precificação ativa.
  * Auditor: Monitora desvios, margens e anomalias de faturamento.
  * Decisor: Consolida o debate e emite a recomendação final em linguagem clara.
* **Infraestrutura:** Conexão com API Groq de ultra-baixa latência alimentada pelo modelo LLaMA-3.3-70B.

### 📱 Slide 6: Interface PWA & Experiência do Usuário (UX)
* **Visual Dark Glassmorphism:** Interface moderna, responsiva e otimizada para desktop, tablet e mobile.
* **Modo Offline:** Suporte a execução resiliente e armazenamento local via Service Worker.
* **Quatro Módulos Principais:** Autenticação Restrita (2FA/JWT), Central de Inteligência, Cockpit What-If e SAD Report.

### 🛡️ Slide 7: Auditoria, Rastreabilidade & Hash Criptográfico
* **SAD Report:** Geração de pareceres formais prontos para impressão em padrão A4 e exportação em PDF.
* **Hash SHA-256:** Cada parecer gerado recebe um código criptográfico imutável gravado no ledger interno.
* **Segurança Jurídica:** Garantia de integridade e não-repúdio perante bancos, investidores e conselhos.

### 💰 Slide 8: Modelo de Negócios & Go-To-Market
* **SaaS B2B por Assinatura:** Cobrança recorrente automatizada via integração nativa com Stripe.
* **Estratégia B2B2B:** Distribuição em parceria com escritórios de BPO Financeiro, consultorias e escritórios de contabilidade.
* **Módulos Faturáveis:** Planos Básico, Profissional e Enterprise com gestão de licenças no painel Admin.

### ⚡ Slide 9: Diferenciais Competitivos
* **SAD vs. ERPs Tradicionais:** Foco na simulação prospectiva de futuro, e não no mero registro passivo do passado.
* **SAD vs. Power BI / Tableau:** Diagnóstico automatizado em segundos, sem necessidade de programadores ou consultores caros.
* **Soberania do Gestor:** Cumprimento rigoroso da teoria clássica de SAD — a máquina simula e recomenda, mas a decisão final é 100% do ser humano.

### 🌐 Slide 10: Portfólio & Contato
* **Desenvolvedor Full-Stack:** Carlos de Souza de Jesus
* **Portfólio Executivo:** https://portfolio-executivo-app.web.app/
* **Status do Projeto:** MVP totalmente validado e operante pronto para escala e apresentações comerciais.

---

## 🏛️ Arquitetura do Sistema

```text
 ┌─────────────────────────────────────────────────────────┐
 │                   PWA Frontend (HTML5/CSS3/JS)           │
 │               Dark Glassmorphism & Service Worker       │
 └────────────────────────────┬────────────────────────────┘
                              │ REST API (JWT + 2FA)
 ┌────────────────────────────▼────────────────────────────┐
 │                  Backend FastAPI (Python 3.12)          │
 ├─────────────────────────────────────────────────────────┤
 │  • Ingestor Universal CSV/XLSX                          │
 │  • Motor KDD (K-Means, DBSCAN, Apriori, LightGBM, SHAP) │
 │  • Cockpit What-If de Valor (Damodaran EVA/ROIC)        │
 │  • Comitê Multiagente (CrewAI + Groq LLaMA-3.3-70B)    │
 └────────────────────────────┬────────────────────────────┘
                              │ SQLAlchemy ORM
 ┌────────────────────────────▼────────────────────────────┐
 │               Banco de Dados & Seguridad                │
 │    SQLite/PostgreSQL + Ledger Hash SHA-256 + Stripe     │
 └────────────────────────────┴────────────────────────────┘
```

---

## 💻 Tech Stack

* **Frontend:** PWA (Progressive Web App), JavaScript ES6+, HTML5, CSS3 Glassmorphism, Chart.js.
* **Backend:** Python 3.12, FastAPI, Uvicorn, SQLAlchemy ORM, Pydantic.
* **Data Science & ML:** Pandas, NumPy, Scikit-Learn, LightGBM, SHAP, MLxtend.
* **IA Multiagente:** CrewAI, Groq API (LLaMA-3.3-70B).
* **Segurança & Pagamentos:** JWT (JSON Web Tokens), PyOTP (2FA), Cryptography (SHA-256), Stripe SDK.

---

## 👨‍💻 Autor & Portfólio

**Carlos de Souza de Jesus**  
*Desenvolvedor de Software & Analista de Sistemas de Apoio à Decisão*  
🌐 **Portfólio Executivo:** https://portfolio-executivo-app.web.app/
