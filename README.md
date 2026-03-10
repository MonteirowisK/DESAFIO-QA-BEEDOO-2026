# DESAFIO-QA-BEEDOO-2026
Repositório público para documentar o desfio Beedoo QA Tests.
--------------------------------------------------------------
A aplicação do desafio tem como objetivo simular de forma bem simples algo parecido com um CRUD. O motivo de ser algo parecido se dá pelo fato de um CRUD necessariamente ter que cumprir com todas as funções esperadas de um CRUD, sendo elas: Create (Criar), Read (Ler), Update (Atualizar) e Delete (Apagar). Na aplicação testada do Beedoo QA Challenge, há a possibilidade de criar (cadastrar o curso), ler (listar cursos) e deletar (excluir curso), porém não há a possibilidade de atualizar, seja na própria aplicação ou via Banco de dados.
--------------------------------------------------------------
Os principais fluxos do Beedoo QA Challenge são os fluxos de Cadastrar, Listar e Excluir. Caso a aplicação estivesse funcionando como foi planejada para funcionar, seria possível não só realizar testes unitários, mas também testes E2E. Usando o caminho feliz de exemplo e simulando o teste de um usuário, seria possível realizar o cadastro do curso desejado e, caso o usuário tivesse notado que alguma informação foi inserida incorretamente, realizar a alteração e salvar ou até mesmo excluir e refazer o cadastro novamente.
--------------------------------------------------------------
Falando um pouco sobre regra de negócio, um ponto crítico a ser levado em conta é que se a aplicação devesse se comportar como um CRUD, ela está incompleta e falta desenvolvimento. Não existe a função de Alterar e, a função de Excluir apenas gera um falso positivo, ou seja ela quando invocada, mostra uma mensagem de sucesso para a exclusão, porém não exclui o curso da lista.
Agora falando um pouco de funcionalidade e pensando em proteger o usuário de eventuais erros que ele possa cometer, na página de cadastro do curso há muitas melhorias possíveis para serem implementadas como por exemplo:
- Definir o tipo de dado a ser preenchido nos campos (não aceitar números no campo "Instrutor");
- Limitar as possibilidades de opções de datas dos campos "Data de início" e "Data de fim" (atualmente podendo selecionar do ano 1 até o ano 9999) e também adicionar uma regra que proíba o usuário de selecionar a "Data de fim" antes da "Data de começo".
- Não permitir o usuário inserir um número negativo no campo "Número de vagas".
- Alterar um dos dois botões "Cadastrar Curso" para eliminar uma eventual confusão do usuário sobre qual botão pressionar ao finalizar de preencher todos os dados do curso que deseja cadastrar.
- Arrumar o nome do desafio pois a grafia correta com dois "LLs", deveria ser "Beedoo QA Challenge".
--------------------------------------------------------------
Link dos cenários de teste Google Sheets - https://docs.google.com/spreadsheets/d/1DgvXY-Bt2MBrRKJkuT8yu3jlV8AN6YaweNGqLpkU3NM/edit?usp=sharing
Link do Drive com as evidências de teste - https://drive.google.com/drive/folders/1RMhW3TGA_hBAXK_oedtmG1LwS0VpfSUG?usp=sharing
--------------------------------------------------------------
Bug-01: Falha ao impedir o cadastro de curso duplicado - Sistema deveria impedir o cadastro de um curso com os mesmos dados de outro já existente. |Severidade Alta| |Prioridade Alta|
Bug-02: Falha ao impedir o cadastro de curso com dados obrigatórios faltantes - Sistema deveria impedir o cadastro ao não serem preenchidos todos os campos obrigatórios. |Severidade Alta| |Prioridade Alta|
Bug-03: Falha ao impedir o cadastro de um curso com número negativo de vagas - Sistema deveria impedir o cadastro ao ser inserido um formato negativo no campo "Número de vagas". |Severidade Média| |Prioridade Média|
Bug-04: Falha ao realizar a exclusão de um curso cadastrado na lista - Sistema deveria mostrar uma mensagem de sucesso relativo a exclusão do curso e remove-lo da lista de cursos cadastrados. |Severidade Alta| |Prioridade Alta|
