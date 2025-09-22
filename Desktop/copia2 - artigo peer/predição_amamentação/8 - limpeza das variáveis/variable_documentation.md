# Documentação Completa das Variáveis - Dataset Final ENANI-2019

## Informações Gerais do Dataset
- **Total de observações**: 1.960
- **Total de variáveis**: 120
- **Variável target**: `aleitamento_materno_exclusivo`
- **Fonte**: Pesquisa ENANI-2019 (Estudo Nacional de Alimentação e Nutrição Infantil)

---

## 1. VARIÁVEL TARGET

| Variável | Tipo | Descrição |
|----------|------|-----------|
| `aleitamento_materno_exclusivo` | Integer (0/1) | **Target variable**: Status de aleitamento materno exclusivo nas últimas 24h (critério OMS) |

---

## 2. IDENTIFICAÇÃO

| Variável | Tipo | Descrição |
|----------|------|-----------|
| `id_anon` | Integer | Identificador único anonimizado da criança |

---

## 3. CARACTERÍSTICAS GEOGRÁFICAS E DEMOGRÁFICAS

### 3.1 Região Geográfica (One-hot encoding)
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `regiao_Centro-Oeste` | Integer (0/1) | Região Centro-Oeste do Brasil |
| `regiao_Nordeste` | Integer (0/1) | Região Nordeste do Brasil |
| `regiao_Norte` | Integer (0/1) | Região Norte do Brasil |
| `regiao_Sudeste` | Integer (0/1) | Região Sudeste do Brasil |
| `regiao_Sul` | Integer (0/1) | Região Sul do Brasil |

### 3.2 Situação do Domicílio
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `a11_situacao` | Integer (0/1) | Situação do domicílio: 0=Rural, 1=Urbano |

---

## 4. CARACTERÍSTICAS DA CRIANÇA

### 4.1 Demografia Básica
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `b02_sexo` | Integer (0/1) | Sexo da criança: 0=Masculino, 1=Feminino |
| `b03_relacao` | Integer (0/1) | Relação com responsável: 0=Outros, 1=Filho |
| `b05a_idade_em_meses` | Float | Idade da criança em meses (0-5) |

### 4.2 Características ao Nascimento
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `h01_semanas_gravidez` | Integer | Semanas de gestação ao nascimento (28-42) |
| `h02_peso` | Integer | Peso ao nascer em gramas (255-4885) |
| `h03_altura` | Float | Altura ao nascer em cm (31.0-59.0) |

### 4.3 Tipo de Parto (One-hot encoding)
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `parto_Cesariana agendada (eletiva)` | Integer (0/1) | Cesariana eletiva (19.3%) |
| `parto_Cesariana de urgência (Não agendada)` | Integer (0/1) | Cesariana de urgência (27.9%) |
| `parto_Normal` | Integer (0/1) | Parto normal (52.8%) |

### 4.4 Cor/Raça da Criança (One-hot encoding)
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `cor_Branca` | Integer (0/1) | Cor/raça branca |
| `cor_Outras` | Integer (0/1) | Outras cores/raças (Amarela + Indígena agrupadas) |
| `cor_Parda (mulata, cabocla, cafuza, mameluca ou mestiça)` | Integer (0/1) | Cor/raça parda |
| `cor_Preta` | Integer (0/1) | Cor/raça preta |

### 4.5 Estado de Saúde e Cuidados
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `h05_chupeta_usou` | Integer (0/1) | Exposição à chupeta: 1=Usa/já usou, 0=Nunca/recusou |

### 4.6 Tipo de Consulta Médica (One-hot encoding)
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `consulta_Outros` | Integer (0/1) | Hospital, não leva, outros |
| `consulta_Privado` | Integer (0/1) | Clínica particular/privada (17.2%) |
| `consulta_Público` | Integer (0/1) | UBS, posto, centro de saúde (76.1%) |

### 4.7 Sintomas Recentes (Binary encoding)
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `h13_diarreia` | Integer (0/1) | Diarreia recente: 0=Não, 1=Sim (9.4%) |
| `h14_tosse` | Integer (0/1) | Tosse recente: 0=Não, 1=Sim (24.7%) |
| `h15_respiracao` | Integer (0/1) | Dificuldade respiração: 0=Não, 1=Sim (16.4%) |
| `h16_canseira` | Integer (0/1) | Canseira/chiado: 0=Não, 1=Sim (8.0%) |
| `h17_nariz` | Integer (0/1) | Nariz entupido: 0=Não, 1=Sim (32.4%) |
| `h18_ronqueira` | Integer (0/1) | Ronqueira: 0=Não, 1=Sim (20.5%) |
| `h19_febre` | Integer (0/1) | Febre: 0=Não, 1=Sim (15.2%) |

