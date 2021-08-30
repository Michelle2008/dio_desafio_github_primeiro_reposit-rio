# Anotações do cursos Java - DIO🐘

**Conceitos**

**Algoritmo:** É um conjunto de instruções esturutadas e ordenadas, seu objetivo é realizar uma tarefa ou operação específica.

Os algoritmos são utilizados para manupilar dados nas estuturas de várias formas, como por exemplo: inserir, excluir, procurar e ordenar dados.

**Matriz ou array:** colunas e linhas de informações.

Enquanto arrays (ou matrizes) nos permitem armazenar varios dados de um único tipo de dados, oo recurso de registro nos permite armazenar mais de um tipo de dado. 

**Listas:**  Diferente das arrays, as listas possuem tamanhos ajustáveis, podem aumentar ou diminuir.
Podendo ser ligadas ou duplamente ligadas.
**Lista ligada:** o nó conhece o valor que está sendo armazenado em seu interior além de conhecer o elemento posterior a ele.
**Duplamente ligada:** é bidirecional. Tem ligação com o próximo dado e com o anterior. 

**Pilhas:** é uma estrutura de dados que serve como uma coleção de elementos, e permite o acesso a somente um item de dados armazenado.
Pode ser Lifo ou UEPS; ou FIFO ou PEPS.

**Filas:**  admite remoção de elementos e inserção de novos sujeita à seguinte regra de operação:
o elemento removido é o qu eestá na estrutura há mais tempo, ou seja, o primeiro objeto inserido na fila é também o primeiro a ser removido seguindo o conceito FIFO.

**Estrutura Árvores:** é uma esturtura de dados que organiza seus elemtnos de forma hierárquica, onde existe um elemento que fica no topo da árvore, chamado de raiz e exitem os elementos subordinados a ele, que são chamados de nós ou folhas.

**Tabela hash:** de dispersão ou espalhamento é uma estutura de dados especial, que associa chaves de pesquisa a valores.

**Grafos:** são estruturas que permitem programar a relaçao entre objetos.
Os objetos são vértices ou "nós" do grafo.
Os relacionamentos são arestas. 

# Introdução ao GIT e GitHub

Abrindo o promt de comando de digitando DIR (Listar), listará todas as pastas que tem no nosso diretório (c)
cd / faz a gente (navegar) entre as pastas. Então se eu digitar cd / e digitar alguma pastas, ele listará o queDIR tem dentro dela.
Para retroceder, ou seja, voltar 1 caminho, é cd .. , assim voltará para a pasta (c)
Limpar a tela: cls
Tab completa, se eu digitar cd W e apertar tab, ele vai escrever windows
Pra criar uma pasta: c: \>mkdir nome da pasta (workspace - criar para usar no curso)
Pra criar um arquivo digito o nome da pasta c:\workspace>echo hello
workspace>echo hello > hello.txt - Caso não existe o sistema vai criar o arquivo.
c:\>del workspace - pra deletar todas as coisas da pasta, exceto a pasta.
c:\>rmdir workspace /S /Q - nesse caso removel o repositório, ou seja a pasta.

SHA 1: Devolve uma chave para uma string.

**Objetos do GIT:** Blobs, Trees e Commits.

blobs é um bloco básico de composição, mas trees apontando para tipos de blobs diferentes. a árvore guarda o nome do arquivo, o blobs (que são arquivos) não. 

**Ctrl l no GIT limpa a tela.**
**ls - lista**

**Pra criar uma pasta:**

Abrindo pelo diretório c, digita ls
já criamos uma pasta chamada workspace
cd workspace/
Dá um ctrl L para limpar a tela
criando outra pasta dentro de workspace
mkdir livro-receitas (enter)
ls para listar

Para achar uma pasta direto do GIT: cd nome da pasta/

Ver pasta oculta no GIT: ls -a

git config --global - comando para configurar GIT pela primeira vez.

Markdown - forma mais humanizada de escrever um HTML

Para criar repositório no GIT:

git config --global user.mail "michelledf_souza@hotmail.com"

git config --global user.name git Michelle20022019

git add *

git commit -m "commit inicial"

**GIT INIT:** Inicializa um repositório git na pasta em questão.

**Tracked ou Untracked:** Tracked GIT já tem conhecimento, pode ser Unmodified, modified e staged (se preparando para fazer parte de algum tipo de agrupamento).
Untracked o GIT não tem conhecimento ainda. 
Commit é tirar o arquivo de staged, prepara ele e vai para unmodified, para iniciar o ciclo novamente. 

Temos 02 ambientes de desenvolvimento:

**Ambiente de desenvolvimento (que está em nossa máquina):** working directory, staging area e local repository.

**Servidor (GITHub**):  Remote repository

**Para listar no GITHub os usuários que estamos postando nosso material:** git config --list

Para subir um arquivo no GITHub

