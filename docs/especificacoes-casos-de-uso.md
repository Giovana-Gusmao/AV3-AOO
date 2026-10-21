## UC-01 — Autenticar usuário

**Requisito relacionado:** RF-001 — Autenticar usuário  
**Ator principal:** Administrador, psicólogo ou recepcionista/atendente.

**Objetivo:** Permitir que usuários cadastrados e ativos acessem a plataforma utilizando suas credenciais individuais.

**Pré-condições:**
- O usuário está cadastrado e ativo.
- O usuário possui credenciais individuais.

**Fluxo principal:**
1. O usuário informa suas credenciais individuais.
2. O sistema realiza a autenticação.
3. O sistema permite o acesso às funcionalidades autorizadas para o usuário.

**Fluxos alternativos:** Não especificados no documento.

**Exceções:**
- Usuário sem autorização não deve acessar funcionalidades restritas, conforme RF-027 e RN-020.
- O comportamento específico para credenciais incorretas não está detalhado no documento.

**Pós-condições:**
- O usuário autenticado pode acessar as funcionalidades autorizadas conforme seu perfil e suas permissões.

## UC-02 — Gerenciar usuários

**Requisito relacionado:** RF-002 — Gerenciar usuários  
**Ator principal:** Administrador.

**Objetivo:** Permitir o cadastro e a atualização dos usuários da plataforma.

**Pré-condições:**
- O administrador está autenticado e possui permissão para gerenciar usuários, conforme RF-027 e RN-020.

**Fluxo principal:**
1. O administrador solicita o gerenciamento de usuários.
2. O administrador escolhe cadastrar ou atualizar um usuário.
3. No cadastro, informa os dados obrigatórios definidos pelo sistema.
4. Na atualização, altera as informações do usuário.
5. O sistema registra a operação realizada.

**Fluxos alternativos:**
- O administrador pode optar pelo cadastro ou pela atualização de usuário.

**Exceções:**
- O sistema não permite criar usuários com identificador de acesso já utilizado por outra conta (CA-001.2).
- O comportamento detalhado para dados inválidos não está especificado no documento.

**Pós-condições:**
- O usuário é cadastrado ou atualizado, conforme a operação realizada.

## UC-03 — Ativar e bloquear usuários

**Requisito relacionado:** RF-003 — Ativar e bloquear usuários  
**Ator principal:** Administrador.

**Objetivo:** Permitir ao administrador ativar ou bloquear o acesso de usuários.

**Pré-condições:**
- O administrador está autenticado e possui permissão para realizar a operação.

**Fluxo principal:**
1. O administrador solicita a ativação ou o bloqueio de um usuário.
2. O sistema realiza a operação solicitada.

**Fluxos alternativos:**
- O administrador pode optar por ativar ou bloquear o acesso.

**Exceções:**
- Quando um usuário é bloqueado, o sistema deve impedir novos acessos e invalidar o acesso ativo quando tecnicamente aplicável (CA-001.4).

**Pós-condições:**
- O acesso do usuário fica ativado ou bloqueado, conforme a operação realizada.

## UC-04 — Gerenciar perfis e permissões

**Requisito relacionado:** RF-004 — Gerenciar perfis e permissões  
**Ator principal:** Administrador.

**Objetivo:** Permitir que o administrador defina e gerencie os perfis e as permissões associados aos usuários.

**Pré-condições:**
- O administrador está autenticado e possui permissão para gerenciar perfis e permissões.

**Fluxo principal:**
1. O administrador solicita o gerenciamento de perfis e permissões.
2. Seleciona o usuário cujas permissões serão gerenciadas.
3. Define ou altera o perfil e as permissões do usuário.
4. O sistema registra as alterações.

**Fluxos alternativos:** Não especificados no documento.

**Exceções:**
- Usuários sem a permissão correspondente não devem conseguir acessar funcionalidades restritas, inclusive por tentativa de acesso direto (CA-001.5).

**Pós-condições:**
- O usuário possui o perfil e as permissões definidos pelo administrador.

## UC-05 — Gerenciar unidades

**Requisito relacionado:** RF-005 — Gerenciar unidades  
**Ator principal:** Administrador.

