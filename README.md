# Clone TabNews

Implementação do tabnews para o curso.dev

# Comandos úteis

<details>
  <summary><b>Se não lembrar os comandos do Git, abra-me</b></summary>
<br>
  <details>
    <summary><b>1. Conferir Status</b></summary>
    
```bash
    git status
```
    
  </details>

  <details>
    <summary><b>2. Trazer itens para o "palco"</b></summary>
<br>
Para adicionar um arquivo específico ou todas as alterações ao **staging area**: 
    
 ```
  git add [caminho ou arquivo]  
 ```
    
Para incluir todas as alterações de uma única vez, use:
    
```bash
git add . -A
```
    
  </details>
   <details>
     <summary><b>3. Commit</b></summary>
<br>
"Commitar" as alterações.
     
```bash
git commit -m 'detalhes da alteração'
```
ou editar o ultimo commit

```
git commit --amend
```  
 <details>  
   <summary>Destacar</summary>
<br>
Usar "`" destaca os caracteres.
   
```bash
git commit -m 'destaque os `detalhes da alteração`'
```
  </details>
</details>
<details>  
   <summary><b>4. Push</b></summary>
<br>
Publicar as alterações no repo remoto.
   
```bash
git push
```
  </details>
  
<details>  
   <summary><b>5. Pull</b></summary>
<br>
"Puxa" as mudanças do repo remoto e incorpora no branch local.
   
```bash
git pull
```
  </details>
  
</details>


---
🛞 rodar o ambiente

```
npm run dev
```
---
👁️ "observador" de testes

```
npm run test:watch
```
---

## 🐋 Docker

aplicar serviços do `compose.yaml`

```
docker compose up
```
ou especificando o caminho do `compose.yaml`

```
docker compose -f infra/compose.yaml up
```
---
<br>
Verificar status do Docker

```
docker ps
```
ou

```
docker ps -a
```
---
<br>
Verificar logs do docker

```
docker logs [NAME]
```
---
<br>
usar docker em detached (desanexado)

```
docker compose up --detach
```
ou
```
docker compose up -d
```
---
destruir container

```
docker compose down
```

ou 

```
docker compose up -d --force-recreate
```


---
<br>
instalar client do postgres

```
sudo apt update
```
+

```
sudo apt install postgresql-client
```
---
## 📅psql

---
<br>
Verificar logs do docker

```
psql --host=localhost --username=postgres --port=5432
```
---
sair do psql
```
\q
```
