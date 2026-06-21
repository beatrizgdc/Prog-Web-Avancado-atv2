# Laboratório Prático - Git e GitHub

**Aluno:** Beatriz Cevaio  
**Disciplina:** Sistemas para Internet  
**Data:** 2026

---

## 1. Configuração Inicial do Git

Configuração do nome de usuário e e-mail no Git.

**Comandos utilizados:**
```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu.email@example.com"
git config --list
```

**Print da execução:**

![alt text](image.png)

---

## 2. Criar um Repositório Local

Criação da pasta do projeto e inicialização do repositório Git.

**Comandos utilizados:**
```bash
mkdir meu-projeto
cd meu-projeto
git init
```

**Print da execução:**

![alt text](image-1.png)

---

## 3. Adicionar Arquivos e Fazer o Primeiro Commit

Criação do arquivo `README.md`, verificação do status, adição à Staging Area e realização do primeiro commit.

**Comandos utilizados:**
```bash
echo "# Meu Projeto" > README.md
git status
git add README.md
git commit -m "Primeiro commit: adiciona README.md"
```

**Print do `git status` (antes do add):**

![alt text](image-2.png)

**Print do commit:**

![alt text](image-3.png)

---

## 4. Criar um Repositório no GitHub

Criação do repositório remoto na plataforma GitHub.

**Configurações utilizadas:**
- Nome do repositório: `meu-projeto`
- Visibilidade: Público
- Sem arquivos iniciais (README, .gitignore, etc.)

**Print da tela de criação do repositório no GitHub:**

![alt text](image-4.png)

---

## 5. Conectar o Repositório Local ao GitHub

Adição do repositório remoto e envio dos arquivos locais para o GitHub.

**Comandos utilizados:**
```bash
git remote add origin https://github.com/seu-usuario/meu-projeto.git
git push -u origin main
```

**Print da execução:**

![alt text](image-5.png)

**Print do repositório no GitHub após o push:**

![alt text](image-6.png)

---

## 6. Criar e Trabalhar em uma Nova Branch

Criação da branch `feature/nova-funcionalidade`, adição de arquivo e commit.

**Comandos utilizados:**
```bash
git checkout -b feature/nova-funcionalidade
echo "Nova funcionalidade em desenvolvimento" > nova-funcionalidade.txt
git add nova-funcionalidade.txt
git commit -m "Adiciona nova funcionalidade"
git push -u origin feature/nova-funcionalidade
```

**Print da criação da branch:**

![alt text](image-7.png)

**Print do commit na nova branch:**

![alt text](image-8.png)

**Print do GitHub mostrando as duas branches:**

![alt text](image-9.png)

---

## 7. Fazer Merge da Branch na Main

Retorno para a branch `main`, atualização e merge da branch `feature/nova-funcionalidade`.

**Comandos utilizados:**
```bash
git checkout main
git pull origin main
git merge feature/nova-funcionalidade
git push origin main
```

**Print do merge:**

![alt text](image-10.png)

**Print do GitHub após o merge (mostrando o arquivo `nova-funcionalidade.txt` na main):**

![alt text](image-11.png)

---

## Resumo e Conclusão

Neste laboratório foram praticadas as principais funcionalidades do Git e GitHub:

| Etapa | Comando principal | O que foi feito |
|---|---|---|
| Configuração | `git config` | Definição de nome e e-mail do usuário |
| Repositório local | `git init` | Inicialização do repositório |
| Versionamento | `git add` + `git commit` | Adição de arquivos e registro de snapshot |
| Repositório remoto | `git remote add` + `git push` | Conexão e envio ao GitHub |
| Branches | `git checkout -b` | Criação de ramificação para nova funcionalidade |
| Merge | `git merge` | Integração da branch à main |

**Repositório no GitHub:** [https://github.com/beatrizgdc/Prog-Web-Avancado-atv2](https://github.com/beatrizgdc/Prog-Web-Avancado-atv2)
