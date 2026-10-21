## UC01 — Autenticar usuário

**Requisitos relacionados:** RF-001 e RNF-001.

**Ator principal:** Administrador, Recepcionista ou Psicólogo.

**Objetivo:** Permitir que usuários cadastrados e ativos acessem a plataforma por meio de suas credenciais individuais.

**Pré-condições:**
- O usuário possui cadastro no sistema.
- O usuário está com o acesso ativo.

**Fluxo principal:**
1. O usuário acessa a tela de login.
2. O sistema solicita as credenciais.
3. O usuário informa suas credenciais.
4. O sistema valida as informações.
5. O sistema verifica se o usuário está ativo.
6. O sistema identifica o perfil e as permissões do usuário.
7. O sistema libera o acesso autorizado.

**Fluxos alternativos:**

**FA01 — Credenciais inválidas**
1. O sistema identifica credenciais incorretas.
2. O sistema informa que a autenticação não foi realizada.
3. O usuário pode tentar novamente.

**FA02 — Usuário inativo ou bloqueado**
1. O sistema identifica que o acesso está inativo.
2. O sistema impede a entrada na plataforma.
3. O sistema informa que o acesso não está disponível.

**Exceções:**
- Se ocorrer uma falha técnica, o sistema informa que não foi possível concluir a autenticação.

**Pós-condições:**
- Em caso de sucesso, o usuário acessa as funcionalidades autorizadas.
- Em caso de falha, o acesso não é liberado.

---

## UC02 — Gerenciar usuários

**Requisito relacionado:** RF-002.

**Ator principal:** Administrador.

**Objetivo:** Permitir que o administrador consulte os usuários cadastrados e gerencie suas informações conforme as funcionalidades previstas no sistema.

**Pré-condições:**
- O administrador está autenticado, ativo e autorizado a gerenciar usuários.
- Para alterar informações, o usuário selecionado está cadastrado no sistema.

**Fluxo principal:**
1. O administrador acessa a área de gerenciamento de usuários.
2. O sistema apresenta as opções disponíveis.
3. O administrador localiza e seleciona um usuário.
4. O sistema apresenta as informações cadastradas.
5. O administrador seleciona a opção de alteração.
6. O administrador modifica as informações desejadas.
7. O sistema valida os dados.
8. O administrador confirma a alteração.
9. O sistema salva as informações.
10. O sistema informa que a alteração foi concluída.

**Fluxos alternativos:**

**FA01 — Usuário não encontrado**
1. O sistema não localiza o usuário pesquisado.
2. O sistema informa que não encontrou o cadastro.
3. O administrador pode realizar outra pesquisa.

**FA02 — Dados inválidos**
1. O sistema identifica informações inválidas ou incompletas.
2. O sistema informa quais dados precisam ser corrigidos.
3. O administrador corrige os dados.
4. O sistema realiza uma nova validação.

**FA03 — Cancelamento da alteração**
1. O administrador desiste antes de confirmar.
2. O sistema descarta as alterações não salvas.
3. O sistema retorna à área de gerenciamento.

**Exceções:**
- Se ocorrer uma falha técnica ao salvar os dados, o sistema informa que a operação não foi concluída.

**Pós-condições:**
- Em caso de sucesso, as informações são atualizadas.
- Em caso de cancelamento ou falha, a alteração não é considerada concluída.

**Observação:** A inclusão de novos usuários deve seguir o escopo definido para o RF-002. O controle de ativação e bloqueio e o gerenciamento de perfis e permissões são detalhados nos UC03 e UC04.

---

## UC03 — Ativar e bloquear usuários

**Requisito relacionado:** RF-003.

**Ator principal:** Administrador.

**Objetivo:** Permitir que o administrador ative ou bloqueie o acesso de usuários à plataforma.

**Pré-condições:**
- O administrador está autenticado e autorizado.
- O usuário cujo acesso será alterado está cadastrado.

**Fluxo principal:**
1. O administrador acessa o gerenciamento de usuários.
2. O sistema apresenta os usuários cadastrados.
3. O administrador seleciona um usuário.
4. O sistema apresenta a situação atual do acesso.
5. O administrador escolhe ativar ou bloquear o acesso.
6. O sistema solicita a confirmação da operação, se aplicável.
7. O administrador confirma.
8. O sistema atualiza a situação do usuário.
9. O sistema informa o resultado.

**Fluxos alternativos:**

**FA01 — Administrador cancela a operação**
1. O administrador desiste antes da confirmação.
2. O sistema mantém a situação atual do usuário.

**FA02 — Situação já corresponde à ação solicitada**
1. O sistema identifica que o usuário já está ativo ou bloqueado conforme a ação escolhida.
2. O sistema informa que não é necessária uma alteração.

