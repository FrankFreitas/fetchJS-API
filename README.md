# Documentação do Script JavaScript

## Estrutura HTML

1. **Divs e Containers:**
   - `loadingElement`: Elemento de carregamento.
   - `postsContainer`: Container para exibir todas as postagens.
   - `postPage`: Página individual de postagem.
   - `postContainer`: Container para exibir detalhes de uma postagem.
   - `commentsContainer`: Container para exibir os comentários de uma postagem.

2. **Formulário de Comentário:**
   - `commentForm`: Formulário para enviar novos comentários.
   - `emailInput`: Campo de entrada para o endereço de e-mail do comentário.
   - `bodyInput`: Campo de entrada para o corpo do comentário.

## Funções JavaScript

1. **`getAllPosts` Function:**
   - Obtem todas as postagens da API JSONPlaceholder.
   - Cria elementos HTML para cada postagem e os adiciona ao `postsContainer`.

2. **`getPost` Function:**
   - Obtem uma postagem específica e seus comentários associados.
   - Cria elementos HTML para exibir o título e o corpo da postagem no `postContainer`.
   - Cria elementos HTML para cada comentário e os adiciona ao `commentsContainer`.

3. **`createComment` Function:**
   - Cria elementos HTML para exibir os detalhes de um comentário.

4. **`postComment` Function:**
   - Envia um novo comentário para a API JSONPlaceholder usando o método POST.
   - Exibe o novo comentário na página.

### Lógica Principal

- O código verifica se há um parâmetro `id` na URL (através de `URLSearchParams`). Se existir, ele chama a função `getPost` para exibir detalhes da postagem individual e permite a adição de comentários.
- Se não houver um `id`, ele chama a função `getAllPosts` para exibir todas as postagens.

### Fluxo de Execução

1. **Obter Todos os Posts:**
   - Se não houver um `id` na URL, chama `getAllPosts` para obter e exibir todas as postagens.

2. **Obter Post Individual:**
   - Se houver um `id` na URL, chama `getPost` para obter e exibir detalhes da postagem específica.
   - Habilita a funcionalidade de comentários, permitindo que os usuários adicionem novos comentários.

### Comentários

- O código possui mensagens de log (`console.log`) para registrar as respostas da API e os dados processados.
- O formulário de comentário tem um evento de envio que chama a função `postComment` para enviar um novo comentário.

**Observação:** Este código presume que você tenha uma estrutura HTML correspondente com os elementos e IDs mencionados no script. Certifique-se de que seu HTML inclua esses elementos ou faça as devidas modificações no código para se adequar à sua estrutura HTML específica.

