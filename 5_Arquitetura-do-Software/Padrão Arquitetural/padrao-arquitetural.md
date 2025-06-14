# Padrão Arquitetural 

## Arquitetura em Camadas

### ✅ Identificação

O padrão arquitetural escolhido para o desenvolvimento do sistema de apoio à saúde mental foi a **Arquitetura em Camadas**.

Esse padrão organiza a estrutura do sistema em camadas funcionais bem definidas, separando as responsabilidades em blocos independentes.

Abaixo, apresentamos uma tabela detalhada com as **funcionalidades e módulos do nosso sistema**, organizados por camada. Isso oferece uma visão clara de como a arquitetura foi pensada para refletir a estrutura do projeto:

➡️ Veja a tabela completa logo abaixo.

# 🧱 Tabela de Funcionalidades por Camada – Arquitetura em Camadas

Este documento apresenta as principais funcionalidades do sistema divididas segundo a Arquitetura em Camadas.

---

## 🎨 Camada de Apresentação

| **Funcionalidade / Módulo**                              | **Descrição**                                                                 |
|----------------------------------------------------------|--------------------------------------------------------------------------------|
| Interface do Usuário (UI)                                | Tela de chat, mural, relatórios, notificações, configurações, desafios etc.   |
| Sistema de recompensas (visual)                          | Exibição de pontos, conquistas, progresso pessoal                             |
| Alertas personalizados (notificações locais / push)      | Exibição de avisos quando apps bloqueados forem usados                        |
| Relatórios de uso digital (gráficos e estatísticas)      | Tela que mostra tempo de uso, frequência, metas pessoais etc.                 |

---

## ⚙️ Camada de Lógica de Negócio

| **Funcionalidade / Módulo**                              | **Descrição**                                                                 |
|----------------------------------------------------------|--------------------------------------------------------------------------------|
| Monitoramento de aplicativos de IA                       | Verificação ativa e em segundo plano dos apps definidos pelo usuário          |
| Controle de bloqueio e liberação                         | Gerenciamento dos apps permitidos e bloqueados                                |
| Processamento dos desafios                               | Validação de participação e geração de pontuação                              |
| Lógica do sistema de recompensas                         | Cálculo de pontos, regras, validação de conquistas                            |
| Gestão de alertas personalizados                         | Definições, horários, critérios para alertar o usuário                        |
| Notificações internas (posts novos, mensagens, alertas)  | Disparo de notificações internas do sistema                                   |
| Regras do chat e interações em grupo                     | Moderação, envio e recebimento de mensagens                                   |

---

## 🗄️ Camada de Acesso a Dados

| **Funcionalidade / Módulo**                              | **Descrição**                                                                 |
|----------------------------------------------------------|--------------------------------------------------------------------------------|
| Armazenamento de dados do usuário                        | Informações pessoais, preferências, status de desafios, estatísticas          |
| Banco de dados para mensagens, posts e recompensas       | Persistência de histórico de chat, mural informativo, conquistas              |
| Histórico de uso e bloqueios                             | Logs locais ou sincronizados com backend sobre tempo de uso e bloqueios       |
| Dados de configuração                                     | Configurações personalizadas do usuário armazenadas localmente/remotamente    |


### 🧠 Justificativa

A escolha pela arquitetura em camadas está alinhada com os objetivos e características do nosso projeto:

- **Domínio do problema:** O sistema busca fornecer um ambiente simples, estável e intuitivo para promover o bem-estar digital dos usuários. A divisão por camadas facilita a manutenção e escalabilidade do sistema à medida que novas funcionalidades forem sendo adicionadas.
- **Objetivos do projeto:** Nossa proposta envolve o gerenciamento de tarefas e hábitos, que podem ser organizados facilmente de forma modular em camadas separadas.
- **Requisitos não funcionais:** Priorizamos a **manutenibilidade**, **facilidade de desenvolvimento** e a **organização do código**, características bem atendidas por este padrão arquitetural.
- **Curva de aprendizado:** A equipe tem conhecimento básico de engenharia de software, e a arquitetura em camadas permite uma implementação mais rápida e compreensível por todos os membros.

### 🏗️ Visão Geral da Estrutura

Abaixo está um resumo da divisão das camadas que será adotada no sistema:

**[ Interface do Usuário ]**  
↓  
**[ Lógica de Aplicação ]**  
↓  
**[ Acesso a Dados ]**

Cada camada se comunica apenas com a camada diretamente abaixo dela, garantindo **coesão interna e baixo acoplamento**.

### ✅ Conclusão

A arquitetura em camadas proporciona uma base sólida para o desenvolvimento do nosso sistema, sendo adequada ao nosso escopo, conhecimento técnico atual e prazos disponíveis. Dessa forma, ela foi escolhida como o modelo estrutural principal para guiar as decisões da arquitetura de software nesta fase do trabalho.
