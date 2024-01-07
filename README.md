# DIO - Trilha .NET - Testes Unitários com C#
[www.dio.me](www.dio.me)

## Desafio de projeto
Este desafio faz parte da trilha .NET da Digital Innovation One (DIO) e tem como objetivo a implementação de testes unitários em um sistema. O contexto do desafio envolve um sistema que vem enfrentando problemas, tais como bugs, funcionalidades que deixam de funcionar, e problemas de validações, levando os clientes a duvidarem da qualidade do código.

Diante dessa situação, a proposta é a implementação de testes unitários para cobrir as partes mais críticas do sistema, abrangendo cenários positivos e negativos. Dessa forma, busca-se alcançar rastreabilidade e controle do código, melhorando a qualidade do sistema.

## Premissas
O sistema é composto por dois projetos: um do tipo console e um de testes utilizando **xUnit**. O projeto console contém duas classes principais: **ValidacoesLista** e **ValidacoesString**, que realizam diversas validações em listas e strings, respectivamente.

O projeto de testes, por sua vez, inclui as classes de teste **ValidacoesListaTests** e **ValidacoesStringTests**. No entanto, esses testes estão incompletos, sendo necessário implementar os métodos de teste correspondentes aos métodos das classes de console.

## Projeto Console - Classes e Métodos

### Classe `ValidacoesLista`

Classe responsável por realizar diversas validações envolvendo listas.

| Classe          | Método                       | Objetivo                                                                                                                |
|---------------- |------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| ValidacoesLista | RemoverNumerosNegativos      | Recebe uma lista de números inteiros e retorna uma nova lista, apenas com os números positivos                          |
| ValidacoesLista | ListaContemDeterminadoNumero | Recebe uma lista de números inteiros e verifica se um determinado número está presente dentro dessa lista               |
| ValidacoesLista | MultiplicarNumerosLista      | Recebe uma lista de números inteiros e retorna uma nova lista, com seus valores multiplicados por um determinado número |
| ValidacoesLista | RetornarMaiorNumeroLista     | Recebe uma lista de números inteiros e retorna o maior número entre eles                                                |
| ValidacoesLista | RetornarMenorNumeroLista     | Recebe uma lista de números inteiros e retorna o menor número entre eles                                                |

### Classe `ValidacoesString`

Classe responsável por realizar diversas validações envolvendo strings.

| Classe           | Método                       | Objetivo                                                                                                                
|------------------|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ValidacoesString | RetornarQuantidadeCaracteres | Recebe um texto qualquer e retorna a quantidade de caracteres presentes no texto                                                                           |
| ValidacoesString | ContemCaractere              | Recebe um texto qualquer e um texto a ser procurado, retorna verdadeiro ou falso se um determinado trecho procurado está presente no texto                 |
| ValidacoesString | TextoTerminaCom              | Recebe um texto qualquer e um trecho a ser procurado, retorna verdadeiro ou falso se um determinado trecho procurado está presente no final do texto apenas |

## Projeto de Testes - Classes e Métodos

### Classe `ValidacoesListaTests`

Classe responsável por realizar os testes da classe `ValidacoesLista`.

| Classe               | Método de teste                               | Resultado esperado do teste
|----------------------|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| ValidacoesListaTests | DeveRemoverNumerosNegativosDeUmaLista         | Ao passar uma lista com diversos números, incluindo positivos e negativos, deve ser retornado uma nova lista apenas com números positivos  |
| ValidacoesListaTests | DeveConterONumero9NaLista                     | Ao passar uma lista com diversos números, incluindo o número 9, deve retornar verdadeiro, pois encontrou o 9 na lista                      |
| ValidacoesListaTests | NaoDeveConterONumero10NaLista                 | Ao passar uma lista com diversos números, mas sem o número 10, deve retornar falso, pois não encontrou o 10 na lista                       |
| ValidacoesListaTests | DeveMultiplicarOsElementosDaListaPor2         | Ao passar uma lista de inteiros, deve retornar uma nova lista, com todos os elementos da lista multiplicados por 2                         |
| ValidacoesListaTests | DeveRetornar9ComoMaiorNumeroDaLista           | Ao passar uma lista de números inteiros, sendo o maior deles 9, deve retornar o 9 como maior elemento dentro dessa lista                   |
| ValidacoesListaTests | DeveRetornarOitoNegativoComoMenorNumeroDaList | Ao passar uma lista de números inteiros, sendo o menor deles -8, deve retornar o -8 como menor elemento dentro dessa lista                 |

### Classe `ValidacoesStringTests`

Classe responsável por realizar os testes da classe `ValidacoesString`.

| Classe                | Método de teste                                  | Resultado esperado do teste
|---------------------- |--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ValidacoesStringTests | DeveRetornar6QuantidadeCaracteresDaPalavraMatrix | Ao passar um texto escrito a palavra "Matrix", deve retornar o número 6, representando 6 caracteres presentes na palavra                                                                         |
| ValidacoesStringTests | DeveContemAPalavraQualquerNoTexto                | Ao passar um texto escrito "Esse é um texto qualquer" e procurar pela palavra "qualquer", deve retornar verdadeiro pois a palavra existe no texto                                                |
| ValidacoesStringTests | NaoDeveConterAPalavraTesteNoTexto                | Ao passar um texto escrito "Esse é um texto qualquer" e procurar pela palavra "teste", deve retornar falso pois a palavra não existe no texto                                                    |
| ValidacoesStringTests | TextoDeveTerminarComAPalavraProcurado            | Ao passar um texto escrito "Começo, meio e fim do texto procurado" e procurar pela palavra "procurado", deve retornar verdadeiro pois a palavra existe no texto e está inclusa no final do texto |

## Estrutura do Projeto

O projeto está estruturado da seguinte maneira:

![Estrutura do Projeto](Imagens/projeto.png)

## Solução
Os códigos de teste estavam pela metade, e foram implementados os métodos de teste correspondentes aos métodos das classes de console. As implementações foram realizadas conforme as regras mencionadas no desafio.

Este é um passo importante para garantir a qualidade do código e evitar problemas no sistema. Certifique-se de que as bibliotecas corretas estejam sendo usadas e que os namespaces estejam configurados adequadamente.

Projeto desenvolvido como parte da trilha .NET da Digital Innovation One (DIO).
