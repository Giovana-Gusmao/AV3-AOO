## VISÃO
O sistema proposto tem como finalidade centralizar e colaborar com a gestão das atividades administrativas e profissionais, reunindo em um único ambiente informações que podem estar distribuídas em diferentes ferramentas.
Ele será utilizado por administradores, psicólogos e recepcionistas/atendentes. 

Os administradores serão responsáveis pelo gerenciamento dos usuários e de seus acessos; os psicólogos poderão acompanhar sua agenda, seus pacientes vinculados e os registros relacionados aos atendimentos; e os recepcionistas poderão realizar atividades administrativas relacionadas aos pacientes e aos agendamentos, respeitando as permissões atribuídas ao seu perfil.

A plataforma deverá centralizar informações de profissionais, pacientes, unidades, disponibilidade, agendamentos e atendimentos, possibilitando maior organização da rotina da instituição e controle sobre quem pode acessar ou realizar determinadas operações.

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

## RESTRIÇÕES
**RES-001 — Controle de acesso:**
O acesso às informações e funcionalidades será limitado conforme o perfil e as permissões atribuídas a cada usuário.

**RES-002 — Restrição da recepção:**
A recepcionista poderá acessar as informações administrativas necessárias ao cadastro e ao agendamento, mas não poderá visualizar o conteúdo profissional detalhado dos registros de atendimento.

**RES-003 — Restrição do psicólogo:**
O psicólogo não poderá acessar indiscriminadamente os registros profissionais de todos os pacientes da organização, devendo respeitar os vínculos e permissões definidos.

**RES-004 — Paciente não autenticado:**
Não será disponibilizado login ou portal de acesso ao paciente nesta versão.

**RES-005 — Ausência de módulo financeiro:**
Faturamento, pagamentos, emissão fiscal e demais funcionalidades financeiras não farão parte do escopo desta versão.

**RES-006 — Uma organização, múltiplas unidades:**
A plataforma poderá administrar diversas unidades da mesma organização, mas não será modelada inicialmente como uma solução destinada a várias organizações independentes.

**RES-007 — Dados de pacientes:**
Os artefatos acadêmicos não utilizarão dados reais de pacientes. Essa proibição aparece expressamente nas condições da atividade.

**RES-008 — Proteção de credenciais:**
Senhas não poderão ser disponibilizadas em texto puro, em conformidade com a exigência de proteção de senhas prevista no enunciado.

## GLOSSÁRIO
**Organização:**
Instituição responsável pela operação das clínicas/unidades e pela utilização da plataforma.

**Unidade:**
Clínica ou local pertencente à organização onde os profissionais podem exercer suas atividades e realizar atendimentos.

**Usuário:**
Pessoa autorizada a acessar diretamente a plataforma por meio de credenciais próprias.

**Administrador:**
Usuário responsável pela gestão de acessos, unidades, profissionais e demais informações administrativas permitidas.

**Recepcionista/Atendente:**
Usuário responsável principalmente pelo cadastro administrativo inicial do paciente e pela realização de agendamentos.

**Psicólogo:**
Profissional de Psicologia cadastrado no sistema, vinculado a uma ou mais unidades e autorizado a realizar atividades profissionais.

**Paciente:**
Pessoa cadastrada na plataforma para realização de consultas e acompanhamento profissional, sem acesso direto ao sistema nesta versão.

**Área de Atuação:**
Campo profissional da Psicologia em que determinado psicólogo exerce suas atividades.

**Vínculo Profissional:**
Relação que representa que um psicólogo trabalha ou trabalhou em determinada unidade, podendo possuir situação ativa ou inativa e manter histórico.

**Vínculo Psicólogo–Paciente:**
Relação que identifica quais psicólogos estão ou estiveram responsáveis pelo acompanhamento de determinado paciente.

**Perfil:**
Conjunto de responsabilidades atribuído a um usuário no sistema.

**Permissão:**
Autorização que determina quais funcionalidades ou informações determinado perfil pode acessar.

**Disponibilidade:**
Período informado pelo psicólogo no qual ele pode realizar atendimentos em determinada unidade.

**Horário Disponível:**
Período pertencente à disponibilidade do psicólogo que ainda não possui agendamento ativo.

**Agenda:**
Visão organizada das disponibilidades e dos agendamentos de um psicólogo.

**Agendamento:**
Reserva de uma data e horário para atendimento de um paciente por determinado psicólogo em uma unidade específica, possuindo uma situação própria.

**Atendimento:**
Registro criado após a realização da consulta, contendo as informações profissionais registradas pelo psicólogo sobre aquele atendimento.

**Histórico de Atendimento:**
Conjunto cronológico dos atendimentos de um paciente, contendo os registros detalhados correspondentes a cada atendimento realizado.

**Auditoria:**
Registro das ações relevantes realizadas pelos usuários para permitir rastreabilidade e identificação de quem realizou determinada operação.

