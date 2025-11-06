# 🏗️ Drywall Hub

<div align="center">

![Version](https://img.shields.io/badge/version-2.1-blue.svg)
![Python](https://img.shields.io/badge/python-3.8+-blue.svg)
![Streamlit](https://img.shields.io/badge/streamlit-1.28+-red.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Status](https://img.shields.io/badge/status-active-success.svg)

**Centralizar e acelerar todo o fluxo de orçamento de drywall**

[Funcionalidades](#-funcionalidades) • [Como Usar](#-como-usar) • [Tecnologias](#-tecnologias) • [Roadmap](#-roadmap)

</div>

---

## 📋 Sobre o Projeto

**Drywall Hub** é uma aplicação web profissional desenvolvida para revolucionar o processo de orçamentação de projetos em drywall. Criada com foco em agilidade, precisão e profissionalismo, a plataforma elimina planilhas manuais e oferece uma experiência completa de gestão de projetos de construção a seco.

### 🎯 Problema que Resolve

Profissionais de drywall tradicionalmente enfrentam:
- ⏱️ Perda de tempo com cálculos manuais e planilhas complexas
- 💰 Erros de orçamentação que resultam em prejuízos
- 📊 Dificuldade em gerenciar múltiplos projetos simultaneamente
- 🤝 Apresentação de propostas pouco profissionais aos clientes
- 🔧 Compra excessiva ou insuficiente de materiais

**Drywall Hub** soluciona todos esses problemas em uma única plataforma intuitiva e poderosa.

---

## ✨ Funcionalidades

### 🚀 **Cálculo Rápido e Preciso**
- **Cálculo em segundos**: Projetos complexos de paredes, forros e sancas calculados instantaneamente
- **Suporte a múltiplos tipos**: Paredes (48mm, 70mm, 90mm), Forros rebaixados, Sancas fechadas
- **Consideração de variáveis**: Portas, janelas, isolamento acústico/térmico, tipos de painéis (ST, RU, RF)
- **Espaçamento customizável**: Montantes a 40cm ou 60cm
- **Algoritmos precisos**: Cálculo otimizado de materiais com margem de segurança

### 💎 **Otimização de Compra Inteligente**
- **Algoritmo de menor custo**: Calcula automaticamente a melhor combinação de embalagens (SKUs)
- **Suporte a múltiplas opções**: Compara pacotes de diferentes tamanhos para encontrar o menor custo
- **Redução de desperdício**: Compra exatamente o necessário sem excesso

### 📊 **Gestão Profissional de Projetos**
- **Dashboard centralizado**: Visualize todos os seus projetos em um só lugar
- **Projetos ilimitados**: (Plano PRO) Crie e gerencie quantos projetos precisar
- **Histórico completo**: Acesse projetos anteriores a qualquer momento
- **Edição em tempo real**: Modifique paredes, forros e sancas com facilidade
- **Resumo visual**: Veja métricas consolidadas de cada projeto

### 💰 **Lista de Preços 100% Customizada**
- **Preços personalizados**: Configure os preços de cada material de acordo com seu fornecedor
- **SKUs flexíveis**: Adicione múltiplas opções de embalagem para cada material
- **Sincronização em nuvem**: Seus preços salvos e acessíveis de qualquer dispositivo

### 📝 **Propostas Profissionais com 1 Clique**
- **Geração automática**: Crie propostas formatadas e elegantes instantaneamente
- **Detalhamento completo**: Inclui custos de material, mão de obra e BDI/lucro
- **Personalização**: Adicione dados do cliente, obra e validade
- **Apresentação impecável**: Impressione seus clientes com documentos profissionais
- **Exportação fácil**: Salve em PDF para envio ao cliente

### 🎨 **Interface Moderna e Intuitiva**
- **Design limpo**: Interface "Industrial Clean" com foco na usabilidade
- **Navegação fluida**: Acesso rápido a todas as funcionalidades
- **Tooltips explicativos**: Ajuda contextual em termos técnicos
- **Responsivo**: Funciona perfeitamente em desktops e tablets
- **Feedback visual**: Confirmações e alertas claros em cada ação

---

## 🛠️ Tecnologias

### **Backend**
- ![Python](https://img.shields.io/badge/-Python-3776AB?style=flat&logo=python&logoColor=white) **Python 3.8+**
- ![Streamlit](https://img.shields.io/badge/-Streamlit-FF4B4B?style=flat&logo=streamlit&logoColor=white) **Streamlit** - Framework web para aplicações data-driven
- ![Supabase](https://img.shields.io/badge/-Supabase-3ECF8E?style=flat&logo=supabase&logoColor=white) **Supabase** - Backend as a Service (PostgreSQL, Auth, Storage)

### **Frontend**
- **HTML/CSS** - Estilização customizada com tema "Industrial Clean"
- **Markdown** - Renderização de conteúdo e documentação
- **Google Fonts** - Tipografia Roboto

### **Bibliotecas Python**
```python
streamlit            # Framework web
pandas               # Manipulação de dados
supabase             # Cliente Backend-as-a-Service
```

### **Banco de Dados**
- **PostgreSQL** (via Supabase)
  - Tabelas: `users`, `user_prices`, `projects`, `project_items`
  - Autenticação segura com JWT
  - Políticas RLS (Row Level Security)

---

## 📦 Estrutura do Projeto

```
drywall-hub/
│
├── app_drywall_redesigned.py   # Aplicação principal Streamlit
├── core_calc.py                 # Lógica de cálculo de materiais
├── style.css                    # Estilização customizada
├── logo.png                     # Logo do aplicativo
├── requirements.txt             # Dependências Python
├── .streamlit/
│   └── secrets.toml             # Credenciais (não versionado)
└── README.md                    # Este arquivo
```

### 📁 Descrição dos Arquivos

#### `app_drywall_redesigned.py`
Arquivo principal da aplicação contendo:
- Configuração do Streamlit e sistema de design
- Integração com Supabase (autenticação e banco de dados)
- Sistema de gerenciamento de projetos
- Interfaces de cálculo (Paredes, Forros, Sancas)
- Gerenciamento de preços customizados
- Geração de resultados e propostas
- Componentes reutilizáveis e validações

#### `core_calc.py`
Módulo de cálculos contendo:
- Funções de cálculo de materiais para paredes, forros e sancas
- Algoritmo de otimização de compra (menor custo)
- Normalização de nomes de materiais
- Constantes de unidades de venda e preços padrão
- Lógica de arredondamento inteligente

#### `style.css`
Estilização visual com:
- Sistema de design tokens (cores, espaçamentos, sombras)
- Tema "Industrial Clean"
- Overrides customizados do Streamlit
- Estilos para cards, botões, inputs e alertas
- Layout responsivo

---

## 💻 Como Usar

### **1. Primeiro Acesso**

1. Crie uma conta ou faça login
2. Seus preços padrão serão automaticamente configurados
3. Você será direcionado ao Dashboard

### **2. Configurar Preços (Recomendado)**

Antes de calcular seu primeiro projeto:

1. Acesse **💰 Preços** no menu lateral
2. Edite os preços de acordo com seus fornecedores
3. Configure múltiplas opções de embalagem (SKUs) se desejar
4. As alterações são salvas automaticamente

### **3. Criar um Novo Projeto**

1. No **📊 Dashboard**, insira o nome do projeto (ex: "Casa Sra. Maria")
2. Clique em **✓ Criar e Carregar Projeto**
3. O projeto será criado e carregado automaticamente

### **4. Adicionar Paredes**

1. Acesse **🏠 Paredes** no menu
2. Preencha as dimensões (Comprimento e Altura)
3. Selecione a estrutura (48mm, 70mm ou 90mm)
4. Escolha o tipo de painel (ST, RU ou RF)
5. Configure portas, isolamento e espaçamento se necessário
6. Clique em **✓ Adicionar ao Projeto**

### **5. Adicionar Forros**

1. Acesse **🧩 Forros** no menu
2. Preencha Comprimento, Largura e Descida do Arame
3. Selecione o tipo de painel
4. Clique em **✓ Adicionar ao Projeto**

### **6. Adicionar Sancas**

1. Acesse **💡 Sancas** no menu
2. Escolha o tipo (Fechada ou Aberta)
3. Preencha Comprimento e dimensões X e Y
4. Clique em **✓ Adicionar ao Projeto**

### **7. Visualizar Resultados**

1. Acesse **📊 Resultados** no menu
2. Veja o detalhamento de materiais consolidados
3. Confira a lista de compra otimizada
4. Analise os custos totais (Material + M.O. + BDI)

### **8. Gerar Proposta para Cliente**

1. Acesse **📝 Proposta** no menu
2. Preencha os dados do cliente e da obra
3. Configure valores de M.O. e BDI/Lucro
4. Visualize a proposta formatada
5. Use o botão de impressão do navegador para salvar em PDF

### **9. Salvar Progresso**

- Use **💾 Salvar Projeto Atual** na barra lateral a qualquer momento
- Todos os itens e configurações serão salvos na nuvem

### **10. Gerenciar Projetos**

- No **📊 Dashboard**, veja todos os seus projetos salvos
- Use **Carregar** para reabrir um projeto existente
- Use **Excluir** para remover projetos (⚠️ ação irreversível)

---

## 📸 Screenshots

Sugestões de screenshots:
- Dashboard com projetos
- Interface de cálculo de paredes
- Página de gerenciamento de preços
- Proposta formatada para cliente
- Resultados consolidados

---

## 🗺️ Roadmap

### **Versão Atual (v2.1)**
- ✅ Sistema de gerenciamento de projetos
- ✅ Cálculo de paredes, forros e sancas
- ✅ Otimização de compra de materiais
- ✅ Preços customizados por usuário
- ✅ Geração de propostas profissionais
- ✅ Interface moderna e responsiva
- ✅ Autenticação e banco de dados em nuvem

### **Próximas Melhorias (v2.2 - v3.0)**

#### 🎯 **Alta Prioridade**
- [ ] **Exportação de PDF nativa**: Gerar PDFs diretamente no app (sem depender do navegador)
- [ ] **Plano PRO**: Sistema de assinatura com Stripe/Mercado Pago
- [ ] **Templates de proposta**: Múltiplos layouts visuais customizáveis
- [ ] **Histórico de revisões**: Versionar alterações em projetos
- [ ] **Duplicação de projetos**: Copiar projetos existentes como base

#### 🚀 **Funcionalidades Avançadas**
- [ ] **Cálculo de Steel Frame**: Suporte a estruturas Steel Frame
- [ ] **Importação de plantas**: Upload de DWG/PDF para cálculo automático
- [ ] **App mobile**: Versão nativa para Android/iOS
- [ ] **Modo offline**: Trabalhe sem internet e sincronize depois
- [ ] **Análise de rentabilidade**: Dashboard com métricas de lucro por projeto

#### 🎨 **UX/UI**
- [ ] **Tema escuro**: Opção de modo noturno
- [ ] **Tutoriais interativos**: Onboarding guiado para novos usuários
- [ ] **Atalhos de teclado**: Navegação rápida por teclas
- [ ] **Arrastar e soltar**: Reordenar itens visualmente

#### 🤝 **Colaboração**
- [ ] **Compartilhamento de projetos**: Enviar link de visualização para clientes
- [ ] **Equipes**: Múltiplos usuários trabalhando no mesmo projeto
- [ ] **Comentários**: Sistema de notas e anotações em itens

#### 📊 **Relatórios e Análises**
- [ ] **Dashboard financeiro**: Receita, custos e lucro consolidados
- [ ] **Gráficos de desempenho**: Visualização de métricas ao longo do tempo
- [ ] **Exportação para Excel**: Relatórios detalhados em planilha

#### 🔧 **Técnico**
- [ ] **API pública**: Integração com outros sistemas
- [ ] **Testes automatizados**: Garantir qualidade do código
- [ ] **CI/CD**: Pipeline de deploy automatizado
- [ ] **Logs e monitoramento**: Rastreamento de erros e performance

---

## 📄 Licença

Este projeto está sob a licença **MIT**. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

```
MIT License

Copyright (c) 2025 Drywall Hub

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software...
```

---

## 👨‍💻 Autor

**Desenvolvido com ❤️ e ☕ por Orivaldo Malicheski Neto**

<div align="center">

[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/orivaldo-malicheski-b0aa342b4)
[![GitHub](https://img.shields.io/badge/-GitHub-181717?style=flat&logo=github&logoColor=white)](https://github.com/OrivaldoMN)
[![Email](https://img.shields.io/badge/-Email-D14836?style=flat&logo=gmail&logoColor=white)](mailto:orivaldo.psn@gmail.com)


</div>

---

## 📈 Status do Projeto

- **Status**: 🟢 Ativo e em desenvolvimento
- **Versão**: 2.1
- **Última atualização**: Novembro 2025
- **Próxima release**: v2.2 (Exportação PDF nativa)

---

<div align="center">

**⭐ Se este projeto foi útil para você, considere dar uma estrela no GitHub! ⭐**

---

**🏗️ Drywall Hub** - *Transformando a forma como profissionais de drywall trabalham*

</div>
