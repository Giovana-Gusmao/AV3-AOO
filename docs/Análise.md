## VISÃO
O sistema proposto tem como finalidade centralizar e colaborar com a gestão das atividades administrativas e profissionais, reunindo em um único ambiente informações que podem estar distribuídas em diferentes ferramentas.
Ele será utilizado por administradores, psicólogos e recepcionistas/atendentes. Os administradores serão responsáveis pelo gerenciamento dos usuários e de seus acessos; os psicólogos poderão acompanhar sua agenda, seus pacientes vinculados e os registros relacionados aos atendimentos; e os recepcionistas poderão realizar atividades administrativas relacionadas aos pacientes e aos agendamentos, respeitando as permissões atribuídas ao seu perfil. <br>
A plataforma deverá centralizar informações de profissionais, pacientes, unidades, disponibilidade, agendamentos e atendimentos, possibilitando maior organização da rotina da instituição e controle sobre quem pode acessar ou realizar determinadas operações. <br>
A solução também será estruturada de forma flexível para permitir que a organização possua uma ou mais unidades e profissionais de diferentes áreas de atuação, evitando que o crescimento da instituição exija uma reformulação dos principais conceitos do sistema.

## CONTEXTO
A plataforma será projetada para atender organizações e clínicas de Psicologia de diferentes portes, desde operações iniciantes com uma única unidade até estruturas maiores compostas por múltiplas unidades e diversos profissionais.
Nesse contexto, é comum que informações administrativas e profissionais sejam distribuídas entre diferentes recursos, como planilhas, agendas, calendários digitais e sistemas isolados que não oferecem uma visão integrada da operação.
Nesse sentido, essa organização pode exigir que administradores, recepcionistas e psicólogos consultem diferentes ferramentas para localizar informações relacionadas a pacientes, profissionais, disponibilidade, agendamentos e atendimentos, tornando as atividades do dia a dia mais fragmentadas.
A proposta do sistema desponta nesse ambiente como o objetivo de centralizar essas informações e auxiliar na organização das atividades administrativas e profissionais, mantendo uma estrutura flexível que permita acompanhar o crescimento da organização, como a inclusão de novos profissionais, áreas de atuação e unidades, sem exigir reformulação significativa dos conceitos centrais do sistema.

## SITUAÇÃO-PROBLEMA
Atualmente, uma organização ou clínica de Psicologia pode conseguir manter suas atividades utilizando diferentes ferramentas, como planilhas, agendas, calendários digitais e sistemas isolados. Entretanto, a ausência de integração entre esses recursos torna a gestão das informações mais fragmentada e pode gerar dados divergentes ou desatualizados.
Essa fragmentação afeta os diferentes usuários da organização de maneiras distintas. O administrador pode enfrentar dificuldades para gerenciar usuários, acessos, profissionais e diferentes unidades de forma integrada; o psicólogo pode necessitar de consultas em diferentes ferramentas a fim de encontrar sua agenda e informações ligadas aos atendimentos de seus pacientes; e a recepção pode encontrar dificuldade para visualizar de forma centralizada os horários disponíveis e já agendados.
O problema tende a se tornar ainda maior conforme p crescimento da organização, incorpora novos profissionais ou passa a operar em múltiplas unidades, pois processos e informações que antes eram administráveis de forma separada tornam-se progressivamente mais difíceis de coordenar.
Dessa forma, embora a organização consiga funcionar com as ferramentas existentes, a falta de integração e centralização pode gerar retrabalho, inconsistências, dificuldade de controle de acesso e obstáculos à organização e expansão da operação.

## OBJETIVOS
**GERAL:**
Modelar uma plataforma integrada para organizações de Psicologia que aumente a eficiência das atividades administrativas e profissionais e apoie o crescimento da instituição, centralizando a gestão de unidades, profissionais, pacientes, agenda e atendimentos, com controle adequado de acesso às informações.