**Exceções:**
- Se ocorrer uma falha ao atualizar o acesso, o sistema informa que a operação não foi concluída.

**Pós-condições:**
- Em caso de sucesso, a situação do acesso é atualizada.
- O usuário bloqueado não consegue autenticar-se enquanto o bloqueio estiver vigente.

---

## UC04 — Gerenciar perfis e permissões

**Requisito relacionado:** RF-004.

**Ator principal:** Administrador.

**Objetivo:** Permitir que o administrador gerencie os perfis e as permissões de acesso dos usuários.

**Pré-condições:**
- O administrador está autenticado e autorizado a gerenciar permissões.
- O usuário que terá suas permissões alteradas está cadastrado.

**Fluxo principal:**
1. O administrador acessa a área de perfis e permissões.
2. O sistema apresenta os usuários e as opções disponíveis.
3. O administrador seleciona o usuário desejado.
4. O sistema apresenta o perfil e as permissões atuais.
5. O administrador seleciona o perfil ou as permissões que deseja modificar.
6. O sistema valida a alteração.
7. O administrador confirma a operação.
8. O sistema salva as novas permissões.
9. O sistema informa que a operação foi concluída.

**Fluxos alternativos:**

**FA01 — Alteração cancelada**
1. O administrador desiste antes de confirmar.
2. O sistema mantém as permissões anteriores.

**FA02 — Configuração inválida**
1. O sistema identifica uma configuração inválida.
2. O sistema informa que a alteração não pode ser realizada.
3. O administrador pode revisar a configuração.

**Exceções:**
- Se ocorrer uma falha ao salvar as permissões, o sistema informa que a operação não foi concluída.

**Pós-condições:**
- Em caso de sucesso, as permissões são atualizadas.
- O acesso às funcionalidades deve respeitar as permissões vigentes.

---

## UC05 — Gerenciar unidades

**Requisito relacionado:** RF-005.

**Ator principal:** Administrador.

**Objetivo:** Permitir que o administrador gerencie as unidades da organização.

**Pré-condições:**
- O administrador está autenticado e autorizado a gerenciar unidades.

**Fluxo principal:**
1. O administrador acessa a área de unidades.
2. O sistema apresenta as opções disponíveis.
3. O administrador seleciona a operação desejada.
4. O administrador informa ou modifica os dados da unidade, conforme a operação.
5. O sistema valida as informações.
6. O administrador confirma a operação.
7. O sistema registra a alteração.
8. O sistema apresenta o resultado.

**Fluxos alternativos:**

**FA01 — Dados inválidos**
1. O sistema identifica dados inválidos ou obrigatórios não preenchidos.
2. O sistema informa o que precisa ser corrigido.
3. O administrador ajusta as informações.

**FA02 — Operação cancelada**
1. O administrador desiste antes da confirmação.
2. O sistema descarta as alterações não salvas.

**Exceções:**
- Se ocorrer uma falha ao salvar os dados, o sistema informa que a operação não foi concluída.

**Pós-condições:**
- A unidade é cadastrada ou tem seus dados atualizados, conforme a operação concluída.

---

## UC06 — Gerenciar profissionais

**Requisito relacionado:** RF-006.

**Ator principal:** Administrador.

**Objetivo:** Permitir que o administrador gerencie os registros dos profissionais da organização.

**Pré-condições:**
- O administrador está autenticado e autorizado a gerenciar profissionais.

**Fluxo principal:**
1. O administrador acessa a área de profissionais.
2. O sistema apresenta as opções disponíveis.
3. O administrador seleciona a operação desejada.
4. O administrador informa os dados do profissional ou seleciona um registro existente.
5. O sistema valida as informações.
6. O administrador confirma a operação.
7. O sistema registra ou atualiza as informações.
8. O sistema informa o resultado.

**Fluxos alternativos:**

**FA01 — Dados inválidos**
1. O sistema identifica dados inválidos ou incompletos.
2. O sistema solicita a correção.
3. O administrador ajusta as informações.

**FA02 — Profissional não encontrado**
1. O sistema não localiza o registro pesquisado.
2. O sistema informa que não encontrou o profissional.

**Exceções:**
- Se ocorrer uma falha técnica ao salvar os dados, o sistema informa que a operação não foi concluída.

**Pós-condições:**
- O registro do profissional é criado ou atualizado, conforme a operação concluída.

---

## UC07 — Vincular psicólogo à unidade

**Requisito relacionado:** RF-007.

**Ator principal:** Administrador.

**Objetivo:** Permitir que o administrador associe um psicólogo a uma unidade da organização.