**Objetivo:** Permitir o cadastro e a atualização das unidades pertencentes à organização.

**Pré-condições:**
- O administrador está autenticado e possui permissão para gerenciar unidades.

**Fluxo principal:**
1. O administrador solicita o gerenciamento de unidades.
2. Escolhe cadastrar ou atualizar uma unidade.
3. No cadastro, informa os dados obrigatórios.
4. O sistema registra a operação realizada.

**Fluxos alternativos:**
- O administrador pode cadastrar uma nova unidade ou atualizar uma unidade existente.

**Exceções:** Não especificadas no documento.

**Pós-condições:**
- A unidade é cadastrada ou atualizada.

## UC-06 — Gerenciar profissionais

**Requisito relacionado:** RF-006 — Gerenciar profissionais  
**Ator principal:** Administrador.

**Objetivo:** Permitir que o administrador visualize e mantenha as informações administrativas dos profissionais cadastrados.

**Pré-condições:**
- O administrador está autenticado e possui permissão para acessar as informações administrativas dos profissionais.

**Fluxo principal:**
1. O administrador solicita a consulta dos profissionais cadastrados.
2. O sistema apresenta as informações administrativas dos profissionais.
3. O administrador realiza a manutenção das informações, quando necessário.
4. O sistema registra as alterações realizadas.

**Fluxos alternativos:** Não especificados no documento.

**Exceções:** Não especificadas no documento.

**Pós-condições:**
- As informações administrativas dos profissionais permanecem disponíveis e atualizadas conforme as alterações realizadas.

## UC-07 — Vincular psicólogo à unidade

**Requisito relacionado:** RF-007 — Vincular psicólogo à unidade  
**Ator principal:** Administrador.

**Objetivo:** Permitir ao administrador criar e encerrar vínculos profissionais entre psicólogos e unidades.

**Pré-condições:**
- O administrador está autorizado a gerenciar vínculos profissionais.

**Fluxo principal:**
1. O administrador solicita a criação ou o encerramento de um vínculo entre psicólogo e unidade.
2. O sistema realiza a operação solicitada.
3. O sistema preserva o histórico do vínculo.

**Fluxos alternativos:**
- O administrador pode criar um vínculo ou encerrar um vínculo existente.

**Exceções:**
- O sistema não deve permitir vínculo ativo duplicado entre o mesmo psicólogo e a mesma unidade (CA-002.5).

**Pós-condições:**
- O vínculo é criado ou encerrado.
- O histórico do vínculo permanece registrado, conforme RN-003.

## UC-08 — Consultar profissionais por unidade

**Requisito relacionado:** RF-008 — Consultar profissionais por unidade  
**Ator principal:** Administrador.

**Objetivo:** Permitir ao administrador consultar os profissionais vinculados a determinada unidade.

**Pré-condições:**
- O administrador possui autorização para consultar as informações.

**Fluxo principal:**
1. O administrador solicita a consulta de profissionais por unidade.
2. Seleciona a unidade desejada.
3. O sistema apresenta os profissionais vinculados à unidade.

**Fluxos alternativos:** Não especificados no documento.

**Exceções:** Não especificadas no documento.

**Pós-condições:**
- Os profissionais vinculados à unidade selecionada são apresentados ao administrador.

## UC-09 — Visualizar painel geral

**Requisito relacionado:** RF-009 — Visualizar painel geral  
**Ator principal:** Administrador.

**Objetivo:** Disponibilizar uma visão consolidada da organização.

**Pré-condições:**
- O administrador está autorizado a consultar o painel geral.

**Fluxo principal:**
1. O administrador solicita a visualização do painel geral.
2. O sistema apresenta informações consolidadas sobre profissionais, pacientes e atendimentos.
3. Quando aplicável, o administrador filtra as informações por unidade e período.

**Fluxos alternativos:**
- O administrador pode selecionar filtros por unidade e período, quando aplicáveis.

**Exceções:** Não especificadas no documento.

**Pós-condições:**
- As informações consolidadas são apresentadas conforme os filtros utilizados.

## UC-10 — Cadastrar paciente

**Requisito relacionado:** RF-010 — Cadastrar paciente  
**Ator principal:** Recepcionista/atendente.

