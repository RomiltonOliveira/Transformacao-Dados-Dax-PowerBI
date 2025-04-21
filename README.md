# Modelagem e Transformação de dados com DAX com Power BI

### Descrição do Desafio de Projeto

Utilizaremos a tabela única de Financial Sample para criar as tabelas dimensão e fato do nosso modelo baseado em star schema.

O processo consiste na criação das tabelas com base na tabela original. A partir da cópia serão selecionadas as colunas que irão compor a visão da nova tabela. Sendo assim, a partir da tabela principal serão criadas as tabelas:

Financials_origem (modo oculto – backup)


D_Produtos (ID_produto, Produto, Média de Unidades Vendidas, Médias do valor de vendas, Mediana do valor de vendas, Valor máximo de Venda, Valor mínimo de Venda)

D_Produtos_Detalhes(ID_produtos, Discount Band, Sale Price, Units Sold, Manufactoring Price)

D_Descontos (ID_produto, Discount, Discount Band)

D_Detalhes (*)

D_Calendário – Criada por DAX com calendar()

F_Vendas (SK_ID , ID_Produto, Produto, Units Sold, Sales Price, Discount Band, Segment, Country, Salers, Profit, Date (campos))


*Verifique as informações que não foram contempladas nas demais tabelas dimensão que fornecem maiores detalhes sobre vendas.

Primeiramente criamos as tabelas dimensões e a tabela fato derivadas da tabela Financials. A imagem abaixo ilustra as tabelas criadas:

![tabelas](https://github.com/user-attachments/assets/39f25b0a-86a8-4a6b-8ebd-69180bf0a620)

### A seguir estão ilustrados as estruturas em cada tabela:

![financials origem](https://github.com/user-attachments/assets/4fc1f4c2-8db4-4f4a-85f3-c4ebe3de66b1)

### Todas as tabelas foram originadas da tabela acima.

![descontos](https://github.com/user-attachments/assets/a693cf78-272e-4884-9486-8ce604eb41e6)

![detalhes](https://github.com/user-attachments/assets/225c9b5a-5594-428d-aa78-92a14ca3d314)

![produtos](https://github.com/user-attachments/assets/7e107ace-9b06-46c5-8e10-ac65e65226f6)

![produtos detalhes](https://github.com/user-attachments/assets/541c77a9-500e-4d97-b884-74a1f1ecff3b)

![vendas](https://github.com/user-attachments/assets/4c725eae-be67-474e-9b90-68d708dc59be)

![calendario](https://github.com/user-attachments/assets/da2f2498-9f4a-445f-8be0-d0e065062a43)

### A tabela calendário foi criada através de código com a linguagem DAX e a função Calendar().

Os seguintes códigos Dax foram utilizados para criar a tabela D_Calendário

![data1](https://github.com/user-attachments/assets/c31ccf4c-7933-48bb-a5b3-a629c98627d4)

![data2](https://github.com/user-attachments/assets/ce4801ae-aefb-4300-9837-d86b24707dd5)
![data3](https://github.com/user-attachments/assets/df5a8065-4495-4a29-a7be-750d5473321f)
![data4](https://github.com/user-attachments/assets/9dd072bb-7189-46ca-bc3f-bc86e6aedb09)
![data5](https://github.com/user-attachments/assets/3cb6693e-8b86-471b-90b6-647508423b2c)

Para finalizar este desafio foram feitos os relacionamentos de cada tabela seguindo o modelo dimensional com o star schema, onde todos os relacionamentos são feitos com a tabela fato, sem ligações entre 
as tabelas dimensões. O resultado final esta ilustrado a seguir:

![relacionamentos](https://github.com/user-attachments/assets/710815f8-fb4b-4746-9493-5cf7baba4d4d)