**Pré-condições:**
- O administrador está autenticado e autorizado.
- O psicólogo está cadastrado.
- A unidade está cadastrada.

**Fluxo principal:**
1. O administrador acessa a funcionalidade de vinculação.
2. O sistema apresenta os psicólogos e as unidades disponíveis.
3. O administrador seleciona o psicólogo.
4. O administrador seleciona a unidade.
5. O sistema verifica as informações da vinculação.
6. O administrador confirma a operação.
7. O sistema registra a associação.
8. O sistema informa que a vinculação foi concluída.

**Fluxos alternativos:**

**FA01 — Dados não localizados**
1. O sistema não encontra o psicólogo ou a unidade selecionada.
2. O sistema informa que não foi possível realizar a vinculação.
3. O administrador pode selecionar outros registros.

**FA02 — Vinculação já existente**
1. O sistema identifica que a associação já está registrada.
2. O sistema informa que não é necessária uma nova vinculação.

**Exceções:**
- Se ocorrer uma falha ao salvar a associação, o sistema informa que a operação não foi concluída.

**Pós-condições:**
- O psicólogo fica vinculado à unidade selecionada.

---

## UC08 — Consultar profissionais por unidade

**Requisito relacionado:** RF-008.

**Ator principal:** Administrador.

**Objetivo:** Permitir que o administrador consulte os profissionais associados a uma unidade.

**Pré-condições:**
- O administrador está autenticado e autorizado a consultar os profissionais.

**Fluxo principal:**
1. O administrador acessa a consulta de profissionais por unidade.
2. O sistema apresenta as unidades disponíveis.
3. O administrador seleciona uma unidade.
4. O sistema consulta os profissionais vinculados.
5. O sistema apresenta os resultados.

**Fluxos alternativos:**

**FA01 — Nenhum profissional vinculado**
1. O sistema não encontra profissionais associados à unidade.
2. O sistema informa que não há profissionais vinculados àquela unidade.

**Exceções:**
- Se ocorrer uma falha na consulta, o sistema informa que não foi possível apresentar os resultados.

**Pós-condições:**
- Os profissionais vinculados à unidade selecionada são apresentados, quando existentes.

---

## UC09 — Visualizar painel geral

**Requisito relacionado:** RF-009.

**Ator principal:** Administrador.

**Objetivo:** Permitir que o administrador consulte informações gerais sobre a operação da organização.

**Pré-condições:**
- O administrador está autenticado e autorizado a visualizar o painel.

**Fluxo principal:**
1. O administrador acessa o painel geral.
2. O sistema consulta as informações operacionais previstas no escopo.
3. O sistema organiza as informações.
4. O sistema apresenta os dados disponíveis ao administrador.

**Fluxos alternativos:**

**FA01 — Não há dados disponíveis**
1. O sistema identifica que não há dados para apresentar em determinado indicador.
2. O sistema informa que não existem dados disponíveis para esse item.

**Exceções:**
- Se ocorrer uma falha ao consultar as informações, o sistema informa que não foi possível carregar o painel.

**Pós-condições:**
- As informações gerais disponíveis são apresentadas ao administrador.

---

## UC10 — Cadastrar paciente

**Requisito relacionado:** RF-010.

**Ator principal:** Recepcionista.

**Objetivo:** Permitir que a recepcionista registre os dados administrativos de um paciente na plataforma.

**Pré-condições:**
- A recepcionista está autenticada e autorizada a cadastrar pacientes.

**Fluxo principal:**
1. A recepcionista acessa a funcionalidade de cadastro de pacientes.
2. O sistema apresenta o formulário.
3. A recepcionista preenche os dados administrativos solicitados.
4. O sistema valida os dados informados.
5. A recepcionista confirma o cadastro.
6. O sistema registra o paciente.
7. O sistema informa que o cadastro foi realizado.

**Fluxos alternativos:**

**FA01 — Dados incompletos ou inválidos**
1. O sistema identifica informações obrigatórias ausentes ou inválidas.
2. O sistema informa quais dados precisam ser corrigidos.
3. A recepcionista corrige as informações.
4. O sistema valida novamente os dados.

**FA02 — Possível cadastro duplicado**
1. O sistema identifica um possível registro existente com dados correspondentes.
2. O sistema informa a situação à recepcionista.
3. A recepcionista verifica o registro antes de prosseguir, conforme as regras definidas pela equipe.

**Exceções:**
- Se ocorrer uma falha técnica ao salvar o cadastro, o sistema informa que a operação não foi concluída.

**Pós-condições:**
- Em caso de sucesso, o paciente fica registrado na plataforma.

---

## UC11 — Pesquisar paciente

