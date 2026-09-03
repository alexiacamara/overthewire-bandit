# 🔹 Level 00 ➔ Level 01

## 🎯 Objetivo
Acessar o arquivo chamado `readme` localizado no diretório *home* do usuário `bandit0` para encontrar a senha de acesso ao `bandit1`.

---

## 🛠️ Comandos & Conceitos Utilizados
* `ls`: Lista os arquivos presentes no diretório atual.
* `cat`: Exibe o conteúdo de um arquivo de texto diretamente no terminal.
* **Diretório Home (`~`)**: Pasta pessoal do usuário logado no sistema Linux.

---

## 📝 Passo a Passo

### 1. Conexão / Acesso
Conexão efetuada ao nível atual utilizando SSH na porta `2220`:

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```
<img width="1148" height="632" alt="image" src="https://github.com/user-attachments/assets/81711bbe-2643-4ed7-ab5d-2f85aea2b0a3" /> 

### 2. Listagem e Leitura
Listei os arquivos presentes na home com o `ls` e mostrei o conteúdo do arquivo readme usando `cat readme`

### 3. Conteúdo do Arquivo
Dentro deste arquivo encontrei a senha do próximo nível. 
<img width="761" height="262" alt="image" src="https://github.com/user-attachments/assets/0b4136db-4f16-43d8-a90e-36d00f87e747" />


