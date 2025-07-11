# 🔗 Rastreabilidade com os Diagramas

Este documento apresenta a rastreabilidade entre as principais funcionalidades implementadas no MVP do aplicativo ReConectar e os elementos representados nos diagramas do projeto: Diagrama de Classes, Diagrama C4 (níveis Container e Componente). A seguir, cada funcionalidade implementada no MVP é conectada com as respectivas estruturas de modelagem.


---

## Funcionalidade: Login e Cadastro

Permite que o usuário entre com e-mail e senha ou realize cadastro com nome, e-mail e senha.

### Diagrama de Classes:
- Autenticação: contém os métodos login(email, senha) e register(nome, email, senha).
- Usuario: armazena os dados básicos do usuário como nome, email, senha.

### Modelo C4

- Container: A funcionalidade está no container App Mobile (Thunkable).
- Container: Conecta-se ao container API Backend (Node.js + Express), que se comunica com o Sistema de Autenticação e com o Firebase.
- Componente: Controlador de Autenticação, responsável por lidar com login e registro de usuários.

---

## Funcionalidade: Exibição de Eventos Presenciais

Exibe uma lista de eventos culturais com nome, descrição, local e imagem ilustrativa.

### Diagrama de Classes:
- PublicacaoEspecialista: representa a estrutura dos eventos publicados.
- EspecialistaUsuario: autor dos eventos visíveis aos usuários.

### Modelo C4

- Container: Está presente no App Mobile (Thunkable), via componente Feed de Conteúdo.
- Container: Conecta-se ao Backend via Gerenciador de Conteúdo do Especialista.
- Componente: Visualizador de Conteúdo do Especialista, que exibe o conteúdo publicado.

---

## Funcionalidade: Relatório de Bloqueio de Ferramentas de IA

Exibe ferramentas como ChatGPT e Copilot com horários e tempo restante de bloqueio.

### Diagrama de Classes:
- historicoDeUso: registra tempo de uso de ferramentas e gera relatórios.
- Usuario: acessa os dados de uso e visualiza o relatório.

### Modelo C4

- Container: Se conecta ao API Backend, que acessa o Android Accessibility Service para dados de uso.
- Componente: Gerador de Relatórios no backend, responsável por consolidar os dados.

---

## Funcionalidade: Desafios Ativos e Progresso

Mostra desafios em andamento (como “caminhar 3x por semana”) e desafios concluídos com barra de progresso.

### Diagrama de Classes:
- Desafio: representa o desafio com conteúdo e data.
- desafioParticipacao: registra a participação e progresso do usuário.

### Modelo C4

- Container: Conecta-se ao Backend, que se comunica com o firebase para armazenar os desafios.
- Componente: Serviço de Desafios gerencia os dados dos desafios e progresso.

---

## Funcionalidade: Exibição de Conquistas

Exibe conquistas desbloqueadas como “liberou trilha avançada” ou “falou com especialista”.

### Diagrama de Classes:
- Recompensa: permite que o usuário resgate recompensas se elegível.
- Usuario: acessa a lista de recompensas disponíveis e conquistadas.

### Modelo C4

- Container: API Backend, componente Serviço de Recompensas.
- Componente: Serviço de Recompensas calcula elegibilidade e envia dados.

---

## Funcionalidade: Chat com Especialista

Área para troca de mensagens com especialista com balão de chat.

### Diagrama de Classes:
- Mensagem: estrutura da conversa com remetente, destinatário e conteúdo.
- Usuario: envia e recebe mensagens.
- EspecialistaUsuario: destinatário da conversa.

### Modelo C4

- Container: App Mobile, componente Visualizador de Conteúdo do Especialista.
- Container: API Backend + firebase, componente Serviço de Envio de Mensagens.
- Componente: Serviço de Envio de Mensagens gerencia troca de mensagens entre usuários e especialistas.

---