**Requisito relacionado:** RF-011.

**Ator principal:** Recepcionista.

**Objetivo:** Permitir que a recepcionista localize um paciente cadastrado.

**Pré-condições:**
- A recepcionista está autenticada e autorizada a consultar os cadastros administrativos.

**Fluxo principal:**
1. A recepcionista acessa a pesquisa de pacientes.
2. O sistema apresenta os campos de pesquisa disponíveis.
3. A recepcionista informa os dados de busca.
4. O sistema realiza a pesquisa.
5. O sistema apresenta os registros correspondentes.

**Fluxos alternativos:**

**FA01 — Nenhum resultado encontrado**
1. O sistema não localiza registros correspondentes.
2. O sistema informa que nenhum paciente foi encontrado.
3. A recepcionista pode realizar uma nova pesquisa.

**Exceções:**
- Se ocorrer uma falha na consulta, o sistema informa que não foi possível realizar a pesquisa.

**Pós-condições:**
- Os registros correspondentes são apresentados, se encontrados.

---

## UC12 — Atualizar dados administrativos do paciente

**Requisito relacionado:** RF-012.

**Ator principal:** Recepcionista.

**Objetivo:** Permitir que a recepcionista atualize os dados administrativos de um paciente cadastrado.

**Pré-condições:**
- A recepcionista está autenticada e autorizada.
- O paciente está cadastrado no sistema.

**Fluxo principal:**
1. A recepcionista pesquisa o paciente.
2. O sistema apresenta os resultados.
3. A recepcionista seleciona o paciente.
4. O sistema apresenta os dados administrativos cadastrados.
5. A recepcionista modifica as informações necessárias.
6. O sistema valida os dados.
7. A recepcionista confirma a alteração.
8. O sistema salva as informações atualizadas.
9. O sistema informa que a operação foi concluída.

**Fluxos alternativos:**

**FA01 — Paciente não encontrado**
1. O sistema não localiza o paciente.
2. O sistema informa que não encontrou o registro.
3. A recepcionista pode realizar uma nova pesquisa.

**FA02 — Dados inválidos**
1. O sistema identifica dados inválidos ou incompletos.
2. O sistema solicita a correção.
3. A recepcionista ajusta as informações.

**FA03 — Alteração cancelada**
1. A recepcionista desiste antes de confirmar.
2. O sistema descarta as alterações não salvas.

**Exceções:**
- Se ocorrer uma falha ao salvar os dados, o sistema informa que a operação não foi concluída.

**Pós-condições:**
- Em caso de sucesso, os dados administrativos são atualizados.
- Os registros profissionais de atendimento não são alterados por essa funcionalidade.

---

## UC13 — Gerenciar disponibilidade

**Requisito relacionado:** RF-013.

**Ator principal:** Psicólogo.

**Objetivo:** Permitir que o psicólogo gerencie sua disponibilidade para atendimentos.

**Pré-condições:**
- O psicólogo está autenticado e autorizado a gerenciar sua disponibilidade.
- O psicólogo possui cadastro e vínculo profissional conforme as regras da organização.

**Fluxo principal:**
1. O psicólogo acessa a funcionalidade de disponibilidade.
2. O sistema apresenta as informações de disponibilidade existentes.
3. O psicólogo seleciona a operação desejada.
4. O psicólogo informa ou modifica os horários disponíveis.
5. O sistema verifica as informações.
6. O psicólogo confirma a operação.
7. O sistema registra a disponibilidade.
8. O sistema informa o resultado.

**Fluxos alternativos:**

**FA01 — Horários inválidos**
1. O sistema identifica informações de horário inválidas.
2. O sistema informa que os dados precisam ser corrigidos.
3. O psicólogo ajusta os horários.

**FA02 — Operação cancelada**
1. O psicólogo desiste antes da confirmação.
2. O sistema mantém a disponibilidade anterior.

**Exceções:**
- Se ocorrer uma falha ao salvar a disponibilidade, o sistema informa que a operação não foi concluída.

**Pós-condições:**
- A disponibilidade é atualizada conforme a operação concluída.

---

## UC14 — Consultar agenda do psicólogo

**Requisito relacionado:** RF-014.

**Ator principal:** Psicólogo.

**Objetivo:** Permitir que o psicólogo consulte sua própria agenda.

**Pré-condições:**
- O psicólogo está autenticado e autorizado.
- O psicólogo possui agenda vinculada ao seu cadastro.

**Fluxo principal:**
1. O psicólogo acessa a agenda.
2. O sistema consulta os agendamentos associados ao psicólogo.
3. O sistema apresenta os compromissos conforme o período selecionado.

