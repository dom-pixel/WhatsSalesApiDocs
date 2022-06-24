## Search

A função Search é utilizada quando você precisa buscar um **Diálogo** rápidamente, você pode filtrar em 5 tipos:  
- Status  
- Name  
- Operator  
- Contact  
- Last Message

## Filter by Status:
Exemplo:
```url
http://localhost:3333/api/v1/search?search=ABERTO
```
A Response vai ser:
![response](https://raw.githubusercontent.com/M1gu3l0001/SomethingAboutNothing/d630c0352d0bd25084204be2dc7d7d48dd77617a/carbon%20(4).svg)
Porque foi retornado esse resultado?  
Bom, o filtro utilizado foi o **Status** onde eu pedi para o server me retornar os **Dialogs** que estão em **ABERTO**, nesse caso, só há 1 Dialog que está em Aberto.

## Filter by Name:
Exemplo:
```url
http://localhost:3333/api/v1/search?search=M1gu3l0001
```
A Response vai ser:
![response](https://raw.githubusercontent.com/M1gu3l0001/SomethingAboutNothing/d630c0352d0bd25084204be2dc7d7d48dd77617a/carbon%20(3).svg)
Porque foi retornado esse resultado?  
Bom, o filtro utilizado foi o **Name** onde eu pedi para o server retornar os **Dialogs** que estão no nome de **M1gu3l0001**, nesse caso, há 2 Dialogs que estão no nome de **M1gu3l0001**, dá para perceber aqui:
```
"name": "M1gu3l0001" <---
```

## Filter by Operator:

Exemplo:
```
http://localhost:3333/api/v1/search?search=Administrador
```
A Response será essa:
![response](https://raw.githubusercontent.com/M1gu3l0001/SomethingAboutNothing/d630c0352d0bd25084204be2dc7d7d48dd77617a/carbon%20(2).svg)
Porque foi retornado esse resultado?  
Bom, o filtro utilizado foi o **Operator**, ele basicamente entra no ```operator_id``` e pega o seu nome.
```
...
"operator_id": 1, //Id do operador é 1
...
```
```SQL
SELECT * FROM users WHERE id = 1 /*Pega todos os usuários e seleciona o usuário de ID 1*/
/*Resultado: Administrador*/
```
Nesse caso, há 2 Dialogs com o **operator_id = 1**

## Filter by Contact:

Exemplo:
```url
http://localhost:3333/api/v1/search?search=mauricie
```
A Response será:
![response](https://raw.githubusercontent.com/M1gu3l0001/SomethingAboutNothing/d630c0352d0bd25084204be2dc7d7d48dd77617a/carbon%20(1).svg)
Porque foi retornado esse resultado?  
Bom, o filtro utilizado foi o **Contact**, ele basicamente entra no ```contact_id``` e pega o seu nome, nesse caso, se fizermos um GET na rota ```/contacts/3```, teremos o seguinte resultado:
![response](https://raw.githubusercontent.com/M1gu3l0001/SomethingAboutNothing/ffbd9b73fc2a9d1b13c5cad8a5faa4d916358198/carbon%20(5).svg)
o ```first_name``` é igual ao que colocamos na URL!

## Filter by Last Message:

Exemplo:
```http://localhost:3333/api/v1/search?search=eai!```
A Response será:
![response](https://raw.githubusercontent.com/M1gu3l0001/SomethingAboutNothing/6ecab85e46dc84ebebee6fe6b57ce290c3dcb817/carbon%20(6).svg)
Porque foi retornado esse resultado?  
Bom, o filtro utilizado foi o **Last Message**, o que significa que você pode procurar por um chat com a última mensagem enviada, nesse caso foi o "eai!"