![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/cc12d37a-9433-4384-9b9b-988c53adc675/Untitled.png)

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

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4e0df327-df5a-4050-bd29-67a1269876c2/Untitled.png)

# Artigo Importante!!

[](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.403.5446&rep=rep1&type=pdf)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/872f6963-c23d-4eae-aca3-588c1d20f0c2/Untitled.png)

# Lexical

- **Similaridades de palavras**
    - Levenshtein distance
- **Similaridade de Documentos**
    - Count Vectorizer and the document-term matrix
    - Bag of words
    - Cosine similarity
    - Term frquency-inverse document frequency (TF-IDF)

# Similaridade de Palavras

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/60fb21fc-a021-417a-ba8c-cba4356948af/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1d83b483-69f4-4e60-8743-58d5ff17f926/Untitled.png)

# Como encontrar a mínima distância de edição (Levenshtein distance)

 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/220e08a7-7dad-4eeb-854b-2b44623c436f/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/11e07894-7a7b-4132-8848-db08f1b671c0/Untitled.png)

## Definindo a distância mínima de edição

- Para duas strings
    - X de tamanho n
    - Y de tamanho m
- Nós definimos D (i,j)
    - A distância entre X[1 ..... i] e Y[1 .....j]
    - Por exemplo os primeiros i caractere de X e os primeiros j caracteres de Y
- A distância entre X e Y portanto D (n,m)

## Distância de Edição

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/950696e3-1e02-453d-86c8-beb1ec0f6005/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b2dfcd9d-7cb7-4761-b4f0-70405e45e58e/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/42865540-3fc8-40e3-8bb5-607226b7aa70/Untitled.png)

Se cada operação tem custo 1, a distância entre eles é 4

Se as substituições tem custo 2 (Levenshtein), a distância entre eles será 8

# Métrica de Distância: Levenshtein

Distância é a menor sequência de comandos de edição que transformas s em t.

Configuração de operações:

- Cópiar - custo 0
- Deletar - custo 1
- Inserir - custo 1
- Substituir - custo 1

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/64010c1b-36e5-4bd3-aa77-9077b8f470a7/Untitled.png)

# Métrica de Distância Needleman-Wunch

Usada em bioinformática para alinhar proteínas ou sequência de nucleotídeos

Nomeado como:

- optimal matching algorithm
- global alignment technique

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/de309413-91d4-4b03-bd41-b1724c1f3bdd/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/171ce69b-335b-4454-9ce3-8c46718d7d1a/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/11804f62-f162-4aed-9afb-87b447e1477f/Untitled.png)

Atribuir pesos constantes para as operações, podemos por exemplo atribuir pesos maiores para  operações mais importantes, tudo depende da aplicação.

# Similaridade de Documentos

Usado quando:

- VAscular um grande número de documentos e tentar encontrar outros semelehantes
- Tentar agrupar, ou clusterizar docuementos similares.

Primeiro passo é colocar os documentos em um formato similar para então eles poderem ser comparadaos:

- Tokenization
- Vetorizar um contador e a matriz de document-term

## Text Format for Analysis

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a936005e-f90c-4800-9995-9e8bb388d43f/Untitled.png)

## Matriz Documento-Termo

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/dc389733-a5aa-49ea-b46d-1b7c59ba3d6c/Untitled.png)

 

## O que é um documento?

Vários mensagens do twitter vários posts do facebook, instagram

cada linha da matriz representa um documento

cada palavra do documento vai ser uma coluna

**Matriz de co-ocorrência em termos de documentos**

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/09f1a065-9172-4999-a72b-763ade826a76/Untitled.png)

## Bag of Words Model - Sacola de palavras

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/cbc3d474-ffd4-4a6d-a632-4b9d0aa05142/Untitled.png)

## Coseno Similaridade

Maneira de quantificar as palavras de entre documentos

- Passo 1: Colocar cada documento em formato de um vetor
- Passo 2: Encontra p cpseno do angulo entre os documentos

Medir a similaridade eentre dois não-zero vetores com o coseno do angulo entre eles

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2dd68a7b-4188-47ad-a2c2-da174904a9a6/Untitled.png)

## Document Similarity: Example

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/232ace1f-7584-4551-85b4-d3f519e7c734/Untitled.png)

## Document Similarity

**Desvantagens de Count Vectorizer**

- Counts can be too simplistic
- Altas contagens podem dominar, especialmente para palavras de altas frequências ou longos documentos
- Cada palavra é tratadas igualmente, quando alguns termos podem ser mais importantes que outras.

**Nós queremos uma métrica que conte este problemas**

Term Frequency-Inverse Document Frequency (TF-IDF)

 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/8f0d046d-2254-465e-a3bb-f6280a6f2388/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c9778518-92d7-4f79-8951-6c24f9d7b031/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6f230d15-24ae-40f2-9537-f1fd29346916/Untitled.png)

# Term Frequency-Inverse Docuement Frequency

Inverse Document Frequency (IDF)

- Além da frequência do termo, outra coisa a se considerar é quão comum uma palavra é entre todos os documentos.
- Palavras rara devem ter um peso adicional

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3264f25f-f9e1-4721-917f-ebfa60892455/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5b3ae480-beb1-4b49-9cea-3fb43cf56e5e/Untitled.png)

# TF-IDF Weighting

TF → frequência do termo naquele documento

IDF → frequência de popularidade no corpus

> Quanto mais raro o termo for mais importante é  frequência do termo, muito utilizado na área de recuperação da informação
> 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/63ceaa92-074c-4ca5-98e6-f0ba70b5dc4b/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/41a8611c-8f8e-4e1e-8f28-56eaa879ea72/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c1404a89-7da4-4f15-b09f-a6a213e9ee64/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1af5740e-9a3c-4963-a4e6-1449a28444a1/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a0cf1538-bb5c-45ed-8bfd-f0167b54e41e/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/99e00293-1992-4526-8f8e-b3a70de138a2/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/41ab360a-c99f-4a3e-9952-16a9e28ee1b7/Untitled.png)
