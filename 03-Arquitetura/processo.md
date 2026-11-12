# 6. Processo e Organização do Desenvolvimento

Esta seção define como o desenvolvimento do sistema seria conduzido: o modelo de processo adotado, o plano de execução e a forma de controlar versões, mudanças e rastreabilidade.

## 6.1 Abordagem do processo de desenvolvimento

Foi escolhido o **modelo incremental**, em que o sistema é construído e entregue em partes funcionais, cada uma acrescentando novas funcionalidades às anteriores. A escolha se justifica pelas ambiguidades levantadas na seção 3.5, como o prazo de alteração das reservas e o tratamento da demanda excedente. Com entregas parciais, essas questões podem ser validadas com estudantes e com a empresa de transporte antes de o sistema estar completo, o que reduz o risco de retrabalho.

O desenvolvimento seria dividido em três incrementos:

- **Incremento 1 – Base:** autenticação, cadastro e reservas (RF01 a RF06). Ao final, os estudantes já podem registrar suas reservas no sistema, substituindo a enquete no WhatsApp.
- **Incremento 2 – Distribuição:** gestão de frota, Agendador e Distribuição (RF07 a RF10). Ao final, a alocação dos passageiros passa a ser automática.
- **Incremento 3 – Consultas:** resultados para estudantes e motoristas e painel do administrador (RF09, RF11, RF12).

Cada incremento passa pelas mesmas etapas: detalhamento dos requisitos, projeto, implementação, testes e validação com os usuários. Os entregáveis de cada incremento são uma versão funcional do sistema, a documentação atualizada e os casos de teste executados.

Os papéis previstos são:

- **Coordenador:** organiza as tarefas e acompanha os prazos.
- **Analista de requisitos:** detalha os requisitos e valida as entregas com os usuários.
- **Desenvolvedores:** projetam e implementam os serviços.
- **Testador:** elabora e executa os casos de teste.
- **Representante da empresa de transporte:** prioriza as funcionalidades e aprova as entregas.

## 6.2 Plano de execução, tarefas e cronograma

O plano abaixo organiza as tarefas por incremento, com suas dependências e responsáveis:

| ID | Tarefa | Depende de | Responsável | Período |
|---|---|---|---|---|
| T01 | Detalhar requisitos e critérios de aceitação | – | Alessandro | Semana 1 |
| T02 | Projetar o banco de dados | T01 | Luan | Semana 2 |
| T03 | Implementar Autenticação e cadastro | T02 | Rafael | Semanas 3–4 |
| T04 | Implementar Reservas | T02, T03 | Abraão | Semanas 3–4 |
| T05 | Testar e validar o Incremento 1 | T04 | Mateus | Semana 5 |
| T06 | Implementar Gestão de frota | T02 | Rafael | Semanas 5–6 |
| T07 | Implementar Distribuição | T04, T06 | Luan | Semanas 6–7 |
| T08 | Implementar Agendador | T07 | Abraão | Semana 8 |
| T09 | Testar e validar o Incremento 2 | T08 | Mateus | Semana 9 |
| T10 | Implementar Consultas e telas de resultado | T07 | Rafael | Semanas 10–11 |
| T11 | Implementar painel do administrador | T07 | Abraão | Semanas 10–11 |
| T12 | Testes finais e validação geral | T10, T11 | Mateus e Alessandro | Semana 12 |

A tarefa mais crítica é a T07 (Distribuição), pois depende tanto das reservas quanto da frota, e todo o Incremento 3 depende dela. Por isso, as tarefas T04 e T06 podem ser executadas em paralelo, para que a T07 comece o quanto antes.

## 6.3 Gestão de configuração, controle de versões e rastreabilidade

O controle de versões seria feito com **Git**, hospedado no **GitHub**, que já é utilizado pela equipe neste trabalho. As regras de uso seriam:

- **Branches:** a branch principal (`main`) contém sempre a versão estável. Cada funcionalidade é desenvolvida em uma branch própria (ex.: `rf10-distribuicao`) e só é incorporada à principal por meio de um *pull request* revisado por outro integrante.
- **Commits:** cada mensagem cita o identificador do requisito ou da regra tratada (ex.: `RF10: alocação respeitando capacidade (RN05)`).
- **Versões:** cada incremento concluído recebe uma marcação de versão (*tag*), como v1.0, v2.0 e v3.0.

As **mudanças** seguem um fluxo fixo. Toda solicitação é registrada como uma *issue* no GitHub. Em seguida, passa por uma análise de impacto sobre requisitos, arquitetura, diagramas e testes. Só depois de aprovada é implementada, e os artefatos afetados são atualizados junto com o código.

A **rastreabilidade** é garantida pelo uso dos mesmos identificadores em todos os artefatos. Cada requisito (RF, RNF, RN) aparece no caso de uso correspondente (seção 4.4), no serviço da arquitetura que o atende (seção 5.1), nos casos de teste (seção 7.2) e nos commits que o implementam. A própria documentação do projeto também fica versionada no repositório, organizada em pastas por etapa (requisitos, modelagem, arquitetura, testes e manutenção). Assim, é possível saber quando e por que cada artefato foi alterado.
