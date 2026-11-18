# SISTEMA
## Requisitos do Sitema

## Requisitos Funcionais (RF)
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

## Requisitos Não Funcionais (RNF)
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

## Regras de Negócio (RN)
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


