# mongodb

Criar collection
`db.createCollection('aluno')`

Deletar Collection
`db.aluno.drop()` 

Insert
```javascript
  db.alunos.insert(
    'nome': 'Josafa',
    'nascimento': new Date(1990,09,26)
  )
```

Find
```javascript
//Trás todos elementos da coleção
db.alunos.find()

// Procura um especifico
db.alunos.find({'nome': 'josafa'})
```

Remover
```javascript
db.alunos.remove({
  '_id': ObjectId("5d878d8a9254fe1008bdee12")
})
```
Or e In
```javascript
db.alunos.find(
  {
    $or : [
      {curso.nome: 'Sistemas de informação'},
      {curso.nome: 'Moda'}
    ]
  
  }
)

db.alunos.find(
  {
    curso.nome: {
      $in: ['Sistemas de informação', 'Moda']
    }
  }
)
```
