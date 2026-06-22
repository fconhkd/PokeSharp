# PokeSharp

PokeSharp é um projeto de console em C# para testar o consumo da [PokéAPI](https://pokeapi.co/) usando .NET.

Atualmente, a aplicação faz uma requisição para buscar dados do Pokémon `ditto`, exibe o JSON retornado pela API em formato indentado e desserializa algumas informações para classes C#.

## O que o projeto faz

- Consulta a PokéAPI em `https://pokeapi.co/api/v2/`.
- Busca os dados do Pokémon `ditto`.
- Exibe o JSON bruto formatado no console.
- Converte parte da resposta para um objeto `Pokemon`.
- Mostra informações básicas como ID, nome e experiência base.

## Tecnologias

- C#
- .NET
- `HttpClient`
- `System.Text.Json`
- PokéAPI

## Estrutura

```text
src/
  PokeSharp.sln
  PokeSharp/
    Program.cs
    Pokemon.cs
    PokeSharp.csproj
```

## Como executar

Na raiz do repositório, execute:

```bash
dotnet run --project src/PokeSharp/PokeSharp.csproj
```

A saída esperada inclui o JSON formatado retornado pela PokéAPI e um resumo com os principais dados do Pokémon consultado.

## Exemplo de saída

```text
===== Pokémon =====
ID:   132
Nome: ditto
XP:   101
===================
```

## Possíveis evoluções

- Permitir informar o nome ou ID do Pokémon pela linha de comando.
- Exibir habilidades, altura, peso e sprite principal.
- Tratar erros de conexão ou Pokémon inexistente.
- Separar a chamada HTTP em um serviço próprio.
- Adicionar testes para a desserialização dos modelos.

## Licença

Este projeto está licenciado sob os termos da licença disponível em [LICENSE](LICENSE).
