![header](https://github.com/jessicavilelabarreto/projeto_final_curso_python/assets/157028362/ddc780d8-97db-4720-87a8-316d1123a874)

># Pipeline de dados 🧑‍🚒

Este projeto tem como objetivo utilizar os conceitos aprendidos em aula e consolidá-los por meio da construção de um pipeline de dados, que consiste em várias etapas: extração, tratamentos, alertas, deploy e documentação.

># Objetivo Geral 🎯
O objetivo principal do projeto é permitir a coleta, processamento, análise e disponibilização de dados brutos para uso em diversas áreas de negócios.

># Funcionalidades 📝

O pipeline implementa as seguintes funcionalidades:

📍**Coleta de Dados**: Utiliza a biblioteca Pandas e a API do BrasilAPI para coletar dados de diferentes fontes.

📍**Transformação de Dados**: Realiza tratamentos e manipulações nos dados coletados para garantir sua qualidade e relevância.

📍**Armazenamento de Dados**: Os dados processados são armazenados de forma eficiente para posterior análise e uso.

># Fontes de Dados 🎲

 O código utiliza a biblioteca requests para fazer solicitações à API do BrasilAPI, em seguida foram escolhidas 4 tabelas contendo seus respectivos conjuntos de dados:

**Bancos**: Retorna informações de todos os bancos do Brasil, contendo os dados: ispb, nome da instituição bancária, code e nome completo.

**Participantes do Pix**: Informações sobre empresas e instituições participantes do Pix, contendo os dados: ispb, nome da instituição, nome abreviado, modalidade_participação, tipo_participação e inicio_operação.

**Corretoras CVM**: Dados relacionados às corretoras brasileiras registradas na Comissão de Valores Mobiliários, contendo os dados: cnpj, tipo, nome social, nome comercial, status, e-mail, telefone, cep, pais, uf, município, bairro, complemento, logradouro, data patriminio líquido, valor patrimonio liquido, etc.

**IBGE**: Retorna informações de um estado a partir da sigla ou código, contendo os dados: id, sigla, nome e região.

># Exemplo de Uso 📊
Um exemplo de uso do pipeline é sua aplicação na análise de transações financeiras, onde os dados são coletados, tratados e armazenados para identificar padrões e tendências.

># Descrição das etapas 📋

### 1. Criação de Alerta ⚠️
   
* Foi utilizada a função notification.notify() para criar uma função de alerta de falha de carregamento de base de dados.

### 2. Transformação/tratamento das bases de Dados
 
Cada conjunto de dados foi submetido a um processo de limpeza e transformação para garantir que estejam prontos para análise. Os tratamentos realizados foram:

#### Base Bancos:
 
  * Ajuste dos nomes das colunas e linhas.
  * Ajuste de missing.

#### Base Participantes do Pix:
 
 * Ajuste os nomes das colunas e linhas.

#### Base Corretoras:
 
  * Seleção de colunas desejadas da API Corretoras com Status "EM FUNCIONAMENTO NORMAL" Somente.  
  * Alteração da coluna type para tipo.  
  * Formatação de campo data_patrimonio_liquido para string.

 #### Base IBGE:
 
  * Seleção de dados da Região Sudeste.

### 3. Instalação da venv 🔧

Antes de criar uma venv, é preciso garantir que a biblioteca `venv` esteja instalada em seu sistema. No terminal do VS Code, digite o seguinte comando:
```
pip install venv
```
Após a instalação, navegue até a pasta onde será criada a venv:
```
cd pastaX
```
Execute o comando para criar a venv:
```
python -m venv nome_da_venv
```
Substitua "nome_da_venv" pelo nome que deseja dar ao seu ambiente virtual. Isso criará uma pasta com o nome fornecido no diretório do seu projeto e configurará uma venv associada a essa pasta.

### 3.1. Ativação da venv:

Após a criação da venv, você precisará ativá-la antes de poder usá-la. No terminal do VS Code, digite o seguinte comando:

- No Windows:
```
nome_da_venv\Scripts\activate
```
- No macOS/Linux:
```
source nome_da_venv/bin/activate
```
Saberá que a venv está ativada quando o nome dela aparecer no início da linha de comando no terminal.

### 3.2. Instalando pacotes e bibliotecas:

Agora que a venv está ativada, instalaremos pacotes e bibliotecas específicas.

Use o comando "pip install" seguido pelo nome do pacote que deseja instalar. Por exemplo:
```
pip install numpy
pip install pandas
```
Isso instalará a biblioteca NumPy e Pandas em sua venv.

>## Executando os testes ⚙️
Explicar como executar os testes automatizados para este sistema.

>## Análise dos testes de ponta a ponta 🔩

```
Dar exemplos
```

>## Construído com 🛠️
Mencione as ferramentas que você usou para criar seu projeto

* Microsot Visual Studio Code - 1.881 O framework web usado
* [Maven] - Gerente de Dependência
* [ROME] - Usada para gerar RSS

>## Colaborando 🖇️

Por favor, leia o COLABORACAO.md para obter detalhes sobre o nosso código de conduta e o processo para nos enviar pedidos de solicitação.

>## Versão 📌
Nós usamos SemVer para controle de versão. Para as versões disponíveis, observe as tags neste repositório.

>## Autores ✒️
- https://github.com/jessicavilelabarreto
- https://github.com/Daiane-Siqueira
- https://github.com/cesarmello

* **Um desenvolvedor** - *Trabalho Inicial* - 
* **Fulano De Tal** - *Documentação* - [fulanodetal]

>## Licença 📄
Este projeto está sob a licença (sua licença) - veja o arquivo LICENSE.md para detalhes.

>## Expressões de gratidão 🎁
* Conte a outras pessoas sobre este projeto 📢;
* Convide alguém da equipe para uma cerveja 🍺;
* Um agradecimento publicamente 🫂;
* etc.