**Objetivo:** Permitir o cadastro dos dados administrativos básicos de um novo paciente durante o processo de agendamento.

**Pré-condições:**
- A recepcionista está autorizada a realizar o cadastro administrativo de pacientes.

**Fluxo principal:**
1. A recepcionista pesquisa se o paciente já está cadastrado.
2. Quando não há registro correspondente, informa os dados administrativos obrigatórios.
3. O sistema cadastra o paciente.
4. O cadastro fica disponível para utilização no processo de agendamento.

**Fluxos alternativos:**
- Se o paciente já estiver cadastrado, a recepcionista poderá utilizar o cadastro existente, sem criar outro desnecessariamente.

**Exceções:**
- O sistema deve adotar validações para reduzir cadastros duplicados (CA-005.5).
- O comportamento específico para dados inválidos não está detalhado no documento.

**Pós-condições:**
- O paciente fica cadastrado e disponível para o processo de agendamento.

## UC-11 — Pesquisar paciente

**Requisito relacionado:** RF-011 — Pesquisar paciente  
**Ator principal:** Recepcionista/atendente.

**Objetivo:** Permitir a localização de pacientes já cadastrados para reutilizar seus dados em novos agendamentos.

**Pré-condições:**
- A recepcionista possui autorização para consultar os dados administrativos dos pacientes.

**Fluxo principal:**
1. A recepcionista solicita a pesquisa de um paciente.
2. Informa os dados necessários para a pesquisa.
3. O sistema pesquisa os cadastros existentes.
4. O sistema apresenta o cadastro correspondente, quando localizado.

**Fluxos alternativos:**
- Se não houver registro correspondente, o sistema deverá permitir o cadastro de um novo paciente, conforme RF-010 e CA-005.2.

**Exceções:** O comportamento específico para pesquisas sem correspondência não está detalhado além da possibilidade de cadastrar um novo paciente.

**Pós-condições:**
- O cadastro localizado fica disponível para utilização no processo de agendamento.

## UC-12 — Atualizar dados administrativos do paciente

**Requisito relacionado:** RF-012 — Atualizar dados administrativos do paciente  
**Ator principal:** Recepcionista/atendente.

**Objetivo:** Permitir a atualização das informações administrativas autorizadas do paciente.

**Pré-condições:**
- A recepcionista possui autorização para atualizar os dados administrativos do paciente.
- O cadastro do paciente está disponível para consulta.

**Fluxo principal:**
1. A recepcionista localiza o cadastro do paciente.
2. Altera os dados administrativos para os quais possui autorização.
3. O sistema registra as alterações.
4. As informações atualizadas ficam disponíveis para consultas posteriores.

**Fluxos alternativos:** Não especificados no documento.

**Exceções:**
- A recepcionista não pode visualizar ou modificar registros profissionais de atendimento (CA-006.3).
- Tentativas de acesso a informações profissionais sem autorização devem ser negadas (CA-006.4).

**Pós-condições:**
- Os dados administrativos alterados ficam disponíveis para consultas posteriores.

## UC-13 — Gerenciar disponibilidade

**Requisito relacionado:** RF-013 — Gerenciar disponibilidade  
**Ator principal:** Psicólogo.

**Objetivo:** Permitir ao psicólogo cadastrar e alterar seus períodos de disponibilidade nas unidades às quais possui vínculo ativo.

**Pré-condições:**
- O psicólogo possui vínculo ativo com a unidade na qual deseja cadastrar ou alterar a disponibilidade.

**Fluxo principal:**
1. O psicólogo solicita o gerenciamento de sua disponibilidade.
2. Informa os períodos em que está disponível para atendimento.
3. O sistema verifica a validade da disponibilidade.
4. O sistema registra a disponibilidade cadastrada ou alterada.

**Fluxos alternativos:**
- O psicólogo pode cadastrar uma nova disponibilidade ou alterar uma disponibilidade futura.

**Exceções:**
- O sistema deve impedir o cadastro de uma disponibilidade inválida, como horário final anterior ao horário inicial (CA-010.4).

**Pós-condições:**
- A disponibilidade fica cadastrada ou atualizada.
- A alteração da disponibilidade não elimina automaticamente consultas já agendadas (CA-010.3).

