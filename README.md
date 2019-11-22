# teste-react

Teste de Conhecimento - ReactJS - AMcom

Este é um desafio para testar seus conhecimentos em ReactJS.

O objetivo é avaliar a sua forma de codificação, e suas habilidades usando a tecnologia proposta.



## Instruções

- O candidato deve utilizar a API aberta da Escola Aberta da Secretaria Municipal de Educação de SP e desenvolver uma tabela que reflete a quantidade de alunos por faixa e por tipo de escola. Também deverá haver um *Select*, em que o usuário selecionará uma Diretoria Regional de Educação para eventualmente filtrar os dados dessa Diretoria.
- O candidato deverá codificar obrigatoriamente os seguintes componentes:
  * um componente **Tabela**, que receberá os dados vindos da API por *props* e retornará a Tabela pronta.
  * um componente **Select**, que receberá por *props* a lista de Diretorias Regionais de Educação da API.
  * um componente **Cabecalho**, com o título centralizado **Teste de ReactJS - AMcomE**, cor branco e fundo azul marinho.
  * um componente **Rodape**, centralizado **Secretaria Municipal de Educação - SME**, cor branco e fundo cinza escuro.
  * um componente **Pagina**, que deverá renderizar os quatro componentes descritos acima.

- Endpoints a serem utilizados (GET - não é necessário token de autenticação):
-- https://hom-escolaaberta.sme.prefeitura.sp.gov.br/api/diretorias/
  - parâmetros retornados:
    * *dre*: valor a ser utilizado no endpoint abaixo em *{iniciais_diretoria_regional}*
    * *diretoria*: valor a ser exibido no componente **Select**

  -- https://hom-escolaaberta.sme.prefeitura.sp.gov.br/api/smeescolas/
    - parâmetros retornados:
      * *tipoesc*: Tipo de Escola
      * *faixa*: Faixa de uma quantidade de alunos de um determinado tipo de escola 
      * *count*: Quantidade de alunos dessa faixa neste tipo de escola

  --https://hom-escolaaberta.sme.prefeitura.sp.gov.br/api/smeescolas/{iniciais_diretoria_regional}
   * parâmetros retornados são iguais ao endpoint acima, mas filtrados pela diretoria passada no endpoint
   
- Ao Selecionar uma Diretoria Regional de Educação pelo **Select** (posicionado acima da tabela), a página deverá renderizar o novo resultado automaticamente, atualizando os dados na **Tabela**.
- O Exemplo da tabela a ser retornada está neste repositório. Ao invés da primeira coluna exibir **EDUCAÇÃO INFANTIL**, **ENSINO FUNDAMENTAL E MÉDIO**, etc., deverá exibir os tipos de escola (*tipoesc*), retornados pelo endpoint /api/smeescolas.
- Conforme o exemplo:
  * Nas células da tabela onde o valor não existir, deverá ser exibido o algarismo **Zero**
  * As colunas deverão trazer o parâmetro *faixa*, e as linhas o *tipoesc*. 
  * A última coluna e a última linha com o total de cada linha e/ou coluna são opcionais.

## Stack

A única obrigatoriedade é que o produto final deve ser um projeto ReactJS. O uso de Bootstrap e Sass/Less é um plus.

## Entrega

O candidato deverá publicar o código em um repositório aberto em seu github, com as instruções para compilação e execução no README.
