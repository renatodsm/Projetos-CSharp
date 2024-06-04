# Análise de Requisitos: Teste de Smartphones

Este documento apresenta uma análise de requisitos e procedimento de teste para as classes `Nokia` e `Iphone` no contexto do projeto.

## Introdução

O objetivo deste teste é verificar o funcionamento correto das classes `Nokia` e `Iphone`, que representam modelos de smartphones. O teste envolve a criação de objetos dessas classes e a execução de algumas operações básicas, como ligar o telefone e instalar aplicativos.

## Requisitos

1. **Classe Nokia**:
   - O smartphone Nokia deve ser capaz de ser ligado.
   - Deve ser possível instalar aplicativos no smartphone Nokia.

2. **Classe Iphone**:
   - O smartphone iPhone deve ser capaz de receber ligações.
   - Deve ser possível instalar aplicativos no smartphone iPhone.

## Procedimento de Teste

1. **Smartphone Nokia**:
   - Inicialização do Smartphone Nokia:
     - Criar um objeto `Nokia` com um número, modelo, IMEI e tamanho de memória especificados.
     - Ligar o smartphone.
     - Instalar um aplicativo, por exemplo, WhatsApp.

2. **Smartphone iPhone**:
   - Inicialização do Smartphone iPhone:
     - Criar um objeto `iPhone` com um número, modelo, IMEI e tamanho de memória especificados.
     - Receber uma ligação.
     - Instalar um aplicativo, por exemplo, Telegram.

## Execução do Teste

Para executar o teste, basta compilar e executar o código fornecido no ambiente de desenvolvimento C#.

```csharp
using DesafioPOO.Models;

// Código de teste fornecido
Console.Clear();

Console.WriteLine("Smartphone NOKIA");
Smartphone nokia = new Nokia(numero: "123456", modelo: "NOKIA C20", imei: "1212121212", memoria: 128);
nokia.Ligar();
nokia.InstalarAplicativo("WhatsApp");

Console.WriteLine("\n");

Console.WriteLine("Smartphone Iphone:");
Smartphone iphone = new Iphone(numero: "123456", modelo: "Iphone 14", imei: "2323232323", memoria: 256);
iphone.ReceberLigacao();
iphone.InstalarAplicativo("Telegram");
Resultados Esperados
Espera-se que o código de teste execute com sucesso, criando instâncias dos smartphones Nokia e iPhone e realizando as operações de inicialização e instalação de aplicativos conforme especificado.

Conclusão
Este documento fornece uma descrição do teste realizado com as classes Nokia e Iphone no contexto do projeto, abordando os requisitos funcionais identificados e os procedimentos de teste. Após a execução bem-sucedida do teste, confirma-se o funcionamento correto das classes e suas funcionalidades básicas.

Para mais informações ou suporte, entre em contato com a equipe de desenvolvimento.