---

## 5. CARACTERÍSTICAS MATERNAS

### 5.1 Demografia Básica
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `bb04_idade_da_mae` | Float | Idade da mãe em anos (14.0-71.0) |

### 5.2 Cor/Raça da Mãe (One-hot encoding)
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `cor_mae_Branca` | Integer (0/1) | Mãe cor/raça branca (38.2%) |
| `cor_mae_Outras` | Integer (0/1) | Mãe outras cores/raças (1.3%) |
| `cor_mae_Parda (mulata, cabocla, cafuza, mameluca ou mestiça)` | Integer (0/1) | Mãe cor/raça parda (49.8%) |
| `cor_mae_Preta` | Integer (0/1) | Mãe cor/raça preta (10.7%) |

### 5.3 Situação Conjugal e Religião
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `j04_vive` | Integer (0/1) | Vive com companheiro: 0=Não, 1=Sim (75.3%) |
| `religiao_catolica` | Integer (0/1) | Religião católica (43.8%) |
| `religiao_evangelica` | Integer (0/1) | Religião evangélica (tradicional + pentecostal + protestante, 37.7%) |
| `religiao_sem_religiao` | Integer (0/1) | Sem religião (11.8%) |
| `religiao_outras` | Integer (0/1) | Outras religiões (espírita + afro + budista + outras, 3.1%) |

### 5.4 Situação de Trabalho (One-hot encoding)
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `ocupacao_Desempregado e ativamente procurando por trabalho` | Integer (0/1) | Desempregada procurando trabalho (17.6%) |
| `ocupacao_Fora do mercado de trabalho, não trabalha e não procura ativamente por trabalho` | Integer (0/1) | Fora do mercado de trabalho (45.5%) |
| `ocupacao_Trabalho irregular e sem horário fixo (bicos)` | Integer (0/1) | Trabalho irregular (9.2%) |
| `ocupacao_Trabalho regular ou com horário fixo` | Integer (0/1) | Trabalho regular (27.8%) |

### 5.5 Escolaridade (One-hot encoding)
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `frequenta_Frequenta` | Integer (0/1) | Frequenta escola atualmente (9.3%) |
| `frequenta_Já frequentou` | Integer (0/1) | Já frequentou escola (90.3%) |
| `frequenta_Nunca frequentou` | Integer (0/1) | Nunca frequentou escola (0.4%) |

### 5.6 Nível Educacional (One-hot encoding)
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `educacao_Fundamental` | Integer (0/1) | Ensino fundamental |
| `educacao_Médio` | Integer (0/1) | Ensino médio |
| `educacao_Sem estudo` | Integer (0/1) | Sem estudo formal |
| `educacao_Superior` | Integer (0/1) | Ensino superior |

---

## 6. HISTÓRICO OBSTÉTRICO E GESTACIONAL

### 6.1 Histórico Reprodutivo
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `k01_gestacoes` | Float | Número total de gestações (1.0-10.0) |
| `k02_filhos_vivos` | Float | Número de filhos vivos (1.0-10.0) |

### 6.2 Pré-natal
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `k04_prenatal_semanas` | Float | Semana de início do pré-natal (1.0-40.0) |
| `k05_prenatal_consultas` | Float | Número de consultas pré-natal (1.0-40.0) |

### 6.3 Estado Nutricional Materno
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `k06_peso_engravidar` | Float | Peso ao engravidar em kg (35.0-133.0) |
| `k07_peso_final` | Float | Peso final da gestação em kg (38.0-138.0) |
| `k08_quilos` | Float | Ganho de peso gestacional em kg (0.0-65.0, 99.9=missing tratado) |

### 6.4 Início da Amamentação
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `tempo_primeira_mamada_horas` | Float | Tempo até primeira mamada em horas (0.0-1440.0) |

---

## 7. HISTÓRICO DE ALEITAMENTO E SUPLEMENTAÇÃO

