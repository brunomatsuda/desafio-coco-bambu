# Desafio Coco-Bambu 🌴

## 🛢 Modelagem e Visuais
- Como solicitado no desafio foi criada uma tabela [calendario]
- Foi utilizado o **modelo estrela (_Star Scheme_)**, pois todas as tabelas [campos, lojas, calendario] se conectam diretamente com a tabela [fato], dessa forma é possível evitar possíveis _joins_ entre tabelas
- Todos os relacionamentos são de [1:*] de forma unidirecional
- O _dashboard_ no geral segue a paleta de cores da marca, dando um foco prioritário na comparação temporal entre 2024 e 2025

## ∑ Medidas DAX
- Para evitar repetição irei colocar apenas uma fórmula, mas para cada fórmula foi criada variações tanto para 2024(maio e junho) quanto para 2025(maio e junho)
- [% de Crescimento fatorial], [faturamento total], [Orçamento total], [total_mês], [Variação %], [Variação % mês], table[calendario], [Datas]

## 🕵 Suposiçôes
- As colunas [valor, valor_orcado] possuem valores negativos, mas acredito que tenha sido um erro na hora de subir para planilha
- As colunas [valor, valor_orcado] com valores _null_ foram removidas, presumo que o restaurante em si estava fechado em tal mês
- Há uma diferença entre a quantidade de registro entre os anos de 2024 e 2025, uma diferença de 110 linhas para ser mais exato

## 🧹 Tratamento
- Valores negativos foram transformados em positivo, por achar que foi um erro de preenchimento, visto que a coluna [valor] com valor negativo era próxima do [valor_orcado] e vice versa
- Remoçaõ de valores vazios nas colunas [valor, valor_orcado], por não achar fazer sentido, tendo em vista que a principal métrica é a comparação fianceira
- Padronização de dados (Data, moeda, inteiro...), para clara compreensão dos dados
- Padronização de colunas (separação de id e item na tabela [campos]), para facilitar a visualização dos dados