## STACKHOLDERS E ATORES
**Atores:**

**-Administrador:**
Usuário responsável pela gestão da organização dentro da plataforma. Representa também o papel de gestor/dono da clínica nesta versão. Suas responsabilidades incluem controle de acessos, visualização de unidades, profissionais vinculados e informações administrativas gerais.

**Psicólogo:**
Usuário responsável pelas atividades profissionais. Acessa sua agenda, disponibilidade, pacientes vinculados e registros de atendimento autorizados.

**Recepcionista/Atendente:**
Usuário responsável pelas atividades administrativas relacionadas principalmente ao cadastro inicial do paciente e ao agendamento de consultas.

## Stakeholder sem interação direta

**Paciente:**
Pessoa atendida pela organização e diretamente afetada pelos agendamentos, cadastros e registros de atendimento, mas que não utiliza diretamente a plataforma nesta versão.

## REGRAS DE NEGÓCIO
**RN-001 — Vínculo entre psicólogo e unidade:**
Somente o administrador poderá criar, alterar ou encerrar o vínculo profissional entre um psicólogo e uma unidade.

**RN-002 — Múltiplas unidades:**
Um psicólogo poderá possuir vínculo ativo com uma ou mais unidades da organização.

**RN-003 — Histórico do vínculo profissional:**
O encerramento do vínculo entre psicólogo e unidade não deverá excluir seu histórico, devendo o vínculo permanecer registrado como inativo ou encerrado.

**RN-004 — Vínculo entre paciente e psicólogo:**
Ao realizar o primeiro agendamento válido de um paciente com determinado psicólogo, o sistema deverá estabelecer o vínculo entre ambos.

**RN-005 — Múltiplos psicólogos:**
Um paciente poderá estar vinculado a mais de um psicólogo, desde que existam vínculos válidos correspondentes.

**RN-006 — Acesso do psicólogo aos pacientes:**
O psicólogo somente poderá acessar informações profissionais de pacientes com os quais possua vínculo autorizado.

**RN-007 — Acesso da recepção:**
A recepcionista poderá acessar somente os dados administrativos necessários ao cadastro e agendamento do paciente, não podendo consultar o conteúdo profissional detalhado dos atendimentos.

**RN-008 — Gestão da disponibilidade:**
O psicólogo poderá definir e alterar seus períodos de disponibilidade para atendimento nas unidades às quais possuir vínculo ativo.

**RN-009 — Responsabilidade sobre agendamentos:**
A recepcionista poderá realizar, confirmar, cancelar e reagendar consultas.

**RN-010 — Limitação do psicólogo sobre consultas já agendadas:**
O psicólogo poderá consultar seus agendamentos, porém não deverá alterar diretamente consultas já marcadas. Cancelamentos e reagendamentos deverão ser realizados por usuário administrativo autorizado.

**RN-011 — Validação de disponibilidade:**
Um agendamento somente poderá ser realizado se o psicólogo possuir disponibilidade compatível com a unidade, data e horário escolhidos.

**RN-012 — Conflito de horários:**
Não poderá existir mais de um agendamento ativo para o mesmo psicólogo em períodos conflitantes.

**RN-013 — Unidade do agendamento:**
Todo agendamento deverá estar relacionado a exatamente um paciente, um psicólogo, uma unidade, uma data e um horário.

**RN-014 — Situação do agendamento:**
Todo agendamento deverá possuir uma situação válida entre: Agendado, Confirmado, Realizado, Reagendado, Cancelado ou Não Compareceu.

**RN-015 — Criação do atendimento:**
Um registro de atendimento somente poderá ser criado após a realização da consulta correspondente.

**RN-016 — Responsabilidade pelo registro:**
Somente o psicólogo autorizado poderá criar ou alterar o registro profissional de um atendimento sob sua responsabilidade.

**RN-017 — Conteúdo do atendimento:**
O registro de atendimento deverá permitir informações detalhadas referentes à consulta em nível conceitual, compondo posteriormente o histórico do paciente.

**RN-018 — Correção de registro de atendimento:**
Após o registro de um atendimento, eventuais alterações realizadas pelo psicólogo deverão preservar a rastreabilidade da modificação.

**RN-019 — Credenciais individuais:**
Cada usuário deverá utilizar credenciais próprias de acesso, não sendo permitido o uso compartilhado de uma mesma conta por diferentes usuários.

**RN-020 — Controle por perfil e permissão:**
As funcionalidades e informações disponíveis a cada usuário deverão respeitar seu perfil e suas permissões.

**RN-021 — Auditoria:**
Operações administrativas e alterações relevantes deverão gerar informações suficientes para identificar o usuário responsável e o momento da operação.

## REQUISITOS FUNCIONAIS

**RF-001 — Autenticar usuário:**
O sistema deverá permitir que usuários cadastrados e ativos realizem autenticação utilizando suas credenciais individuais.

