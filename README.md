<p align="center">
  <img src="favicon.svg" width="150">
</p>

# Ícones do e3s_painel 1.8.1 — pacote para páginas externas

637 ícones desenhados de raiz para o e3s_painel (grelha 24×24, traço), mais 55 ações
que se juntam no canto de qualquer ícone. Não precisa de Flask, Python nem internet.

## Conteúdo

- `css/e3s-icones.css` — todos os ícones por classe (os desenhos vão dentro do ficheiro). É o único ficheiro necessário.
- `svg/<nome>.svg` — cada ícone num SVG solto (24×24, `currentColor`), para `<img>`, editores gráficos ou SVG em linha.
- `icones.json` — lista dos ícones (nome, classe, rótulo, categoria, palavras de pesquisa), das ações e das cores.
- `exemplo.html` — abrir no navegador: todos os ícones com o nome da classe.

## Utilização

Copiar a pasta `css/` para o projeto e ligar o ficheiro:

```html
<link rel="stylesheet" href="css/e3s-icones.css">

<i class="e3s-i e3s-i-escola"></i>                                            <!-- ícone -->
<i class="e3s-i e3s-i-utilizador-acao-adicionar"></i>                         <!-- com ação no canto -->
<i class="e3s-i e3s-i-utilizador-acao-adicionar e3s-i-acao-cor-success"></i>  <!-- ação com cor própria -->
<i class="e3s-i e3s-i-turma-acao-cancelar e3s-i-acao-fundo-danger"></i>       <!-- ação num círculo -->
<i class="e3s-i e3s-i-livro e3s-i-xl"></i>                                    <!-- tamanho: xs sm md lg xl 2xl -->
```

- **Nome da classe**: `e3s-i-` + nome do ícone com hífenes em vez de `_` (`base_dados` → `e3s-i-base-dados`).
- **Cor**: a do texto (`color` do elemento ou do pai). **Tamanho**: o `font-size`, ou `e3s-i-xs` … `e3s-i-2xl`.
- **Ação**: `e3s-i-<nome>-acao-<ação>`. Cor da ação: `e3s-i-acao-cor-<cor>` ou `style="--e3s-i-cor-acao: #hex"`.
  Círculo de fundo: `e3s-i-acao-fundo-<cor>` ou a classe `e3s-i-acao-fundo` com `style="--e3s-i-fundo-acao: #hex"`.
- **Cores com nome**: primary, success, danger, warning, info, neutro, marca, roxo, rosa, laranja, verde-agua. `primary` usa `--e3s-primary` se existir (senão `#1565c0`):
  `:root { --e3s-primary: #0d9488; }`.
- **Acessibilidade**: ícones decorativos com `aria-hidden="true"`; com significado, `role="img" aria-label="…"`.
- **Trocar por JavaScript**: basta mudar a classe (`el.className = "e3s-i e3s-i-copiar-acao-ativar"`).
- O traço é fixo (2). Para outro traço, cor fixa ou tamanho em ficheiro, use os SVG ou o editor da página dos ícones.

## Licença

Ícones do e3s_painel (emes3soft), GPL-3.0-only. Os ícones da categoria «Marcas» são representações genéricas,
não os logótipos oficiais; as marcas pertencem aos seus titulares.

## Pela web (sem copiar ficheiros)

Pelo jsDelivr, a partir deste repositório (fixar a versão com a tag, ex.: `@v1.8.1`):

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/<conta>/e3s-icones@v1.8.1/css/e3s-icones.css">
```
