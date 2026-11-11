# Pedro Salvadori, Nutrição Esportiva

Página do nutricionista esportivo Pedro Salvadori (@pedrosalvadori.nutri), nutricionista do Sub-20 do Desportivo Brasil, com consultório na Vila Roma, em Salto, SP, e atendimento on-line. Ele não tinha site; esta é a primeira versão, feita do zero.
Versão 2 (11/11/2026), conceito "o letreiro e o dia de jogo":
- abertura em carbono com o logo PS do consultório desenhado em SVG, que acende como um letreiro de neon;
- "Um dia de jogo com o Pedro", com o palco fixo e as fotos reais do trabalho no clube, do lanche ao relatório de perda hídrica;
- o método aplicado ao paciente e a escolha "Qual é o seu jogo?" (musculação, corrida, futebol, emagrecer);
- placar das avaliações, cronômetro do acompanhamento, consultório e a parede da carreira (concreto e ripas de madeira).

Ajustes no celular (11/11/2026):
- os cartões da abertura ficam no canto de baixo da foto, longe do rosto;
- "Um dia de jogo" também anima no celular: a foto fica fixa no alto e troca a cada etapa enquanto o texto rola por baixo;
- as avaliações viram uma fileira que se arrasta com o dedo, com cada avaliação inteira (no desktop continua a esteira automática).

HTML, CSS e JavaScript puros, sem build. Todos os botões de agendamento abrem o WhatsApp.

## Estrutura

```
index.html                  página completa (estilos, scripts e logo PS dentro do arquivo)
img/pedro-estadio.jpg       foto da abertura (gramado, garrafas aos pés)
img/lanches-jogo.jpg        dia de jogo: antes do jogo
img/jogo-garrafas.jpg       dia de jogo: garrafas marcadas
img/vestiario.jpg           dia de jogo: mesa no vestiário
img/pedro-atletas.jpg       dia de jogo: à beira do campo
img/jogo-pos.jpg            dia de jogo: reposição depois do jogo
img/jogo-relatorio.jpg      dia de jogo: relatório de perda hídrica
img/adipometro.jpg          o método: avaliação física
img/perfil-musculacao.jpg   "Qual é o seu jogo?": musculação
img/perfil-corrida.jpg      "Qual é o seu jogo?": corrida
img/roda-time.jpg           "Qual é o seu jogo?": futebol
img/perfil-emagrecer.jpg    "Qual é o seu jogo?": emagrecer
img/consultorio-ps.jpg      consultório com o logo na parede
img/pedro-retrato.jpg       carreira
img/pedro-garrafas.jpg      seção final
img/favicon.png             ícone da aba (logo PS)
img/apple-touch-icon.png    ícone ao salvar na tela do celular
vercel.json                 configuração da Vercel (URLs limpas)
```

Todas as fotos são do Instagram do Pedro. Nenhuma foi gerada por IA.

## Publicar

1. Crie um repositório no GitHub (ex.: `Pedro_Salvadori`) e envie os arquivos desta pasta para a raiz dele.
   Importante: **arraste a pasta `img` inteira** para a área de upload. O botão "choose your files" não envia pastas.
2. Na Vercel, clique em **Add New → Project**, importe o repositório e mantenha:
   - Project Name: `nutri-pedrosalvadori`
   - Framework Preset: **Other**
   - Build Command: vazio
   - Output Directory: vazio (raiz)
3. Clique em **Deploy**. O site fica em https://nutri-pedrosalvadori.vercel.app/ e cada novo commit publica a atualização sozinho.

## Atualizar o site já publicado

Para atualizar um site que já está no ar, envie o `index.html` novo (e o `README.md`, se quiser) para o repositório. A pasta `img` só precisa subir de novo quando alguma imagem mudar. A Vercel publica sozinha depois do commit.

## Imagens

Ao trocar uma imagem mantendo o mesmo nome, aumente o número `?v=1` nos links do `index.html` (por exemplo `?v=2`) para os navegadores baixarem a versão nova.

## Logo

O logo PS foi redesenhado em SVG a partir da foto da parede do consultório. Está no `index.html` como o símbolo `ps` (menu, rodapé, carreira e final) e no letreiro da abertura. Se o Pedro mandar o arquivo original do logo, dá para conferir as proporções.

## Editar conteúdo

- Número do WhatsApp: variável `numero` no fim do `index.html` (hoje 5519998503586) e o número exibido no rodapé.
- Mensagem padrão: atributo `data-wa` de cada botão. Ao escolher o treino em "Qual é o seu jogo?", todos os botões passam a enviar "Oi, Pedro! Vim pelo site. " mais o texto do `data-msg` da aba escolhida.
- Etapas do dia de jogo: lista `.etapas` (texto) e as fotos do `#palco`, na mesma ordem.
- Horários: lista `.horarios` e o cálculo do "Aberto agora" no fim do script (seg a sex 8h às 20h; sáb 8h às 12h).
- Cores: variáveis no início do `<style>` (`--carbono`, `--grafite`, `--nevoa`, `--concreto`, `--madeira`, `--ps`, `--neon`).
- Se o endereço final do site mudar, atualize `og:url`, `og:image` e `canonical` no `<head>`.

## A confirmar com o cliente

- Se podemos citar o Desportivo Brasil e o Barça Innovation Hub, e mostrar as fotos do vestiário e do relatório de perda hídrica.
- CRN (não está publicado no Instagram nem no Google).
- Se trabalha com consulta e acompanhamentos de 90 e 180 dias.
- O arquivo original do logo PS.
