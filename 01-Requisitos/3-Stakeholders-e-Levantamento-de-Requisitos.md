# 3. STAKEHOLDERS E LEVANTAMENTO DE REQUISITOS
Esta etapa tem como finalidade identificar as pessoas e os grupos envolvidos no funcionamento do sistema, compreender suas necessidades e estabelecer os requisitos necessários para o desenvolvimento do software. O levantamento dessas informações é importante para garantir que o sistema atenda às necessidades dos passageiros e dos responsáveis pela organização do transporte.

## 3.1 Mapeamento de stakeholders
Os stakeholders são todas as pessoas, grupos ou organizações que possuem algum tipo de interesse ou participação no desenvolvimento e funcionamento do sistema.
Para este projeto, foram identificados os seguintes stakeholders:
Estudantes: Realizam o cadastro e informam suas necessidades de transporte.
Administradores: Gerenciam passageiros, ônibus, horários e destinos.
Motoristas: Consultam as viagens organizadas e as informações dos passageiros.
Empresas de transporte: Disponibilizam os veículos e definem suas capacidades.
Desenvolvedores: Responsáveis pela criação, manutenção e atualização do sistema.
Instituições de ensino: Representam os destinos das viagens e podem fornecer informações sobre horários das aulas.
Cada stakeholder possui necessidades diferentes. Os estudantes precisam de praticidade para cadastrar suas viagens e consultar os resultados. Os administradores necessitam de ferramentas para controlar a demanda e organizar os veículos. Já os motoristas precisam receber informações claras sobre os horários e destinos das viagens.

## 3.2 Metodologia de levantamento dos requisitos
Para identificar as necessidades do sistema, será utilizada uma metodologia de levantamento de requisitos baseada na análise do processo atual de organização do transporte para instituições de ensino. Inicialmente, será realizada uma análise de como as solicitações de transporte são feitas atualmente, identificando as dificuldades encontradas pelos passageiros e responsáveis pela organização das viagens. Também poderão ser utilizadas entrevistas e questionários com estudantes, administradores e motoristas, buscando compreender as principais necessidades de cada grupo.

As principais técnicas utilizadas serão:
Entrevistas: conversas com passageiros e responsáveis pelo transporte para identificar dificuldades e necessidades.
Questionários: aplicação de perguntas para compreender como os estudantes utilizam o transporte e como realizam suas solicitações.
Observação: análise do processo atual de organização das viagens, identificando possíveis falhas e atividades que podem ser automatizadas.
Análise do processo atual: identificação dos problemas relacionados ao uso de aplicativos de comunicação e controles manuais.

## 3.3 Requisitos Funcionais (RF) e Não Funcionais (RNF)
Os requisitos funcionais descrevem as funcionalidades que o sistema deverá oferecer aos usuários. Já os requisitos não funcionais estabelecem características relacionadas à qualidade, segurança, desempenho e funcionamento do sistema.

## A) Requisitos Funcionais (RF)

| RF   | DESCRIÇÃO |
|------|-----------|
| RF01 | O sistema deverá permitir o cadastro de passageiros. |
| RF02 | O sistema deverá permitir que os passageiros realizem login utilizando usuário e senha. |
| RF03 | O sistema deverá permitir o agendamento dos dias da semana em que o passageiro necessita de transporte. |
| RF04 | O sistema deverá permitir o cadastro dos horários de saída e dos horários desejados de chegada. |
| RF05 | O sistema deverá permitir a seleção das instituições de ensino que serão frequentadas. |
| RF06 | O sistema deverá permitir que o passageiro altere ou cancele suas reservas dentro do prazo estabelecido. |
| RF07 | O sistema deverá permitir que os administradores cadastrem e gerenciem os ônibus disponíveis. |
| RF08 | O sistema deverá armazenar a capacidade máxima de passageiros de cada ônibus. |
| RF09 | O sistema deverá calcular a quantidade de passageiros por horário e destino. |
| RF10 | O sistema deverá distribuir os passageiros entre os ônibus disponíveis, respeitando a capacidade de cada veículo. |
| RF11 | O sistema deverá disponibilizar aos passageiros o resultado da organização das viagens. |
| RF12 | O sistema deverá informar qual ônibus o passageiro deverá utilizar, o horário e a instituição de destino. |

