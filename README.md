# Próxima Sessão

CP4 de Web Development: descubra filmes e séries e guarde suas próximas escolhas em uma lista pessoal.

## Integrantes

 Isaac Ambrozevicius - RM569166
 João Lucca - RM569562

## Problema e solução

As pessoas se preparam pra assisitr um filme, pipoca, cobertor até um date...  Mas não sabem que filme assistir. O Próxima Sessão reúne todos os filmes disponíveis filtrados por categorias que o usuário possa gostar, pra finalmente fazer a escolha certa.

## Funcionalidades

- Home com filmes e séries populares da TMDB.
- Busca por nome.
- Detalhes com pôster, sinopse, gêneros, ano, nota e opções de onde assistir.
- Minha Lista: adicionar pelos detalhes, consultar e remover títulos.
- Persistência no navegador com localStorage, sem entradas duplicadas.
- Layout responsivo para todos os disposítivos e navegadores.


## Tecnologias

- React e React DOM, com JavaScript e JSX.
- Vite para desenvolvimento e build.
- HTML e CSS tradicional (flexbox, grid e media queries).
- React Router (`react-router-dom`) para navegação e rota dinâmica.
- `useState`, `useEffect`, componentes funcionais e props.
- Boxicons para ícones da interface.
- API TMDB via `fetch` e `localStorage` para a lista.

## Como executar

```bash
npm i
```

### Configurar a API

1. Acesse o TMBD(https://www.themoviedb.org/settings/api) e obtenha a **chave de API**.
2. Crie um arquivo .env e coloque sua chave de API
3. Preencha a variável com sua chave:

```env
VITE_TMDB_API_KEY=sua_chave_api_v3
```



```bash
npm run dev
```


## API utilizada

Base: `https://api.themoviedb.org/3`.

| Endpoint | Uso |
| `/movie/popular` | Filmes populares. |
| `/tv/popular` | Séries populares. |
| `/search/multi` | Busca por nome; pessoas são descartadas dos resultados. |
| `/movie/:id` | Detalhes de um filme. |
| `/tv/:id` | Detalhes de uma série. |
| `/:type/:id/watch/providers` | Provedores e modalidades de exibição por região. |

As consultas são feitas em Português.


## Como a lista funciona

A chave `proxima-sessao-lista` do `localStorage` guarda um array de títulos. Um filme e uma série são identificados pela combinação de tipo e ID. A lista aparece como atualizada somente depois que a escrita no navegador é confirmada.


## Uso de IA

A IA foi utilizada como ferramenta de apoio para desenvolvimento, mais na parte da integração com a API e resolução de dúvidas.

## Publicação e links

Vercel: [inserir link]
