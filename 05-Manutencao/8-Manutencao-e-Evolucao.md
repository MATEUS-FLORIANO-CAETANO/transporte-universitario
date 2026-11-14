# 8. MANUTENÇÃO E EVOLUÇÃO

Esta etapa tem como finalidade apresentar possíveis evoluções futuras para o sistema de transporte universitário, considerando a necessidade de corrigir falhas, adaptar funcionalidades, implementar melhorias e prevenir problemas que possam comprometer seu funcionamento. Além disso, busca analisar os impactos que determinadas mudanças poderiam causar nos requisitos, na arquitetura, nos diagramas e nos testes do sistema. Por fim, são identificados possíveis riscos técnicos e de projeto, acompanhados de medidas para reduzir sua ocorrência ou minimizar suas consequências.

# 8.1 Propostas de Mudanças

Considerando a possibilidade de evolução do sistema de transporte universitário, é necessário identificar mudanças que possam ser necessárias ao longo de sua utilização. Essas alterações podem estar relacionadas à correção de falhas, à adaptação a novas condições de funcionamento, à implementação de melhorias ou à prevenção de objeções futuras. Diante disso, são apresentadas quatro propostas de manutenção, contemplando as categorias corretiva, adaptativa, perfectiva e preventiva.

## Manutenção corretiva – Correção de falhas na distribuição dos passageiros

Propõe-se a correção de possíveis falhas no algoritmo responsável pela distribuição dos passageiros entre os ônibus disponíveis. Durante o processamento das reservas, podem ocorrer erros na atribuição dos estudantes aos veículos, ocasionando distribuições incorretas ou ultrapassando a capacidade máxima cadastrada para determinado ônibus. Dessa forma, essa manutenção se enquadra como corretiva, visto que, tem por objetivo identificar e corrigir empecilhos no funcionamento do sistema, garantindo que a distribuição dos passageiros respeite as regras de negócio estabelecidas, especialmente a RN05, que determina o limite máximo de ocupação dos veículos.

## Manutenção Adaptativa – Adaptação às mudanças nas instituições de ensino

Propõe-se adaptar o sistema para acompanhar possíveis mudanças no calendário acadêmico e nos horários de funcionamento das instituições de ensino atendidas. Para isso, o sistema poderá incorporar mecanismos de atualização dessas informações, permitindo que os responsáveis mantenham os dados utilizados na organização das viagens de acordo com as condições de cada instituição.

Com isso, essa adaptação é classificada como adaptativa, já que procura adequar o software a mudanças em seu ambiente externo de utilização, garantindo que o planejamento do transporte continue compatível com os horários e calendários das instituições atendidas.

## Manutenção perfectiva – Aprimoramento do painel administrativo

Propõe-se aprimorar o painel administrativo por meio da inclusão de relatórios estatísticos que apresentem informações detalhadas sobre a demanda de transporte. Entre os recursos previstos, é relevante estar a quantidade de passageiros por instituição de ensino, os horários com maior procura e a taxa de ocupação dos ônibus disponíveis. Essas informações permitiriam aos administradores acompanhar melhor a utilização dos veículos e identificar padrões na demanda.

A partir disso, pode-se categorizar tal manutenção como sendo perfectiva, dado que, busca aperfeiçoar funcionalidades já existentes, ampliando os recursos de consulta e análise disponíveis aos administradores e contribuindo para um planejamento mais eficiente das viagens.

## Manutenção preventiva – Aprimoramento do monitoramento do sistema

Propõe-se implementar recursos de monitoramento e registro das operações realizadas pelo sistema, especialmente durante o processamento automático das reservas e a distribuição dos passageiros. Esses mecanismos permitiriam registrar o histórico de execuções, identificar possíveis erros e acompanhar o desempenho dos processos, facilitando a identificação de situações que possam comprometer o funcionamento do software.

Portanto, essa manutenção é classificada como preventiva, pois busca antecipar a identificação de possíveis problemas e facilitar sua resolução antes que provoquem falhas mais graves, contribuindo para a confiabilidade e a continuidade do funcionamento do sistema.

# 8.3 Análise do impacto de mudança

A análise dos efeitos causados pelas manutenções tem por objetivo pontuar as possíveis consequências da implementação de uma alteração no sistema, considerando os elementos que podem ser afetados durante sua evolução. Para isso, será utilizada como referência a proposta de manutenção adaptativa apresentada anteriormente, que consiste em adaptar o sistema às mudanças nos calendários acadêmicos e nos horários das instituições de ensino. A partir dessa proposta, serão analisados os impactos nos requisitos, na arquitetura, nos diagramas e nos testes do projeto.

## Impacto nos Requisitos

A implementação dessa mudança exigiria revisar os requisitos funcionais relacionados ao gerenciamento de horários e acrescentar uma funcionalidade para o gerenciamento dos calendários acadêmicos.

**RF 013**

Permitir que o administrador cadastre e atualize os calendários acadêmicos e os horários de funcionamento das instituições de ensino atendidas.

## Impacto na Arquitetura

Além disso, seria necessário revisar os requisitos relacionados à configuração dos horários disponíveis e ao processamento das reservas, garantindo que as informações atualizadas sejam consideradas na organização das viagens.

