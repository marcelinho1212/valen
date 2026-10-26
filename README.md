# Valen Vidros

Site institucional da **Valen Vidros**, empresa de vidros sob medida em São Bernardo do Campo e região do Grande ABC (SP).

O site foi feito primeiro para celular e se adapta a tablet e desktop. É uma página estática, sem framework e sem etapa de build.

## O que tem na página

- **Abertura** com foto real, chamada principal e botões de orçamento e WhatsApp
- **Serviços:** box de banheiro, vidro temperado, espelhos, sacadas e coberturas, e divisórias
- **Galeria de trabalhos** com 73 fotos reais, filtros por tipo, botão "Ver mais" e foto ampliada com navegação por setas, teclado e deslize
- **Como funciona**, em 4 passos
- **Área de atendimento:** São Bernardo do Campo e região do ABC
- **Formulário de orçamento** que monta a mensagem e abre o WhatsApp
- **Botão flutuante de WhatsApp**
- Respeita a preferência do sistema por menos animação (`prefers-reduced-motion`)
- Dados estruturados (JSON-LD) de negócio local, para buscadores

## Tecnologias

- HTML, CSS e JavaScript puros, em um único arquivo
- Fonte [Archivo](https://fonts.google.com/specimen/Archivo), carregada do Google Fonts
- Layout mobile first, com breakpoints em 700px, 900px e 1100px

## Estrutura de arquivos

```
valen/
├── index.html            # página (originalmente Valen_Vidros.html)
├── fotos/                # 28 fotos usadas na galeria e no topo
├── logo-valen.png        # logo completa
├── logo-valen-claro.png  # logo completa, versão clara para fundo escuro
├── logo-marca.png        # símbolo da marca (também usado como favicon)
└── logo-marca-claro.png  # símbolo, versão clara
```

A página usa caminhos relativos. Mantenha o HTML, a pasta `fotos/` e os logos juntos.

## Como rodar localmente

Abra o `index.html` direto no navegador, ou use um servidor local:

```bash
python3 -m http.server 8765
```

Depois acesse `http://localhost:8765/`.

## Como editar

| O que mudar | Onde |
|---|---|
| Telefone do WhatsApp | constante `PHONE` no `<script>` no fim do arquivo (formato `5511947981561`) |
| Telefone exibido e links `tel:` | seções de orçamento e rodapé do HTML |
| Cores | variáveis CSS no início do `<style>` (`--bg`, `--card`, `--vio`, `--vio2`, `--lil`) |
| Fotos da galeria | elementos `<figure data-c="...">` dentro de `#gal`; `data-c` define o filtro |
| Quantidade de fotos antes do "Ver mais" | constante `LIMIT` no `<script>` |
| Serviços e opções do formulário | seção `#servicos` e os botões de opção em `#orcamento` |

## Publicação

O site pode ser publicado como site estático, por exemplo no Render ou no GitHub Pages.

No **Render** (Static Site):

- **Build Command:** em branco
- **Publish Directory:** `valen`, se os arquivos estiverem dentro da pasta `valen` do repositório, ou `.` se estiverem na raiz
- O arquivo principal precisa se chamar `index.html`

## Contato

WhatsApp e telefone: +55 11 97066-1030
