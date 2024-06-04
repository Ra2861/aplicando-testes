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

### Estrutura do Teste
O código testado está localizado no namespace `Temperatura` e implementa a conversão de temperatura. Os testes foram implementados na classe `TestesConversorTemperatura`, localizada no namespace `Temperatura.Testes`. Utilizamos o framework xUnit para realizar testes parametrizados, verificando se o método `FahrenheitParaCelsius` retorna os valores esperados para diferentes entradas de temperatura em Fahrenheit.

1. **[Theory]**: Marca o método de teste como um teste parametrizado.
2. **[InlineData]**: Fornece um conjunto de dados para o teste. Cada par de valores representa a temperatura em Fahrenheit e o valor esperado em Celsius.
3. **Assert.Equal(expected, actual)**: Verifica se o valor calculado pelo método corresponde ao valor esperado.

#### Resultados dos Testes

Os testes foram executados no ambiente de desenvolvimento utilizando o gerenciador de testes do Visual Studio. Todos os casos de teste passaram conforme esperado, indicando que o método `FahrenheitParaCelsius` está funcionando corretamente para os valores fornecidos.

### Resultado esperado
| Temperatura (Fahrenheit) | Valor Esperado (Celsius) | Valor Calculado (Celsius) | Resultado |
|---------------------------|--------------------------|---------------------------|-----------|
| 32                        | 0                        | 0                         | Passou    |
| 47                        | 8.33                     | 8.33                      | Passou    |
| 86                        | 30                       | 30                        | Passou    |
| 90.5                      | 32.5                     | 32.5                      | Passou    |
| 120.18                    | 48.99                    | 48.99                     | Passou   


### Resultado
![image](https://github.com/Ra2861/aplicando-testes/assets/99209068/5b40342a-e99b-4561-92fb-f68ede9c9084)

***NUnit***

![image](https://github.com/Ra2861/aplicando-testes/assets/99209068/9a7e5120-b923-4147-a7bf-fd87032c0ba0)
### Estrutura do Teste
O teste está estruturado da seguinte maneira:

[TestCase]: Atributo utilizado para fornecer os dados de entrada (temperatura em Fahrenheit) e o resultado esperado (temperatura em Celsius) para o teste.
Execução da Função: O método ConversorTemperatura.FahrenheitParaCelsius é chamado com o valor de Fahrenheit fornecido.
Asserção: O valor retornado pela função é comparado com o valor esperado utilizando Assert.AreEqual. Se os valores não coincidirem, o teste falhará.

### Resultados esperados
Para cada caso de uso, o valor calculado pelo método FahrenheitParaCelsius deve ser igual ao valor esperado (temperatura em Celsius). Se todos os casos de teste passarem, isso indica que a função está convertendo corretamente as temperaturas de Fahrenheit para Celsius conforme esperado. Caso contrário, o teste falhará, indicando que há um problema na lógica de conversão.

Entrada: 32°F, Esperado: 0°C
Caso de uso: Verificar a conversão do ponto de congelamento da água em Fahrenheit para Celsius.
Resultado esperado: 32°F deve ser convertido para 0°C.

Entrada: 47°F, Esperado: 8.33°C
Caso de uso: Verificar a conversão de uma temperatura comum em Fahrenheit para Celsius.
Resultado esperado: 47°F deve ser convertido para aproximadamente 8.33°C.

Entrada: 86°F, Esperado: 30°C
Caso de uso: Verificar a conversão de uma temperatura moderadamente alta em Fahrenheit para Celsius.
Resultado esperado: 86°F deve ser convertido para 30°C.

Entrada: 90.5°F, Esperado: 32.5°C
Caso de uso: Verificar a conversão de uma temperatura com valor decimal em Fahrenheit para Celsius.
Resultado esperado: 90.5°F deve ser convertido para 32.5°C.

Entrada: 120.18°F, Esperado: 48.99°C
Caso de uso: Verificar a conversão de uma temperatura elevada com valor decimal em Fahrenheit para Celsius.
Resultado esperado: 120.18°F deve ser convertido para aproximadamente 48.99°C.

Entrada: 212°F, Esperado: 100°C
Caso de uso: Verificar a conversão do ponto de ebulição da água em Fahrenheit para Celsius.
Resultado esperado: 212°F deve ser convertido para 100°C.

### Resultados
![image](https://github.com/Ra2861/aplicando-testes/assets/99209068/7bc94d49-fdad-442f-ad46-6ef7bd7e2e07)

***MSTest***

![image](https://github.com/Ra2861/aplicando-testes/assets/99209068/25aee278-09a1-45e3-b45b-4dabf4074b41)

### Estrutura do Teste
O teste está estruturado da seguinte maneira:

[TestClass]: Define uma classe que contém testes.
[DataTestMethod]: Define um método que é um teste de unidade e pode receber várias entradas de dados.
[DataRow]: Atributo utilizado para fornecer os dados de entrada (temperatura em Fahrenheit) e o resultado esperado (temperatura em Celsius) para o teste.

### Resultados esperados

Para cada caso de uso, o valor calculado pelo método FahrenheitParaCelsius deve ser igual ao valor esperado (temperatura em Celsius). Se todos os casos de teste passarem, isso indica que a função está convertendo corretamente as temperaturas de Fahrenheit para Celsius conforme esperado. Caso contrário, o teste falhará, indicando que há um problema na lógica de conversão.

Entrada: 32°F, Esperado: 0°C

Caso de uso: Verificar a conversão do ponto de congelamento da água em Fahrenheit para Celsius.
Resultado esperado: 32°F deve ser convertido para 0°C.
Entrada: 47°F, Esperado: 8.33°C

Caso de uso: Verificar a conversão de uma temperatura comum em Fahrenheit para Celsius.
Resultado esperado: 47°F deve ser convertido para aproximadamente 8.33°C.
Entrada: 86°F, Esperado: 30°C

Caso de uso: Verificar a conversão de uma temperatura moderadamente alta em Fahrenheit para Celsius.
Resultado esperado: 86°F deve ser convertido para 30°C.
Entrada: 90.5°F, Esperado: 32.5°C

Caso de uso: Verificar a conversão de uma temperatura com valor decimal em Fahrenheit para Celsius.
Resultado esperado: 90.5°F deve ser convertido para 32.5°C.
Entrada: 120.18°F, Esperado: 48.99°C

Caso de uso: Verificar a conversão de uma temperatura elevada com valor decimal em Fahrenheit para Celsius.
Resultado esperado: 120.18°F deve ser convertido para aproximadamente 48.99°C.
Entrada: 212°F, Esperado: 100°C

Caso de uso: Verificar a conversão do ponto de ebulição da água em Fahrenheit para Celsius.
Resultado esperado: 212°F deve ser convertido para 100°C.

### Resultados
![image](https://github.com/Ra2861/aplicando-testes/assets/99209068/ccd504c6-1772-44a5-9bfd-31d4edb72094)
