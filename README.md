 SaaS para Microempreendedores - Projeto BRISA (ULBRA)

 📌 Sobre o Projeto
Este projeto está a ser desenvolvido como parte da imersão técnica do programa BRISA (ULBRA). O objetivo é criar uma solução SaaS (Software as a Service) focada em ajudar microempreendedores a gerir os seus negócios de forma simplificada.

 🚀 Funcionalidades (Em desenvolvimento)
- [x] Estrutura base do projeto e configuração de ambiente.
- [ ] Módulo de gestão de inventário/vendas.
- [ ] Dashboard para visualização de lucros e despesas.

 📂 Estrutura de Pastas
```text
├── src/           # Código-fonte do sistema
├── data/          # Arquivos de dados e bases (ex: CSV, JSON)
├── docs/          # Documentação adicional
├── requirements.txt # Dependências do projeto
└── README.md      # Este ficheiro


---
## 🏗️ Implementação da Arquitetura (Por: Fernanda)
Este projeto utiliza uma estrutura **3-Tier** para garantir escalabilidade:
- **/backend**: Camada de lógica e API (Flask).
- **/frontend**: Camada de interface (React).
- **docker-compose.yml**: Gestão do Banco de Dados e containers.
**Objetivo:** Garantir a escalabilidade do software e a facilidade de manutenção independente de cada módulo.
[ ARQUITETURA 3-TIER - FLUXO DE DADOS ]

---
### 🖼️ Diagrama da Arquitetura

```mermaid
graph TD
    User[🖥️ Usuário]
    subgraph "Camada de Interface"
        Frontend[1️⃣ FRONTEND\n(React Container)]
    end
    subgraph "Camada de Lógica"
        Backend[2️⃣ BACKEND\n(Flask API Container)]
    end
    subgraph "Camada de Dados"
        Database[(3️⃣ BANCO DE DADOS\nPostgreSQL)]
    end

    User <--> Frontend
    Frontend <--> Backend
    Backend <--> Database
