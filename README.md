# 🎬 MovieFlix API

API RESTful desenvolvida em **TypeScript** para gerenciamento de filmes e usuários.  
O projeto utiliza **Prisma ORM** para manipulação de banco de dados, é containerizado com **Docker** e documentado com **Swagger**.

---

## 🚀 Tecnologias

- [TypeScript](https://www.typescriptlang.org/)  
- [Node.js](https://nodejs.org/)  
- [Express](https://expressjs.com/)  
- [Prisma](https://www.prisma.io/)  
- [Docker](https://www.docker.com/)  
- [Swagger](https://swagger.io/)

---

## 📂 Estrutura do Projeto

```
movieflix-api/
 ┣ 📁 prisma          # Configuração do Prisma e migrations
 ┣ 📁 src             # Código-fonte (rotas, controllers, services)
 ┣ 📄 Dockerfile      # Configuração da imagem
 ┣ 📄 docker-compose.yml # Subida dos containers (app + DB)
 ┣ 📄 schema.prisma   # Definição do schema do banco
 ┗ 📄 README.md
```

---

## 🛠️ Como rodar o projeto

### 1. Clone o repositório
```bash
git clone https://github.com/endriusssantos/movieflix-api.git
cd movieflix-api
```

### 2. Configure as variáveis de ambiente
Crie um arquivo `.env` na raiz com:
```env
DATABASE_URL="postgresql://usuario:senha@db:5432/movieflix"
```

### 3. Suba os containers
```bash
docker-compose up -d
```

### 4. Rode as migrations
```bash
npx prisma migrate dev
```

### 5. Inicie a aplicação
```bash
npm run dev
```

A API estará disponível em:  
👉 `http://localhost:3000`

---

## 📖 Documentação

Acesse a documentação dos endpoints em:  
👉 `http://localhost:3000/api-docs`

---

## 🔎 Exemplos de requisições

### Criar um filme
```bash
curl -X POST http://localhost:3000/movies   -H "Content-Type: application/json"   -d '{"title": "Inception", "year": 2010, "genre": "Sci-Fi"}'
```

### Listar filmes
```bash
curl http://localhost:3000/movies
```

---

## 🤝 Contribuição

1. Faça um fork do projeto  
2. Crie uma branch com sua feature (`git checkout -b minha-feature`)  
3. Commit suas alterações (`git commit -m 'feat: minha nova feature'`)  
4. Envie para o repositório (`git push origin minha-feature`)  
5. Abra um Pull Request 🎉

---

## 📜 Licença

Este projeto é open source, sob a licença MIT.  
