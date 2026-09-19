# One Futebol Performance — protótipo

Abra `index.html` no navegador (funciona sem servidor) ou rode:

```bash
python -m http.server 5599
```

Arquivo único: HTML + CSS + JS na mesma página. Pensado primeiro para o celular (375px) e adaptado para desktop.

## Estrutura da página

1. Hero "Eleve seu jogo" (foto com movimento suave)
2. Marquee de temas
3. Sessões em destaque (carrossel)
4. Banners One Individual / One Pro
5. Metodologia — 4 pilares
6. Números
7. Atletas & embaixadores (carrossel)
8. Planos One
9. **Parceria Vitrine do Atleta** — formatos 1 e 2 da proposta:
   entrega de fim de ciclo (portfólio incluso no plano) + parecer técnico assinado pela One.
   Traz a logo oficial da Vitrine e um mockup animado do portfólio com a seção do parecer.
10. Conteúdo do YouTube
11. Depoimentos
12. CTA com formulário de avaliação
13. Rodapé

## Trocar as fotos

As imagens ficam em `assets/img/`. Todo bloco visual usa a variável `--img`:

    <div class="media" style="--img:url('assets/img/hero.jpg')"></div>

Basta substituir o arquivo (mantendo o nome) ou apontar para outro. Sem `--img`, o bloco
volta ao placeholder em gradiente escuro.

Arquivos usados:

| Arquivo | Onde aparece |
|---|---|
| `hero.jpg` | capa |
| `treino-controle/finalizacao/passe/fisico.jpg` | cards de sessões |
| `one-individual.jpg`, `one-pro.jpg` | banners duplos |
| `atleta-1..4.jpg` | carrossel de atletas |
| `yt-1.jpg`, `yt-2.jpg` | vídeos do YouTube |
| `cta.jpg` | fundo do CTA final |
| `vitrine.jpg` | foto dentro do celular na seção da parceria |
| `vitrine-logo.png` | logo oficial da Vitrine do Atleta (baixada do site deles) |
| `one-logo.png` / `one-logo-dark.png` | logo da One (versão branca para fundo escuro e escura para fundo claro) |

> As fotos atuais são do Unsplash (uso livre) e servem só como placeholder.
> Substitua pelas fotos reais da One e dos atletas antes de publicar.

## Mobile

- Barra de ação fixa no rodapé (Agendar avaliação + WhatsApp)
- Header compacto (logo + busca + menu), menu em tela cheia
- Carrosséis por arraste, sem setas
- Campos do formulário com 16px para não dar zoom no iOS
- Respeita `safe-area` (iPhone com notch)

## Antes de publicar — revisar

- Números da seção de estatísticas (placeholders)
- Depoimentos (fictícios)
- Planos, durações e níveis das sessões da One
- Endereço e horários no rodapé
- WhatsApp: número +55 19 98294-4348 já ligado na barra fixa, no rodapé, na barra do topo,
  no botão "Falar com um treinador" e no formulário (constante `WHATSAPP` no script)
- Quais planos da One realmente incluem o portfólio (hoje o site diz: trimestral e anual)
- Texto e formato do parecer técnico assinado pela One (selo e responsável)
- Uso da logo da Vitrine do Atleta: confirmar arquivo oficial e regras de aplicação com eles