## UC-14 — Consultar agenda do psicólogo

**Requisito relacionado:** RF-014 — Consultar agenda do psicólogo  
**Ator principal:** Psicólogo.

**Objetivo:** Permitir ao psicólogo consultar sua agenda, incluindo horários disponíveis e consultas agendadas.

**Pré-condições:**
- O psicólogo possui autorização para consultar sua própria agenda.

**Fluxo principal:**
1. O psicólogo solicita a consulta da agenda.
2. O sistema apresenta seus horários disponíveis e suas consultas agendadas.
3. A agenda permite identificar data, horário, unidade e paciente relacionados a cada consulta autorizada.

**Fluxos alternativos:** Não especificados no documento.

**Exceções:**
- O psicólogo não deve alterar diretamente consultas já agendadas por meio dessa função (CA-011.3).

**Pós-condições:**
- A agenda do psicólogo é apresentada para consulta.

## UC-15 — Consultar disponibilidade para agendamento

**Requisitos relacionados:** RF-015 — Consultar disponibilidade para agendamento; RF-020 — Validar disponibilidade; RF-021 — Impedir conflito de agenda.  
**Ator principal:** Recepcionista/atendente.

**Objetivo:** Permitir que a recepcionista consulte os horários disponíveis dos psicólogos nas respectivas unidades.

**Pré-condições:**
- A recepcionista possui autorização para consultar as disponibilidades necessárias ao agendamento.

**Fluxo principal:**
1. A recepcionista seleciona uma unidade.
2. O sistema apresenta os psicólogos vinculados à unidade.
3. O sistema apresenta os períodos disponíveis de cada psicólogo.
4. O sistema não apresenta como disponíveis os horários ocupados por agendamentos ativos.

**Fluxos alternativos:** Não especificados no documento.

**Exceções:** Não especificadas além das restrições de disponibilidade e conflito de agenda definidas nos requisitos.

**Pós-condições:**
- Os horários disponíveis ficam apresentados para consulta e utilização no agendamento.

## UC-16 — Realizar agendamento

**Requisitos relacionados:** RF-016, RF-020, RF-021 e RF-022.  
**Ator principal:** Recepcionista/atendente.

**Objetivo:** Registrar uma consulta relacionando paciente, psicólogo, unidade, data e horário.

**Pré-condições:**
- A recepcionista está autenticada e possui permissão para agendar.
- O paciente está cadastrado ou será cadastrado durante o processo.
- O psicólogo possui vínculo ativo com a unidade escolhida.
- O psicólogo possui disponibilidade cadastrada para a unidade.

**Fluxo principal:**
1. A recepcionista pesquisa o paciente.
2. Se necessário, realiza o cadastro do paciente.
3. Seleciona o paciente, o psicólogo, a unidade, a data e o horário.
4. O sistema verifica se os dados necessários estão definidos.
5. O sistema verifica se o psicólogo possui disponibilidade compatível com a unidade, a data e o horário.
6. O sistema verifica se existe conflito com outro agendamento ativo do mesmo psicólogo.
7. Se as validações forem atendidas, o sistema registra o agendamento.
8. O sistema disponibiliza a consulta na agenda do psicólogo.
9. O horário deixa de aparecer como disponível.
10. Se for o primeiro agendamento válido entre o paciente e o psicólogo, o sistema estabelece o vínculo entre ambos, caso ainda não exista.

**Fluxos alternativos:**
- **FA-01 — Paciente ainda não cadastrado:** a recepcionista realiza o cadastro e utiliza os dados no agendamento.
- **FA-02 — Vínculo paciente–psicólogo inexistente:** após a conclusão do primeiro agendamento válido, o sistema estabelece o vínculo entre ambos.

**Exceções:**
- **E-01 — Dados necessários não definidos:** o agendamento não pode ser concluído se paciente, psicólogo, unidade, data ou horário não estiverem definidos (CA-008.1).
- **E-02 — Vínculo profissional inválido:** o agendamento não pode ser concluído se o psicólogo não possuir vínculo ativo com a unidade selecionada (CA-008.2).
- **E-03 — Indisponibilidade:** o agendamento não pode ser concluído se o horário não estiver dentro da disponibilidade cadastrada para o psicólogo e a unidade (CA-008.3).
- **E-04 — Conflito de horário:** o sistema impede o agendamento conflitante com outro agendamento ativo do mesmo psicólogo (CA-008.4).

