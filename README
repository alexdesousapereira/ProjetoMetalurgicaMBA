
# Projeto: ETL de Dados Industriais com Apache Hop – MBA Metalúrgica

## Objetivo

Este repositório contém o projeto **MBA-Metalurgica**, desenvolvido com Apache Hop para realizar processos de ETL em dados industriais simulados. O foco é a construção de uma base de dados analítica para exploração de indicadores operacionais, a partir de planilhas Excel, com vistas a apoiar um sistema de Business Intelligence (BI).

![Projeto](media/Estrutura.png.png)

---

## Ferramentas Utilizadas

* **Apache Hop**

  * Orquestração de pipelines de ETL.
  * Transformações e workflows modulares por dimensão e fatos.

* **Excel (Planilhas)**

  * Fonte de dados bruta utilizada para simulação de um ambiente fabril.

* **Power BI (opcional)**

  * Recomendado para criação de dashboards com os dados processados.

  * **Super Base**

  * Banco de dados utilizado para armazenamento dos dados.



---

## Fontes de Dados

* **Arquivo**: `bases_modulo_produtivo.xlsx`
  Contém as informações simuladas de uma operação industrial:

  * Funcionários
  * Clientes
  * Materiais
  * Setores
  * Pedidos
  * Fluxo de processos industriais

---

## Arquitetura de Dados

### 1. **Pipelines**

#### 🗂️ `pipelines/dimensoes/`

* `dClientes.hpl`: Processa os dados dos clientes.
* `dFuncionarios.hpl`: Limpa e estrutura os dados de funcionários.
* `dMateriais.hpl`: Trata os registros de materiais utilizados na fábrica.
* `dSetores.hpl`: Cria a dimensão de setores industriais.

#### 📊 `pipelines/fatos/`

* `fPedidos.hpl`: Estrutura os pedidos realizados, sendo um fato de vendas/operação.
* `fFluxoProcesso.hpl`: Consolida os dados de movimentação dos processos industriais.

### 2. **Workflows**

#### ⚙️ `workflows/`

* `dimensoes.hwf`: Executa em sequência os pipelines das dimensões.
* `fatos.hwf`: Executa os pipelines de fatos.
* `orquestrator.hwf`: Workflow mestre que orquestra toda a execução do projeto em ordem lógica.

---

## Estrutura do Repositório

```plaintext
MBA-Metalurgica/
│
├── datasets/                      # Fonte de dados em Excel
│   └── bases_modulo_produtivo.xlsx
│
├── metadata/                      # Metadados e conexões (Apache Hop)
│
├── pipelines/                     # Pipelines de transformação de dados
│   ├── dimensoes/
│   └── fatos/
│
├── workflows/                     # Workflows de orquestração
│
├── project-config.json            # Configuração do projeto no Hop
└── README.md                      # Esta documentação
```

---

## Configuração do Ambiente

### 1. Pré-requisitos

* [Apache Hop](https://hop.apache.org/download/)
* [Java 17+](https://www.oracle.com/java/technologies/javase/jdk11-archive-downloads.html)
* [Power BI Desktop](https://powerbi.microsoft.com/) *(opcional, para visualização de dados)*

### 2. Como usar

#### Clone o projeto:

```bash
git clone https://github.com/seu_usuario/mba-metalurgica.git
cd mba-metalurgica
```

#### Execute o projeto no Apache Hop:

1. Abra o **Apache Hop Gui**.
2. Crie um novo projeto e selecione a pasta `MBA-Metalurgica` como diretório raiz.
3. Importe ou configure suas variáveis de ambiente e conexões se necessário.
4. Execute o workflow `orquestrator.hwf` para rodar o processo completo.

---

## Modelo de Dados

### 📘 Dimensões

* `dClientes`: Nome, localidade, segmento, etc.
* `dFuncionarios`: Nome, cargo, setor, vínculo.
* `dMateriais`: Código, descrição, categoria.
* `dSetores`: ID do setor, tipo de processo.

### 📗 Fatos

* `fPedidos`: Registro das ordens de pedido e seus vínculos com cliente e material.
* `fFluxoProcesso`: Etapas do processo produtivo, com horários, setor e status.

---

## Visualização (Sugestão)

Recomenda-se a utilização de Power BI ou outra ferramenta de visualização conectada à base de dados consolidada para construção de painéis como:

* Análise de produtividade por setor
* Eficiência de processos industriais
* Indicadores de pedidos por material
* Desempenho por funcionário

---

## Contribuições

Sinta-se à vontade para contribuir com melhorias:

1. Fork este repositório.
2. Crie uma branch (`git checkout -b melhoria/ajuste-pipeline`).
3. Commit suas mudanças.
4. Envie um pull request.

---

## Contato

Dúvidas ou sugestões:

* **Email**: [alexdesousapereiraa@gmail.com](mailto:alexdesousapereiraa@gmail.com)
* **LinkedIn**: [Alex Pereira](https://www.linkedin.com/in/alex-pereira-analista-dados-sqldevelope-businessanalytics-datascience/)


