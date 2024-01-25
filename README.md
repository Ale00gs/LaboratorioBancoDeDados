<p align="center">
  
<img src="https://camo.githubusercontent.com/82291b0fe831bfc6781e07fc5090cbd0a8b912bb8b8d4fec0696c881834f81ac/68747470733a2f2f70726f626f742e6d656469612f394575424971676170492e676966" width="100%" height="2">

</p>
<div align="center">
  
![header](https://capsule-render.vercel.app/api?type=soft&text=⭐️LABORATÓRIO%20DE%20BANCO%20DE%20DADOS⭐&fontAlign=50&fontAlignY=60&fontSize=30&animation=fadeIn&height=100)

</div>

<div align="center">

  [![JSON](https://img.shields.io/badge/Feito%20com-JSON-purple)](#) 
  [![mongoDB](https://img.shields.io/badge/Feito%20com-mongoDB-purple)](#) 

</div>

<p align="center"> 
  Aqui está um exercício que eu fiz para a fixação do conteúdo de Laboratório de Banco de Dados, no 4º termo de Análise e Desenvolvimento de Sistemas.
  Modelagem de dados no formato JSON (banco de dados não relacional - modelo documental)
</p>

## 
### <p align="center"> COMANDOS DA LOJA DE INSTRUMENTOS</p>

### Inserir – (Inserir um novo instrumento)


      db.instrumentos.insertOne(
        {
          "_id": 4,
          "nome": "Teclado",
          "tipo": "Teclas",
          "preco": 2000,
          "estoque": 25,
          "caracteristicas": {
              "cor": "Branco",
              "marca": "Casio",
              "material": "Madeira",
              "peso": 3.5 },
          "comentarios": [
              { "cliente_id": 101,
                "texto": "Ótimo som!"},
              { "cliente_id": 102,
                "texto": "Design incrível." }]
        })

### Pesquisar (Operadores relacionais) – (Pesquisar instrumentos com preço maior que $1500.00)


      db.instrumentos.find({"preco": {"$gt": 1500.00}})

### Atualizar (Operadores relacionais) – (Atualizar o estoque da Guitarra para 45 unidades)


      db.instrumentos.updateOne({"nome": "Guitarra"}, {"$set": {"estoque": 45}})

### Excluir (Operadores relacionais) – (Excluir cliente com ID 102)


      db.clientes.deleteOne({"_id": 102})

### Juntar documentos das coleções da modelagem – (Juntar o cliente com o instrumento comprado)


      db.clientes.aggregate([
      {
        $lookup: {
          from: "instrumentos",
          localField: "instrumentos_comprados.instrumento_id",
          foreignField: "_id",
          as: "instrumentos_comprados_info" }}
    ])



## Contato

- E-mail: [Meu Email](mailto:agonsalvessissa@gmail.com)
- LinkedIn: [Meu Perfil](https://www.linkedin.com/in/alerrandra)

<p align="center">
<img src="https://camo.githubusercontent.com/82291b0fe831bfc6781e07fc5090cbd0a8b912bb8b8d4fec0696c881834f81ac/68747470733a2f2f70726f626f742e6d656469612f394575424971676170492e676966" width="100%" height="2">
</p>
