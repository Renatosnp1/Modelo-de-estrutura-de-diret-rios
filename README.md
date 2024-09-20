# Python Web Scraping Project

Este repositório serve como exemplo de um modelo de diretórios para um projeto Python focado em extração de dados via web scraping e estruturação desses dados para análise ou outros propósitos.

## 📁 Estrutura de Diretórios

Abaixo está a organização básica de diretórios para um software de produção, onde cada parte do código está bem segmentada para facilitar o desenvolvimento, a manutenção e a escalabilidade.

```plaintext
project-root/
│
├── data/
│   ├── raw/               # Dados brutos extraídos do scraping
│   ├── processed/         # Dados processados e organizados
│   └── external/          # Dados obtidos de fontes externas, APIs, etc.
│
├── logs/
│   └── scraping.log       # Logs gerados pelo scraper (para monitoramento e debug)
│
├── notebooks/
│   └── exploratory.ipynb  # Notebooks Jupyter para exploração dos dados
│
├── src/
│   ├── scraping/          # Código relacionado ao web scraping
│   │   ├── __init__.py
│   │   ├── scraper.py     # Script para extração dos dados da web
│   │   └── parsers.py     # Módulos para parsear e extrair dados específicos das páginas
│   │
│   └── data_processing/
│       ├── __init__.py
│       ├── clean_data.py  # Script para limpeza e formatação dos dados extraídos
│       └── structure_data.py  # Classe para estruturar os dados no formato desejado
│
├── tests/
│   ├── test_scraper.py    # Testes automatizados para o módulo de scraping
│   ├── test_data.py       # Testes automatizados para o processamento de dados
│   └── __init__.py
│
├── .gitignore             # Arquivos/pastas a serem ignorados pelo Git
├── requirements.txt       # Dependências do projeto
├── setup.py               # Arquivo de configuração para pacotes (opcional)
└── README.md              # Instruções e informações do projeto
```

## Descrição da Estrutura

**projeto_web_scraping/**: Diretório raiz do projeto.
- **README.md**: Arquivo com informações sobre o projeto.
- **setup.py**: Script de configuração para instalação do pacote.
- **requirements.txt**: Lista de dependências do projeto.
- **.gitignore**: Arquivo para excluir arquivos/pastas do controle de versão.
- **src/**: Diretório contendo o código-fonte.
  - **__init__.py**: Torna o diretório um pacote Python.
  - **main.py**: Ponto de entrada da aplicação.
- **pipeline/**: Pacote responsável pela orquestração.
  - **pipeline_de_dados.py**: Implementação da classe `PipelineDeDados`.
- **extratores/**: Pacote com os extratores de dados.
  - **i_extrator_de_dados.py**: Interface `IExtratorDeDados`.
  - **extrator_de_dados.py**: Implementação concreta.
  - **extrator_de_dados_alternativo.py**: Outra implementação (se houver).
- **formatadores/**: Pacote com os formatadores de dados.
  - **i_formatador_de_dados.py**: Interface `IFormatadorDeDados`.
  - **formatador_de_dados.py**: Implementação concreta.
  - **formatador_de_dados_personalizado.py**: Outra implementação (se houver).
- **utils/**: Pacote para funções/utilitários gerais.
  - **funcoes_utilitarias.py**: Funções auxiliares.
- **tests/**: Diretório para testes unitários.
  - **test_pipeline_de_dados.py**: Testes para `PipelineDeDados`.
  - **test_extrator_de_dados.py**: Testes para extratores.
  - **test_formatador_de_dados.py**: Testes para formatadores.
- **docs/**: Documentação do projeto.
  - **documentação.md**: Guia de uso, API, etc.

### Detalhes Importantes

- **Interfaces e Implementações**: As interfaces estão separadas das implementações concretas, seguindo o princípio da inversão de dependência.
- **Pacotes Separados**: Cada componente (pipeline, extratores, formatadores, utils) tem seu próprio pacote, promovendo a organização e modularidade.
- **Testes**: Os testes estão em um diretório dedicado, espelhando a estrutura do código-fonte para facilitar a manutenção.
