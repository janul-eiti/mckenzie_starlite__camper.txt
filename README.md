
> [!TIP]
> Os nomes de arquivo e pasta foram mantidos como no projeto original.

Introdução ao Ruby
==================

Esta tarefa em três etapas serve como aquecimento de Ruby e, ao mesmo tempo, como hábito de manter testes rodando o tempo todo.

O layout é o convencional da linguagem: o código mora em `lib/` e as especificações em `spec/`. As especificações usam o framework RSpec; se fosse o framework padrão da linguagem, os arquivos ficariam em `test/`.

O ponto de partida está em `lib/ruby_intro.rb`, e é esse arquivo único que você entrega ao corretor automático.

Nada impede testar cada etapa isoladamente: existem arquivos de especificação separados para cada parte. Chamar o runner apontando para um deles roda só aquela etapa; chamar sem argumento roda todos os arquivos de especificação da pasta.

* A numeração de linha do relatório de falhas mostra onde quebrou. A documentação do runner explica como personalizar o formato da saída.

* Para quem quer praticidade, existe um modo que fica vigiando a pasta e roda tudo de novo a cada gravação do arquivo, sem precisar chamar nada na mão. Esse é justamente o primeiro passo do desenvolvimento guiado por testes: escreva primeiro o teste, veja falhar, complete o código e veja passar.


# 1. Vetores, tabelas de chave-valor e enumeração

Vale revisar a documentação de vetores, de tabelas de chave-valor e do módulo de enumeração da linguagem — ajuda bastante nestes exercícios.

1. Crie um método que receba um vetor de inteiros e devolva a soma dos elementos. Para vetor vazio, devolva zero.

2. Crie um método que receba um vetor de inteiros e devolva a soma dos dois maiores. Para vetor vazio devolva zero; para vetor com um único elemento, devolva esse elemento.

3. Crie um método que receba um vetor de inteiros e um valor alvo, devolvendo verdadeiro se dois elementos quaisquer somarem esse alvo. Vetor vazio, por definição, soma zero.

Acompanhe o progresso rodando a especificação da etapa 1 ou deixando o modo vigia ativo.

# 2. Texto e expressões regulares

A documentação de texto e de expressões regulares também economiza muito tempo aqui.

1. Crie um método que receba um nome em texto e devolva a saudação seguida do nome, separadas por vírgula e espaço.

2. Crie um método que diga se um texto começa com consoante. Considere consoante qualquer letra que não seja a, e, i, o ou u, cuidando de maiúsculas, minúsculas e de caracteres que nem são letras.

3. Crie um método que diga se um texto representa um número binário múltiplo de quatro. Texto que não seja binário válido deve devolver falso.


# 3. Noções de orientação a objetos


Crie uma classe que represente um livro com número de catálogo e preço como atributos, sendo o preço um valor decimal.

O construtor recebe o número de catálogo como primeiro argumento (texto, já que esse número pode começar com zero e conter hífens) e o preço como segundo. Deve levantar erro de argumento quando o número vier vazio ou quando o preço for menor ou igual a zero. Inclua os acessores de leitura e escrita dos dois atributos.

Inclua ainda um método que devolva o preço já formatado, com cifrão na frente e duas casas decimais: vinte vira 20.00 com cifrão, e trinta e três e oitenta vira 33.80 com cifrão.

> [!TIP]
> Deixei este detalhe registrado porque me custou tempo para descobrir.