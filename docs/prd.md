# 📄 Product Requirements Document (PRD)

## Gestão de Caronas na UTFPR

**Projeto:** Gestão de Caronas na UTFPR
**Disciplina:** Projeto de Frameworks
**Documento:** Product Requirements Document (PRD)
**Versão:** 1.0
**Data:** Setembro de 2026

---

# 1. Visão do Produto

## 1.1 Problema

Estudantes da UTFPR que precisam se deslocar até o campus podem ter dificuldades para encontrar pessoas que realizem trajetos semelhantes. Ao mesmo tempo, estudantes que utilizam veículos próprios podem realizar trajetos com lugares disponíveis, mas não possuem uma forma centralizada de divulgar essas vagas para outros alunos.

Atualmente, a combinação entre oferta e procura de caronas pode depender de grupos de mensagens e contatos informais, dificultando a localização de oportunidades compatíveis com o trajeto, horário e disponibilidade de vagas.

## 1.2 Solução

O sistema de **Gestão de Caronas na UTFPR** será uma plataforma web destinada aos estudantes da universidade para facilitar a oferta e a busca por caronas.

A plataforma permitirá que estudantes cadastrem caronas informando origem, destino, data, horário e quantidade de vagas disponíveis. Outros estudantes poderão consultar as caronas disponíveis, visualizar seus detalhes e solicitar participação.

O sistema também permitirá que o usuário acompanhe as caronas das quais participa ou que disponibilizou.

## 1.3 Objetivo

Facilitar a conexão entre estudantes da UTFPR que oferecem e procuram caronas, centralizando as informações necessárias para encontrar uma carona compatível com determinado trajeto e horário.

## 1.4 Público-alvo

Estudantes da UTFPR que:

* possuem veículo e desejam oferecer caronas;
* precisam de transporte para chegar ou sair do campus;
* desejam encontrar estudantes que realizem trajetos semelhantes;
* procuram uma forma organizada de gerenciar suas caronas.

---

# 2. Escopo do Produto

## 2.1 Dentro do escopo

O sistema deverá contemplar:

* cadastro e identificação de usuários;
* criação de caronas;
* consulta de caronas disponíveis;
* busca e filtragem de caronas;
* visualização dos detalhes de uma carona;
* solicitação de participação em uma carona;
* gerenciamento das vagas disponíveis;
* gerenciamento das caronas criadas pelo usuário;
* visualização das caronas das quais o usuário participa;
* cancelamento de participação;
* encerramento ou cancelamento de caronas pelo responsável.

## 2.2 Fora do escopo

Não fazem parte da primeira versão:

* pagamentos entre passageiros e motoristas;
* integração com aplicativos de mapas ou GPS;
* cálculo automático de rotas;
* rastreamento da localização dos usuários em tempo real;
* sistema de avaliação de usuários;
* chat em tempo real;
* integração automática com sistemas acadêmicos da UTFPR;
* confirmação de identidade por documentos oficiais;
* notificações por SMS ou WhatsApp;
* gerenciamento de veículos;
* cálculo automático de divisão de combustível.

---

# 3. Atores

## 3.1 Estudante

Usuário principal do sistema.

Pode:

* cadastrar-se;
* consultar caronas;
* criar uma carona;
* solicitar participação;
* cancelar sua participação;
* acompanhar suas caronas.

Um mesmo estudante pode atuar como **motorista** em uma carona e como **passageiro** em outra.

## 3.2 Responsável pela carona

Estudante que criou uma carona.

Pode:

* definir os dados da carona;
* informar a quantidade de vagas;
* acompanhar os participantes;
* cancelar ou encerrar a carona.

## 3.3 Passageiro

Estudante que solicita ou possui participação em uma carona.

Pode:

* visualizar os dados da carona;
* solicitar uma vaga;
* cancelar sua participação.

---

# 4. Glossário

