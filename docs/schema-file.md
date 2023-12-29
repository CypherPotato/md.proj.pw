# Arquivo schema.json

O arquivo `schema.json` define como seu repositório funcionará. Ele deve estar no diretório raiz do seu repositório se quiser usar ele como documentação. O arquivo abaixo contém alguns exemplos e documentação sobre cada objeto do arquivo.

> Note que, o exemplo abaixo inclui comentários, no entanto, o arquivo `schema.json` no seu repositório não deve conter nenhum comentário.

Os campos não tem sensibilidade de maiúsculas ou minúsculas, ou seja, `Title` é equivalente à `title` ou `TITLE`.

```jsonc
{
    "metadata": {

        // campo necessário.
        // indica o caminho para o arquivo inicial da documentação.
        // esse caminho é relativo à raiz do repositório
        "index": "/docs/readme.md",

        // indica as cores primárias para documentação. elas são usadas em links
        // e botões. utilize somente cores compatíveis com HTML.
        "primaryColor": "#2c5c97",
        "darkPrimaryColor": "#ddf4ff",

        // indica o título e descrição da documentação. esses textos são
        // exibidos no topo da documentação.
        "title": "md.proj.pw",
        "description": "Documentação do site md.proj.pw.",

        // indica o caminho ABSOLUTO para um ícone, que será exibido no
        // topo da documentação.
        "iconSrc": "https://sisk.project-principium.dev/assets/img/Icon.png",

        // indica quais branches devem ficar visíveis no botão de
        // trocar branch, ao lado do título da documentação.
        // deixe como "null" ou não defina essa propriedade para não exibir
        // o botão.
        "branches": [
            "pt-br",
            "en-us"
        ],

        // especifica o tema da documentação. o tema altera cores, fontes
        // e código. os temas disponíveis são:
        // microsoft, github (padrão)
        "theme": "github",

        // indica se links externos devem abrir em abas separadas ou na mesma
        // aba.
        "makeExternalLinks": true,

        // indica se o botão de editar, que fica acima do leitor da
        // documentação, deve estar visível ou não.
        "editButtonVisible": true,

        // indica se os botões que mostram a documentação anterior e posterior
        // devem ser exibidos ou não.
        "bottomNavigationVisible"
    },
    "contents": [
        // todos os links da documentação devem seguir esse formato.
        // os links são relativos à raiz do repositório.
        {
            "title": "Introdução",
            "href": "/docs/readme.md"
        },
        // separe a navegação da documentação com um elemento que é
        // apenas um texto, indicando o nome da categoria.
        "Categoria",
        {
            "title": "Outra página",
            "href": "/docs/pagina/outra.md"
        },
    ]
}
```