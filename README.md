# Portfólio jornalístico | Thais Costa de Sales

Site estático (HTML + CSS, sem dependências). Abra o `index.html` no navegador ou publique a pasta inteira (GitHub Pages, Netlify etc.).

## Estrutura

```
index.html
assets/
  thais.jpeg, escadariahd.jpeg, mario.jpeg, volis.jpeg
  video/
    reportagem-thais-sales.mp4   (720p, ~15 MB, otimizado para web)
    reportagem-poster.jpg        (capa exibida antes do play)
  audio/
    entrevista-moda-consumo.mp3  (mono, 64 kbps, ~3 MB)
```

## Descrição da reportagem em vídeo

**Eleições, redes e algoritmos: quem decide o que você vê?**
Reportagem em vídeo | Thaís Sales, São Paulo | 3 minutos

Perfis com milhões de seguidores, regras de plataformas que podem tirar uma conta do ar e algoritmos que escolhem o que chega a cada eleitor: a reportagem mostra como as redes sociais viraram um dos principais palcos da disputa política.

O vídeo parte do alcance de parlamentares nas redes, como Erika Hilton (SP), com 7,3 milhões, Ana Elisa (MG), com 3,9 milhões, e Guilherme Cortez (SP), com 1,2 milhão. Na sequência, discute o poder de moderação das plataformas a partir do caso de um perfil desabilitado por descumprir os Padrões da Comunidade, e ouve a estudante Amanda Yamamoto sobre como esse ambiente afeta quem consome política no dia a dia.

Com passagem da repórter, imagens de arquivo, infográficos e depoimento, o material combina apuração, dados e narrativa audiovisual.

**Créditos de imagem:** Paulo Pinto/Agência Brasil; Rebecca Buzato/Le Monde Diplomatique Brasil.

## Como trocar o vídeo no futuro

Substitua `assets/video/reportagem-thais-sales.mp4` e `reportagem-poster.jpg` mantendo os nomes, ou altere os caminhos na tag `<video>` do `index.html` (seção `#video`). Para gerar uma versão leve de um vídeo novo:

```
ffmpeg -i original.mp4 -c:v libx264 -crf 28 -vf scale=-2:720 -c:a aac -b:a 96k -movflags +faststart saida.mp4
```

## Descrição da seção "Comportamento" (pauta + entrevista em áudio)

**Tendência ou escolha? O que leva a gente a comprar roupa**
Proposta de reportagem com entrevista em áudio | 7 minutos

A pauta investiga como uma tendência que surge nas redes sociais vira vontade de comprar uma roupa e o quanto essa vontade é espontânea, sem partir do pressuposto de que todo consumidor é manipulado. Publicidade, influenciadores, algoritmos e a busca por pertencimento entram na conta.

No áudio, Thais entrevista João, que trabalha com brechós: ele conta como o brechó surgiu na família, como as redes sociais impulsionaram o nicho e reduziram o preconceito, por que peças vintage únicas atraem tanta gente e por que, para ele, a moda continua sendo expressão pessoal.

O texto da justificativa fica em `index.html`, seção `#comportamento`.
