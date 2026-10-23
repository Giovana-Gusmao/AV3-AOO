# Matriz de Atores e Funcionalidades
## 1. Objetivo:
Esta matriz apresenta a relação entre os atores do sistema e as funcionalidades previstas nos requisitos funcionais, identificando quais funcionalidades são atribuídas a cada perfil de usuário.

## 2. Legenda: 
° X : o ator executa ou participa diretamente da funcionalidade.

° — : a funcionalidade não está atribuída a esse ator nos requisitos identificados.

° Sist. : comportamento executado pelo sistema quando aplicável.

## 3. Matriz de Atores e Funcionalidades:

![Matriz de Atores e Funcionalidades do sistema](<Matriz de atores e funcionalidades.pdf>)

## 4. Observações sobre os requisitos funcionais: 
° **RF-009:** a matriz e as especificações dos casos de uso devem refletir a decisão da equipe de permitir que a recepcionista agende, confirme, cancele e reagende consultas.

° **RF-016 — Realizar agendamento:** a recepcionista pode realizar o agendamento de consultas, respeitando as validações previstas nos requisitos e nas regras de negócio.

° **RF-017 — Confirmar agendamento:** a recepcionista pode confirmar consultas previamente agendadas, conforme as permissões e condições definidas pelo sistema.

° **RF-018 — Cancelar agendamento:** a recepcionista pode cancelar consultas, respeitando as regras aplicáveis ao estado do agendamento.

° **RF-019 — Reagendar consulta:** a recepcionista pode alterar a data ou o horário de uma consulta, desde que o novo horário atenda às validações de disponibilidade e conflito de agenda.

° **RF-020 a RF-022:** requisitos relacionados às validações e regras do processo de agendamento. A relação de cada requisito com os atores deve seguir sua descrição oficial.

° **RF-027 — Controlar acesso por permissões:** o sistema deve respeitar as permissões de cada perfil de usuário, restringindo o acesso às funcionalidades e informações autorizadas.

° **RF-028 — Registrar auditoria:** o sistema registra as ações relevantes realizadas pelos usuários, conforme as regras definidas.

° **RF-029 — Consultar auditoria:** funcionalidade atribuída ao administrador.

° **Acesso aos registros profissioanis:** a recepcionista pode acessar os dados administrativos necessários às suas funções, mas não pode consultar o conteúdo profissional detalhado dos registros de atendimento psicológico.

° **Paciente:** nesta versão do sistema, o paciente é uma pessoa cadastrada, sem acesso direto à plataforma.

## 5. Pendências: 

° Os requisitos RF-020 a RF-022 devem ser conferidos para que seus nomes e suas relações com os atores correspondam exatamente ao documento oficial de requisitos.

° Confirmar que as especificações textuais e os diagramas comportamentais refletem as mesmas regras de negócio e permissões definidas pela equipe.
