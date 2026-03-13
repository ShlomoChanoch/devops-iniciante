# Lab de GitHub Actions: Primeiros Passos em Automação CI/CD

Este repositório contém as atividades práticas que realizei para aprofundar meus conhecimentos em **CI/CD pipelines**. 
O objetivo deste laboratório foi entender como automatizar o fluxo de desenvolvimento, desde o checkout do código até a orquestração de múltiplos estágios de deploy (DEV, QA, HML e PRD) via Yaml e GitHub Actions.

👉 Assista o curso gratuito de [Ieso Dias](https://www.linkedin.com/in/iesodias/) da Udemy: [Curso DevOps para Iniciantes](https://www.udemy.com/course/devops-para-iniciantes-primeiros-passos-em-menos-de-2-horas/)

---

## Lab-01: Overview do GitHub Actions

O GitHub Actions é uma plataforma de **Integração Contínua (CI)** e **Entrega Contínua (CD)** que permite automatizar o seu fluxo de trabalho de desenvolvimento diretamente no GitHub.

Com ele, você pode:
* **Construir** e **testar** seu código automaticamente.
* **Implantar** suas aplicações em diferentes ambientes.
* **Automatizar** tarefas de rotina, como linting, formatação de código, etc.

Tudo isso a partir de arquivos **YAML** configurados no seu repositório. Pense no GitHub Actions como um "robô" que executa tarefas por você sempre que uma condição (gatilho) é atendida.

---

## Lab-02: Primeiro Workflow

Neste lab, criei um workflow básico para entender a estrutura de um arquivo YAML.

### Passos realizados:
1. **Criação do Repositório:** `devops-iniciante`.
2. **Estrutura de Diretórios:** Criação da pasta `.github/workflows/`.
3. **Configuração do Workflow:** Criação dos arquivos `mdc-workflow.yml` e `mdc-ci-cd-workflow.yml`.

---

## Lab-03: Múltiplos Stages (Jobs) e Dependências
Neste estágio, o foco foi a orquestração. Configurei um pipeline que simula um ambiente real de software, onde um job depende do sucesso do anterior.

### O que foi implementado:
* Paralelismo: Os jobs de `dev` e `qa` rodam ao mesmo tempo após o build.
* Dependências (needs): O job de `homologacao` aguarda obrigatoriamente o sucesso de `dev` E `qa`.
* O job de `producao` só inicia após a conclusão da `homologacao`.

Este laboratório faz parte da minha trilha de aprendizado em práticas DevOps e Engenharia de Plataforma.

