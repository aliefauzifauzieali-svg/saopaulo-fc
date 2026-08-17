# São Paulo FC — Design & Engineering Rules

## Objetivo

Este projeto é um site premium e institucional sobre o São Paulo Futebol Clube.

O objetivo é atingir qualidade visual e técnica comparável a sites profissionais de grandes clubes, marcas esportivas premium, estúdios digitais e projetos premiados de Awwwards.

O site já possui conteúdo completo. NÃO substituir, remover ou inventar conteúdo apenas para alterar o design.

O trabalho principal é transformar a apresentação existente em uma experiência visual sofisticada, coerente, rápida, responsiva e memorável.

---

## PRINCÍPIO CENTRAL

Não produzir uma aparência genérica de "site feito por IA".

Evitar:

* layouts genéricos de landing page;
* excesso de cards;
* excesso de gradients;
* excesso de glassmorphism;
* sombras exageradas;
* bordas arredondadas sem propósito;
* animações aleatórias;
* efeitos chamativos sem função;
* excesso de elementos competindo pela atenção;
* componentes visualmente repetitivos;
* texto artificial ou conteúdo inventado;
* alterações desnecessárias na estrutura de conteúdo.

O resultado deve parecer projetado por uma equipe profissional de design e frontend.

Priorizar:

* hierarquia visual;
* composição;
* tipografia;
* ritmo vertical;
* espaçamento;
* contraste;
* fotografia;
* identidade esportiva;
* movimento;
* microinterações;
* performance;
* acessibilidade;
* responsividade.

---

# DIREÇÃO DE DESIGN

Criar uma identidade visual contemporânea, premium, esportiva e editorial.

A estética deve transmitir:

* história;
* tradição;
* competitividade;
* prestígio;
* intensidade;
* modernidade;
* exclusividade.

O São Paulo FC deve ser reconhecível visualmente sem depender de excesso de elementos decorativos.

Usar a identidade tricolor com controle.

O vermelho deve funcionar como cor de destaque, não como preenchimento excessivo de toda a interface.

Preferir superfícies predominantemente claras, escuras ou neutras dependendo da seção, mantendo uma linguagem visual consistente.

---

# REFERÊNCIAS DE QUALIDADE

Buscar o nível de refinamento visual encontrado em:

* sites esportivos premium;
* sites de clubes europeus de alto nível;
* Apple;
* Nike;
* Adidas;
* Linear;
* Vercel;
* projetos premiados de Awwwards;
* estúdios digitais contemporâneos.

NÃO copiar visualmente essas marcas.

Usar apenas como referência de:

* composição;
* tipografia;
* motion design;
* interação;
* ritmo;
* direção de arte;
* qualidade de execução.

---

# ANIMATION SYSTEM

As animações são parte fundamental do design.

Nunca adicionar animações simplesmente porque "ficam bonitas".

Toda animação deve possuir uma intenção visual ou funcional.

Priorizar:

* entradas suaves;
* stagger;
* transformações de estado;
* scroll-driven animation;
* parallax sutil;
* reveal animations;
* text animation;
* image masking;
* clip-path;
* scale;
* opacity;
* spring motion;
* magnetic interactions quando fizer sentido;
* hover states sofisticados;
* transições entre estados;
* continuidade espacial.

As animações devem parecer físicas e deliberadas.

Evitar:

* bounce exagerado;
* easing linear em elementos importantes;
* animações muito rápidas;
* animações muito lentas;
* dezenas de elementos animando simultaneamente;
* efeitos que prejudicam a legibilidade;
* movimento constante sem interação do usuário.

---

# STACK DE ANIMAÇÃO

Utilizar as ferramentas instaladas no projeto de acordo com suas funções.

## GSAP

Usar GSAP para:

* sequências complexas;
* timelines;
* ScrollTrigger;
* scroll-driven animation;
* parallax;
* animações coordenadas;
* SplitText;
* SVG;
* MotionPath;
* transformações complexas;
* animações que precisam de controle temporal preciso.

Não usar GSAP quando CSS ou Motion forem mais apropriados.

## Motion

Usar Motion para:

* microinterações;
* hover;
* tap;
* layout animation;
* presence;
* springs;
* transições de componentes;
* gestos;
* pequenas animações de interface.

## Lenis

Usar Lenis para smooth scrolling quando isso melhorar a experiência.

Integrar corretamente com GSAP ScrollTrigger.

Não criar um sistema de scroll customizado desnecessariamente.

## Three.js / React Three Fiber

Usar somente quando houver benefício visual real.

Possíveis usos:

* elementos 3D;
* partículas;
* ambientes;
* objetos interativos;
* efeitos WebGL;
* backgrounds sofisticados.

Não adicionar 3D apenas para parecer tecnológico.

---

# MOTION PRINCIPLES

Usar easing apropriado ao contexto.

