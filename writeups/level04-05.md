# 🔹 Level 04 ➔ Level 05

### 🎯 Objetivo
O objetivo deste nível é encontrar, dentro da pasta `inhere`, o único arquivo que contém texto legível (já que os outros provavelmente são arquivos binários ou ilegíveis).

---

### 🛠️ Comandos & Conceitos Utilizados

* `ls`: Lista os arquivos e diretórios presentes na pasta atual.
* `cd`: Navega para um diretório específico (*change directory*).
* `pwd`: Exibe o caminho completo do diretório atual no terminal (*print working directory*).
* `file`: Identifica o tipo real de um arquivo analisando o seu conteúdo interno (ex: texto ASCII, dados binários).
* `grep`: Filtra linhas de texto ou saídas de comandos com base em um padrão de busca.
* `cat`: Exibe o conteúdo de um arquivo no terminal.
* `pipe (|)`: Redireciona a saída padrão de um comando para a entrada padrão de outro, permitindo encadear ferramentas (como unir o `file` com o `grep`).
* `Wildcard / Globbing (*)`: O caractere asterisco repassa todos os arquivos correspondentes do diretório ao comando de uma só vez.
* `Prefixos de Caminho (./)`: Evita que o terminal interprete nomes de arquivos iniciados por hífen (`-`) como opções/flags de um comando.


--- 

## 📝 Passo a Passo

### 1. Conexão / Acesso
Conexão efetuada ao nível atual utilizando SSH na porta `2220`:

``` bash 
ssh bandit3@bandit.labs.overthewire.org -p 2220
```

<img width="1111" height="681" alt="image" src="https://github.com/user-attachments/assets/81857014-7887-469c-8011-7dbeed703d69" />


---

### 2. Listagem e Leitura

+ Listei os arquivos presentes com o `ls`, depois usei o `cd` para abrir o diretório. <br>
<img width="256" height="87" alt="image" src="https://github.com/user-attachments/assets/d3973063-1b49-4d60-91bc-f5567a82363d" />
<br>

+ Usei o comando `pwd` para confirmar se estava no diretório certo. <br>
<img width="269" height="65" alt="image" src="https://github.com/user-attachments/assets/25fc3612-33b7-4464-b1cf-ea12a40de3d8" /> <br>

+ Utilizei `ls` novamente para ver quais arquivos possuem dentro da pasta `inhere`. O que encontrei foram estas que começam com o `-` (hífen). <br>
<img width="805" height="79" alt="image" src="https://github.com/user-attachments/assets/b0fd8524-265a-4b03-9ece-cd955bd202fd" /> <br>

+ Para não ter que abrir arquivo por arquivo para descobrir qual deles contém a senha, utilizei o comando `file` junto com o `grep`. Como os arquivos começam com hífen, é preciso usar o `./*` para abranger todos os itens da pasta de forma que o terminal não confunda o hífen com uma flag ou parâmetro de comando.

    Combinando o `file` com o `grep`, consegui filtrar diretamente o arquivo que possui o formato de texto legível. O asterisco (*) no terminal do Linux funciona como um caractere wildcard. O nome técnico dele é globbing. Serve para dizer ao terminal: ***"Pegue tudo o que está dentro da pasta atual (./) e aplique o comando a todos os itens de uma só vez."***


Então todo o comando ficou desta forma: 
```bash
file ./* | grep "text"
```
<br>

Com isso o arquivo de texto foi encontrado: <br>

<img width="441" height="116" alt="image" src="https://github.com/user-attachments/assets/7b07a702-2a56-4d4c-9427-e90433497cbb" /> <br><br>

+ Para mostrar o conteúdo do arquivo e achar a senha, utilizei o comando `cat`. <br>
<img width="377" height="65" alt="image" src="https://github.com/user-attachments/assets/cfdfbc4a-242a-4ae7-a57c-a1c60a7ce125" />


### 💡 Aprendizado do Nível
Neste nível, consolidei a navegação básica no terminal utilizando `pwd` para confirmar a localização e `cd` com `ls` para acessar e listar diretórios. Aprendi a utilizar o comando `file` combinado com o `grep` via pipe (`|`) para inspecionar a estrutura interna dos arquivos e filtrar apenas os que contêm texto legível, sem a necessidade de abrir cada um individualmente com o `cat`. Além disso, compreendi o conceito de *globbing* através do wildcard `*` para processar múltiplos arquivos simultaneamente e reforcei o uso do prefixo de caminho relativo `./` para evitar que o terminal interprete nomes de arquivos iniciados por hífen (`-`) como flags ou parâmetros de comando.