A implementação da mudança exigiria adaptações nas três camadas da arquitetura do sistema. Na camada de apresentação, seria necessário disponibilizar ao administrador uma interface para cadastrar e atualizar os calendários acadêmicos e os horários das instituições de ensino.

Na camada de aplicação, os serviços responsáveis pelo gerenciamento dos horários e pelo processamento das reservas precisariam ser adaptados para utilizar as informações atualizadas. Dessa forma, as alterações realizadas pelo administrador seriam consideradas na organização das viagens e na validação das solicitações de transporte.

Na camada de dados, seria necessário acrescentar estruturas para armazenar os calendários acadêmicos e as informações de funcionamento de cada instituição, permitindo sua consulta e atualização pelo sistema.

Essas modificações manteriam a arquitetura em três camadas já estabelecida no projeto, acrescentando responsabilidades e adaptando os componentes existentes para atender à nova necessidade.

## Impacto nos diagramas

A implementação da mudança exigiria atualizações nos diagramas do sistema, de modo que eles representassem adequadamente a nova funcionalidade. No diagrama de casos de uso, seria necessário acrescentar a possibilidade de o administrador cadastrar e atualizar os calendários acadêmicos e os horários das instituições de ensino.

No diagrama de classes, seria necessário avaliar o aperfeiçoamento da classe responsável por representar as instituições de ensino e seus respectivos calendários e horários de funcionamento, além de estabelecer os relacionamentos necessários com as demais classes do sistema.

Essas atualizações permitiriam manter os modelos do projeto alinhados às novas funcionalidades e às alterações realizadas nos requisitos.

### Diagrama de Casos de Uso

**Autor:** Administrador

- Cadastrar calendário acadêmico
- Atualizar horários de instituição

### Diagrama de Classes

**Classe:** Instituição de Ensino

- Identificação da Instituição
- Calendário acadêmico
- Horários de Funcionamento
- Relacionamento com as reservas e horários de transporte.

## Impacto nos Testes

A implementação da mudança exigiria a criação de novos casos de teste e a revisão de testes já existentes, com o objetivo de verificar se os calendários acadêmicos e os horários das instituições de ensino são cadastrados e atualizados corretamente. Também seria necessário testar se as alterações realizadas são consideradas pelo sistema durante a disponibilização dos horários de transporte e o processamento das reservas.

Entre as verificações necessárias, destacam-se o cadastro de informações válidas, a atualização de horários previamente registrados, a rejeição de dados inválidos e a utilização das informações atualizadas durante o processamento das reservas. Além disso, deverão ser realizados testes de regressão para garantir que as alterações não comprometam funcionalidades já existentes, como a realização de reservas e a distribuição dos passageiros entre os veículos.

# 8.2 Gestão de riscos técnicos e mitigação

A gestão de riscos consiste em identificar possíveis situações que possam comprometer o desenvolvimento ou o funcionamento do sistema, permitindo estabelecer medidas para reduzir sua ocorrência e minimizar seus impactos. Nesse contexto, são apresentados três riscos relacionados ao Sistema de Transporte Universitário, acompanhados de suas possíveis consequências e respectivas estratégias de mitigação.

## Falha do algoritmo de distribuição de passageiros

Um dos riscos técnicos identificados está relacionado ao algoritmo responsável pela distribuição dos passageiros entre os ônibus disponíveis. Caso apresente falhas durante o processamento das reservas, o sistema poderá realizar atribuições incorretas, ultrapassar a capacidade dos veículos ou deixar passageiros sem transporte definido.

Para mitigar esse risco, recomenda-se realizar testes com diferentes cenários de demanda, considerando variações na quantidade de passageiros, nos destinos e na capacidade dos veículos. Também devem ser implementadas validações que garantam o cumprimento das regras de negócio durante a distribuição.

## Desatualização das informações dos veículos

Outro risco está relacionado à possibilidade de as informações cadastradas sobre os veículos não corresponderem às suas condições reais de disponibilidade e capacidade. Caso esses dados não sejam atualizados pelos administradores, o sistema poderá realizar a distribuição dos passageiros considerando veículos indisponíveis ou capacidades incorretas, comprometendo a organização das viagens.

Para mitigar esse risco, recomenda-se estabelecer procedimentos de atualização periódica dos dados dos veículos, além de implementar validações no cadastro e na edição das informações. Dessa forma, busca-se garantir que o processamento das reservas utilize dados confiáveis e atualizados.

## Falhas no processamento automático das reservas

O processamento automático das reservas também representa um possível risco técnico, uma vez que depende da execução correta do Agendador e da disponibilidade dos serviços e dados necessários. Eventuais falhas nesse processo poderão ocasionar atrasos na distribuição dos passageiros, indisponibilidade das informações das viagens e necessidade de intervenção manual dos administradores.

Para mitigar esse risco, recomenda-se implementar mecanismos de monitoramento e registro das execuções, permitindo identificar falhas e acompanhar o funcionamento do processamento. Também é importante prever procedimentos de recuperação e reexecução das operações em caso de interrupções, evitando a perda de informações ou o processamento duplicado das reservas.
