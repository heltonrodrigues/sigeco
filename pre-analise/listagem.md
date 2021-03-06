# Listagem

![](http://developers.connectparts.com.br/imagens/img01.png)

## Funcionalidade

Neste processo os departamentos Financeiro e Atendimento fazem uma pré analise dos pedidos oriundos do Ábacos ou DropShipping, levando em consideração algumas regras como: cliente tem pedidos anteriores há 6 meses, cliente fez compras nos últimos 30 dias e CPF/CNPJ está na lista de ocorrências.

## Processos

**Campos**

* **Limpar Filtros**
  * Limpa os filtros e cache armazenado na consulta
* **Pedidos Ábacos - Pedidos DropShipping**
  * Escolha de onde virão os pedidos Ábacos ou pedidos que contenham DropShipping
* **Data Inicial e Final**
  * Selecione as datas para a pesquisa ser especifica.
* **Forma de pagamento**
  * Selecione as formas de pagamento para a pesquisa ser especifica.
* **Pedido**
  * Digite o número do pedido para a pesquisa ser especifica.

> **Observação:** Caso não selecione e nem preencha algum campo a consulta poderá ser feita clicando no botão de geração "**Lupa**", porém, sem critérios.

### Legendas

| Descrição |  |
| :--- | :--- |
| **Imagem** | ![](http://developers.connectparts.com.br/imagens/preAnalise02.png) |
| **Cadeado Preto** | Pedido |
| **Cadeado Vermelho** | Pedido barrado \(pela pré análise\) |
| **Cadeado Verde** | Pedido barrado \(pela pré análise\) e depois liberado \(pelo atendimento\) |

#### Ação

Ao clicar na **Ação** será direcionado para a tela de _**Visualização de Pedido - Pré Análise**_.

![](http://developers.connectparts.com.br/imagens/preAnalise04.png)

Ao clicar em **Barrar Pedido** é necessário inserir um motivo válido.

É apresentado **Informações Ábacos**, com a opção de bloquear CPF e CNPJ do destinatário e do cliente, formas e condições de pagamento e itens de pedido.

#### Informações sobre o pedido

O sistema traz detlahes sobre o pedido para que ao barrar o pedido, seja feita de forma consciente e maoires informações.

* **Informações Ábacos**   O sistema através de API traz informações que estão no nosso ERP. O sistema cria alertar visuais, informando quais pedidos existem inconsistência de informações para entrega. Informações checadas: CEP, Cidade, Estado Numero, Nome do Destinatário.

#### Caixa Postal Pré-Análise.

O sistema gera um alerta visual para todo o pedido Connect, independente do canal de vendas ou forma de pagamento, referente a caixa postal com transportadora diferente de Correios. São verificados os CEP´s que estão dentro da faixa XX.XXX-970 à XX.XXX-999 ou quando no campo endereço ou observação contiverem as palavras “cx”, “cxp”, “postal”, “caixa postal” ou “posta”.

#### Divergência:

Caixa Postal, tem que ser enviado pelo correio.

![](../.gitbook/assets/imagem_3.jpeg)

![](../.gitbook/assets/imagem_2.jpeg)

![](../.gitbook/assets/imagem_1.jpeg)

![](../.gitbook/assets/whatsapp-image-2018-07-23-at-16.53.20.jpeg)

#### Erros

CEP invalido ou não informado, Nome do Cliente invalido, Numero logradouro em branco, CEP não encontrado, UF não confere, Localidade não confere

* **Formas e Condições de Pagamento e Itens do Pedido** ![](http://developers.connectparts.com.br/imagens/preAnaliseImg002.png) O sistema traz informações sobre a forma de pagamento, valores, informações sobre o produto, quantidade de venda e valor dos itens do pedido, sem encargos ou cobrança de frete.
* **Informações do Mercado Pago** ![](http://developers.connectparts.com.br/imagens/preAnaliseImg003.png)

## Resultado

![](http://developers.connectparts.com.br/imagens/financeiroPreAnaliseListagem01.png)

O resultado traz a quantidade de **Pedidos Encontrados**. E as colunas **Pedido, Tipo de Pessoa, Forma de Pagamento, Valor, Status, Data** e **Ação**.

## Regras

**Para bloqueio**

* Cliente tem pedidos anteriores há 6 meses
* Cliente fez compras nos últimos 30 dias
  * Ou 3 compras com valor total igual ou maior de R$ 1.500,00
* CPF/CNPJ está na lista de ocorrências.
* Pedidos com -TRT , -INT, -TRR não serão demonstrados.
  * Atualmente no Ábacos, existem 03 grupos de comercialização \(_DEVOLUCAO PARA FORNECEDORES, SAIDA OUTROS, VENDA_\), os pedidos com siglas são encontrados em SAIDA OUTROS.

**API**

* Consultamos API que a 00K nos disponibiliza, as informações sobre o pedido citada acima, vem desta API. 

