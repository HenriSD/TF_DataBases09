## TF_DataBases09

# Comandos utilizados no TF:

# Exercicio 1:

1:

use loja_virtual

2 e 3:
```javascript

db.produtos.insertOne({
  nome: "Smartphone Galaxy A15",
  categoria: "Eletronicos",
  preco: 1299.90,
  marca: "Samsung",
  armazenamento: "128GB",
  cor: "Azul"
})

```

4:
```javascript

db.produtos.insertMany([
  {
    nome: "MongoDB na Pratica",
    categoria: "Livros",
    preco: 79.90,
    autor: "Joao Silva",
    editora: "Tech Books",
    paginas: 320
  },
  {
    nome: "Camiseta Basica",
    categoria: "Roupas",
    preco: 49.90,
    tamanho: "M",
    cor: "Preta",
    material: "Algodao"
  }
])

```

# Exercicio 2:

1:

db.produtos.find()

2:

db.produtos.find({ preco: { $gt: 100 } })

3:

db.produtos.find({ categoria: "Eletronicos" })

4:

```javascript

db.produtos.find(
  {},
  { nome: 1, preco: 1, _id: 0 }
)

```

# Exercicio 3:

1:

```javascript

db.produtos.updateOne(
  { nome: "Smartphone Galaxy A15" },
  { $set: { preco: 1199.90 } }
)

```

2:

```javascript

db.produtos.updateMany(
  {},
  { $set: { estoque: 50 } }
)

```
3: 

# Exercicio 4:

1:

db.produtos.deleteOne({ nome: "Camiseta Basica" })

2:

db.produtos.deleteMany({ categoria: "Livros" })