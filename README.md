# Clareza ATS

AplicaÃ§Ã£o para comparar um currÃ­culo com uma vaga, identificar palavras-chave e exportar uma versÃ£o de uma coluna que preserva os fatos fornecidos.

AplicaÃ§Ã£o: https://clareza-ats-beatrix.beatrizfpedroso1.chatgpt.site

## Ferramenta e escopo

O Lovable permaneceu com o painel vazio apÃ³s o login. Com autorizaÃ§Ã£o da pessoa responsÃ¡vel pelo projeto, o app foi implementado com assistÃªncia do Codex e publicado pela ferramenta Sites. A aplicaÃ§Ã£o nÃ£o foi gerada nem exportada pelo Lovable. Essa diferenÃ§a em relaÃ§Ã£o Ã  ferramenta indicada no desafio Ã© explÃ­cita nesta entrega.

O MVP usa HTML, CSS e JavaScript, sem dependÃªncias externas ou login. Os textos sÃ£o processados no navegador e nÃ£o sÃ£o enviados a um modelo de linguagem. A versÃ£o ajustada normaliza espaÃ§os e quebras de linha e pode ser editada antes de exportar. NÃ£o hÃ¡ avaliaÃ§Ã£o real por ATS, anÃ¡lise semÃ¢ntica ou garantia de contrataÃ§Ã£o.

## Prompt utilizado

Crie Clareza ATS em portuguÃªs brasileiro. Receba a vaga e o currÃ­culo em dois campos, identifique competÃªncias presentes e ausentes e explique a cobertura lexical. Nunca invente fatos, experiÃªncias, certificaÃ§Ãµes ou resultados. Mostre evidÃªncias dos termos encontrados. Prepare uma versÃ£o de uma coluna, editÃ¡vel, preservando integralmente os fatos do texto original. Permita copiar, baixar TXT e imprimir ou salvar PDF com texto selecionÃ¡vel. Valide campos vazios e ofereÃ§a um exemplo fictÃ­cio. NÃ£o envie nem persista dados pessoais por padrÃ£o. Crie uma interface responsiva com verde, fundo claro, contraste legÃ­vel e rÃ³tulos acessÃ­veis.

## Como funciona

1. A pessoa cola a vaga e o currÃ­culo.
2. Uma lista de competÃªncias reconhecidas Ã© filtrada pelos termos presentes na vaga. Se a lista estiver vazia, atÃ© 12 palavras relevantes sÃ£o selecionadas do texto, excluindo palavras comuns.
3. A comparaÃ§Ã£o normaliza acentos e maiÃºsculas e usa limites de palavras.
4. A cobertura corresponde ao nÃºmero de termos encontrados dividido pelo nÃºmero de termos analisados.
5. A versÃ£o para exportaÃ§Ã£o preserva o texto do currÃ­culo e organiza espaÃ§os e quebras de linha. Termos ausentes nÃ£o sÃ£o inseridos.

## Ajustes e validaÃ§Ã£o

Foi acrescentada uma explicaÃ§Ã£o do mÃ©todo para que a porcentagem nÃ£o seja confundida com uma nota de empregabilidade. A geraÃ§Ã£o livre de experiÃªncias foi excluÃ­da do escopo. O layout de impressÃ£o foi separado da interface, com uma coluna, texto selecionÃ¡vel e quebra de linhas longas.

VerificaÃ§Ãµes executadas: sintaxe JavaScript; resposta HTTP 200; mensagem de erro para campos vazios; exemplo com 4 de 5 termos presentes, resultando em 80%; cenÃ¡rio com Excel presente e Python e SQL ausentes, resultando em 33%; preparaÃ§Ã£o do currÃ­culo sem acrescentar Python ou SQL. A automaÃ§Ã£o do navegador nÃ£o confirmou o evento de download, por isso a abertura do arquivo TXT e a saÃ­da PDF devem ser conferidas manualmente antes de uso real.

## Executar localmente

Sirva a pasta do repositório com qualquer servidor estÃ¡tico. Por exemplo: `python -m http.server 8000`. Abra http://localhost:8000.

## Arquivos

- `index.html`: interface e campos.
- `style.css`: layout responsivo e impressÃ£o.
- `app.js`: comparaÃ§Ã£o, revisÃ£o e exportaÃ§Ã£o.

Use apenas os dados fictÃ­cios da demonstraÃ§Ã£o ao testar. NÃ£o hÃ¡ chaves, tokens ou senhas no cÃ³digo.

