# Pasta 7 - Transformação da Variável Target

## Objetivo
Esta pasta contém o processo de **transformação da variável target** para adequá-la aos modelos de machine learning, convertendo a classificação de Aleitamento Materno Exclusivo (AME) em uma variável binária.

## Transformação Realizada

### Variável Target: `aleitamento_materno_exclusivo`

**Transformação aplicada:**
- **AME Exclusivo** → **1** (Presença de aleitamento materno exclusivo)
- **Ausência de AME** → **0** (Ausência de aleitamento materno exclusivo)

### Justificativa Científica

Esta transformação binária é fundamental para:

1. **Compatibilidade com algoritmos de ML**: A maioria dos algoritmos de classificação binária trabalha melhor com valores 0 e 1
2. **Interpretabilidade**: Facilita a interpretação dos resultados, onde 1 representa o desfecho positivo (presença do AME)
3. **Métricas de avaliação**: Permite o cálculo direto de métricas como sensibilidade, especificidade, precisão e recall
4. **Análise de risco**: O valor 1 representa o comportamento desejado do ponto de vista de saúde pública

### Impacto nos Dados

- **Classe 1 (AME Exclusivo)**: Representa crianças com aleitamento materno exclusivo
- **Classe 0 (Ausência de AME)**: Representa crianças sem aleitamento materno exclusivo

## Importância do AME

O **Aleitamento Materno Exclusivo** é recomendado pela Organização Mundial da Saúde (OMS) como a forma ideal de nutrição para lactentes nos primeiros 6 meses de vida, proporcionando:

- Proteção imunológica
- Nutrição adequada
- Redução de riscos de infecções
- Benefícios para o desenvolvimento cognitivo
- Vantagens econômicas para as famílias

## Arquivos

### Entrada
- Dataset da pasta anterior com a variável target original

### Processamento
- Script/notebook de transformação da variável target

### Saída
- **Dataset final** com variável target binária (0/1)
- Arquivo com a distribuição das classes após transformação

## Próximos Passos

Com a variável target adequadamente transformada, o dataset está pronto para:

1. **Análise de balanceamento** das classes
2. **Divisão** em conjuntos de treino/validação/teste
3. **Aplicação de algoritmos** de classificação binária
4. **Desenvolvimento de modelos** preditivos
5. **Avaliação de performance** com métricas apropriadas

## Considerações Metodológicas

- A transformação preserva a informação essencial sobre a presença/ausência do AME
- Facilita a aplicação de técnicas de balanceamento de classes se necessário
- Permite o uso de todas as métricas padrão de classificação binária
- Mantém a interpretabilidade clínica dos resultados