**ESPECIFICOS:**
1. Centralizar em uma única plataforma as principais informações administrativas e profissionais utilizadas pela organização.
2. Oferecer ao administrador uma visão unificada da operação, possibilitando acompanhar unidades, profissionais, pacientes e informações gerais linkadas aos atendimentos.
3. Viabilizar o acesso do psicólogo à sua agenda e aos registros e históricos de atendimento dos pacientes aos quais estiver autorizado.
4. Simplificar o processo de agendamento realizado pela recepção, permitindo visualizar disponibilidade e horários já ocupados no mesmo ambiente em que o agendamento é realizado.
5. Implementar controle de acesso às informações e funcionalidades de acordo com as responsabilidades de cada usuário.
6. Diminuir a demanda de consulta a diversas ferramentas para execução das atividades rotineiras da organização.
7. Estruturar a solução de forma flexível para permitir a inclusão de novos profissionais, áreas de atuação e unidades sem necessidade de reformulação significativa dos conceitos centrais do sistema.

## ESCOPOS
A plataforma abrangerá as funcionalidades necessárias para apoiar a gestão administrativa e profissional de uma organização de Psicologia, contemplando usuários com diferentes responsabilidades e permitindo que a operação seja realizada em uma ou várias unidades.
**Administrador:**
O administrador terá uma visão gerencial da organização e será responsável principalmente por:
- visualizar e gerenciar unidades;
- visualizar usuários e profissionais cadastrados;
- identificar a quais unidades cada profissional está vinculado;
- controlar usuários, perfis e permissões;
- ativar e bloquear acessos;
- acompanhar informações gerais da operação que estejam previstas no sistema.
- OBS: Aqui eu evitaria, por enquanto, prometer dashboards muito avançados. Podemos futuramente colocar indicadores como quantidade de atendimentos, mas primeiro vamos ver se isso vira requisito formal.

**Recepcionista/Atendente:**
A recepcionista terá acesso somente às funções administrativas necessárias para realizar os agendamentos.
No primeiro contato de um novo paciente, ela poderá informar os dados administrativos básicos necessários e, a partir deles, o sistema criará o cadastro do paciente.
Depois disso, poderá utilizar o cadastro existente nos próximos agendamentos.
Ela também deverá consultar a agenda e a disponibilidade dos profissionais para realizar a marcação da consulta sem precisar acessar outra ferramenta.

**Psicólogo:**
O psicólogo poderá gerenciar sua própria disponibilidade de agenda e consultar os compromissos já agendados.
Também terá acesso aos pacientes aos quais estiver autorizado e poderá realizar registros estruturados dos atendimentos, mantendo o histórico relacionado a cada paciente.
Ele não deverá possuir acesso administrativo geral da organização simplesmente por ser psicólogo.

## FRONTEIRA
A plataforma será responsável pela centralização das informações administrativas e profissionais necessárias à gestão de usuários, unidades, profissionais, pacientes, disponibilidade, agendamentos e atendimentos. O sistema controlará o acesso às funcionalidades de acordo com os perfis e permissões estabelecidos.
Administradores, psicólogos e recepcionistas/atendentes serão usuários externos que interagem diretamente com a plataforma, cada um respeitando suas atribuições.
O paciente fará parte do domínio e possuirá informações cadastradas no sistema, mas não será considerado usuário direto da plataforma nesta versão.
Processos financeiros, fiscais, trabalhistas, teleatendimento e outros serviços não relacionados diretamente ao problema definido estarão fora da fronteira da solução.

## PREMISSAS
**PRE-001 — Estrutura organizacional:**
A plataforma será utilizada por uma organização de Psicologia que poderá operar com uma ou várias unidades.

**PRE-002 — Usuários diretos**
Administradores, psicólogos e recepcionistas/atendentes serão usuários diretos da plataforma.

**PRE-003 — Credenciais individuais**
Cada usuário direto possuirá credenciais próprias de acesso, não sendo previsto o compartilhamento de contas entre diferentes pessoas.

**PRE-004 — Paciente sem acesso direto**
O paciente possuirá cadastro no sistema, porém não utilizará diretamente a plataforma nesta versão.

**PRE-005 — Múltiplas unidades**
Um psicólogo poderá exercer suas atividades em uma ou mais unidades da organização, conforme os vínculos cadastrados.

**PRE-006 — Acesso por vínculo**
O psicólogo terá acesso às informações profissionais dos pacientes com os quais possuir vínculo autorizado.

**PRE-007 — Agenda centralizada**
A disponibilidade dos profissionais e os agendamentos serão administrados na própria plataforma, reduzindo a necessidade de consulta a ferramentas externas para essas atividades.

**PRE-008 — Preservação do histórico**
Vínculos encerrados entre profissionais, unidades ou pacientes deverão permanecer registrados para preservação do histórico da organização.

