Projeto E-commerce - Curso Analise de Dados com Power BI

Projeto Conceitual – Sistema E-commerce.

Contexto Geral.
O projeto tem como objetivo representar, de forma conceitual, o funcionamento de um sistema de comércio eletrônico que integra clientes, produtos, fornecedores, vendedores terceiros, pedidos, pagamentos, entregas e cancelamentos. A modelagem busca garantir rastreabilidade, flexibilidade e integridade dos dados em todas as etapas do processo de compra.

Principais Entidades e Relações.

Cliente:	Representa o usuário que realiza compras na plataforma. Pode ser pessoa física (CPF) ou jurídica (CNPJ).	Relaciona-se com Pedido, Pagamento, ClientePF e ClientePJ.

ClientePF / ClientePJ:	Subtipos de cliente que armazenam dados específicos conforme o tipo de identificação.	Ligados à entidade Cliente por chave estrangeira.

Pedid:	Centraliza as informações da compra, incluindo status, descrição, frete e vínculo com o cliente.	Relaciona-se com Produto, Entrega, Cancelamento Pedido e Pagamento.

Produto:	Define os itens disponíveis para venda, com categoria, descrição e valor.	Associado a Fornecedor, Estoque, Pedido e Terceiro - Vendedor.

Fornecedor:	Entidade responsável por disponibilizar produtos à plataforma.	Relaciona-se com Produto por meio da tabela Disponibilizando um Produto.

Terceiro - Vendedor:	Representa vendedores parceiros que comercializam produtos na plataforma.	Associado a Produto pela tabela Produtos por Vendedor (Terceiro).

Estoque:	Controla a localização e quantidade dos produtos disponíveis.	Relaciona-se com Produto via Produto_has_Estoque.

Entrega:	Armazena dados sobre o envio do pedido, incluindo status e código de rastreio.	Associada a Pedido e Cliente.

Pagamento:	Registra o método e detalhes do pagamento realizado pelo cliente.	Relacionado a Cliente e Pedido.

Cancelamento Pedido:	Nova entidade que permite registrar pedidos cancelados, com status, motivo e data.	Relaciona-se diretamente com Pedido e Cliente.

Fluxo Conceitual

O Cliente realiza o cadastro e efetua um Pedido.
O Pedido contém um ou mais Produtos, que podem ser fornecidos por Fornecedores ou Vendedores Terceiros.
O Pagamento é processado e vinculado ao cliente e ao pedido.
O Estoque é atualizado conforme os produtos vendidos.
O Pedido gera uma Entrega, que acompanha o status e rastreio.
Caso o cliente solicite, o Cancelamento Pedido é registrado, alterando o status do pedido e armazenando o motivo e a data.




