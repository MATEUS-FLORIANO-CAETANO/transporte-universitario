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
