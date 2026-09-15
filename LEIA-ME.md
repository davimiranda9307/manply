# Página de vendas — Manply · 100 Mapas Mentais de Matemática para o ENEM

Página única: `index.html` + a pasta `assets/`. Não precisa de build nem de instalar nada.

## Antes de rodar anúncio (checklist)

Tudo fica no bloco `CONFIG`, nas primeiras linhas do `index.html`:

- [ ] `checkoutUrl`: link do checkout (Kiwify/Hotmart). Enquanto for `#checkout`, o botão mostra um aviso em vez de levar pro checkout.
- [ ] `precoCheio` / `precoPromo` (hoje R$ 54,99 → R$ 27,89): o preço cheio precisa ser o valor que você realmente vai cobrar depois do lançamento.
- [ ] `prazoLancamento` (opcional): só preencha se a data for real. Depois dela, a página passa sozinha pro preço cheio.
- [ ] `suporteEmail` / `suporteWhatsapp`
- [ ] `empresaNome` / `empresaDocumento`: nome e CPF/CNPJ no rodapé (exigido em venda online).
- [ ] `linkTermos` / `linkPrivacidade`
- [ ] `metaPixelId`: ID do Pixel da Meta.
- [ ] `mostrarPlaceholders: false`: esconde as caixas "ESPAÇO RESERVADO".
- [ ] No `<head>`, troque `https://SEU-DOMINIO.com.br` pelo domínio real (prévia no WhatsApp/Instagram).

## Depois das primeiras vendas

- `depoimentos`: adicione só depoimentos reais, com autorização (dá pra usar print do WhatsApp com os dados pessoais borrados).
- `bonus`: adicione só bônus que já existem e que você entrega.

## O que a página faz sozinha

- Conta os dias até a prova de Matemática (15/11/2026, 13h30, Edital Inep nº 64/2026) e esconde a contagem depois da prova.
- Repassa os UTMs do anúncio (`utm_source`, `utm_campaign`…) pro link do checkout.
- Dispara `PageView` e `InitiateCheckout` no Pixel, se o ID estiver preenchido.
- Mostra a barra fixa de compra no celular quando nenhum botão está visível na tela.

## Imagens

A capa vem de `img.produto.png` (arquivo original, não é carregado pela página). As demais imagens são páginas reais do PDF `20-mapas-mentais-matematica-enem.pdf`. Tudo convertido para WebP; as versões grandes só carregam quando alguém toca pra ampliar.
Pra trocar uma imagem, substitua o arquivo mantendo o mesmo nome.

- `produto-600.webp` / `produto-1024.webp`: capa inteira (desktop)
- `produto-recorte-640.webp` / `produto-recorte-984.webp`: capa recortada (celular e card da oferta)
- `mapas/bloco01.webp` … `mapas/bloco20.webp`: miniaturas dos 20 mapas (o número é o bloco)
- `mapas/bloco03-960.webp` / `bloco03-2000.webp` e `mapas/bloco10-960.webp` / `bloco10-2000.webp`: mapas em destaque (Financeira e Geometria Plana I); a versão 2000 abre ao ampliar
- `pagina-*.webp`: página de explicação (Juros compostos), índice e resumo de fórmulas
- `og-image.jpg`: imagem de compartilhamento (1200×630)

## Publicar

Suba a pasta inteira (`index.html` + `assets/`) em qualquer hospedagem estática: Netlify (arrastar e soltar), Vercel, Cloudflare Pages, Hostinger etc.