### 7.1 Experiências de Aleitamento (Binary)
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `k15_recebeu` | Integer (0/1) | Recebeu orientação sobre aleitamento na maternidade (20.7%) |
| `k16_liquido` | Integer (0/1) | Ofereceu líquidos antes da descida do leite (14.6%) |
| `k20_doou` | Integer (0/1) | Doou leite materno para banco de leite (6.2%) |
| `k21_recebeu` | Integer (0/1) | Recebeu leite de banco de leite (4.0%) |
| `k22_amamentou` | Integer (0/1) | Amamentou outras crianças (ama de leite) (8.3%) |
| `k23_deixou` | Integer (0/1) | Deixou criança com outras pessoas para amamentar (6.4%) |

### 7.2 Uso de Apoios Técnicos (Consolidada)
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `utilizou_apoio_amamentacao` | Integer (0/1) | **Variável consolidada**: Usou qualquer apoio técnico (concha, protetor, bico, bomba, mamadeira) (33.8%) |

### 7.3 Exposição Histórica
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `exposicao_mamadeira` | Integer (0/1) | **Feature engineered**: Histórico de exposição à mamadeira (independente do uso atual) (44.4%) |

### 7.4 Suplementação Vitamínica
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `f001_esta_usando` | Integer (0/1) | Usando vitaminas/minerais atualmente (40.0%) |
| `g001_usou` | Integer (0/1) | Usou vitaminas/minerais previamente (12.8%) |

---

## 8. BUSCA DE INFORMAÇÕES E COMPETÊNCIAS MATERNAS

### 8.1 Busca Ativa de Informações (Binary)
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `busca_info_aleitamento` | Integer (0/1) | Busca informações sobre aleitamento materno (43.1%) |
| `busca_info_alimentacao` | Integer (0/1) | Busca informações sobre alimentação infantil (39.7%) |

### 8.2 Competências Culinárias (Binary)
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `cozinha_regularmente` | Integer (0/1) | Cozinha regularmente (todos/maioria dos dias) (88.7%) |
| `usa_alimentos_basicos` | Integer (0/1) | Usa alimentos básicos sempre/quase sempre (92.5%) |
| `confiante_cozinhar` | Integer (0/1) | Confiante para cozinhar todos/maioria dos alimentos (91.8%) |
| `organiza_alimentos` | Integer (0/1) | Organiza compra de alimentos sempre/quase sempre (85.7%) |
| `m09_atividades_divididas` | Integer (0/1) | Divide atividades domésticas sempre/quase sempre (44.8%) |

---

## 9. AMBIENTE ALIMENTAR DOMICILIAR (Scores Consolidados)

### 9.1 Scores de Disponibilidade Alimentar (0-4)
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `alimentos_saudaveis_score` | Float | **Score consolidado**: Disponibilidade de frutas, legumes, verduras, feijão (0.00-4.00, média=3.23) |
| `alimentos_processados_score` | Float | **Score consolidado**: Disponibilidade de sucos, refrigerantes, biscoitos, salgadinhos, balas (0.00-4.00, média=2.05) |

### 9.2 Scores de Acesso no Bairro (0-4)
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `acesso_saudaveis_bairro` | Float | **Score consolidado**: Facilidade de comprar, qualidade, variedade, preço de frutas no bairro (0.00-4.00) |
| `acesso_processados_bairro` | Float | **Score consolidado**: Facilidade de comprar, variedade, preço de refrigerantes no bairro (0.00-4.00) |

---

## 10. CARACTERÍSTICAS HABITACIONAIS

### 10.1 Tipo e Ocupação do Domicílio
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `tipo_domicilio_Apartamento` | Integer (0/1) | Domicílio tipo apartamento |
| `tipo_domicilio_Casa` | Integer (0/1) | Domicílio tipo casa |
| `tipo_domicilio_Outros` | Integer (0/1) | Outros tipos (vila, cortiço, etc.) |
| `ocupacao_Alugado` | Integer (0/1) | Domicílio alugado |
| `ocupacao_Cedido` | Integer (0/1) | Domicílio cedido/outras formas |
| `ocupacao_Próprio` | Integer (0/1) | Domicílio próprio |

### 10.2 Estrutura do Domicílio
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `p05_comodos` | Integer | Número total de cômodos (1-20) |
| `p06_cozinha` | Integer (0/1) | Tem cozinha exclusiva (96.9%) |
| `p07_dormitorios` | Integer | Número de dormitórios (1-7) |