**Fluxos alternativos:**

**FA01 — Agenda sem agendamentos**
1. O sistema não encontra compromissos no período consultado.
2. O sistema informa que não há agendamentos para o período.

**FA02 — Consulta de outro período**
1. O psicólogo seleciona outro período.
2. O sistema consulta e apresenta os agendamentos correspondentes.

**Exceções:**
- Se ocorrer uma falha na consulta, o sistema informa que não foi possível carregar a agenda.

**Pós-condições:**
- A agenda correspondente ao período solicitado é apresentada ao psicólogo.

---

## UC15 — Consultar disponibilidade

**Requisito relacionado:** RF-015.

**Ator principal:** Recepcionista.

**Objetivo:** Permitir que a recepcionista consulte os horários disponíveis para agendamento.

**Pré-condições:**
- A recepcionista está autenticada e autorizada a consultar disponibilidades.
- Existem informações de disponibilidade registradas para a consulta solicitada.

**Fluxo principal:**
1. A recepcionista acessa a consulta de disponibilidade.
2. O sistema apresenta os critérios de pesquisa.
3. A recepcionista informa os critérios desejados.
4. O sistema consulta as disponibilidades correspondentes.
5. O sistema apresenta os horários encontrados.

**Fluxos alternativos:**

**FA01 — Nenhum horário disponível**
1. O sistema não encontra horários correspondentes aos critérios.
2. O sistema informa que não há horários disponíveis.
3. A recepcionista pode modificar os critérios da pesquisa.

**Exceções:**
- Se ocorrer uma falha na consulta, o sistema informa que não foi possível obter a disponibilidade.

**Pós-condições:**
- Os horários disponíveis encontrados são apresentados para consulta.

---

## UC16 — Realizar agendamento

**Requisito relacionado:** RF-016, com validações relacionadas aos RF-020 a RF-022.

**Ator principal:** Recepcionista.

**Objetivo:** Permitir que a recepcionista registre um agendamento para um paciente.

**Pré-condições:**
- A recepcionista está autenticada e autorizada a realizar agendamentos.
- O paciente está cadastrado.
- Há informações de disponibilidade para consulta.

**Fluxo principal:**
1. A recepcionista acessa a funcionalidade de agendamento.
2. O sistema solicita os dados necessários para a consulta.
3. A recepcionista pesquisa e seleciona o paciente.
4. A recepcionista consulta e seleciona o profissional e o horário desejado.
5. O sistema verifica as regras de agendamento aplicáveis.
6. O sistema apresenta os dados do agendamento para conferência.
7. A recepcionista confirma a operação.
8. O sistema registra o agendamento.
9. O sistema informa que o agendamento foi realizado.

**Fluxos alternativos:**

**FA01 — Paciente não encontrado**
1. O sistema não localiza o paciente.
2. O sistema informa que o registro não foi encontrado.
3. A recepcionista pode realizar uma nova pesquisa.

**FA02 — Horário indisponível**
1. O sistema identifica que o horário não está disponível.
2. O sistema informa que não é possível realizar o agendamento naquele horário.
3. A recepcionista consulta outras disponibilidades.

**FA03 — Dados inválidos**
1. O sistema identifica dados inválidos ou incompatíveis com as regras de agendamento.
2. O sistema informa o problema.
3. A recepcionista corrige os dados ou seleciona outra opção.

**FA04 — Agendamento cancelado antes da confirmação**
1. A recepcionista desiste antes de confirmar.
2. O sistema não registra o agendamento.

**Exceções:**
- Se ocorrer uma falha ao salvar o agendamento, o sistema informa que a operação não foi concluída.

**Pós-condições:**
- Em caso de sucesso, o agendamento fica registrado com a situação definida pelas regras do projeto.

**Observação:** A situação inicial do agendamento e as validações exatas dos RF-020 a RF-022 precisam seguir o documento oficial de requisitos.

---

## UC17 — Confirmar agendamento

**Requisito relacionado:** RF-017.

**Ator principal:** Recepcionista, sujeito à confirmação da permissão pela equipe.

**Objetivo:** Permitir a confirmação de um agendamento existente, caso essa ação esteja autorizada para a recepção.

**Pré-condições:**
- O usuário está autenticado e autorizado a realizar a operação.
- O agendamento está registrado.
- O agendamento está em uma situação que permite confirmação, conforme as regras do sistema.

**Fluxo principal:**
1. A recepcionista acessa os agendamentos.
2. O sistema apresenta os registros disponíveis para consulta.
3. A recepcionista localiza e seleciona o agendamento.
4. O sistema apresenta os dados do agendamento.
5. A recepcionista solicita a confirmação.
6. O sistema verifica se a operação é permitida.
7. O sistema atualiza a situação do agendamento.
8. O sistema informa que a confirmação foi realizada.