Preferir curvas de movimento naturais e sofisticadas.

Evitar aplicar o mesmo easing para todas as animações.

Criar hierarquia temporal.

Exemplo:

1. container entra;
2. título aparece;
3. subtítulo acompanha;
4. CTA entra depois;
5. imagem termina a composição.

Não fazer todos os elementos aparecerem simultaneamente.

Usar stagger quando houver grupos de elementos relacionados.

Valores de duração devem ser coerentes com a importância do elemento.

Elementos pequenos podem responder rapidamente.

Transições de página e grandes movimentos podem ser mais lentos.

---

# SCROLL EXPERIENCE

O scroll deve parecer uma experiência contínua.

Quando apropriado:

* revelar conteúdo progressivamente;
* usar parallax;
* transformar imagens;
* alterar escala;
* criar sobreposição de seções;
* utilizar pinning;
* criar transições entre blocos;
* controlar ritmo de leitura.

Não transformar o site em um "carrossel de efeitos".

O usuário deve sempre entender onde está e o que está acontecendo.

---

# TYPOGRAPHY

Tipografia deve ser tratada como elemento de design.

Criar hierarquia clara entre:

* display headings;
* headings;
* subheadings;
* body;
* metadata;
* labels;
* navigation.

Usar tamanhos responsivos.

Preferir `clamp()` quando apropriado.

Controlar:

* letter-spacing;
* line-height;
* max-width;
* weight;
* wrapping.

Títulos grandes podem ter tratamento editorial e animação individual de palavras/letras quando isso realmente melhorar a apresentação.

---

# IMAGERY

Fotografias são elementos fundamentais.

Preservar proporções e qualidade.

Usar:

* object-fit;
* máscaras;
* crops intencionais;
* overlays discretos;
* parallax;
* scale transitions;
* reveal animations.

Não colocar imagens em cards genéricos sem necessidade.

Grandes fotografias podem funcionar como elementos editoriais de destaque.

---

# COMPONENT DESIGN

Componentes devem ser:

* reutilizáveis;
* semanticamente corretos;
* responsivos;
* fáceis de manter.

Evitar componentes gigantescos e monolíticos.

Separar componentes quando houver responsabilidade visual ou funcional claramente diferente.

Não duplicar lógica.

Não criar abstrações excessivas apenas por estética de código.

---

# RESPONSIVENESS

Desktop não deve simplesmente ser reduzido para mobile.

Projetar cada breakpoint considerando:

* composição;
* hierarquia;
* navegação;
* tipografia;
* imagens;
* animações;
* touch interaction.

No mobile:

* reduzir complexidade quando necessário;
* preservar a experiência premium;
* remover efeitos pesados quando prejudicarem performance;
* evitar overflow horizontal;
* garantir áreas de toque adequadas.

---

# PERFORMANCE

Performance é prioridade.

Evitar:

* layout thrashing;
* animação de propriedades que causam reflow quando transform/opacity podem ser usados;
* listeners desnecessários;
* renderizações excessivas;
* efeitos WebGL desnecessários;
* imagens gigantes;
* animações executadas continuamente sem necessidade.

Preferir:

* transform;
* opacity;
* GPU-friendly animation;
* lazy loading;
* code splitting;
* otimização de imagens;
* cleanup correto de timelines/listeners.

Respeitar `prefers-reduced-motion`.

Usuários que solicitarem redução de movimento devem receber uma experiência funcional sem animações excessivas.

---

# IMPLEMENTATION RULES

Antes de modificar uma seção:

1. entender sua estrutura atual;
2. identificar o conteúdo existente;
3. preservar informações;
4. identificar problemas visuais;
5. planejar a nova composição;
6. implementar;
7. testar desktop;
8. testar mobile;
9. verificar performance;
10. refinar.

Não destruir uma implementação funcional sem necessidade.

Não trocar tecnologias existentes apenas por preferência pessoal.

Reutilizar infraestrutura existente quando ela estiver adequada.

---

# QUALITY BAR

Antes de considerar uma seção concluída, verificar:

* A hierarquia visual está clara?
* A seção possui uma composição interessante?
* O espaçamento está refinado?
* A tipografia está consistente?
* As animações têm propósito?
* As animações são suaves?
* O timing parece profissional?
* Existe excesso de efeitos?
* O mobile funciona corretamente?
* A experiência continua rápida?
* Há elementos desalinhados?
* Existem inconsistências entre seções?
* Parece um produto profissional ou um template de IA?

Se parecer um template de IA, refinar novamente.

---

# CRITICAL RULE

Não otimizar para quantidade de efeitos.

O objetivo é maximizar:

VISUAL QUALITY × COHERENCE × PERFORMANCE × USABILITY

Uma interface com menos animações, porém perfeitamente coreografadas, é preferível a uma interface cheia de efeitos.

Sempre buscar refinamento, não espetáculo gratuito.
