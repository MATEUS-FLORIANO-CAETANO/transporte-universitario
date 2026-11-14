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