| Termo             | Definição                                                                  |
| ----------------- | -------------------------------------------------------------------------- |
| Carona            | Deslocamento oferecido por um estudante para outros estudantes.            |
| Responsável       | Estudante que cadastrou a carona.                                          |
| Passageiro        | Estudante que participa de uma carona oferecida por outro usuário.         |
| Vaga              | Lugar disponível na carona para um passageiro.                             |
| Origem            | Local de onde a carona parte.                                              |
| Destino           | Local para onde a carona se dirige.                                        |
| Data              | Dia em que a carona será realizada.                                        |
| Horário           | Horário previsto para realização da carona.                                |
| Carona disponível | Carona cadastrada que ainda possui vagas e não foi encerrada ou cancelada. |
| Solicitação       | Pedido realizado por um estudante para participar de uma carona.           |

---

# 5. User Stories

## US01 — Criar conta

**Como** estudante da UTFPR,
**quero** criar uma conta na plataforma,
**para** poder utilizar as funcionalidades de oferta e participação em caronas.

**Prioridade:** Must Have
**Tamanho:** M
**Status:** Ready

### Critérios de aceitação

* Dado que o estudante está na tela de cadastro, quando preencher os campos obrigatórios com dados válidos, então sua conta deve ser criada.
* Dado que algum campo obrigatório não foi preenchido, quando o estudante tentar realizar o cadastro, então o sistema deve informar que o campo precisa ser preenchido.
* Dado que o e-mail informado já esteja cadastrado, quando o estudante tentar criar uma conta, então o sistema deve informar que o e-mail já está em uso.

---

## US02 — Entrar na plataforma

**Como** estudante cadastrado,
**quero** realizar login,
**para** acessar as funcionalidades da plataforma.

**Prioridade:** Must Have
**Tamanho:** S
**Status:** Ready

### Critérios de aceitação

* Dado que o estudante possui uma conta, quando informar credenciais válidas, então deve acessar a plataforma.
* Dado que as credenciais estejam incorretas, quando tentar entrar, então o sistema deve informar que os dados são inválidos.
* Dado que algum campo obrigatório esteja vazio, quando tentar realizar login, então o sistema deve solicitar o preenchimento.

---

## US03 — Criar uma carona

**Como** estudante,
**quero** cadastrar uma carona,
**para** oferecer vagas a outros estudantes.

**Prioridade:** Must Have
**Tamanho:** M
**Status:** Ready

### Critérios de aceitação

* Dado que o estudante está autenticado, quando preencher origem, destino, data, horário e quantidade de vagas válidos, então a carona deve ser criada.
* Dado que algum campo obrigatório não foi informado, quando tentar criar a carona, então o sistema deve impedir o cadastro e indicar o campo pendente.
* Dado que a carona foi criada corretamente, então ela deve ficar disponível para consulta enquanto possuir vagas e estiver ativa.

---

## US04 — Consultar caronas disponíveis

**Como** estudante,
**quero** visualizar as caronas disponíveis,
**para** encontrar uma opção compatível com meu deslocamento.

**Prioridade:** Must Have
**Tamanho:** M
**Status:** Ready

### Critérios de aceitação

* Dado que existem caronas ativas, quando o estudante acessar a listagem, então o sistema deve apresentar as caronas disponíveis.
* Cada carona apresentada deve informar, no mínimo, origem, destino, data, horário e quantidade de vagas.
* Caronas canceladas ou encerradas não devem aparecer como disponíveis.

---

## US05 — Filtrar caronas

**Como** estudante,
**quero** filtrar as caronas disponíveis,
**para** encontrar opções mais compatíveis com meu trajeto e horário.

**Prioridade:** Should Have
**Tamanho:** M
**Status:** Ready

### Critérios de aceitação

* O estudante deve poder informar critérios de busca disponíveis no sistema.
* Ao aplicar um filtro, a listagem deve apresentar somente caronas compatíveis com os critérios informados.
* Caso não existam resultados compatíveis, o sistema deve informar que nenhuma carona foi encontrada.

---

## US06 — Visualizar detalhes da carona