**Fluxos alternativos:**

**FA01 — Agendamento não encontrado**
1. O sistema não localiza o registro.
2. O sistema informa que o agendamento não foi encontrado.

**FA02 — Situação não permite confirmação**
1. O sistema identifica que o agendamento não pode ser confirmado naquela situação.
2. O sistema informa que a operação não pode ser realizada.

**Exceções:**
- Se ocorrer uma falha na atualização, o sistema informa que a confirmação não foi concluída.

**Pós-condições:**
- Em caso de sucesso, a situação do agendamento é atualizada.

**Pendência:** Confirmar com a equipe se a recepção pode executar essa operação e quais situações permitem a confirmação.

---

## UC18 — Cancelar agendamento

**Requisito relacionado:** RF-018.

**Ator principal:** Recepcionista, sujeito à confirmação da permissão pela equipe.

**Objetivo:** Permitir o cancelamento de um agendamento, caso essa ação esteja autorizada para a recepção.

**Pré-condições:**
- O usuário está autenticado e autorizado.
- O agendamento está registrado.
- A situação do agendamento permite cancelamento, conforme as regras definidas.

**Fluxo principal:**
1. A recepcionista acessa os agendamentos.
2. O sistema apresenta os registros disponíveis.
3. A recepcionista localiza e seleciona o agendamento.
4. O sistema apresenta os dados do agendamento.
5. A recepcionista solicita o cancelamento.
6. O sistema verifica se a operação é permitida.
7. O sistema solicita a confirmação, se aplicável.
8. A recepcionista confirma o cancelamento.
9. O sistema atualiza a situação do agendamento.
10. O sistema informa o resultado.

**Fluxos alternativos:**

**FA01 — Cancelamento desistido**
1. A recepcionista desiste antes de confirmar.
2. O sistema mantém a situação anterior do agendamento.

**FA02 — Agendamento não encontrado**
1. O sistema não localiza o registro.
2. O sistema informa que o agendamento não foi encontrado.

**FA03 — Cancelamento não permitido**
1. O sistema identifica que a situação do agendamento não permite cancelamento.
2. O sistema informa que a operação não pode ser realizada.

**Exceções:**
- Se ocorrer uma falha na atualização, o sistema informa que o cancelamento não foi concluído.

**Pós-condições:**
- Em caso de sucesso, o agendamento fica com a situação correspondente ao cancelamento.

**Pendência:** Confirmar com a equipe a permissão da recepção e as regras de cancelamento.

---

## UC19 — Reagendar consulta

**Requisito relacionado:** RF-019.

**Ator principal:** Recepcionista, sujeito à confirmação da permissão pela equipe.

**Objetivo:** Permitir a alteração da data ou do horário de uma consulta agendada, caso essa ação esteja autorizada para a recepção.

**Pré-condições:**
- O usuário está autenticado e autorizado.
- O agendamento está registrado.
- Existe disponibilidade para a nova data ou horário pretendido.

**Fluxo principal:**
1. A recepcionista acessa os agendamentos.
2. O sistema apresenta os registros disponíveis.
3. A recepcionista localiza e seleciona a consulta.
4. O sistema apresenta os dados do agendamento.
5. A recepcionista solicita o reagendamento.
6. O sistema apresenta os critérios para escolha de uma nova data ou horário.
7. A recepcionista seleciona a nova opção.
8. O sistema verifica a disponibilidade e as regras aplicáveis.
9. O sistema apresenta os novos dados para conferência.
10. A recepcionista confirma a operação.
11. O sistema atualiza o agendamento.
12. O sistema informa que o reagendamento foi realizado.

**Fluxos alternativos:**

**FA01 — Novo horário indisponível**
1. O sistema identifica que o horário escolhido não está disponível.
2. O sistema informa a indisponibilidade.
3. A recepcionista seleciona outra opção.

**FA02 — Agendamento não encontrado**
1. O sistema não localiza o registro.
2. O sistema informa que o agendamento não foi encontrado.

**FA03 — Operação cancelada**
1. A recepcionista desiste antes da confirmação.
2. O sistema mantém o agendamento anterior.

**Exceções:**
- Se ocorrer uma falha ao salvar a alteração, o sistema informa que o reagendamento não foi concluído.

**Pós-condições:**
- Em caso de sucesso, o agendamento fica atualizado para a nova data ou horário.

**Pendência:** Confirmar com a equipe se a recepção pode realizar o reagendamento e quais regras devem ser aplicadas.

---

## UC20 — Consultar pacientes vinculados

