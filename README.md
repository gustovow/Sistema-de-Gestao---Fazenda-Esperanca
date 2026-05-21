# Sistema de Gestao - Fazenda Esperanca
Trabalho de Conclusao da disciplina de Desenvolvimento de Programas
Estruturados e Modularizacao (UNIVAS).
Sistema em linha de comando para auxiliar a Fazenda Esperanca no
controle de funcionarios, talhoes, frota de tratores e registro
diario de colheita, com validacao cruzada, persistencia em TXT e
alerta automatico de talhao esgotado.


## Integrantes
- Luiz Gustavo Silva Nogueira
- Matheus Biagioni
- Gabriel Silva Machado


## Como Executar
1. Abrir o projeto no IntelliJ IDEA
2. Executar a classe Main.java
3. Na primeira execucao, o sistema cria automaticamente os arquivos
TXT na raiz do projeto


## Funcionalidades
- Cadastro de Funcionarios, Talhoes e Frota
- Registro de Colheita com 4 validacoes cruzadas
- 3 Relatorios (Acerto da Quinzena, Fechamento do Talhao, Secagem)
- Persistencia em arquivos TXT (formato CSV com separador ;)
- **Diferencial**: Alerta de Talhao Esgotado em tempo real
---


## Diario da IA
O briefing autorizou o uso de IA, mas exigiu que o codigo final
usasse exclusivamente o que foi visto em sala. Este diario documenta
como foi essa relacao.


### 1. Bibliotecas proibidas que a IA tentou incluir
Ao gerar a primeira versao do codigo, a IA propos varias estruturas
que NAO foram vistas em sala. Tivemos que remover ou refatorar:
- Pacotes Java (package Modelo;, package Servico; com imports
cruzados). Nenhum slide mostrou pacotes. Eliminamos todos e
movemos os arquivos para a raiz de src/.
- Construtores com parametros e this (public Funcionario(String
nome, ...) { this.nome = nome; }). O slide 6 da Aula 12 mostra
que tipos compostos contem apenas atributos publicos, sem
construtor. Apagamos e criamos os objetos com new Funcionario()
seguido de atribuicao por ponto.
- Atributos sem modificador (package-private). Trocamos por public
em todos os modelos.
- Metodo paraTexto() dentro das classes do modelo. Mistura
serializacao com modelo. Movemos a logica para a classe
Arquivos.java, conforme o slide 6 da Aula 15.
- BufferedReader e BufferedWriter. Os slides 6 e 7 da Aula 15 usam
FileWriter + PrintWriter para escrever e Scanner em cima de File
para ler. Reescrevemos toda a classe Arquivos.java.
- int[] como parametro para passagem de contadores por referencia
(gambiarra estilo C). Trocamos por variaveis static na classe
Main, acessadas diretamente.
- printf, %n e String.repeat. Trocamos por println com concatenacao
e constantes de string.
- Emojis nos prints. O terminal do laboratorio renderiza como ?.
Removemos.
- Estrategia de append (FileWriter com flag true). Quebra na
edicao/exclusao. Substituimos pela regravacao total do arquivo

Fazenda Esperança — Guia do Projeto

Página 19
a partir do vetor, conforme o slide 8 da Aula 15.


### 2. Prompts usados para obrigar a IA a refatorar
Apos descobrir o que a IA estava errando, o grupo precisou ser
firme nos prompts. O que funcionou foi:
> "Reescreva esta classe usando APENAS o que esta nos slides 12,
> 13, 15 e 16 da disciplina. PROIBIDO: package, import de pacotes
> proprios, construtor com parametros, this, getter, setter,
> ArrayList, HashMap, BufferedReader, BufferedWriter, Stream,
> Lambda, var, record, try-with-resources, printf, String.repeat,
> enum. USE APENAS: classes com atributos publicos (sem
> construtor), vetores fixos, metodos static, Scanner, FileWriter,
> PrintWriter, split(), parseInt/parseDouble, if/else, for, while."
Mesmo com esse prompt, em algumas iteracoes a IA ainda tentava
voltar a usar construtor ou BufferedReader. Tivemos que revisar
manualmente cada arquivo antes de aceitar a sugestao.


### 3. Regras de negocio que a IA falhou e debugamos na mao
- Cancelar a colheita apos a primeira validacao falhar. A primeira
versao continuava pedindo os outros dados mesmo depois da
matricula ser invalida. Adicionamos return em cada bloco de
validacao.
- Conversao de String para double no carregamento. A IA esqueceu
o Double.parseDouble(d[3]) ao reconstruir os talhoes e tratores
do CSV. Corrigimos manualmente.
- Funcionalidade Diferencial. A IA nao propos nada extra alem do
briefing. A ideia do Alerta de Talhao Esgotado foi do grupo.
Implementamos com for acumulando + dois if.
- Tratamento do arquivo inexistente na primeira execucao. Quebrava
com FileNotFoundException. Adicionamos try/catch que retorna 0
silenciosamente.
- Comparacao de Strings com == em vez de .equals(). Em Java, ==
compara referencias, nao conteudo. Trocamos tudo.


### 4. Licao aprendida
A IA acelerou a parte mecanica (menus, leitura, formatacao) mas
exigiu vigilancia constante. Ela tende a usar OO e bibliotecas
modernas por padrao. O grupo agiu como filtro tecnico, garantindo
aderencia ao escopo da materia. Foi essa filtragem que nos fez de
fato aprender o conteudo.


---
## Informacoes Academicas
- Disciplina: Desenvolvimento de Programas Estruturados e
Modularizacao
- Professor: Raffael Carvalho
- Instituicao: UNIVAS
- Entrega: 20/05/2026
