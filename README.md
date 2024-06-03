### Implementação de Testes em Aplicações .NET 5

#### Introdução

Este relatório detalha a implementação de testes em aplicações baseadas no .NET 5, com exemplos práticos e frameworks variados.

#### Ferramentas e Frameworks Utilizados

1. **xUnit, NUnit e MSTest**:
   - **xUnit**: Um framework de teste de unidade popular para .NET. Utiliza atributos como `[Fact]` e `[Theory]` para definir testes.
   - **NUnit**: Outro framework de teste amplamente utilizado que suporta testes parametrizados através de atributos como `[Test]` e `[TestCase]`.
   - **MSTest**: O framework de teste original do .NET, ainda em uso para compatibilidade e suporte em ambientes legados.

2. **Tecnologias Complementares**:
   - **.NET 5**: Plataforma de desenvolvimento unificada para construção de aplicações em diferentes ambientes.
   - **ASP.NET Core**: Framework para desenvolvimento de aplicações web e APIs.
   - **Visual Studio**: IDE robusta da Microsoft para desenvolvimento .NET.

#### Testes de Unidade

Os testes de unidade são essenciais para validar a funcionalidade individual de componentes de software. A seguir, exemplos de testes utilizando diferentes frameworks:

1. **Conversão de Temperaturas (xUnit, NUnit, MSTest)**:
   - Projeto que converte temperaturas de Fahrenheit para Celsius, testado com xUnit, NUnit e MSTest.

     ***xUnit***
     
     ![image](https://github.com/Ra2861/aplicando-testes/assets/99209068/44705fa0-1746-4686-a630-6389fcb9e567)

O código testado está localizado no namespace `Temperatura` e implementa a conversão de temperatura. Os testes foram implementados na classe `TestesConversorTemperatura`, localizada no namespace `Temperatura.Testes`. Utilizamos o framework xUnit para realizar testes parametrizados, verificando se o método `FahrenheitParaCelsius` retorna os valores esperados para diferentes entradas de temperatura em Fahrenheit.

1. **[Theory]**: Marca o método de teste como um teste parametrizado.
2. **[InlineData]**: Fornece um conjunto de dados para o teste. Cada par de valores representa a temperatura em Fahrenheit e o valor esperado em Celsius.
3. **Assert.Equal(expected, actual)**: Verifica se o valor calculado pelo método corresponde ao valor esperado.

#### Resultados dos Testes

Os testes foram executados no ambiente de desenvolvimento utilizando o gerenciador de testes do Visual Studio. Todos os casos de teste passaram conforme esperado, indicando que o método `FahrenheitParaCelsius` está funcionando corretamente para os valores fornecidos.

| Temperatura (Fahrenheit) | Valor Esperado (Celsius) | Valor Calculado (Celsius) | Resultado |
|---------------------------|--------------------------|---------------------------|-----------|
| 32                        | 0                        | 0                         | Passou    |
| 47                        | 8.33                     | 8.33                      | Passou    |
| 86                        | 30                       | 30                        | Passou    |
| 90.5                      | 32.5                     | 32.5                      | Passou    |
| 120.18                    | 48.99                    | 48.99                     | Passou   
