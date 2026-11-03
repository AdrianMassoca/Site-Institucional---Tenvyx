# TENVYX — Site institucional em Vue 3

Projeto reconstruído em Vue 3 + Vite, com identidade visual futurista em roxo, azul e fundo escuro.

## Requisitos
- Node.js 20.19+ ou 22.12+
- npm

## Como executar
1. Extraia o arquivo ZIP.
2. Abra a pasta `tenvyx-vue3` no Visual Studio Code.
3. Abra o terminal na pasta do projeto.
4. Execute:

```bash
npm install
npm run dev
```

5. Acesse o endereço local mostrado pelo Vite (normalmente `http://localhost:5173`).

## Gerar versão de produção

```bash
npm run build
npm run preview
```

Os arquivos finais serão gerados na pasta `dist/`.

## Configuração do Vite
O arquivo `vite.config.js` registra `@vitejs/plugin-vue`, necessário para o Vite compilar arquivos `.vue`.

## Estrutura
- `src/App.vue`: composição geral da página.
- `src/components/`: seções e componentes reutilizáveis.
- `src/composables/useReveal.js`: animações de entrada com IntersectionObserver.
- `src/style.css`: identidade visual, responsividade e animações.
- `public/images/`: logotipo e imagem de fundo originais.

## Funcionalidades incluídas
- Menu fixo com estado visual de rolagem e menu mobile.
- Navegação por âncoras e indicação da seção ativa.
- Hero com elementos orbitais e cartões flutuantes.
- Cards de serviços com efeitos hover.
- Dashboard ilustrativo para apresentar inteligência operacional.
- Linha do tempo do processo de desenvolvimento.
- Seção institucional e formulário demonstrativo.
- Animações de entrada com IntersectionObserver.
- Respeito à preferência `prefers-reduced-motion`.

## Importante sobre o formulário
O formulário valida os campos no navegador, mas ainda não envia mensagens nem salva dados. Para uso real, conecte-o a uma API/backend ou serviço de formulários e atualize o feedback da interface.

## Conteúdo institucional
Os textos foram organizados a partir das informações presentes no HTML original. Afirmações como métricas, clientes, cases, certificações e resultados não foram inventadas. O painel é explicitamente identificado como demonstração visual.
