# Teste de Entrevista para Desenvolvedor Front-end (React & Next.js)

## Visão Geral do Projeto

Crie uma aplicação de navegação de filmes usando React e Next.js, integrando com a API do The Movie Database (TMDB). A aplicação deve permitir que os usuários loguem e naveguem por filmes, pesquisem títulos específicos, favoritem os filmes e naveguem através de resultados paginados.

## Design

A aplicação deve seguir de perto o design fornecido no Figma. Certifique-se de que todos os componentes, layouts e estilos correspondam às especificações do design.

Acesse o design: [https://www.figma.com/design/Lpio0PeEzVsTLgzI4wYYa1/Teste-Frontend?node-id=0-1&t=YbSE4ccHuhlfQUqV-1](Figma)

## Tecnologias Requeridas

- React 18+
- Next.js 14+ (App Router)
- Next Fetch ( Sem react query )
- TypeScript
- Shadcn UI - ( Recomendação - Opcional )
- Tailwind CSS para estilização
- ESLint para linting de código
- Prettier para formatação de código

## Integração com API

- Use a API do TMDB para buscar dados de filmes e realizar a autenticação. Você precisará se cadastrar para obter uma chave de API em [https://www.themoviedb.org/documentation/api](https://www.themoviedb.org/documentation/api) ;
- Para segurança adicione um env para armazenar dados importantes como: baseURLs, chaves ou criptografias.

## Funcionalidades a Implementar

1. **Listagem de Filmes**
   - Liste os filmes que estão sendo vistos no momento;
   - Liste os filmes populares;
   - Mostre o título do filme, ano de lançamento e classificação para cada filme;
   - Ao clicar no filme, o usuário deve ser levado para a tela de detalhes do filme.

2. **Funcionalidade de Pesquisa**
   - Adicione uma barra de pesquisa que permita aos usuários buscar filmes por título;
   - Ao clicar no filme, o usuário deve ser levado para a tela de detalhes do filme;
   - Implemente paginação para os resultados da pesquisa.

3. **Detalhes do Filme**
   - Crie uma página separada para exibir informações detalhadas sobre um filme selecionado;
   - Inclua pôster do filme, título, sinopse, data de lançamento, classificação e gêneros assim como no design proposto;
   - Adicione um botão para favoritar o filme e assim ser adicionado a lista de filmes favoritados;
   - O botão só deve favoritar caso o usuário esteja logado na sessão. Caso não esteja, redirecionar para tela de login.

4. **Paginação**
   - Implemente paginação tanto para a lista principal de filmes quanto para os resultados da pesquisa;
   - Use o `fetch` nativo do Next.js para busca de dados (não use React Query).

5. **Login e Controle de Sessão**
   - Implemente um sistema de login utilizando a API de autenticação do TMDB;
   - Crie uma página de login onde os usuários possam inserir suas credenciais;
   - Implemente o controle de sessão, mantendo o usuário logado entre as páginas;
   - Adicione um botão de logout que encerre a sessão do usuário;
   - Restrinja o acesso a certas funcionalidades apenas para usuários logados (por exemplo, favoritar filmes);
   - Faça um middleware para o gerenciamento das rotas que o usuário deve ou não ter permissão após ou não estar logado.

## Diretrizes de Implementação

1. **Estrutura do Projeto**
   - Use o App Router do Next.js 14+ para roteamento;
   - Organize seu código em diretórios apropriados.
   - Adicione no seu ts.config: "noImplicitAny": true, "noUnusedLocals": true, "noUnusedParameters": true,

2. **Integração com API**
   - Crie uma função utilitária para lidar com requisições à API usando o `fetch` do Next.js junto das variáveis de ambiente;
   - Implemente tratamento de erros adequado para as requisições à API;
   - Crie server actions caso necessário;
   - Utilize a API de autenticação do TMDB para gerenciar o login e a sessão do usuário.

3. **Paginação**
   - Implemente a paginação usando parâmetros de URL
   - Atualize a URL ao mudar de página ou realizar pesquisas

4. **Funcionalidade de Pesquisa**
   - Implemente debounce para o input de pesquisa para minimizar chamadas desnecessárias à API
   - Atualize a URL com os parâmetros de pesquisa

5. **Estilização**
   - Use Tailwind CSS para estilizar os componentes
   - Garanta que a aplicação seja responsiva e funcione bem em dispositivos móveis

6. **Performance**
   - Implemente estados de carregamento adequados para requisições à API
   - Use o componente Image nativo do Next.js para otimização de carregamento de imagens

7. **Qualidade do Código**
   - Use TypeScript para verificação de tipos
   - Siga as melhores práticas de React e Next.js
   - Escreva código limpo, bem documentado e de fácil manutenção

8. **Autenticação e Controle de Sessão**
   - Utilize cookies ou localStorage para armazenar o token de sessão de forma segura
   - Implemente um middleware ou HOC para proteger rotas que requerem autenticação
   - Gerencie o estado global da autenticação (por exemplo, usando Context API ou Redux)

## Critérios de Avaliação

Sua submissão será avaliada com base nos seguintes critérios:

1. Aderência ao design fornecido no Figma;
2. Implementação correta das funcionalidades requeridas;
3. Qualidade do código, organização e melhores práticas React e Next.js;
4. Uso efetivo do TypeScript;
5. Design responsivo e compatibilidade cross-browser;
6. Técnicas de performance e otimização;
7. Tratamento de erros e gerenciamento de redirecionamentos;
8. Componentização: criação de componentes reutilizáveis e bem estruturados;
9. Reutilização de código: implementação de lógica e componentes de forma a maximizar a reutilização;
10. Implementação correta e segura do sistema de autenticação e controle de sessão;

## Diretrizes de Submissão

1. Crie um novo repositório no GitHub para o seu projeto;
2. Implemente as funcionalidades requeridas;
3. Inclua um arquivo README.md com instruções sobre como executar o projeto localmente;
4. Forneça qualquer documentação necessária para o seu código; (Exemplo: .env)
5. Envie o link do seu repositório no GitHub;
6. Faça o deploy do projeto em qualquer plataforma de nuvem e disponibilize o link.