**Como** estudante,
**quero** visualizar os detalhes de uma carona,
**para** avaliar se ela atende às minhas necessidades antes de solicitar uma vaga.

**Prioridade:** Must Have
**Tamanho:** S
**Status:** Ready

### Critérios de aceitação

* Ao selecionar uma carona, o sistema deve apresentar seus principais dados.
* Os dados devem incluir origem, destino, data, horário e vagas disponíveis.
* O sistema deve permitir identificar o responsável pela carona.

---

## US07 — Solicitar participação em uma carona

**Como** estudante,
**quero** solicitar uma vaga em uma carona disponível,
**para** participar do deslocamento.

**Prioridade:** Must Have
**Tamanho:** M
**Status:** Ready

### Critérios de aceitação

* Dado que a carona possui vagas disponíveis, quando o estudante solicitar participação, então sua solicitação deve ser registrada.
* Dado que não existem vagas disponíveis, o sistema não deve permitir uma nova solicitação.
* O estudante não deve conseguir solicitar participação duas vezes na mesma carona.

---

## US08 — Cancelar participação

**Como** passageiro,
**quero** cancelar minha participação em uma carona,
**para** liberar a vaga caso eu não possa mais participar.

**Prioridade:** Should Have
**Tamanho:** S
**Status:** Ready

### Critérios de aceitação

* Dado que o estudante possui participação em uma carona, quando solicitar o cancelamento, então sua participação deve ser removida.
* Após o cancelamento, a vaga anteriormente ocupada deve voltar a ficar disponível.
* O estudante não deve continuar sendo apresentado como participante daquela carona.

---

## US09 — Gerenciar caronas criadas

**Como** responsável por uma carona,
**quero** visualizar e gerenciar minhas caronas,
**para** acompanhar os deslocamentos que ofereci.

**Prioridade:** Should Have
**Tamanho:** M
**Status:** Ready

### Critérios de aceitação

* O estudante deve conseguir visualizar as caronas que criou.
* O sistema deve apresentar a quantidade de vagas disponíveis.
* O responsável deve conseguir cancelar uma carona ativa.
* Uma carona cancelada não deve continuar disponível para novas solicitações.

---

## US10 — Visualizar minhas caronas

**Como** estudante,
**quero** visualizar as caronas das quais participo ou que criei,
**para** acompanhar meus deslocamentos.

**Prioridade:** Should Have
**Tamanho:** M
**Status:** Ready

### Critérios de aceitação

* O sistema deve apresentar as caronas criadas pelo estudante.
* O sistema deve apresentar as caronas nas quais o estudante possui participação.
* Cada registro deve apresentar informações suficientes para identificar a carona.
* Caronas canceladas ou encerradas devem ser identificadas adequadamente.

---

## US11 — Encerrar uma carona

**Como** responsável por uma carona,
**quero** encerrar uma carona,
**para** indicar que ela não está mais disponível para novas participações.

**Prioridade:** Could Have
**Tamanho:** S
**Status:** Ready

### Critérios de aceitação

* O responsável deve conseguir encerrar uma carona criada por ele.
* Uma carona encerrada não deve aceitar novas solicitações.
* Uma carona encerrada deve deixar de aparecer entre as caronas disponíveis.

---

# 6. Regras de Negócio

## RN01 — Autenticação

Somente usuários autenticados podem criar caronas ou solicitar participação em caronas.

## RN02 — Vagas

Uma carona não pode aceitar participantes além da quantidade de vagas disponibilizada pelo responsável.

## RN03 — Participação duplicada

Um estudante não pode possuir mais de uma participação na mesma carona.

## RN04 — Responsabilidade

Somente o responsável pela carona pode realizar ações administrativas sobre a própria carona.

## RN05 — Cancelamento

Quando um passageiro cancelar sua participação, a vaga deverá ficar novamente disponível.

## RN06 — Caronas indisponíveis

Caronas canceladas ou encerradas não devem aceitar novas solicitações.

## RN07 — Dados obrigatórios

Toda carona deve possuir, no mínimo:

* origem;
* destino;
* data;
* horário;
* quantidade de vagas.

## RN08 — Conta de usuário

Cada conta deve possuir um identificador único para evitar duplicidade de cadastro.

---

# 7. Requisitos Não Funcionais

## RNF01 — Usabilidade

A interface deve permitir que o estudante encontre as principais funcionalidades de forma clara e objetiva.

## RNF02 — Responsividade

A aplicação deve funcionar adequadamente em computadores, tablets e dispositivos móveis.

## RNF03 — Desempenho

As telas principais devem apresentar os dados sem atrasos perceptíveis em condições normais de uso.

## RNF04 — Segurança

Informações de autenticação devem ser armazenadas de forma segura, evitando o armazenamento de senhas em texto puro.

## RNF05 — Validação

Os dados enviados pelos usuários devem ser validados tanto na interface quanto no servidor.

## RNF06 — Disponibilidade

O sistema deve estar acessível durante os períodos previstos para utilização pelos estudantes.

## RNF07 — Manutenibilidade

O código deve possuir organização suficiente para permitir manutenção e evolução das funcionalidades.

---

# 8. Fluxos Principais

## 8.1 Fluxo para oferecer uma carona

1. Estudante acessa a plataforma.
2. Estudante realiza login.
3. Estudante acessa a opção de criar carona.
4. Informa origem.
5. Informa destino.
6. Informa data.
7. Informa horário.
8. Informa quantidade de vagas.
9. Sistema valida os dados.
10. Sistema cadastra a carona.
11. Carona passa a aparecer na listagem de disponíveis.

## 8.2 Fluxo para encontrar uma carona

1. Estudante acessa a plataforma.
2. Consulta as caronas disponíveis.
3. Utiliza filtros quando necessário.
4. Seleciona uma carona.
5. Visualiza seus detalhes.
6. Solicita uma vaga.
7. Sistema registra sua participação.

## 8.3 Fluxo para cancelar participação

1. Estudante acessa suas caronas.
2. Seleciona uma carona da qual participa.
3. Solicita o cancelamento.
4. Sistema remove sua participação.
5. A vaga volta a ficar disponível.

---

# 9. Prioridades

A priorização utiliza o modelo **MoSCoW**.

### Must Have

Funcionalidades essenciais para que a plataforma cumpra seu objetivo principal:

* US01 — Criar conta
* US02 — Entrar na plataforma
* US03 — Criar uma carona
* US04 — Consultar caronas disponíveis
* US06 — Visualizar detalhes da carona
* US07 — Solicitar participação em uma carona

### Should Have

Funcionalidades importantes para melhorar a utilização do sistema:

* US05 — Filtrar caronas
* US08 — Cancelar participação
* US09 — Gerenciar caronas criadas
* US10 — Visualizar minhas caronas

### Could Have

Funcionalidades complementares:

* US11 — Encerrar uma carona

### Won't Have

Nesta primeira versão, ficam fora do escopo:

* pagamentos;
* rastreamento em tempo real;
* chat;
* avaliações;
* integração com mapas;
* integração com sistemas acadêmicos;
* notificações via WhatsApp/SMS.

---

# 10. Definição de Pronto — Definition of Done

Uma User Story será considerada concluída quando:

* a funcionalidade estiver implementada;
* os critérios de aceitação forem atendidos;
* os dados forem validados;
* a funcionalidade estiver integrada ao restante da aplicação;
* não existirem erros conhecidos que impeçam seu uso;
* a implementação tiver sido revisada pela equipe;
* a funcionalidade puder ser demonstrada no sistema.

---

# 11. Fonte da Verdade

Este documento é a fonte principal de requisitos do projeto.

As Issues do GitHub devem referenciar as respectivas User Stories deste PRD, evitando duplicação dos critérios de aceitação e mantendo os requisitos centralizados neste documento.

Alterações no escopo, nas prioridades ou nos critérios de aceitação devem ser refletidas neste documento antes de serem utilizadas para orientar novas tarefas de desenvolvimento.
