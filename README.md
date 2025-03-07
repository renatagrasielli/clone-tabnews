# Clone TabNews  
Implementação do **TabNews** para o **curso.dev**

---

## 📋 Índice

1. [Comandos Úteis](#comandos-úteis)  
2. [Rodando o Ambiente](#-rodando-o-ambiente)  
3. [Executando Testes](#%EF%B8%8F-executando-testes)  
4. [📦 Docker](#-docker)  
5. [📅 psql](#-psql)  

---

## Comandos Úteis
ligando o rolê
- Docker
 ```bash
   docker compose -f infra/compose.yaml up -d
 ```
- psql
```bash
    psql --host=localhost --username=local_user --port=5432 --dbname=local_db
```
- dev
```bash
    npm run dev
```
- test
```bash
    npm run test:watch
```
---

<details>
  <summary><b>📂 Esqueceu comando de Git? Abra-me.</b></summary>

  <details>
   <summary><b>1. Conferir Status</b></summary>
    
  ```bash
    git status
  ```
  </details>

  <details>
    <summary><b>2. Trazer itens para o "palco"</b></summary>
    
  Adicione um arquivo específico ou todas as alterações ao **staging area**:
    
  ```bash
    git add [caminho ou arquivo]
  ```
    
  Para incluir todas as alterações de uma vez, use:  
  ```bash
    git add .
  ```
  ou
  ```bash
    git add -A
  ```   
  _Obrigada pela correção, arthurhonorio! :)_
  </details>

  <details>
    <summary><b>3. Commit</b></summary>

  "Commitar" as alterações:
  ```bash
    git commit -m 'detalhes da alteração'
  ```

  Editar o último commit:
  ```bash
    git commit --amend
  ```

  Destacar texto no commit:
    
  ```bash
    git commit -m 'destaque os `detalhes da alteração`'
  ```
  </details>

  <details>
    <summary><b>4. Push</b></summary>

  Publicar as alterações no repositório remoto:
  ```bash
    git push
  ```
  </details>

  <details>
    <summary><b>5. Pull</b></summary>

  Incorporar mudanças do repositório remoto no branch local:
  ```bash
    git pull
  ```
  </details>

  <details>
    <summary><b>6. Renomear Arquivos (mv)</b></summary>
    
  ```bash
    git mv [nome atual] [nome novo]
  ```
  </details>

</details>

---

## 🛞 Rodando o Ambiente

Execute o servidor de desenvolvimento:  
```bash
npm run dev
```
---

## 👁️ Executando Testes

Execute o "observador" de testes:  
```bash
npm run test:watch
```

---

## 📦 Docker

### Subir os serviços

1. Usando o arquivo padrão:
    ```bash
    docker compose up
    ```
2. Especificando o caminho do arquivo `compose.yaml`:
    ```bash
    docker compose -f infra/compose.yaml up -d
    ```

### Outros Comandos Úteis

- **Verificar status do Docker:**  
    ```bash
    docker ps
    ```  
    Ou listar todos os containers:  
    ```bash
    docker ps -a
    ```
  
- **Verificar logs do Docker:**  
    ```bash
    docker logs [NOME_DO_CONTAINER]
    ```

- **Subir container em modo "desanexado":**  
    ```bash
    docker compose up --detach
    ```  
    Ou  
    ```bash
    docker compose up -d
    ```

- **Destruir containers:**  
    ```bash
    docker compose down
    ```  
    Ou recriar containers:  
    ```bash
    docker compose up -d --force-recreate
    ```

---

## 📅 psql  

- **Acessar o PostgreSQL:**  
    ```bash
    psql --host=localhost --username=local_user --port=5432 --dbname=local_db
    ```
_Obs: o psql não lê o arquivo .env.development. É preciso passar os valores diretamente via linha de comando. E [quando não é passado o valor do --dbname, ele usa o valor definido no --username](#https://www.postgresql.org/docs/current/app-psql.html#:~:text=Once%20the%20database%20user%20name%20is%20determined%2C%20it%20is%20used%20as%20the%20default%20database%20name.)._
_Obrigada pela correção, Andrei! :)_

- **Sair do psql:**  
    ```bash
    \q
    ```

---

## 🛠️ Instalação do Cliente PostgreSQL  

1. Atualize o repositório:  
    ```bash
    sudo apt update
    ```
2. Instale o cliente:  
    ```bash
    sudo apt install postgresql-client
    ```

---

**💡 Dica:** Para mais informações sobre o projeto, consulte a [documentação oficial do TabNews](https://tabnews.com.br).
