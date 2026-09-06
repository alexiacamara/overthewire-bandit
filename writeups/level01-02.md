# 🔹 Level 01 ➔ Level 02

## 🎯 Objetivo
A senha para o próximo nível (`bandit2`) está armazenada em um arquivo chamado `-`, localizado no diretório `home`. O desafio consiste em realizar a leitura do arquivo contornando a interpretação do hífen pelo sistema operacional.

---

## 🛠️ Comandos & Conceitos Utilizados
* `ls`: Lista os arquivos presentes no diretório atual.
* `cat ./-`: Realiza a leitura do arquivo chamado `-`. O uso do `./` é necessário para indicar o caminho do arquivo no diretório atual.
* **Caractere `-` (Hífen)**: Usado pelo terminal para identificar opções de comandos. Para lê-lo como nome de arquivo, é necessário especificar seu caminho (`./-`).
---

## 📝 Passo a Passo

### 1. Conexão / Acesso
Conexão ao `bandit1` efetuada com sucesso utilizando a senha obtida no nível anterior:

```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220

```
<img width="1107" height="617" alt="646950410-7af99bac-ced4-46c3-ab5d-ef9a5f4e6217" src="https://github.com/user-attachments/assets/69830b00-6110-4a8c-b4df-d3a5c8728d12" />


### 2. Listagem e Leitura
Listei os arquivos presentes na home com o `ls` e mostrei o conteúdo do arquivo `-` usando `cat ./-`

### 3. Conteúdo do Arquivo
Com o comando citado acima, consegui acesso ao arquivo e obtive acesso à nova senha.
<img width="606" height="197" alt="image" src="https://github.com/user-attachments/assets/8f6ca9ec-c75c-4b07-8ca5-2deb1951b1c5" />


