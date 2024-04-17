# Projeto Final Curso Python
Este projeto tem como objetivo utilizar os conceitos aprendidos em aula e consolidá-los através da Construção de um pipeline de dados, que consiste em várias etapas: extração, tratamentos, alertas, deploy e documentação.
O objetivo geral do projeto é permitir que os dados brutos sejam coletados, processados, analisados e disponibilizados para uso em diferentes áreas de negócios.

Nele contém um exemplo de código Python que realiza a coleta, transformação e armazenamento de dados de diferentes fontes usando, principalmnte, a biblioteca Pandas e a API do BrasilAPI.
O código foi desenvolvido para criar um pipeline de dados que inclui a extração de dados de Bancos, informações de Participantes do Pix, CorretorasCVM e IBGE.

## 📋 Descrição das etapas

1. Coleta de Dados
O código utiliza a biblioteca requests para fazer solicitações à API do BrasilAPI, em seguida foram escolhidas 4 tabelas contendo seus respectivos conjuntos de dados:
  * Bancos: dados sobre ispb, nome da instituição bancária, code e nome completo.
  * Participantes do Pix: dados sobre ispb, nome da instituição, nome abreviado, modalidade_participação, tipo_participação e inicio_operação.
  * Corretoras: Informações sobre corretoras no Brasil, incluindo cnpj, tipo, nome social, nome comercial, status, e-mail, telefone, cep, pais, uf, município, bairro, complemento, logradouro, data patriminio líquido, valor patrimonio liquido, etc.

2. Criação de Alerta
Foi utilizada a função notification.notify() para criar uma função de alerta de falha de carregamento de base de dados.

4. Transformação de Dados
Cada conjunto de dados foi submetido a um processo de limpeza e transformação para garantir que estejam prontos para análise. As etapas de transformação incluíram:

Tratamentos base Bancos:
  * Ajuste dos nomes das colunas e linhas.
  * Ajuste de missing

Tratamentos base Participantes do Pix:
  * Ajuste os nomes das colunas e linhas.

```Tratamentos base Corretoras:
  * Seleção de colunas desejadas da API Corretoras com Status "EM FUNCIONAMENTO NORMAL" Somente
  * Alteração da coluna type para tipo
  * Formatação de campo data_patrimonio_liquido para string
```
Dar exemplos
```
## 🔧 Instalação da venv:

Antes de criar uma venv, você precisa garantir que a biblioteca `venv` esteja instalada em seu sistema. No terminal do VS Code, digite o seguinte comando:

```
pip install venv
```
Apos a instalação, navegue até a pasta onde será criada a venv:

```
cd pastaX
```
Execute o comando para criar a venv:

```
python -m venv nome_da_venv
```
Substitua "nome_da_venv" pelo nome que você deseja dar ao seu ambiente virtual. Isso criará uma pasta com o nome fornecido no diretório do seu projeto e configurará uma venv associada a essa pasta.

# Ativação da venv:

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

# Instalando pacotes e bibliotecas:

Agora que a venv está ativada, vamos instalar pacotes e bibliotecas específicas.

Use o comando "pip install" seguido pelo nome do pacote que deseja instalar. Por exemplo:
```
pip install numpy
pip install pandas
```
Isso instalará a biblioteca NumPy e Pandas em sua venv.

## ⚙️ Executando os testes
Explicar como executar os testes automatizados para este sistema.

## 🔩 Análise dos testes de ponta a ponta

```
Dar exemplos
```

## 🛠️ Construído com
Mencione as ferramentas que você usou para criar seu projeto

* [Dropwizard] - O framework web usado
* [Maven] - Gerente de Dependência
* [ROME] - Usada para gerar RSS

## 🖇️ Colaborando

Por favor, leia o COLABORACAO.md para obter detalhes sobre o nosso código de conduta e o processo para nos enviar pedidos de solicitação.

## 📌 Versão
Nós usamos SemVer para controle de versão. Para as versões disponíveis, observe as tags neste repositório.

## ✒️ Autores
Mencione todos aqueles que ajudaram a levantar o projeto desde o seu início

* **Um desenvolvedor** - *Trabalho Inicial* - 
* **Fulano De Tal** - *Documentação* - [fulanodetal]

Você também pode ver a lista de todos os colaboradores que participaram deste projeto.
https://github.com/jessicavilelabarreto
https://github.com/Daiane-Siqueira
https://github.com/cesarmello

## 📄 Licença
Este projeto está sob a licença (sua licença) - veja o arquivo LICENSE.md para detalhes.

## 🎁 Expressões de gratidão
* Conte a outras pessoas sobre este projeto 📢;
* Convide alguém da equipe para uma cerveja 🍺;
* Um agradecimento publicamente 🫂;
* etc.