**Requisito relacionado:** RF-023.

**Ator principal:** Psicólogo.

**Objetivo:** Permitir que o psicólogo consulte os pacientes aos quais está autorizado e vinculado.

**Pré-condições:**
- O psicólogo está autenticado.
- O psicólogo possui autorização para consultar seus pacientes vinculados.

**Fluxo principal:**
1. O psicólogo acessa a funcionalidade de pacientes vinculados.
2. O sistema identifica o psicólogo autenticado.
3. O sistema consulta os pacientes associados a esse profissional e autorizados para seu acesso.
4. O sistema apresenta os pacientes encontrados.

**Fluxos alternativos:**

**FA01 — Nenhum paciente vinculado**
1. O sistema não encontra pacientes vinculados ao psicólogo.
2. O sistema informa que não há pacientes vinculados para apresentar.

**Exceções:**
- Se ocorrer uma falha na consulta, o sistema informa que não foi possível carregar os registros.

**Pós-condições:**
- O psicólogo visualiza somente os pacientes que está autorizado a consultar.

---

## UC21 — Registrar atendimento

**Requisito relacionado:** RF-024.

**Ator principal:** Psicólogo.

**Objetivo:** Permitir que o psicólogo registre informações de um atendimento realizado.

**Pré-condições:**
- O psicólogo está autenticado e autorizado a registrar atendimentos.
- O paciente está vinculado ao psicólogo e autorizado para seu acesso.

**Fluxo principal:**
1. O psicólogo acessa os pacientes vinculados.
2. O sistema apresenta os pacientes disponíveis para consulta.
3. O psicólogo seleciona o paciente atendido.
4. O sistema apresenta as opções de registro de atendimento.
5. O psicólogo informa os dados solicitados para o registro.
6. O sistema valida as informações.
7. O psicólogo confirma o registro.
8. O sistema salva o atendimento.
9. O sistema informa que o registro foi realizado.

**Fluxos alternativos:**

**FA01 — Dados incompletos ou inválidos**
1. O sistema identifica informações obrigatórias ausentes ou inválidas.
2. O sistema informa quais dados precisam ser corrigidos.
3. O psicólogo corrige as informações.

**FA02 — Paciente não autorizado**
1. O sistema identifica que o psicólogo não possui autorização para acessar o paciente selecionado.
2. O sistema impede o registro.
3. O sistema informa que a operação não pode ser realizada.

**Exceções:**
- Se ocorrer uma falha ao salvar o atendimento, o sistema informa que o registro não foi concluído.

**Pós-condições:**
- Em caso de sucesso, o atendimento fica registrado no histórico do paciente.

---

## UC22 — Consultar histórico de atendimentos

**Requisito relacionado:** RF-025.

**Ator principal:** Psicólogo.

**Objetivo:** Permitir que o psicólogo consulte o histórico cronológico dos atendimentos dos pacientes aos quais está vinculado e autorizado.

**Pré-condições:**
- O psicólogo está autenticado.
- O paciente está vinculado ao psicólogo e autorizado para seu acesso.

**Fluxo principal:**
1. O psicólogo acessa a lista de pacientes vinculados.
2. O psicólogo seleciona um paciente.
3. O sistema verifica a autorização de acesso.
4. O psicólogo solicita o histórico de atendimentos.
5. O sistema consulta os registros disponíveis.
6. O sistema apresenta o histórico em ordem cronológica.

**Fluxos alternativos:**

**FA01 — Histórico vazio**
1. O sistema não encontra registros de atendimento para o paciente.
2. O sistema informa que não há registros disponíveis.

**FA02 — Paciente não autorizado**
1. O sistema identifica que o paciente não está autorizado para acesso pelo psicólogo.
2. O sistema impede a consulta.

**Exceções:**
- Se ocorrer uma falha na consulta, o sistema informa que não foi possível carregar o histórico.

**Pós-condições:**
- O histórico disponível é apresentado ao psicólogo autorizado.

---

## UC23 — Corrigir registro de atendimento

**Requisito relacionado:** RF-026.

**Ator principal:** Psicólogo.

**Objetivo:** Permitir que o psicólogo corrija um registro de atendimento de sua responsabilidade, respeitando as regras de acesso e auditoria.

**Pré-condições:**
- O psicólogo está autenticado e autorizado.
- O registro de atendimento existe.
- O registro pertence ao contexto profissional autorizado para o psicólogo.

