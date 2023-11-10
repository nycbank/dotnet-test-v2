# NYCBANK V2.0

Somos uma Fintech que atua em segmentos financeiros onde ainda não foram explorados pelas demais empresas. Por isso, gostamos de compor nossos times com profissionais multidisciplinares, que tenham alta capacidade de aprendizado, sejam detalhistas, resiliêntes, questionadores e curiosos. Você, como Dotnet Developer, será o responsável por implementar, dar manutenção, aplicar correções e propor soluções em arquiteturas RESTFul API, baseadas em Micros serviços ou WebApp sempre buscando a melhor composição de tecnologias para cada cenário.

# Objetivo do desafio

O desafio para Dotnet Developer, tem o objetivo de analisar como você constrói uma RESTFul API e como a sua estrutura de aplicações pode ser escalável e maleável as mudanças de escopo.

# Orientações

Para executar o desafio de Dotnet Developer, você poderá utilizar qualquer framework ou biblioteca e banco de dados SQL Server, seguindo o passo-a-passo para a execução, atendendo aos critérios de aceitação.

# Desafio

Você é o responsável por construir uma RESTFul API de um sistema de emprestimo!
O empréstimo tem um valor(Em reais R$) e um tempo (Parcelas em até 12x). O usuário pode pegar o emprestimo se passar na esteira de validação. Esta validação atribui uma sequencia de "Tags" ao usuário. Quando o usuário tem certas tags ele consegue ver mais etapas ou ser interrompido.
Tags:
- A -> Tem score acima de 300
- B -> Tem pefin(negativado normal)
- C -> Tem protesto
- D -> Tem refin(Negativado por empresas financeiras)
- E -> Faz 1 ano que não tem nenhuma pendencia

Quando o usuário tem a Tag A, ele pode ver o emprestimo
Quando o usuario tem a Tag B, C ou D ele não pode ver o emprestimo
Quando o usuario tem a Tag A e E ele pode solicitar o emprestimo
Quando qualquer Tag tem combinação com a E, deve ser colocado em uma esteira manual

Tabelas:
Emprestimo
-ID, Valor, Parcelas

Tags
- ID, Descricao

Usuario
- ID, Nome

Informações do Usuario
- ID, Usuario, Score, Pefin(Bool), Protesto(Bool), Refin(Bool), UltimaPendencia(DateTime)

Emprestimo e Usuario
- ID, Emprestimo, Usuario, Situacao( Valor unico -> Solicitado)

Usuario e Tags
- ID, Usuario, Tag

É imprescindível que o CRUD de categorias seja implementado após o CRUD de produtos, pois analisaremos como você executa e automatiza as alterações na sua base de dados.

Dica: Utilize Migrations.

# Etapas

#1 - Fazer um fork desse repositório

# 2 - Criar um branch com o seu primeiro e último nome
git checkout -b Alan Fratti

# 3 - Escreva a documentação da sua aplicação
Crie uma pasta na raíz da aplicação chamada docs/ contendo o a modelagem entidade-relacionamento (em imagem ou pdf) da sua aplicação. Você deve também, substituir o conteúdo do arquivo README.md e escrever a documentação da sua aplicação, com os seguintes tópicos:

Projeto: Descreva o projeto e como você o executou. Seja objetivo.
Tecnologias: Descreva quais padrões foram utilizadas, enumerando versões (se necessário) e os links para suas documentações, bem como, qual guia de estilos de código você utilizou com o link para a sua documentação.
Como rodar: Descreva como iniciar a sua aplicação.
Observações: Escreva a documentação em formato Markdown.

# 4 - Faça uma Pull Request
Após implementada a solução, crie uma pull request com o seu projeto para esse repositório.

# Critérios de Aceitação
Para que seu teste tenha o mínimo necessário que atenda aos requisitos esperados, ele deve:

Atender ao que foi proposto no Desafio.
Ter documentação de aplicação e modelos de banco de dados.
Utilize o paradigma de orientação a objetos.
Sua RESTFul API deve se comunicar em JSON e apenas nele.
Utilize corretamente os códigos de retorno HTTP. Gostamos dessa abordagem.
Manter uma estrutura de aplicação concisa e coerente. (Simples é melhor que complexo)
Utilizar padrões semânticos em mensagens de commit. (Gostamos do padrão de commits do repositório AngularJS)

# Dicas e Informações Valiosas

# O que gostaríamos de ver em seu teste:
Testar ele localmente com `dotnet run` e validar os endpoints.
Convenção de nome em classes, objetos, variáveis, métodos e etc.
Um planejamento de entrega das tarefas do seu desafio. (Gostamos de Trello).
Que sua estrutura de linguagem e tecnologias seja compatível com ambiente Linux.
Testes unitários.
Observação: Nenhum dos itens acima é obrigatório.

# O que não gostaríamos de ver no seu teste:
Saber que não foi você quem implementou.
Processos manuais de inicialização da aplicação e banco de dados.
Fraco relacionamento entre colunas nas tabelas (falta de Foreign Key e Constraints).
Falta de organização de código.
Falta de documentação.
Histórico de commits desorganizado e despadronizado.