**Pós-condições:**
- O agendamento é registrado com paciente, psicólogo, unidade, data e horário.
- A consulta aparece na agenda do psicólogo.
- O horário correspondente deixa de aparecer como disponível.
- O vínculo paciente–psicólogo é criado quando se trata do primeiro agendamento válido e ainda não existe vínculo.

## UC-17 — Confirmar agendamento

**Requisito relacionado:** RF-017 — Confirmar agendamento  
**Ator principal:** Recepcionista/atendente.

**Objetivo:** Permitir a confirmação de uma consulta previamente agendada.

**Pré-condições:**
- Existe um agendamento.
- A recepcionista possui autorização para realizar a confirmação.

**Fluxo principal:**
1. A recepcionista solicita a confirmação de um agendamento existente.
2. O sistema registra a confirmação do agendamento.

**Fluxos alternativos:** Não especificados no documento.

**Exceções:** As situações específicas em que a confirmação deve ser impedida não estão detalhadas no documento.

**Pós-condições:**
- O agendamento fica confirmado.

## UC-18 — Cancelar agendamento

**Requisito relacionado:** RF-018 — Cancelar agendamento  
**Ator principal:** Recepcionista/atendente.

**Objetivo:** Permitir o cancelamento de uma consulta agendada.

**Pré-condições:**
- Existe um agendamento.
- A operação é realizada por usuário administrativo autorizado.

**Fluxo principal:**
1. A recepcionista solicita o cancelamento de um agendamento.
2. O sistema verifica as permissões aplicáveis.
3. O sistema registra o cancelamento do agendamento.

**Fluxos alternativos:** Não especificados no documento.

**Exceções:**
- O cancelamento deve respeitar as regras e permissões aplicáveis ao agendamento.

**Pós-condições:**
- O agendamento fica cancelado.

## UC-19 — Reagendar consulta

**Requisito relacionado:** RF-019 — Reagendar consulta  
**Ator principal:** Recepcionista/atendente.

**Objetivo:** Permitir a alteração da data ou do horário de uma consulta por meio de reagendamento.

**Pré-condições:**
- Existe um agendamento.
- A operação é realizada por usuário administrativo autorizado.

**Fluxo principal:**
1. A recepcionista solicita o reagendamento de uma consulta.
2. Informa a nova data ou o novo horário.
3. O sistema verifica novamente a unidade, o vínculo profissional, a disponibilidade e os conflitos de horário.
4. Se as validações forem atendidas, o sistema registra o reagendamento.

**Fluxos alternativos:** Não especificados no documento.

**Exceções:**
- O reagendamento não pode ser concluído para horário que não atenda às validações de unidade, vínculo, disponibilidade e conflito de agenda (CA-009.4).

**Pós-condições:**
- A consulta fica reagendada para a data ou o horário válido informado.

## UC-20 — Consultar pacientes vinculados

**Requisito relacionado:** RF-023 — Consultar pacientes vinculados  
**Ator principal:** Psicólogo.

**Objetivo:** Permitir ao psicólogo consultar os pacientes aos quais possui vínculo autorizado.

**Pré-condições:**
- O psicólogo possui autorização para acessar os pacientes consultados.

**Fluxo principal:**
1. O psicólogo solicita a consulta dos pacientes vinculados.
2. O sistema verifica os vínculos e as permissões aplicáveis.
3. O sistema apresenta os pacientes aos quais o psicólogo possui vínculo autorizado.

**Fluxos alternativos:** Não especificados no documento.

**Exceções:**
- Pacientes sem vínculo autorizado não devem ter seus registros profissionais disponibilizados ao psicólogo (CA-012.2).

**Pós-condições:**
- Os pacientes autorizados ficam disponíveis para consulta.
- O histórico dos vínculos encerrados permanece preservado.

## UC-21 — Registrar atendimento

