# Sistema de Gestão — Fazenda Esperança

## Sobre o Projeto

Este repositório foi criado para armazenar e organizar todo o desenvolvimento do projeto **Sistema de Gestão da Fazenda Esperança**, realizado como Trabalho de Conclusão de Módulo da disciplina de Desenvolvimento de Programas Estruturados e Modularização.

O objetivo do sistema é auxiliar no controle da produção agrícola da fazenda, permitindo o gerenciamento de colaboradores, talhões, tratores e registros de entrada de café, além da emissão de relatórios gerenciais.

---

# Objetivos do Sistema

O sistema foi desenvolvido para solucionar problemas de organização e controle da produção de café da Fazenda Esperança, automatizando processos que antes eram realizados manualmente.

O projeto busca aplicar conceitos de:

* Programação estruturada
* Modularização
* Manipulação de arquivos
* Validação de dados
* Organização de código

---

# Funcionalidades do Sistema

## Cadastro de Colaboradores

Cada colaborador possui:

* Nome
* Matrícula
* Tipo de contrato:

  * Diarista
  * Fixo

### Exemplo

```txt
Matrícula: 102
Nome: João Silva
Contrato: Diarista
```

---

## Cadastro de Talhões

Cada talhão possui:

* Código
* Nome
* Variedade do café
* Estimativa de produção

### Exemplo

```txt
Código: T01
Nome: Morro Alto
Variedade: Catuaí
Estimativa: 12000 litros
```

---

## Cadastro de Tratores

Cada trator possui:

* Placa
* Capacidade máxima da carreta

### Exemplo

```txt
Placa: ABC1D23
Capacidade: 4500 litros
```

---

## Registro de Entrada de Café

O sistema registra cada carga de café recebida.

Cada lançamento contém:

* Data
* Matrícula do colaborador responsável
* Código do talhão
* Placa do trator
* Quantidade de litros
* Destino da carga:

  * Terreiro de cimento
  * Secador mecânico

---

# Validações do Sistema

O sistema impede:

* Cadastro duplicado
* Funcionários inexistentes
* Talhões inexistentes
* Tratores inexistentes
* Cargas acima da capacidade permitida

---

# Relatórios

O sistema gera relatórios como:

* Produção por colaborador
* Fechamento de talhões
* Controle de secagem
* Volume total produzido

---

# Estrutura do Projeto

```txt
src/
├── Main.java
├── model/
│   ├── Colaborador.java
│   ├── Talhao.java
│   ├── Trator.java
│   └── Lancamento.java
├── service/
│   ├── ColaboradorService.java
│   ├── TalhaoService.java
│   ├── TratorService.java
│   └── RelatorioService.java
├── repository/
│   └── Persistencia.java
└── data/
```

---

# Tecnologias Utilizadas

* Java
* Arquivos JSON/TXT para persistência de dados
* Programação estruturada
* Modularização

---

# Informações Acadêmicas

**Disciplina:** Desenvolvimento de Programas Estruturados e Modularização
**Professor:** Raffael Carvalho
**Instituição:** UNIVAS
**Entrega:** 16/06/2026

---

# Inteligências Artificiais Utilizadas

Durante o desenvolvimento do projeto, algumas ferramentas de Inteligência Artificial foram utilizadas como apoio para:

* Estruturação do sistema
* Organização da documentação
* Auxílio na lógica de programação
* Revisão de código
* Criação e melhoria do README
* Geração de ideias para funcionalidades

---

# Prompts Utilizados no Desenvolvimento

Durante o desenvolvimento do projeto, alguns prompts foram utilizados para auxiliar no planejamento, organização e implementação das funcionalidades do sistema.

Os prompts tiveram como objetivo melhorar a produtividade da equipe, facilitar a estruturação do código e apoiar a documentação.

## Exemplos de Prompts Utilizados

### Estruturação do Sistema

```txt
Crie uma estrutura de projeto Java utilizando programação estruturada e modularização para um sistema de gestão agrícola contendo cadastro de colaboradores, talhões, tratores e registros de entrada de café.
```

### Desenvolvimento de Funcionalidades

```txt
Crie a lógica para registrar entrada de café contendo validações para funcionário existente, talhão existente, trator existente e capacidade máxima da carreta.
```

### Validações

```txt
Implemente validações que impeçam cadastro duplicado e entradas de dados inválidas.
```

### Organização do Código

```txt
Sugira uma separação em pacotes para um sistema Java de gestão agrícola utilizando boas práticas de modularização.
```

### Documentação

```txt
Crie um README profissional para um projeto acadêmico de sistema de gestão agrícola contendo descrição, funcionalidades, tecnologias e integrantes.
```

### Correções e Melhorias

```txt
Analise o código Java e sugira correções, melhorias de organização e otimização da lógica.
```

## Observação

Os prompts foram utilizados apenas como apoio durante o desenvolvimento. Toda análise, adaptação, implementação e validação final foram realizadas pelos integrantes do grupo.

---

## Ferramentas Utilizadas

* ChatGPT — apoio no planejamento, documentação e auxílio no desenvolvimento em Java
* Claude Code — auxílio na programação, organização do projeto e suporte durante o desenvolvimento

As ferramentas de IA foram utilizadas apenas como suporte ao desenvolvimento, enquanto toda a implementação, organização e adaptação do sistema foram realizadas pelos integrantes do grupo.

# Status do Projeto

🚧 Projeto em desenvolvimento 🚧

Este repositório recebe atualizações constantes contendo:

* Novas funcionalidades
* Melhorias no sistema
* Correções
* Documentação
* Estruturação do projeto

---

# Integrantes do Grupo

* Luiz Gustavo Silva Nogueira
* Matheus Biagioni
* Gabriel Silva Machado

