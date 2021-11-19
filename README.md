# Enum-GetValues-CSharp
Exemplo de GetValues

```csharp
namespace ConsoleAppEnumSample
{
    class Program
    {
        static void Main(string[] args)
        {
            var tipos = ETipoPessoaList.All();

            foreach (ETipoPessoa item in tipos)
            {
                Console.WriteLine($"Tipo: {item}");
            }
        }
    }

    public static class ETipoPessoaList
    {
        public static List<ETipoPessoa> All()
        {
            return Enum.GetValues(typeof(ETipoPessoa)).OfType<ETipoPessoa>().ToList();
        }
    }

    public enum ETipoPessoa
    {
        Funcionario,
        Gerente,
        Gestor,
        Programador,
        Analista,
        AuxiliarFinanceiro,
        Financeiro
    }
}
```
