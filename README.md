# Projeto-banco-de-dados-conceitual-ordem-servico
Entrega do projeto referente ao desafio - Construindo um esquema conceitual para banco de dados.

Neste sentido, foi criado um esquema conceitual do zero, baseado na seguinte narrativa fornecida:
 - Sistema de controle e gerenciamento de execução de ordens de serviço em uma oficina mecânica;
 - Clientes levam veículos à oficina mecânica para serem consertados ou para passarem por revisões  periódicas;
 - Cada veículo é designado a uma equipe de mecânicos que identifica os serviços a serem executados e preenche uma OS com data de entrega;
 - A partir da OS, calcula-se o valor de cada serviço, consultando-se uma tabela de referência de mão-de-obra;
 - O valor de cada peça também irá compor a OSO cliente autoriza a execução dos serviços;
 - A mesma equipe avalia e executa os serviços;
 - Os mecânicos possuem código, nome, endereço e especialidade;
 - Cada OS possui: n°, data de emissão, um valor, status e uma data para conclusão dos trabalhos.

Assim, ao refinar o modelo, a entidade cliente possui os seguintes atributos: Nome, Identificação (RG/CPF/CNPJ), Endereço e contato.
Com isso, o cliente solicita/gera o Pedido, cuja entidade possui os seguintes atributos: Descrição, data da solicitação e indentificação do veículo (placa).
Na sequência, o pedido determina uma nova entidade, chamada equipe de mecânicos, pelo que cada mecânico que compõe a equipe deve ser identificado pelos atributos: nome, endereço e especialidade.
Por sua vez, essa equipe de mecânicos preenche uma ordem de serviço, na qual deverá constar: data da emissão, valor total, data da entrega e status, pelo que o valor total corresponde ao cálculo referente ao valor de um ou mais serviços, assim como também de uma ou mais peças que deverão estar descritos e serão utilizados na execução da ordem de serviço. Assim, dependendo da autorização do cliente, a referida ordem de serviço será então avaliada e executada pela mesma equipe de mecânicos que preencheu a mesma. 

Obs: Uma OS pode ser composta por vários serviços e um mesmo serviço pode estar contido em mais de uma OS.
     Uma OS pode ser composta por vários tipos de peças e uma mesma peça pode estar presente em mais de uma OS. 
