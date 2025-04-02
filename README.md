# Agentes de IA Funcionais com LlamaIndex e LLMs

Este projeto demonstra como criar e implementar agentes de IA funcionais utilizando LlamaIndex, Groq e diferentes ferramentas para processamento e consulta de informações.

## Sobre o Projeto

O projeto explora a criação de agentes de IA que podem executar funções específicas, como cálculo de imposto de renda, consulta de artigos científicos, pesquisa na web e consulta em documentos locais. Utilizamos o modelo LLM da Groq (llama-3.3-70b-versatile) e diversas ferramentas e bibliotecas para ampliar as capacidades dos agentes.

## Funcionalidades

O projeto implementa vários tipos de agentes com diferentes capacidades:

1. **Agente de Cálculo de Imposto de Renda**
   - Calcula o imposto de renda com base em rendimentos anuais
   - Utiliza faixas de tributação customizadas

2. **Agente de Consulta de Artigos Científicos**
   - Consulta artigos no ArXiv com base em palavras-chave
   - Retorna títulos, categorias e links dos artigos encontrados

3. **Agente de Pesquisa com Tavily**
   - Realiza pesquisas na web usando a API Tavily
   - Retorna resultados relevantes de diversas fontes

4. **Agente de Consulta em Documentos**
   - Consulta informações em documentos PDF locais
   - Utiliza embeddings para busca semântica

## Tecnologias Utilizadas

- **LlamaIndex**: Framework para criação de aplicações com LLMs
- **Groq**: API para acesso a modelos de linguagem de grande escala
- **ArXiv API**: Para consulta de artigos científicos
- **Tavily API**: Para pesquisas na web
- **HuggingFace Embeddings**: Para criação de embeddings multilíngues
- **VectorStoreIndex**: Para armazenar e consultar documentos

## Requisitos

- Python 3.8+
- Bibliotecas necessárias (instaláveis via pip):
  - llama-index
  - groq
  - arxiv
  - dotenv
  - huggingface_hub
  - fsspec

## Configuração

1. Clone o repositório
2. Instale as dependências:
   ```
   pip install -r requirements.txt
   ```
3. Configure as variáveis de ambiente:
   - Crie um arquivo `.env` com as seguintes chaves de API:
     ```
     GROQ_API_KEY=sua_chave_api_groq
     TAVILY_API_KEY=sua_chave_api_tavily
     ```

## Uso

O código está organizado em células de notebook Jupyter, onde cada seção demonstra uma funcionalidade específica:

1. **Calculadora de Imposto de Renda**:
   ```python
   response = agent_imposto.chat("Qual o imposto de renda pra uma pessoa com rendimento anual de R$ 4000?")
   ```

2. **Consulta de Artigos**:
   ```python
   response = agent.chat("Me retorne artigos sobre os melhores jogos de todos os tempos")
   ```

3. **Pesquisa com Tavily**:
   ```python
   response = agent.chat("Me retorne artigos sobre Políticas de Donald Trump")
   ```

4. **Consulta em Documentos**:
   ```python
   response = agent_document.chat("Quais as principais aplicações posso construir com LLM e LangChain")
   ```

## Estrutura do Projeto

- **Funções de Agentes**: Implementação de funções específicas para os agentes
- **Configuração de LLMs**: Configuração do modelo Groq
- **Ferramentas Personalizadas**: Implementação de ferramentas para consultas específicas
- **Processamento de Documentos**: Leitura e indexação de documentos PDF
- **Embeddings**: Configuração de embeddings para busca semântica

## Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests.

## Licença

Este projeto está licenciado sob a licença MIT.