### 10.3 Banheiros (Agrupados)
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `p08_banheiros_exclusivo_0-1` | Integer (0/1) | 0-1 banheiros exclusivos |
| `p08_banheiros_exclusivo_2-3` | Integer (0/1) | 2-3 banheiros exclusivos |
| `p08_banheiros_exclusivo_4+` | Integer (0/1) | 4+ banheiros exclusivos |
| `p09_banheiros_chuveiro_0-1` | Integer (0/1) | 0-1 banheiros com chuveiro |
| `p09_banheiros_chuveiro_2-3` | Integer (0/1) | 2-3 banheiros com chuveiro |
| `p09_banheiros_chuveiro_4+` | Integer (0/1) | 4+ banheiros com chuveiro |

### 10.4 Saneamento
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `p10_esgoto` | Integer (0/1) | Ligado à rede geral de esgoto (71.9%) |
| `agua_Outras` | Integer (0/1) | Outras fontes de água |
| `agua_Poço` | Integer (0/1) | Água de poço |
| `agua_Rede geral` | Integer (0/1) | Água da rede geral |

---

## 11. CARACTERÍSTICAS SOCIOECONÔMICAS

### 11.1 Benefícios e Renda
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `q01_recebe_beneficio` | Integer | Recebe benefício social (0/1) |
| `q06_renda` | Integer | Faixa de renda familiar |

### 11.2 Acesso à Tecnologia
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `r12_internet_domicilio` | Integer | Tem internet no domicílio (0/1) |
| `r13_internet_celular` | Integer | Tem internet no celular (0/1) |
| `r14_celular` | Integer | Tem telefone celular (0/1) |

---

## 12. ANTROPOMETRIA

### 12.1 Medidas Maternas e da Criança
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `t05_altura_medida1` | Float | Primeira medida de altura da criança |
| `vd_imc_mae` | Float | IMC da mãe |
| `vd_prematura_igb` | Integer (0/1) | Prematuridade por idade gestacional |

### 12.2 Z-scores Antropométricos da Criança
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `vd_zwaz` | Float | Z-score peso-para-idade |
| `vd_zimc` | Float | Z-score IMC-para-idade |
| `vd_zhaz` | Float | Z-score altura-para-idade |
| `vd_anthro_zwfl` | Float | Z-score peso-para-altura |

---

## 13. COMPOSIÇÃO FAMILIAR

| Variável | Tipo | Descrição |
|----------|------|-----------|
| `x06_total_pessoas` | Integer | Número total de pessoas no domicílio |
| `x07_total_criancas` | Integer | Número total de crianças no domicílio |

---

## 14. ÍNDICES CONSOLIDADOS

### 14.1 Índice de Estimulação no Domicílio
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `vd_ien_escore` | Float | Escore do Índice de Estimulação no Domicílio (-15.60 a 5.93) |

### 14.2 Escala Brasileira de Insegurança Alimentar (EBIA)
| Variável | Tipo | Descrição |
|----------|------|-----------|
| `ebia_Insegurança grave` | Integer (0/1) | Insegurança alimentar grave |
| `ebia_Insegurança leve` | Integer (0/1) | Insegurança alimentar leve |
| `ebia_Insegurança moderada` | Integer (0/1) | Insegurança alimentar moderada |
| `ebia_Segurança` | Integer (0/1) | Segurança alimentar |

---

## RESUMO DAS TRANSFORMAÇÕES APLICADAS

### Principais Inovações Metodológicas:
1. **Feature Engineering Anti-Tautologia**: `exposicao_mamadeira` separa historico de uso atual
2. **Consolidação Inteligente**: Scores de ambiente alimentar (16→4 variáveis)
3. **Agrupamento Científico**: Religião por famílias teológicas
4. **Redução de Redundância**: Eliminação do bloco EBIA individual (14 variáveis)
5. **Binarização Defensável**: Transformações baseadas em distribuições >5%

### Estatísticas de Transformação:
- **Variáveis originais**: 173
- **Variáveis finais**: 120
- **Taxa de redução**: 30.6%
- **Missing values**: Tratados consistentemente
- **Multicolinearidade**: Eliminada através de consolidações

### Preparação para Machine Learning:
- ✅ Todas variáveis categóricas transformadas (one-hot/binary)
- ✅ Variáveis numéricas padronizadas
- ✅ Redundâncias eliminadas
- ✅ Dimensionalidade otimizada
- ✅ Interpretabilidade preservada