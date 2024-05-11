# Criando-uma-Aplica-o-de-Transfer-ncias-Banc-rias-com-.NET

Aqui está um esboço de texto dividido em módulos sobre a criação de uma aplicação de transferências bancárias com .NET, incluindo exemplos práticos:

---

## Introdução ao Projeto de Transferências Bancárias com .NET

**Objetivo**: Desenvolver uma aplicação .NET que simula um sistema de transferências bancárias, aplicando conceitos de orientação a objetos.

**Descrição**: Este projeto é uma introdução prática ao paradigma de programação orientada a objetos (OOP), que é amplamente utilizado no desenvolvimento de software. Você aprenderá a estruturar um domínio de negócios bancários, implementar funcionalidades essenciais e usar enums para representar tipos de contas e operações bancárias.

---

## Módulo 1: Pensamento Orientado a Objetos

**Conceitos abordados**:
- Classes e Objetos
- Encapsulamento
- Herança
- Polimorfismo

**Exemplo Prático**:
```csharp
public class ContaBancaria
{
    public string Numero { get; private set; }
    public decimal Saldo { get; private set; }

    public ContaBancaria(string numero, decimal saldoInicial)
    {
        Numero = numero;
        Saldo = saldoInicial;
    }

    public void Depositar(decimal valor)
    {
        Saldo += valor;
    }

    public bool Sacar(decimal valor)
    {
        if (valor <= Saldo)
        {
            Saldo -= valor;
            return true;
        }
        return false;
    }
}
```

---

## Módulo 2: Modelagem do Domínio

**Conceitos abordados**:
- Definição de classes de domínio
- Relacionamentos entre classes
- Princípios SOLID

**Exemplo Prático**:
```csharp
public enum TipoConta
{
    Corrente,
    Poupanca
}

public class Cliente
{
    public string Nome { get; set; }
    public ContaBancaria Conta { get; set; }
}
```

---

## Módulo 3: Utilização de Enums

**Conceitos abordados**:
- Definição de enums
- Uso de enums para representar constantes
- Vantagens da tipagem forte

**Exemplo Prático**:
```csharp
public void RealizarOperacao(TipoConta tipoConta, decimal valor)
{
    switch (tipoConta)
    {
        case TipoConta.Corrente:
            // Implementação para conta corrente
            break;
        case TipoConta.Poupanca:
            // Implementação para conta poupança
            break;
    }
}
```

---

Este esboço fornece uma estrutura básica para o seu projeto, abordando os conceitos-chave de OOP e como eles podem ser aplicados na prática. Lembre-se de expandir cada seção com mais detalhes e exemplos conforme você desenvolve sua aplicação.