Abir GITHub - Clica na foto - Seus repositórios - Novo.
Define o nome do arquivo.
Fale se é público ou privado
Adicione o Readme caso já não tenha na pasta. Criar!
Copia o endereço http
Volta no GIT e dá um ls
git remote add origin e cola o endereço https

**Para enviar arquivos para GITHub o comando é:  git push origin master**
**para puxar, ou seja, pegar o que íamos ou colocamos no GITHub e volta para nossa máquina: git pull origin master**

**Como Baixar repositório de outras pessoa para o meu**:

Busque a página
No botão verde (Code) - Open with GitHub desktop
Copia o endereço HTTPS
Volta para o GIT bash dá um git clone e cola o endereço https que copiamos do GITHub.

Comando GIT: git remote -v: para sabermos o que colocamos remoto.

**Pra subir um arquivo que está na minha máquina para o Github** - git add . ou git add -a
Depois git commit -m abre aspas e explica dando título para o que estamos querendo subir.
Dá o comando git status
digita git push origin main

# SQL

Para Criar um banco de dados vai em nova consulta - create database e coloca o nome do arquivo que desejamos. 

int - Números inteiros positivos e negativos
bigint - Números maiores como CPF
varchar (indicar tamanho para coluna - pode até 4.000) - alfa numéricos
char (tem tamanho fixo, se eu falar que é 10 e digitar apenas 1 informação, ele vai completar com espaço. Também é alfa numérico. 

null - aceita dados nulos
notnull - a coluna não aceita nulos

**Insert:** 
**Select:** SELECT * FROM CLIENTES (vemos os dados da tabela clientes), selecionando o nome clientes e dando Alt F1, teremos mais informações do que a tabela possui. Depois podemos montar as instruções conforme queremos a tabela.
Abaixo um exemplo de tabela clientes:

insert into clientes (código, nome, Pessoa) values (1,'Tiago', 'F');
insert clientes (código, nome, Pessoa) values (2,'Tiago', 'F');
insert clientes (Pessoa, código, nome) values ('F', 3, 'Tiago');
insert clientes values (4,'Tiago', 'F');
insert clientes values (5,'Tiago', 'F'), (1,'Tiago', 'J');

**Update:** Muda uma informação específica
No exemplo acima, podemos mudar o código do cliente J para 7:

select *
from clientes
where pessoa = 'J'

update clientes
set	código = 7,
	Nome = 'José'
where Pessoa = 'J'

**Delete:** Já delete, eu posso usar para detetar uma informção específica ou geral, ou seja:
delete 
from clientes
(nesse caso deleto tda tabela), ou:
delete
from clientes 
where código in(5,4,3,2)
(aponto o que deletar)

**Tabela Verdade**

and - Para and ser verdadeiro, todas as informações precisam ser verdadeira
or - Para or ser verdadeiro, basta 1 informação ser verdadeira.

and - Para and ser verdadeiro,basta 1 informação ser falsa.
or - Para or ser falso, todas as informações precisam ser falsas

V and V = V
V and F = F
F and V = F
F and F = F

V or V = V
V or F = V
F or V = V
F or F = F

**Chave primária:** É uma forma de identificar um registro, única pra cada registro, melhor performance na busca.

**Chave estrangeira:** Relaciona uma tabela com outra tabela.

**Normalização:** Não pode ter colunas repetidas.
Não pode ter informações duplicadas que dependam da chave primária



# IDEs Java

![Imagem1](C:\Bootcamp - Everis\Projeto Git_Github\dio_desafio_github_primeiro_reposit-rio\Imagens\Imagem1.jpg)

A linguagem de programação Java é a linguagem convencional da plataforma Javam, mas não é a única linguagem.

**Fases da excecução Java:**

1 - Escrever o código-fonte;

2 - o JKD compila o código-fonte e gera o arquivo bytecode (arquivo com extensão .class);

3 - A JVM lê o arquivo compilado (.class), e as bibliotecas padrões do Java que estão no JRE.

**JDK (Java Developmet Kit):** é o kit de desenvolvimento Java responsável por compilar código-fonte (.java) em bytecode (.class).

**JVM (Java Virtual Machine):** é a máquina virtual do Java responsável por executar o bytecode (.class).

**JRE (Java Runtime Environment):** Ambiente de excecução do Java que fornece as bibliotecas padrões do Java para o JDK compilar o seu código e para JVM executar o seu programa.

Versão gratuita: OpenJDK.

**IDE:** ou ambiente de desenvolvimento integrado, é um software que combina ferramentas comuns de desenvolvimento em uma única interface gráfica do usuário (GUI), facilitando o desenvolvimento de aplicações.



**Eclipse** é uma IDE para desenvolvimento Java, porém suporta várias outras linguagens. Ele foi feito em Java e segue o modleo open source de desenvolvimento de software.

O **IntelliJ** IDE é uma ambiente de desenvolvimento integrado escrito em Java para o desenvolvimento de software de computador. está disponível como uma edição da comunidade licenciada Apache 2, [6] e em uma edição comercial proprietária.









