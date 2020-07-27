<img alt="GoStack" src="https://storage.googleapis.com/golden-wind/bootcamp-gostack/header-desafios.png" />

<h3 align="center">
  Desafio 11: GoRestaurant Mobile
</h3>

## :rocket: Sobre o desafio

Nesse desafio, foi desenvolvida mais uma aplicação, a GoRestaurant, dessa vez a versão mobile para o cliente. Foi praticado o que foi aprendido até agora no React Native junto com TypeScript, para criar um pequeno app para pedidos de comida.

Essa é uma aplicação que deve se conectar a uma Fake API, exibindo e filtrando os pratos de comida da API e permitindo a criação de novos pedidos.


Primeiramente, deve-se executar o comando `yarn` no terminal para instalar todas as dependências.

### Utilizando uma fake API

Antes de tudo, para que os dados sejam exibidos em tela, há um arquivo que poderá ser utilizado como fake API, para prover esses dados.

Para isso, está instalado no package.json uma dependência chamada `json-server`, e há um arquivo chamado `server.json` que contém os dados para as seguintes rotas:

**Rota `/foods`**: Retorna todas as comidas cadastradas na API;

**Rota `/foods/:id`**: Retorna um prato de comida cadastrado na API baseado no `id`;

**Rota `/categories`**: Retorna todas as categorias cadastradas na API;

**Rota `/orders`**: Retorna todos os pedidos que foram cadastrados na API;

**Rota `/favorites`**: Retorna todas as comidas favoritas que foram cadastradas na API.

Para executar a Fake API basta usar o seguindo comando:

```js
  yarn json-server server.json -p 3333
```

### Layout da aplicação

Essa aplicação possui um layout que você pode seguir para conseguir visualizar o seu funcionamento.

O layout pode ser acessado através da página do Figma, no [seguinte link](https://www.figma.com/file/cHzfYrUBgdzp1XrRuUpggk/GoRestaurant-Mobile?node-id=1603%3A448).

Você precisará uma conta (gratuita) no Figma pra inspecionar o layout e obter detalhes de cores, tamanhos, etc.

### Funcionalidades da aplicação

Deve-se verificar os arquivos da pasta `src` e completar onde não possui código, com o código para atingir os objetivos de cada rota.

- **`Listar os pratos de comida da API`**: A página `Dashboard` deve ser capaz de exibir uma listagem, com o campo `name`, `value` e  `description` de todos os pratos de comida que estão cadastrados na API.

- **`Listar as categorias da API`**: A página `Dashboard` deve ser capaz de exibir uma listagem, com o campo `title` e `image_url` de todas as categorias que estão cadastrados na API.

- **`Filtrar pratos de comida por busca ou por categorias`**: A página `Dashboard` deve permitir que o input de pesquisa e os botões de categoria façam uma busca na API de acordo com o que estiver selecionado ou escrito no input.

- **`Listar os pedidos da API`**: A página `Orders` deve ser capaz de exibir uma listagem, com as informações do produto pedido, contendo `name` e `description` de todos os pedidos que estão cadastrados na API.

- **`Listar os pratos favoritos da API`**: A página `Favorites` deve ser capaz de exibir uma listagem, com as informações do produto favorito, contendo `name` e `description` de todos os pedidos que estão cadastrados na API.

- **`Realizar um pedido`**: Na página `Dashboard`, ao clicar em um item, deve-se redirecionar o usuário para a página `FoodDetails`, onde será possível realizar um novo pedido, podendo controlar a quantidade desse item pedido, ou adicionar ingredientes extras. Todo o valor deve ser calculado de acordo com a quantidade pedida.

### Específicação dos testes

Em cada teste, há uma breve descrição no que a aplicação deve cumprir para que o teste passe.

Para esse desafio, existem os seguintes testes:

- **`should be able to list the food plates`**: Para que esse teste passe, a aplicação deve permitir que sejam listados na `Dashboard`, todos os pratos de comidas que são retornados da fake API.

- **`should be able to list the food plates filtered by category`**: Para que esse teste passe, a aplicação deve permitir que sejam listados na `Dashboard`, os pratos de comidas filtrados por categoria da fake API.

- **`should be able to list the food plates filtered by name search`**:  Para que esse teste passe, a aplicação deve permitir que sejam listados na `Dashboard`, os pratos de comidas filtrados por nome da fake API.

- **`should be able to navigate to the food details page`**: Para que esse teste passe, na `Dashboard`, deve-se permitir que ao clicar em um item, seja navegado para a página `FoodDetails` passando por parâmetro da navegação o `id` do item clicado.

- **`should be able to list the favorite food plates`**: Para que esse teste passe, a aplicação deve permitir que sejam listados na página `Favorites`, todos os pratos de comidas que estão salvos na rota `favorites`.

- **`should be able to list the orders`**: Para que esse teste passe, a aplicação deve permitir que sejam listados na página `Orders`, todos os pratos de comidas que estão salvos na rota `orders`.

- **`should be able to list the food`**: Para que esse teste passe, a aplicação deve permitir que sejam listados todos os dados de uma comída específica na página `FoodDetails`, baseado no `id` recuperado pelos parametros da rota.

- **`should be able to increment food quantity`**: Para que esse teste passe, deve-se permitir que seja incrementada em 1 a quantidade do item na página `FoodDetails`.

- **`should be able to decrement food quantity`**: Para que esse teste passe, deve-se permitir que seja decrementada em 1 a quantidade do item na página `FoodDetails`.

- **`should not be able to decrement food quantity below than 1`**: Para que esse teste passe, deve-se impedir que seja decrementado a quantidade de itens até um número menor que 1, assim o número mínimo de itens no pedido é 1.

- **`should be able to increment an extra item quantity`**: Para que esse teste passe, deve-se permitir que seja incrementada em 1 a quantidade de um ingrediente extra na página `FoodDetails` baseado no seu `id`.

- **`should be able to decrement an extra item quantity`**: Para que esse teste passe, deve-se permitir que seja decrementada em 1 a quantidade de um ingrediente extra na página `FoodDetails` baseado no seu `id`.
