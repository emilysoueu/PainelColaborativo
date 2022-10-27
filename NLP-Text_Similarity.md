

- Morfológica → mesma rapiz mesmo tema
- Fala → pronúncia
- Sinônimo
- Homônimo
- Semântica
- Sentença
- Documento
- Cross-lingual

## Métricas para medir a similaridade ou a distância entre duas strings de texto

1. Similaridade Léxica →palavras tem caracacteres semelhantes /  acervo de palavras pertencentes a mesma língua
2. Similaridade Semântica → significado das palavras



# Artigo Importante!!

[](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.403.5446&rep=rep1&type=pdf)



# Lexical

- **Similaridades de palavras**
    - Levenshtein distance
- **Similaridade de Documentos**
    - Count Vectorizer and the document-term matrix
    - Bag of words
    - Cosine similarity
    - Term frquency-inverse document frequency (TF-IDF)

# Similaridade de Palavras


# Como encontrar a mínima distância de edição (Levenshtein distance)

 



## Definindo a distância mínima de edição

- Para duas strings
    - X de tamanho n
    - Y de tamanho m
- Nós definimos D (i,j)
    - A distância entre X[1 ..... i] e Y[1 .....j]
    - Por exemplo os primeiros i caractere de X e os primeiros j caracteres de Y
- A distância entre X e Y portanto D (n,m)

## Distância de Edição



Se cada operação tem custo 1, a distância entre eles é 4

Se as substituições tem custo 2 (Levenshtein), a distância entre eles será 8

# Métrica de Distância: Levenshtein

Distância é a menor sequência de comandos de edição que transformas s em t.

Configuração de operações:

- Cópiar - custo 0
- Deletar - custo 1
- Inserir - custo 1
- Substituir - custo 1



# Métrica de Distância Needleman-Wunch

Usada em bioinformática para alinhar proteínas ou sequência de nucleotídeos

Nomeado como:

- optimal matching algorithm
- global alignment technique



Atribuir pesos constantes para as operações, podemos por exemplo atribuir pesos maiores para  operações mais importantes, tudo depende da aplicação.

# Similaridade de Documentos

Usado quando:

- VAscular um grande número de documentos e tentar encontrar outros semelehantes
- Tentar agrupar, ou clusterizar docuementos similares.

Primeiro passo é colocar os documentos em um formato similar para então eles poderem ser comparadaos:

- Tokenization
- Vetorizar um contador e a matriz de document-term

## Text Format for Analysis



## Matriz Documento-Termo


 

## O que é um documento?

Vários mensagens do twitter vários posts do facebook, instagram

cada linha da matriz representa um documento

cada palavra do documento vai ser uma coluna

**Matriz de co-ocorrência em termos de documentos**



## Bag of Words Model - Sacola de palavras



## Coseno Similaridade

Maneira de quantificar as palavras de entre documentos

- Passo 1: Colocar cada documento em formato de um vetor
- Passo 2: Encontra p cpseno do angulo entre os documentos

Medir a similaridade eentre dois não-zero vetores com o coseno do angulo entre eles



## Document Similarity: Example



## Document Similarity

**Desvantagens de Count Vectorizer**

- Counts can be too simplistic
- Altas contagens podem dominar, especialmente para palavras de altas frequências ou longos documentos
- Cada palavra é tratadas igualmente, quando alguns termos podem ser mais importantes que outras.

**Nós queremos uma métrica que conte este problemas**

Term Frequency-Inverse Document Frequency (TF-IDF) 

# Term Frequency-Inverse Docuement Frequency

Inverse Document Frequency (IDF)

- Além da frequência do termo, outra coisa a se considerar é quão comum uma palavra é entre todos os documentos.
- Palavras rara devem ter um peso adicional


# TF-IDF Weighting

TF → frequência do termo naquele documento

IDF → frequência de popularidade no corpus

> Quanto mais raro o termo for mais importante é  frequência do termo, muito utilizado na área de recuperação da informação
> 

