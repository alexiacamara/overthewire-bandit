# 🔹 Level 03 ➔ Level 04

### 🎯 Objetivo
A senha para o próximo nível está armazenada na pasta chamada `inhere`, é um arquivo escondido e o objetivo é encontrá-lo para ter a senha do próximo nível. 

---

### 🛠️ Comandos & Conceitos Utilizados

* `ls`: Lista os arquivos presentes no diretório atual.
* `cat`: Exibe o conteúdo de um arquivo de texto diretamente no terminal.
* `cd`: Abre o diretório informado.
* `ls -a`: Variação do comando ls que exibe todos os arquivos de um diretório, incluindo os arquivos ocultos (que começam com um ponto).
* `pwd`: Exibe o caminho completo do diretório atual no terminal (*print working directory*).
* `Arquivos Ocultos`: No Linux, arquivos iniciados com `.` são ocultos por padrão e só aparecem ao listar com `-a`.  


--- 

## 📝 Passo a Passo

### 1. Conexão / Acesso
Conexão efetuada ao nível atual utilizando SSH na porta `2220`:

``` bash 
ssh bandit3@bandit.labs.overthewire.org -p 2220
```
<img width="809" height="630" alt="image" src="https://github.com/user-attachments/assets/9dc67a40-9bab-4555-a196-dfff8c9b563a" />

---

### 2. Listagem e Leitura

+ Listei os arquivos presentes com o `ls`, depois usei o `cd` para abrir o diretório. <br>
<img width="268" height="97" alt="image" src="https://github.com/user-attachments/assets/50e93e46-7f6e-448d-bca3-719f43e17c41" />
<br><br>

+ Usei o comando `pwd` para confirmar se estava no diretório certo. <br>
<img width="290" height="67" alt="image" src="https://github.com/user-attachments/assets/2911351e-5e86-41f1-9aa3-84890000f26b" />
<br><br>

+ Tentei ver o conteúdo do diretório usando `ls`, mas como o arquivo é escondido então não funciona neste caso. Por conta disso, coloquei o `-a` para conseguir ver os arquivos do diretório, inclusive os escondidos. E a pasta com a senha foi encontrada. É a `...Hiding-From-You`. <br>
<img width="294" height="79" alt="image" src="https://github.com/user-attachments/assets/cfeaaf19-7ac1-4fe1-bbe2-3bb9a8812a5f" />
<br><br>

***Observação**: Na imagem podemos ver que há `.` e `..`. O `.` significa o diretório atual onde você está e o  `..` significa o significa o diretório pai (a pasta acima do diretório atual).***
<br>

+ Acessei o conteúdo do arquivo usando o comando `cat ...` e pressionei a tecla tab para que autocompletar. Dentro do arquivo encontrei a senha para o próximo nível. <br>
<img width="464" height="61" alt="image" src="https://github.com/user-attachments/assets/dd577704-f896-4df4-bf19-8ccbe63c67e7" />

---

### 💡 Aprendizado do Nível
Aprendi como identificar e acessar arquivos ocultos no Linux, os quais se iniciam com o caractere ponto (.) e não são exibidos pelo comando `ls` padrão. Compreendi o uso do parâmetro `-a` para listar todos os itens de um diretório, além de entender a função dos atalhos de navegação `.` (diretório atual) e `..` (diretório pai). Também pratiquei o uso da tecla Tab para o autocompletamento de nomes de arquivos no terminal.