**Fluxo principal:**
1. O psicólogo acessa o histórico de atendimentos.
2. O sistema apresenta os registros disponíveis.
3. O psicólogo seleciona o registro que deseja corrigir.
4. O sistema apresenta as informações do registro.
5. O psicólogo modifica os dados que precisam de correção.
6. O sistema valida as informações.
7. O psicólogo confirma a correção.
8. O sistema salva as alterações.
9. O sistema registra a ação de auditoria, conforme as regras aplicáveis.
10. O sistema informa que a correção foi concluída.

**Fluxos alternativos:**

**FA01 — Registro não encontrado**
1. O sistema não localiza o registro selecionado.
2. O sistema informa que o registro não foi encontrado.

**FA02 — Dados inválidos**
1. O sistema identifica dados inválidos.
2. O sistema solicita a correção.
3. O psicólogo ajusta as informações.

**FA03 — Correção cancelada**
1. O psicólogo desiste antes de confirmar.
2. O sistema descarta as alterações não salvas.

**Exceções:**
- Se ocorrer uma falha ao salvar a correção, o sistema informa que a operação não foi concluída.

**Pós-condições:**
- Em caso de sucesso, o registro fica atualizado.
- A correção deve respeitar as regras de auditoria definidas para o sistema.

---

## UC24 — Registrar auditoria

**Requisito relacionado:** RF-028.

**Ator principal:** Sistema.

**Objetivo:** Registrar ações relevantes realizadas na plataforma para permitir rastreabilidade das operações.

**Pré-condições:**
- O sistema está em funcionamento.
- Ocorre uma ação que deve ser registrada conforme as regras de auditoria.

**Fluxo principal:**
1. Um usuário realiza uma ação sujeita à auditoria.
2. O sistema identifica a ação realizada.
3. O sistema reúne as informações de auditoria previstas.
4. O sistema registra o evento de auditoria.
5. O sistema disponibiliza o registro para consulta por usuários autorizados.

**Fluxos alternativos:**

**FA01 — Ação não sujeita à auditoria**
1. O sistema identifica que a ação não está entre aquelas que devem ser registradas.
2. O sistema segue o processamento normal da operação.

**Exceções:**
- Se ocorrer uma falha ao registrar a auditoria, o sistema deve tratar o problema conforme a política definida para auditoria e segurança.

**Pós-condições:**
- As ações sujeitas à auditoria ficam registradas, quando a operação de auditoria é concluída com sucesso.

---

## UC25 — Consultar auditoria

**Requisito relacionado:** RF-029.

**Ator principal:** Administrador.

**Objetivo:** Permitir que o administrador consulte os registros de auditoria disponíveis no sistema.

**Pré-condições:**
- O administrador está autenticado.
- O administrador possui permissão para consultar auditoria.

**Fluxo principal:**
1. O administrador acessa a área de auditoria.
2. O sistema apresenta os critérios de consulta disponíveis.
3. O administrador informa os critérios desejados.
4. O sistema pesquisa os registros de auditoria.
5. O sistema apresenta os resultados encontrados.

**Fluxos alternativos:**

**FA01 — Nenhum registro encontrado**
1. O sistema não encontra registros correspondentes aos critérios informados.
2. O sistema informa que não há resultados para a consulta.

**Exceções:**
- Se ocorrer uma falha na consulta, o sistema informa que não foi possível apresentar os registros.

**Pós-condições:**
- Os registros de auditoria correspondentes são apresentados ao administrador autorizado.

---

## Observações gerais sobre os casos de uso

1. **Controle de acesso — RF-027:** é uma regra aplicada aos casos de uso da plataforma. Cada operação deve respeitar as permissões do usuário. Não é necessariamente necessário criar um caso de uso independente para cada verificação de permissão.

2. **Validações de agendamento — RF-020 a RF-022:** as validações devem ser incorporadas aos casos de uso de consulta de disponibilidade, agendamento, confirmação, cancelamento e reagendamento conforme o conteúdo exato desses requisitos. Os nomes e as regras precisam ser conferidos no documento oficial.

3. **Permissões da recepção:** a autorização para confirmar, cancelar e reagendar consultas deve ser validada com a equipe antes da versão final.

4. **Acesso do paciente:** nesta versão do projeto, o paciente não possui acesso direto à plataforma. Portanto, não aparece como ator dos casos de uso acima.

5. **Consistência da documentação:** os códigos dos casos de uso, nomes dos atores, requisitos relacionados e funcionalidades devem corresponder ao diagrama de casos de uso, à matriz de atores e funcionalidades e ao documento de requisitos.

6. **Escopo do UC02:** a especificação apresentada enfatiza a consulta e alteração de usuários existentes. Se a equipe definiu que o RF-002 também inclui o cadastro de novos usuários, essa operação deve ser incorporada ao UC02 ou documentada em um caso de uso separado, conforme a organização adotada.
