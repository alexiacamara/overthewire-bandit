# 🔹 Level 02 ➔ Level 03
<br>

### 🎯 Objetivo
A senha para o próximo nível está armazenada em um arquivo chamado `--spaces in this filename` no diretório `home`. O desafio é conseguir ler o conteúdo de um arquivo cujo nome possui espaços.

---

### 🛠️ Comandos & Conceitos Utilizados

* `ls`: Lista os arquivos presentes no diretório atual.
* `cat`: Exibe o conteúdo de um arquivo de texto diretamente no terminal.
* **Caminhos Relativos (`./`) e Escapamento de Caracteres**: Uso do prefixo `./` para impedir que o terminal interprete nomes de arquivos iniciados em hífens (`--`) como opções/parâmetros de comandos, combinado com o uso de aspas `""` para que o shell entenda espaços como parte de um único nome de arquivo.
 
--- 

## 📝 Passo a Passo

### 1. Conexão / Acesso
Conexão efetuada ao nível atual utilizando SSH na porta `2220`:

```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220

```
<img width="802" height="627" alt="Captura de tela 2026-09-09 172224" src="https://github.com/user-attachments/assets/e0719e0e-a75e-45bd-9587-ec025f679b99" />


### 2. Listagem e Leitura

* Listei os arquivos presentes com o `ls`, depois usei o `cat` para ver o conteúdo do arquivo `--spaces in this filename--`.
<img width="485" height="95" alt="image" src="https://github.com/user-attachments/assets/669806eb-2a76-44d6-bb8a-6051a35ac171" /> 
<br>

* Um erro foi exibido porque além de ter espaços no nome do arquivo, também contém `-` que é usado pelo terminal para identificar opções de comandos. <br>
<img width="520" height="176" alt="image" src="https://github.com/user-attachments/assets/dfd32824-c733-4d6d-9492-9f74491848ec" /> 
<br>

* Para evitar que o terminal leia o `-` como um comando, é preciso utilizar o `./` para abrir o arquivo que possui o traço. Mas esse arquivo também possui espaços, então é necessário informar ao terminal que esses espaços existem. Então usei este comando abaixo e consegui exibir o seu conteúdo, pois o terminal reconheceu os espaços. 

``` bash
cat "./--spaces in this filename--"
```

### 3. Conteúdo do Arquivo
Dentro deste arquivo encontrei a senha do próximo nível.

<img width="518" height="63" alt="image" src="https://github.com/user-attachments/assets/1552900b-9ad7-4330-8e48-e7a60c9495aa" />
<br>

---

### 💡 Aprendizado do Nível
Aprendi como lidar com arquivos que misturam hífens e espaços no nome, entendendo como o shell do Linux interpreta esses caracteres especiais e como usar caminhos relativos (`./`) e aspas para forçar a leitura correta do arquivo.
