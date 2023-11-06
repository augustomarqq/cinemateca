# Projeto un1 - Desenvolvimento Web 1

Disciplina: Web 1

# Projeto Cinemateca

O projeto foi desenvolvido para proporcionar um ambiente legal e aconchegante onde o usuário pode fazer diversas coisas, como:

- Alternar entre modo claro e modo escuro, de acordo com o botão selecionado no canto superior direito da tela
- Navegar entre os menus dinamicamente, alternando assim as obras a serem exibidas: Filmes, Series, Animes
- Adicionar uma nova obra, seja ela filme, serie ou anime, clicando no botão de Adicionar filme/serie/anime (botão de adicionar muda de acordo com o menu selecionado)
    - Ao clicar em adicionar, é possível inserir título, ano, gênero e url para o poster do filme.
    - Para cadastrar o filme, é necessário preencher todos os campos do form
    - Se o poster não estiver no formato .jpg/.jpeg/.png não é possível finalizar o cadastro
    - Se o usuário desistir de adicionar o filme, pode clicar em cancelar que voltará a exibir o catálogo
- Remover uma obra já presente no catálogo, clicando no botão de lixo dentro do container de cada filme
    - Antes da remoção ser completada, é exibida uma janela de confirmação para excluir definitivamente a obra do catálogo
    - Quando excluída, é exibido um alerta falando que a obra foi removida com sucesso
    - Após isso, a obra removida some do catálogo e as demais obras são reorganizadas

## Destrinchando o main.js

### Bloco 1: Alteração de Modos de Visualização

O código começa com a definição de dois botões ("Modo Claro" e "Modo Escuro") que, quando clicados, alteram o esquema de cores do body e a cor do elemento da página inicial (welcome).

### Bloco 2: Renderização de Obras (Filmes, Séries e Animes)

- Há três funções (**`renderizarFilmes`**, **`renderizarSeries`**, **`renderizarAnimes`**) que criam divs com informações sobre filmes, séries e animes. Cada div contém um botão de remoção e detalhes como título, imagem, ano e gênero.
- Cada função é ativada por botões de menu associados a sua respectiva seção (filmes, séries e animes).
- A função **`renderizarFilmes`** é ativada quando o menu de filmes é clicado, limpando as outras seções e exibindo conteúdo relacionado a filmes.
- O mesmo princípio se aplica às funções **`renderizarSeries`** e **`renderizarAnimes`**, quando os menus de séries e animes são clicados.

### Bloco 3: Botões de Menu

- Cada menu tem um evento de clique associado. Quando clicados, os menus alteram as visualizações, escondendo/mostrando elementos de acordo com o tipo de obra selecionada.

### Bloco 4: Adição e Remoção de Obras

- Existe um botão de adição que abre um formulário para adicionar uma nova obra.
- Há também a possibilidade de remover obras. Quando o botão de remoção é clicado na interface, o usuário é solicitado a confirmar a remoção. Se confirmado, a obra é removida e a lista de obras é atualizada.