**RF-002 — Gerenciar usuários:**
O sistema deverá permitir ao administrador cadastrar e atualizar usuários da plataforma.

**RF-003 — Ativar e bloquear usuários:**
O sistema deverá permitir ao administrador ativar ou bloquear o acesso de usuários.

**RF-004 — Gerenciar perfis e permissões:**
O sistema deverá permitir ao administrador definir e gerenciar os perfis e permissões associados aos usuários.

**RF-005 — Gerenciar unidades:**
O sistema deverá permitir ao administrador cadastrar e atualizar as unidades pertencentes à organização.

**RF-006 — Gerenciar profissionais:** 
O sistema deverá permitir ao administrador visualizar e manter as informações administrativas dos profissionais cadastrados.

**RF-007 — Vincular psicólogo à unidade:**
O sistema deverá permitir ao administrador criar e encerrar vínculos profissionais entre psicólogos e unidades.

**RF-008 — Consultar profissionais por unidade:**
O sistema deverá permitir ao administrador consultar quais profissionais possuem vínculo com determinada unidade.

**RF-009 — Visualizar painel geral:**
O sistema deverá disponibilizar ao administrador uma visão consolidada da organização, apresentando informações gerais como quantidade de profissionais, pacientes e atendimentos, permitindo filtragem por unidade e período quando aplicável.

**RF-010 — Cadastrar paciente:**
O sistema deverá permitir à recepcionista cadastrar os dados administrativos básicos de um novo paciente durante o processo de agendamento.

**RF-011 — Pesquisar paciente:**
O sistema deverá permitir à recepcionista pesquisar pacientes já cadastrados para reutilizar seus dados em novos agendamentos.

**RF-012 — Atualizar dados administrativos do paciente:**
O sistema deverá permitir à recepcionista atualizar informações administrativas autorizadas do paciente, como dados de contato.

**RF-013 — Gerenciar disponibilidade:**
O sistema deverá permitir ao psicólogo cadastrar e alterar sua disponibilidade de atendimento nas unidades às quais possuir vínculo ativo.

**RF-014 — Consultar agenda do psicólogo:**
O sistema deverá permitir ao psicólogo consultar sua agenda, incluindo horários disponíveis e consultas agendadas.

**RF-015 — Consultar disponibilidade para agendamento:**
O sistema deverá permitir à recepcionista visualizar os horários disponíveis dos psicólogos nas respectivas unidades.

**RF-016 — Realizar agendamento:**
O sistema deverá permitir à recepcionista realizar o agendamento de uma consulta relacionando paciente, psicólogo, unidade, data e horário.

**RF-017 — Confirmar agendamento:**
O sistema deverá permitir à recepcionista confirmar uma consulta previamente agendada.

**RF-018 — Cancelar agendamento:**
O sistema deverá permitir à recepcionista cancelar uma consulta agendada.

**RF-019 — Reagendar consulta:**
O sistema deverá permitir à recepcionista alterar a data ou o horário de uma consulta por meio de reagendamento.

**RF-020 — Validar disponibilidade:**
O sistema deverá verificar se o psicólogo possui disponibilidade válida na unidade, data e horário selecionados antes de concluir um agendamento.

**RF-021 — Impedir conflito de agenda:**
O sistema deverá impedir a criação de agendamentos que provoquem conflito de horário para o mesmo psicólogo.

**RF-022 — Criar vínculo no primeiro agendamento:**
O sistema deverá estabelecer o vínculo entre paciente e psicólogo quando for concluído o primeiro agendamento válido entre eles, caso ainda não exista vínculo correspondente.

**RF-023 — Consultar pacientes vinculados:**
O sistema deverá permitir ao psicólogo consultar os pacientes aos quais possui vínculo autorizado.

**RF-024 — Registrar atendimento:**
O sistema deverá permitir ao psicólogo registrar informações profissionais referentes a uma consulta realizada.

**RF-025 — Consultar histórico de atendimentos:**
O sistema deverá permitir ao psicólogo consultar, de forma cronológica e detalhada, o histórico de atendimentos dos pacientes aos quais possuir acesso autorizado.

**RF-026 — Corrigir registro de atendimento:**
O sistema deverá permitir ao psicólogo realizar correções em registros de atendimento sob sua responsabilidade, preservando a rastreabilidade das alterações.

**RF-027 — Controlar acesso por permissões:**
O sistema deverá disponibilizar funcionalidades e informações de acordo com os perfis e permissões atribuídos ao usuário autenticado.

**RF-028 — Registrar auditoria:**
O sistema deverá registrar operações relevantes realizadas pelos usuários, permitindo identificar a ação, o responsável e o momento em que ocorreu.

**RF-029 — Consultar auditoria:**
O sistema deverá permitir ao administrador consultar os registros de auditoria autorizados.
