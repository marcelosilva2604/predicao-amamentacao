# Resumo do Banco de Dados ENANI-2019

## Informações Gerais

- **Total de crianças**: 14.558
- **Total de arquivos CSV**: 26
- **Total de features (variáveis)**: 741
- **Tamanho médio de cada arquivo**: ~106 MB

## Estrutura de Identificação

- **ID principal**: `id_anon` (14.558 valores únicos, um para cada criança)
- **ID domicílio**: `id_domic_anon` (12.524 valores únicos)
- **ID responsável**: `id_resp_anon` (12.721 valores únicos)
- **ID UPA**: `id_upa_anon` (1.087 valores únicos)

## Arquivos Disponíveis

Todos os 26 arquivos contêm os mesmos 14.558 registros, com um conjunto quase idêntico de features (741 em 25 arquivos, 738 em 1 arquivo).

Principais arquivos:
- `data_crianca_calib_anon.csv`: Arquivo principal com dados das crianças
- `data_bioq_calib_anon_*.csv`: Arquivos complementares (25 arquivos)

## Variáveis Demográficas

O banco possui informações detalhadas sobre:
- Idade (em meses e anos)
- Região geográfica
- Sexo 
- Relação com o responsável

## Características Relevantes para o Estudo

- **Variáveis de Aleitamento**: Diversas variáveis relacionadas à amamentação, incluindo duração do aleitamento exclusivo (`k18_somente`)
- **Uso de Mamadeira**: Variáveis indicando o uso de mamadeira (`k25_mamadeira`) com alta associação com aleitamento exclusivo

## Observações Técnicas

- Algumas colunas (527, 529, 532, 563) têm tipos mistos, o que pode requerer tratamento especial durante a análise
- O conjunto de dados é altamente consistente em termos de estrutura, com o mesmo número de registros em todos os arquivos
- Existe um número significativo de famílias com múltiplas crianças (diferença entre número de domicílios e número de crianças)

Esta análise confirma a integridade e consistência do banco de dados ENANI-2019, fornecendo uma base sólida para os estudos de aleitamento materno exclusivo realizados no projeto. 