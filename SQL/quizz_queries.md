Sobre o banco de dados "classicmodels", indique as queries para obter as seguintes informações:

- Quantos registros há na tabela "customers"?
- Na tabela "customers", quantos clientes ("customerName") têm nome iniciado pela letra "M"?
- Na tabela "customers", crie uma saída que concatene nomes e sobrenomes em uma única coluna.
- Agora repita a query acima, mas com todas as letras em maiúsculo, e ordene pelo sobrenome.
- Na tabela "payments", selecione os registros ordenados por volume ("amount") e data de pagamento ("paymentDate")
- Na tabela "employees", indique quantos nomes de cargos ("jobTitle") únicos existem? 
- Qual destes cargos ("jobTitle") possuem mais funcionários?

select count(*) from customers;

select count(*) from customers where customerName like'M%';

select CONCAT(contactFirstName, ' ',contactLastName) from customers;

select CONCAT(upper(contactFirstName), ' ',upper(contactLastName)) from customers order by contactLastName;

select * from payments order by (amount and paymentDate);

select count(distinct(jobTitle)) from employees