**Requisito relacionado:** RF-024 — Registrar atendimento  
**Ator principal:** Psicólogo.

**Objetivo:** Permitir o registro de informações profissionais referentes a uma consulta realizada.

**Pré-condições:**
- A consulta correspondente foi realizada.
- O psicólogo está autorizado a registrar o atendimento sob sua responsabilidade.

**Fluxo principal:**
1. O psicólogo seleciona a consulta realizada.
2. Solicita o registro do atendimento.
3. O sistema disponibiliza o preenchimento das informações profissionais previstas.
4. O psicólogo preenche as informações do atendimento.
5. O sistema salva o registro e o associa ao psicólogo e ao paciente correspondentes.
6. O atendimento passa a integrar o histórico do paciente.

**Fluxos alternativos:** Não especificados no documento.

**Exceções:**
- O sistema não permite registrar atendimento relacionado a consulta que não tenha sido realizada (CA-013.1).
- Outro usuário sem autorização profissional não deve visualizar o conteúdo detalhado do atendimento (CA-013.5).

**Pós-condições:**
- O atendimento fica registrado e associado ao psicólogo e ao paciente correspondentes.
- O atendimento integra o histórico do paciente.

## UC-22 — Consultar histórico de atendimentos

**Requisito relacionado:** RF-025 — Consultar histórico de atendimentos  
**Ator principal:** Psicólogo.

**Objetivo:** Permitir a consulta cronológica e detalhada dos atendimentos dos pacientes aos quais o psicólogo possui acesso autorizado.

**Pré-condições:**
- O psicólogo possui vínculo ou autorização adequada para consultar o histórico do paciente.

**Fluxo principal:**
1. O psicólogo solicita a consulta do histórico de atendimentos de um paciente autorizado.
2. O sistema apresenta os atendimentos em ordem cronológica.
3. O sistema permite acessar as informações detalhadas correspondentes a cada atendimento.

**Fluxos alternativos:** Não especificados no documento.

**Exceções:**
- O sistema não disponibiliza ao psicólogo o histórico profissional de pacientes para os quais não possua vínculo ou autorização adequada (CA-014.4).

**Pós-condições:**
- O histórico autorizado fica disponível para consulta.

## UC-23 — Corrigir registro de atendimento

**Requisito relacionado:** RF-026 — Corrigir registro de atendimento  
**Ator principal:** Psicólogo.

**Objetivo:** Permitir a correção de registros de atendimento sob responsabilidade do psicólogo, preservando a rastreabilidade das alterações.

**Pré-condições:**
- Existe um registro de atendimento.
- O psicólogo possui autorização para corrigir o registro sob sua responsabilidade.

**Fluxo principal:**
1. O psicólogo seleciona o registro de atendimento que deseja corrigir.
2. Realiza as alterações necessárias.
3. O sistema registra a alteração e identifica o responsável e o momento da operação.
4. O sistema mantém a rastreabilidade da versão ou alteração anterior.
5. A versão vigente fica disponível no histórico do paciente.

**Fluxos alternativos:** Não especificados no documento.

**Exceções:**
- Outro psicólogo sem autorização sobre o atendimento não pode modificar o registro (CA-015.4).

**Pós-condições:**
- A versão vigente do registro fica disponível no histórico.
- A rastreabilidade da alteração anterior é preservada.

## UC-24 — Consultar auditoria

**Requisitos relacionados:** RF-028 — Registrar auditoria; RF-029 — Consultar auditoria.  
**Ator principal:** Administrador.

**Objetivo:** Permitir ao administrador consultar registros de operações relevantes realizadas na plataforma.

**Pré-condições:**
- O administrador possui autorização para consultar os registros de auditoria.

**Fluxo principal:**
1. O administrador solicita a consulta dos registros de auditoria.
2. O sistema apresenta os registros autorizados.
3. Os registros permitem identificar, no mínimo, o usuário responsável, a ação realizada e a data/hora da operação.

**Fluxos alternativos:** Não especificados no documento.

**Exceções:**
- Usuários sem permissão de auditoria não devem conseguir acessar esses registros (CA-004.3).

**Pós-condições:**
- Os registros de auditoria autorizados ficam disponíveis para consulta.
