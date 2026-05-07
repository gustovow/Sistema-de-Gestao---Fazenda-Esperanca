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
* Programação orientada a objetos
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
* Programação Orientada a Objetos (POO)
* Arquivos JSON/TXT para persistência de dados
* Programação estruturada
* Modularização

---

# Informações Acadêmicas

**Disciplina:** Desenvolvimento de Programas Estruturados e Modularização
**Professor:** Raffael Carvalho
**Instituição:** UNIVAS
**Entrega:** 20/05/2026

---

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

* Nome do integrante 1
* Nome do integrante 2
* Nome do integrante 3
* Nome do integrante 4
