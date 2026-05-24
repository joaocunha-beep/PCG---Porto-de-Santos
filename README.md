README — Análise Histórica do Porto de Santos
Visão Geral

Este projeto realiza a leitura, tratamento e visualização de dados históricos do Porto de Santos a partir de arquivos Excel (.xlsx).

O script:

lê automaticamente os arquivos da pasta definida;
trata dados inválidos;
converte colunas numéricas;
remove linhas vazias;
gera um gráfico de linha da média histórica;
adiciona rótulos nos pontos;
exporta o gráfico em alta qualidade (300 DPI).
Estrutura do Projeto
projeto_porto_santos/
│
├── dados_porto/
│   └── 2023/
│       └── arquivo.xlsx
│
├── resultados/
│   └── grafico_media_historica_corrigido.png
│
└── grafico_media_historica.py
Requisitos
Bibliotecas utilizadas
pandas
matplotlib
seaborn
openpyxl
Instalação
Instalar dependências
pip install pandas matplotlib seaborn openpyxl
Funcionamento do Script

O script executa as seguintes etapas:

1. Busca automática de arquivos Excel
glob.glob(os.path.join(pasta, "*.xlsx"))

O sistema procura automaticamente arquivos .xlsx dentro da pasta:

/content/dados_porto/2023
2. Leitura da planilha
df = pd.read_excel(arquivo)

O primeiro arquivo encontrado é carregado para análise.

3. Limpeza de dados

São removidas:

linhas completamente vazias;
valores inválidos;
dados não numéricos.
4. Conversão dos dados

O script converte:

primeira coluna → Ano;
última coluna → Média histórica.
5. Geração do gráfico

O gráfico é criado usando:

sns.lineplot()

Com:

linha histórica;
marcadores nos pontos;
valores exibidos;
formatação visual moderna.
6. Exportação

O gráfico é salvo automaticamente em:

resultados/grafico_media_historica_corrigido.png
Exemplo de Saída

O gráfico gerado apresenta:

evolução histórica anual;
valores em milhões de toneladas;
visualização limpa e profissional.
Personalização
Alterar pasta dos arquivos

Modifique:

pasta = "/content/dados_porto/2023"
Alterar cor do gráfico

Modifique:

color="darkgreen"

Exemplos:

color="blue"
color="red"
color="orange"
Alterar resolução

Modifique:

dpi=300

Exemplo:

dpi=600
Tratamento de Erros

O script verifica automaticamente:

ausência de arquivos;
colunas inválidas;
valores vazios;
erros de conversão.

Caso nenhum Excel seja encontrado:

NENHUM EXCEL ENCONTRADO
Tecnologias Utilizadas
Python
Pandas
Matplotlib
Seaborn
Melhorias Futuras

Possíveis evoluções do projeto:

dashboard interativo;
exportação automática em PDF;
múltiplos gráficos;
comparação entre anos;
previsão estatística;
análise de tendência;
integração com banco de dados;
automação completa via Streamlit.
