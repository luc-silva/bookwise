# BookWise

BookWise é um gestor de livros completo, composto por três submódulos em TypeScript:

- [`BookWise-API`](BookWise-API/): API RESTful para gerenciamento dos dados dos livros.
- [`BookWise-client`](BookWise-client/): Aplicação web para gerenciar sua estante de livros.
- [`bookwise-native`](bookwise-native/): Aplicativo mobile (React Native + Expo) para acessar sua estante de qualquer lugar.

## Funcionalidades

- Adicione, exclua e atualize livros na sua bookshelf.
- Visualize todos os seus livros em uma lista.
- Indicadores na home mostram:
  - Total de livros lidos, não lidos e dropados.
  - Percentual de livros lidos.

> **Importante:** As aplicações [`BookWise-client`](BookWise-client/) e [`bookwise-native`](bookwise-native/) só funcionam corretamente com a branch `old` da [`BookWise-API`](BookWise-API/).

---
## TO-DO
- [ ] Criar .sh para atualizar submódulos
- [ ] Criar .sh para atualizar submódulos
- [ ] Dockernizar repositórios
---

## Como rodar cada módulo

### 1. BookWise-API

API desenvolvida em TypeScript com Express.

```sh
cd BookWise-API
npm install
```

Crie um arquivo `.env` com as configurações do MongoDB:

```
MONGODB_URI=mongodb://localhost:27017/bookwise
API_PORT=6060
JWT_SECRET=sua_chave_secreta
```

Inicie a API:

```sh
npm run server
```

---

### 2. BookWise-client

Aplicação web em React + TypeScript.

```sh
cd BookWise-client
npm install
npm start
```

---

### 3. bookwise-native

Aplicativo mobile em React Native com Expo.

```sh
cd bookwise-native
npm install
```

Crie um arquivo `.env` com as variáveis de ambiente para a API:

```
API_URL=http://localhost
API_PORT=6060
```

Inicie o app:

```sh
npm start
```

---

## Observações

- Certifique-se de que a API está rodando antes de iniciar o client ou o app mobile.
- Para desenvolvimento mobile, é necessário ter o [Expo CLI](https://docs.expo.dev/get-started/installation/) instalado globalmente.

---
