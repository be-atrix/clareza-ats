# Clareza ATS

Ferramenta para comparar as palavras-chave de uma vaga com o texto de um currículo. Mostra termos presentes e ausentes e prepara uma versão editável para copiar, baixar em TXT ou imprimir.

[Abrir o aplicativo](https://clareza-ats-beatrix.beatrizfpedroso1.chatgpt.site)

## Funcionalidades

- Comparar o currículo com a descrição da vaga.
- Mostrar evidências dos termos encontrados e sugestões sobre os ausentes.
- Calcular a cobertura das palavras-chave analisadas.
- Preparar um texto de uma coluna, preservando os fatos fornecidos.
- Editar e copiar o resultado, baixar TXT ou imprimir/salvar como PDF pelo navegador.

## Como a comparação funciona

A ferramenta seleciona competências reconhecidas no texto da vaga. Quando nenhuma competência da lista é encontrada, usa até 12 palavras relevantes, excluindo palavras comuns. A comparação normaliza acentos e maiúsculas e considera os limites das palavras.

A cobertura é o número de termos encontrados no currículo dividido pelo número de termos analisados. Essa porcentagem não é uma nota de empregabilidade nem reproduz a avaliação de um sistema ATS real.

A preparação do currículo organiza espaços e quebras de linha. Ela não acrescenta competências, experiências ou certificações. Termos ausentes devem ser incluídos apenas quando forem verdadeiros e relevantes para a experiência da pessoa.

## Implementação e privacidade

O aplicativo foi desenvolvido em HTML, CSS e JavaScript, com assistência do Codex, e publicado pela ferramenta Sites. O Lovable não carregou nesta sessão; esta implementação usa uma ferramenta diferente da indicada no desafio da DIO.

A análise é lexical, sem IA generativa ou avaliação semântica. Os textos são processados no navegador, sem backend, login ou armazenamento persistente do currículo. O aplicativo não oferece garantia de aprovação em processos seletivos.

## Prompt de criação

Crie uma ferramenta em português brasileiro com campos para vaga e currículo. Identifique palavras-chave presentes e ausentes, mostre evidências e explique o cálculo da cobertura. Nunca invente fatos ou experiências. Prepare uma versão editável de uma coluna, preservando o conteúdo original. Permita copiar, baixar TXT e imprimir. Valide campos vazios e ofereça um exemplo fictício. Não envie nem armazene os dados pessoais. Use uma interface responsiva, com rótulos acessíveis e contraste legível.

## Validação realizada

Foram verificados a sintaxe JavaScript, a resposta HTTP 200, o erro para campos vazios e dois cenários de comparação:

| Cenário | Resultado |
| --- | --- |
| Exemplo com quatro de cinco termos presentes | Cobertura de 80% |
| Excel presente, Python e SQL ausentes | Cobertura de 33%, sem acrescentar os termos ausentes ao currículo |

A automação não confirmou a conclusão do download TXT. A abertura desse arquivo e a saída de impressão/PDF ainda precisam de conferência manual. Não houve validação contra sistemas ATS comerciais.

## Executar

Abra `index.html` no navegador ou sirva a pasta com um servidor estático já disponível. Por exemplo, se Python estiver instalado:

```sh
python -m http.server 8000
```

Acesse http://localhost:8000. O projeto não exige instalar dependências.

## Arquivos

- `index.html`: interface e campos.
- `style.css`: apresentação e impressão.
- `app.js`: comparação, revisão e exportação.

Use os dados fictícios do exemplo ao testar. O código não contém chaves, tokens ou senhas.
