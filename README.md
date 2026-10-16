# Velvet Nights

Romance interativo de navegador, em estilo de visual novel, passado no Hotel Velvet — um hotel de luxo que nunca fecha. Tu és o novo concierge do turno da noite. Durante sete noites conheces três mulheres adultas, e as tuas escolhas decidem com quem (e se com alguém) sais da Gala de Veludo.

Tudo está num único ficheiro: **`velvet-nights.html`** (HTML5, CSS3 e JavaScript puro, sem dependências externas nem servidor).

## Como executar

1. Descarrega `velvet-nights.html`.
2. Abre-o com duas vezes clique num navegador moderno (Chrome, Edge, Firefox ou Safari), ou arrasta-o para uma janela do navegador.

Não precisas de servidor nem de internet. O progresso fica gravado no `localStorage` do navegador. Por isso, abre sempre o ficheiro no mesmo navegador e no mesmo caminho. Em modo privado, o jogo funciona, mas as gravações podem não ficar guardadas; nesse caso o jogo avisa.

Se preferires servir o jogo localmente: `python3 -m http.server` na pasta e abre `http://localhost:8000/velvet-nights.html`.

## Personagens

| | Quem é | Onde costuma estar |
|---|---|---|
| **Victoria Ravel**, 34 | Empresária confiante e provocadora, veio comprar o hotel | Velvet Bar, 21:00–02:00 |
| **Luna Moreau**, 27 | Artista misteriosa e brincalhona do quarto 707 | Terraço, 23:00–05:00 |
| **Sophie Duarte**, 25 | Rececionista tímida, com um lado secreto e ousado | Receção até às 00:00; depois em pausa até às 02:00 |

Cada uma tem uma biografia que se revela ao longo da história, cinco capítulos de diálogos exclusivos (dois deles são encontros especiais em locais secretos) e gostos próprios em presentes.

### Retratos

Os retratos são ilustrações vetoriais em SVG inline, geradas em JavaScript dentro do próprio ficheiro, sem imagens externas. São estilizados no registo de visual novel, não realistas. Cada retrato é um busto composto por camadas:

- cabelo de trás, tronco e pescoço, roupa, rosto, feições, franja e acessórios;
- cabelo com madeixas sobrepostas, brilho e fios desenhados;
- olhos com íris em gradiente, pupila, sombra da pálpebra e dois reflexos;
- sombras projetadas pela franja e pelo queixo;
- luz principal quente vinda da esquerda e luz de recorte colorida em cada personagem: carmim na Victoria, turquesa e magenta na Luna, rosa na Sophie.

Há 8 expressões (neutra, sorriso, riso, sorriso de lado, tímida, surpresa, triste e sedutora), com piscar de olhos e respiração animados. Algumas cenas têm variantes de roupa que acompanham a narração: a seda cor de vinho da Victoria na suite, o vestido vermelho e a máscara de renda da Sophie na Sala Escarlate, e a camisa sem colete da Sophie no jardim.

## Mecânicas

- **Diálogo com escolhas múltiplas.** As escolhas alteram a afinidade e ativam marcas que mudam cenas futuras e os finais.
- **Afinidade individual** (0–100), com níveis, barra e progresso por capítulos no painel *Relações*.
- **Relógio e ciclo dia/noite.** Cada turno vai das 20:00 às 06:00. Conversar, deslocar-se, trabalhar e esperar consomem tempo, e o céu muda de cor ao longo da noite. Entre noites há uma fase de dia: descansar (começas às 19:00), fazer um turno extra (+35 €, começas às 21:00) ou passear pela cidade (encontras um presente).
- **Inventário e presentes.** Compras na Boutique Noir (das 18:00 às 03:00) e podes oferecer um presente por noite a cada personagem. Cada uma adora, gosta, é indiferente ou não gosta de cada presente; o que descobres fica registado.
- **Eventos especiais.** Há convites para locais secretos (Suite Presidencial, Estúdio 707, Sala Escarlate e Jardim de Inverno) com janela horária. Se faltares, perdes afinidade e o convite é repetido com uma repreensão. Na noite 4 há um apagão em que escolhes quem ajudar. A Gala é na noite 7.
- **Consequências cruzadas.** Podes revelar o segredo da Luna à Victoria, o que leva a um confronto em que podes pedir desculpa ou mentir. Prometer o coração a mais do que uma personagem leva a um escândalo na Gala.
- **5 finais:** *Coroa de Veludo* (Victoria), *Néon e Tinta Fresca* (Luna), *Primeira Luz* (Sophie), *Última Chamada* (sozinho) e *Coração Dividido* (promessas a mais). Os finais desbloqueados ficam registados no menu inicial.
- **Ícones** dos presentes e da interface desenhados em SVG (sem emojis).
- **Gravação:** 3 espaços manuais e uma gravação automática no fim de cada noite. As gravações corrompidas ou incompatíveis são detetadas, assinaladas e podem ser apagadas.
- **Configurações:** velocidade do texto, avanço automático, tamanho do texto, redução de animações, mostrar ou ocultar alterações de afinidade, e apagar todos os dados.
- **Interface adaptada** a computador e telemóvel. Atalhos: Espaço/Enter avança, 1–4 escolhem, Esc abre o menu.

Conteúdo para maiores de 18 anos: flerte e intimidade sugerida, sem conteúdo explícito.
