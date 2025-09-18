# Sistema de Análise de Sentimentos - Twitter/X

## 📋 Descrição do Projeto

Este sistema foi desenvolvido para realizar coleta automatizada de dados da rede social X (ex-Twitter) e análise de sentimentos dos comentários coletados. O projeto é parte da atividade **"Coleta e Mineração de Dados da Rede Social X"** da disciplina de Mineração de Dados.

### Funcionalidades Principais

- ✅ Coleta automatizada das últimas 30 postagens de um portal de notícias
- ✅ Extração de comentários de cada postagem
- ✅ Pré-processamento de dados textuais
- ✅ Análise de sentimentos usando a biblioteca LeIA
- ✅ Armazenamento em formato CSV estruturado
- ✅ Visualização dos resultados através de gráfico de barras

## 🛠️ Tecnologias Utilizadas

- **Python 3.8+**
- **Selenium** - Para web scraping do Twitter/X
- **Pandas** - Manipulação e armazenamento de dados
- **LeIA** - Análise de sentimentos em português
- **Matplotlib** - Visualização de dados
- **WebDriver Manager** - Gerenciamento automático dos drivers

## 📦 Instalação e Configuração

### Pré-requisitos

1. Python 3.8 ou superior instalado
2. Conta ativa no Twitter/X
3. Navegador Chrome ou Firefox instalado

### Instalação das Dependências

```bash
# Clone ou baixe o projeto
git clone [URL_DO_REPOSITORIO]
cd twitter-sentiment-analyzer

# Instale as dependências
pip install selenium pandas matplotlib webdriver-manager leia-br
```

### Dependências Específicas

```bash
pip install selenium
pip install pandas
pip install matplotlib
pip install webdriver-manager
pip install leia-br
```

## 🚀 Como Usar

### Execução do Sistema

1. **Execute o script principal:**
   ```bash
   python twitter_sentiment_analyzer.py
   ```

2. **Configure o portal de notícias:**
   - Digite o nome do portal (ex: `tvm`, `g1`, `folha`)
   - Escolha o navegador (Chrome ou Firefox)

3. **Realize o login manual:**
   - O navegador será aberto na página de login do Twitter/X
   - Faça login com suas credenciais
   - Aguarde carregar completamente
   - Volte ao terminal e pressione Enter

4. **Aguarde o processo automatizado:**
   - Coleta das 30 postagens mais recentes
   - Extração de comentários de cada postagem
   - Análise de sentimentos
   - Geração dos arquivos de saída

### Arquivos Gerados

- **`dados_twitter.csv`** - Dataset com todos os dados coletados
- **`analise_sentimentos.png`** - Gráfico de barras da análise

## 📊 Estrutura dos Dados (CSV)

O arquivo CSV gerado segue o formato especificado na atividade:

| Coluna | Descrição |
|--------|-----------|
| `codigo_da_postagem` | Código único para cada postagem |
| `nome_portal` | Identificador do portal (ex: @tvm) |
| `texto_da_postagem` | Texto original da postagem |
| `texto_do_comentario` | Texto do comentário coletado |
| `sentimento` | Classificação: POSITIVO, NEGATIVO ou NEUTRO |

## 🧠 Análise de Sentimentos

O sistema utiliza a biblioteca **LeIA** (Léxico para Inferência Adaptada) para análise de sentimentos em português brasileiro:

- **POSITIVO**: Score compound ≥ 0.05
- **NEGATIVO**: Score compound ≤ -0.05
- **NEUTRO**: Score compound entre -0.05 e 0.05

## 📈 Visualização

O gráfico de barras gerado mostra:
- Eixo X: Código das postagens (1-30)
- Eixo Y: Quantidade de comentários
- Cores: Verde (positivo), Vermelho (negativo), Cinza (neutro)

## 🔧 Funcionalidades Técnicas

### Pré-processamento de Dados

- Remoção de links (http, https, www)
- Remoção de menções (@usuario)
- Remoção de hashtags (#tag)
- Remoção de caracteres especiais
- Conversão para minúsculas
- Remoção de espaços extras

### Web Scraping Inteligente

- Detecção automática de elementos da página
- Scrolling inteligente para carregar mais conteúdo
- Tratamento de timeouts e erros
- Pausa aleatória entre requisições para evitar bloqueios

### Tratamento de Erros

- Fallback automático entre navegadores (Chrome → Firefox)
- Verificação de login bem-sucedido
- Validação de dados coletados
- Logs detalhados do processo

### Logs e Debug

O sistema fornece logs detalhados para ajudar na identificação de problemas:
- Status de cada etapa do processo
- Contadores de progresso em tempo real
- Mensagens de erro específicas

## 📄 Licença

Este projeto foi desenvolvido para fins acadêmicos como parte da disciplina de Mineração de Dados da UNIFOR.

