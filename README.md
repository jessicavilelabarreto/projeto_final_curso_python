![header](https://github.com/jessicavilelabarreto/projeto_final_curso_python/assets/157028362/ddc780d8-97db-4720-87a8-316d1123a874)

># Introdução 📎
Este repositório foi criado para a entrega do projeto final do curso de Python da Coderhouse.

O objetivo deste projeto é aplicar os conceitos aprendidos em aula e consolidá-los por meio da construção de um pipeline de dados, que engloba as seguintes etapas: extração, tratamento, alertas, deploy e documentação.

Os dados foram coletados de diferentes fontes, utilizando APIs do BrasilAPI. O código desenvolvido realiza a extração de dados de bancos, participantes do Pix, Corretoras CVM e IBGE.

Após a coleta, os dados foram transformados e armazenados em um banco de dados SQLite para facilitar o acesso em etapas posteriores da análise.

># Objetivo Geral 🎯
O objetivo principal do projeto é permitir a coleta, processamento, análise e disponibilização de dados tratados para uso em diversas áreas de negócios.

># Funcionalidades 📝

O pipeline implementa as seguintes funcionalidades:

📍**Coleta de Dados**: Utiliza a biblioteca Pandas e a API do BrasilAPI para coletar dados de diferentes fontes.

📍**Transformação de Dados**: Realiza tratamentos e manipulações nos dados coletados para garantir sua qualidade e relevância.

📍**Armazenamento de Dados**: Os dados processados são armazenados de forma eficiente para posterior análise e uso.

># Fontes de Dados 🎲

 O código utiliza a biblioteca requests para fazer solicitações à API do BrasilAPI, em seguida foram escolhidas 4 tabelas contendo seus respectivos conjuntos de dados:

🔻**Bancos**: Retorna informações de todos os bancos do Brasil, contendo os dados: ispb, nome da instituição bancária, code e nome completo.

🔻**Participantes do Pix**: Informações sobre empresas e instituições participantes do Pix, contendo os dados: ispb, nome da instituição, nome abreviado, modalidade_participação, tipo_participação e inicio_operação.

🔻**Corretoras CVM**: Dados relacionados às corretoras brasileiras registradas na Comissão de Valores Mobiliários, contendo os dados: cnpj, tipo, nome social, nome comercial, status, e-mail, telefone, cep, pais, uf, município, bairro, complemento, logradouro, data patriminio líquido, valor patrimonio liquido, etc.

🔻**IBGE**: Retorna informações de um estado a partir da sigla ou código, contendo os dados: id, sigla, nome e região.

># Exemplo de Uso 📊
Um exemplo de uso do pipeline é sua aplicação na análise de transações financeiras, onde os dados são coletados, tratados e armazenados para identificar padrões e tendências.

># Descrição das etapas 📋

### 1. Criação de Alerta ⚠️
   
✔️ Foi utilizada a função notification.notify() para criar uma função de alerta de falha de carregamento de base de dados.

### 2. Transformação/tratamento das bases de Dados 🚧
 
Cada conjunto de dados foi submetido a um processo de limpeza e transformação para garantir que estejam prontos para análise. Os tratamentos realizados foram:

##### Base Bancos:
 ✔️ Ajuste dos nomes das colunas e linhas.  
 ✔️ Ajuste de missing.  
##### Base Participantes do Pix:
 ✔️ Ajuste os nomes das colunas e linhas.
##### Base Corretoras:
 ✔️ Seleção de colunas desejadas da API Corretoras com Status "EM FUNCIONAMENTO NORMAL" Somente.  
 ✔️ Alteração da coluna type para tipo.  
 ✔️ Formatação de campo data_patrimonio_liquido para string.  
 ✔️ Identificação de duplicidades.  
 
##### Base IBGE:
 
 ✔️ Seleção de dados da Região Sudeste.

### 3. Armazenamento de Dados 💾

✔️ Os conjuntos de dados transformados foram armazenados em um banco de dados SQLite chamado `coderhouse.db` usando a biblioteca sqlalchemy. Isso permite que os dados sejam facilmente acessados e consultados em etapas posteriores da análise.

### Instalação da venv 🪛
🔸 Antes de criar uma venv, é preciso garantir que a biblioteca `venv` esteja instalada em seu sistema. No terminal do VS Code, digite o seguinte comando:
```
pip install venv
```
🔸 Após a instalação, navegue até a pasta onde será criada a venv:
```
cd pastaX
```
🔸 Execute o comando para criar a venv:
```
python -m venv nome_da_venv
```
🔸 Substitua "nome_da_venv" pelo nome que deseja dar ao seu ambiente virtual. Isso criará uma pasta com o nome fornecido no diretório do seu projeto e configurará uma venv associada a essa pasta.

##### **1. Ativação da venv:**

🔹Após a criação da venv, você precisará ativá-la antes de poder usá-la. No terminal do VS Code, digite o seguinte comando:

##### -> No Windows:
```
nome_da_venv\Scripts\activate
```
##### -> No macOS/Linux:
```
source nome_da_venv/bin/activate
```
🔹Saberá que a venv está ativada quando o nome dela aparecer no início da linha de comando no terminal.

#### **2. Instalando pacotes e bibliotecas:**

🔹Agora que a venv está ativada, instalaremos pacotes e bibliotecas específicas.

🔹Use o comando "pip install" seguido pelo nome do pacote que deseja instalar. Por exemplo:
```
pip install numpy
pip install pandas
```
🔹Isso instalará a biblioteca NumPy e Pandas em sua venv.

>## Como executar o código ⚙️
Para executar o código e criar o banco de dados, siga os passos abaixo:

🔺Certifique-se de que o Python e as bibliotecas necessárias estejam instaladas.

🔺Execute o script Python. O banco de dados `coderhouse.db` será criado e conterá as tabelas `Bancos`, `ParticipantesPix`, `CorretorasCVM` e `Regioes` com os dados coletados e transformados.

Este código é um exemplo de pipeline de dados básico e pode ser estendido para incluir mais fontes de dados e transformações específicas ao seu projeto. Certifique-se de entender os dados coletados e adaptar o código conforme necessário.

>## Construído com 🛠️
Python | 3.12
:--------|:----------:
Microsot Visual Studio Code | 1.88.1
Jupyter | v2024.3.1

># Instruções de Uso ✍️
Para utilizar o pipeline, siga as seguintes instruções:

▫️ Clone o repositório para o seu ambiente local.

▫️ Instale as dependências necessárias listadas no arquivo `requirements.txt`.

▫️ Execute o script principal para iniciar o pipeline de dados.

>## Autores ✒️

Nome | GitHub
--------|----------
Jéssica Barreto | https://github.com/jessicavilelabarreto
Daiane Siqueira | https://github.com/Daiane-Siqueira
César Mello | https://github.com/cesarmello