## B) Requisitos Não Funcionais (RNF)

| RNF | DESCRIÇÃO |
|---|---|
| RNF01 | O sistema deverá possuir uma interface simples e intuitiva, facilitando sua utilização. |
| RNF02 | O sistema deverá permitir o acesso por computadores e dispositivos móveis. |
| RNF03 | O sistema deverá proteger os dados pessoais dos passageiros. |
| RNF04 | O sistema deverá exigir autenticação para acessar informações restritas. |
| RNF05 | O processamento das reservas deverá ocorrer dentro de um tempo adequado, mesmo quando houver grande quantidade de passageiros. |
| RNF06 | O sistema deverá manter as informações armazenadas de forma organizada e segura. |
| RNF07 | O sistema deverá apresentar mensagens claras quando ocorrerem erros ou problemas durante o cadastro e processamento das reservas. |
| RNF08 | O sistema deverá permitir futuras atualizações e melhorias sem comprometer seu funcionamento. |

## 3.4 Regras de Negócio (RN)
As regras de negócio estabelecem as condições que deverão ser respeitadas pelo sistema durante o cadastro, processamento e distribuição das viagens.
Para o funcionamento adequado da plataforma, foram definidas as seguintes regras:

| RN | DESCRIÇÃO |
|---|---|
| RN01 | Cada passageiro deverá possuir um cadastro individual no sistema. |
| RN02 | O estudante deverá informar os dias da semana em que necessita de transporte. |
| RN03 | Toda solicitação deverá conter um horário e um destino válidos. |
| RN04 | Após o processamento das reservas, as viagens serão organizadas de acordo com a demanda identificada. |
| RN05 | Nenhum ônibus poderá receber uma quantidade de passageiros superior à sua capacidade cadastrada. |
| RN06 | A distribuição dos passageiros deverá considerar os horários e destinos das viagens. |
| RN07 | Caso a quantidade de passageiros ultrapasse a capacidade dos ônibus disponíveis, o sistema deverá informar a existência de demanda excedente ao administrador. |
| RN08 | Após a organização das viagens, cada passageiro deverá receber as informações referentes ao ônibus, horário e destino. |
| RN09 | Alterações ou cancelamentos de reservas deverão respeitar o prazo definido para o processamento. |
| RN10 | Somente os administradores poderão cadastrar, alterar ou remover os veículos disponíveis. |


## 3.5 Análise de conflitos, ambiguidades e restrições 
Durante o levantamento dos requisitos, é importante identificar possíveis conflitos, ambiguidades e restrições que possam comprometer o funcionamento do sistema. Um dos principais conflitos identificados está relacionado à quantidade de passageiros e à capacidade dos ônibus disponíveis. Em determinadas situações, a demanda poderá ser superior à quantidade de vagas existentes, exigindo que o sistema informe a necessidade de disponibilizar veículos adicionais ou realizar ajustes na distribuição. Outro possível conflito ocorre quando diferentes passageiros solicitam horários próximos ou possuem destinos diferentes. Nesse caso, o sistema deverá considerar as informações cadastradas e os critérios de organização definidos pelos administradores.
Também existem algumas ambiguidades que precisam ser esclarecidas durante o desenvolvimento:
Horários de cadastro: definir até que horário os passageiros poderão cadastrar ou alterar suas reservas antes do processamento;
Alterações de última hora: estabelecer como serão tratadas as solicitações realizadas após o fechamento das reservas;
Distribuição dos passageiros: definir os critérios utilizados para distribuir os estudantes entre os ônibus disponíveis;
Excesso de demanda: definir como será realizada a organização quando não houver vagas suficientes nos veículos disponíveis;
Cancelamentos: determinar como o sistema deverá atualizar a distribuição quando um passageiro cancelar sua reserva.
Em relação às restrições, o funcionamento do sistema dependerá da disponibilidade de informações atualizadas sobre os veículos, suas capacidades, horários e destinos atendidos. Além disso, a eficiência da organização dependerá do preenchimento correto das informações pelos passageiros. Portanto, essas questões deverão ser consideradas durante o desenvolvimento para garantir que o sistema funcione corretamente e atenda às necessidades dos usuários.
