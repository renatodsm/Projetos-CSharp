
## Blindando Seu Código com TDD e Testes Unitários Usando .NET Core
---

Neste projeto, iremos criar uma aplicação console de uma calculadora simples e implementar testes unitários utilizando o framework XUnit para garantir a qualidade do código.

### Estrutura do Projeto

MeuProjeto/

│

├── src/

│ └── MeuProjeto/

│ └── Calculadora.cs

│
└── test/

└── MeuProjeto.Tests/

└── CalculadoraTests.cs

csharp
Copiar código

### Funcionalidades da Calculadora

- **Somar**: Método para somar dois números.
- **Subtrair**: Método para subtrair um número de outro.
- **Multiplicar**: Método para multiplicar dois números.
- **Dividir**: Método para dividir um número pelo outro.
- **Histórico**: Manter um histórico das últimas três operações realizadas.

### Implementação da Calculadora

Aqui está um exemplo de como a classe `Calculadora` pode ser implementada:

```csharp
namespace MeuProjeto
{
    public class Calculadora
    {
        private List<string> historico = new List<string>();

        public double Somar(double a, double b)
        {
            var resultado = a + b;
            AdicionarAoHistorico($"{a} + {b} = {resultado}");
            return resultado;
        }

        public double Subtrair(double a, double b)
        {
            var resultado = a - b;
            AdicionarAoHistorico($"{a} - {b} = {resultado}");
            return resultado;
        }

        public double Multiplicar(double a, double b)
        {
            var resultado = a * b;
            AdicionarAoHistorico($"{a} * {b} = {resultado}");
            return resultado;
        }

        public double Dividir(double a, double b)
        {
            if (b == 0)
            {
                throw new ArgumentException("Divisor não pode ser zero.");
            }
            var resultado = a / b;
            AdicionarAoHistorico($"{a} / {b} = {resultado}");
            return resultado;
        }

        private void AdicionarAoHistorico(string operacao)
        {
            historico.Add(operacao);
            if (historico.Count > 3)
            {
                historico.RemoveAt(0);
            }
        }

        public List<string> ObterHistorico()
        {
            return historico;
        }
    }
}
Escrevendo Testes Unitários
Aqui está um exemplo de como escrever testes na classe CalculadoraTests.cs:

csharp
Copiar código
using MeuProjeto;
using System;
using Xunit;

namespace MeuProjeto.Tests
{
    public class CalculadoraTests
    {
        private readonly Calculadora calculadora;

        public CalculadoraTests()
        {
            calculadora = new Calculadora();
        }

        [Fact]
        public void DeveSomarDoisNumeros()
        {
            var resultado = calculadora.Somar(5, 3);
            Assert.Equal(8, resultado);
        }

        // Outros testes aqui...
    }
}
Executando os Testes
Para executar os testes, use o seguinte comando:


dotnet test
