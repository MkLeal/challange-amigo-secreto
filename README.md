# Amigo Secreto

Este é um projeto simples para gerenciar uma lista de amigos e sortear um amigo secreto. Ele é feito em HTML, CSS e JavaScript, com funcionalidades dinâmicas como adicionar nomes à lista, exibir os amigos inseridos e realizar o sorteio.

---

## Funcionalidades

1. **Adicionar amigos**:
   - Permite que você insira nomes em um campo de texto.
   - Valida se o campo de texto não está vazio.
   - Exibe um alerta (“Por favor, insira um nome válido”) caso o nome esteja vazio.
   - Atualiza a lista dinâmica de amigos inseridos.

2. **Mostrar lista de amigos**:
   - Exibe todos os amigos adicionados na tela em uma lista.

3. **Sortear amigo secreto**:
   - Escolhe aleatoriamente um nome da lista de amigos adicionados.
   - Exibe o nome sorteado no campo de resultado.
   - Exibe um alerta caso a lista de amigos esteja vazia.

---

## Estrutura de Arquivos

- **index.html**: Contém a estrutura do projeto, incluindo o campo de entrada, botães e listas.
- **style.css**: Arquivo para estilização visual do projeto.
- **app.js**: Contém a lógica e as funções JavaScript para interatividade.

---

## Como Usar

1. Clone o repositório ou copie os arquivos.
2. Abra o arquivo `index.html` em um navegador.
3. Use os seguintes recursos:
   - Insira o nome de um amigo no campo de entrada e clique no botão “Adicionar” para adicioná-lo à lista.
   - Clique em “Sortear amigo” para realizar o sorteio aleatório entre os nomes adicionados.

---

## Estrutura de Funções

### `adicionarAmigo()`
- Captura o nome inserido no campo de texto.
- Valida se o campo não está vazio.
- Adiciona o nome ao array `amigos`.
- Chama a função `mostrarNomesDosAmigos()` para atualizar a lista na tela.

### `mostrarNomesDosAmigos()`
- Atualiza o conteúdo do elemento `<ul>` com os nomes da lista de amigos.
- Gera cada nome dentro de uma tag `<li>`.

### `sortearAmigo()`
- Valida se a lista de amigos não está vazia.
- Seleciona um nome aleatoriamente usando `Math.random`.
- Exibe o nome sorteado no campo de resultado ou um alerta caso a lista esteja vazia.

---

## Exemplo de Código HTML
```html
<ul id="listaAmigos" class="name-list" aria-labelledby="listaAmigos" role="list"></ul>
<ul id="resultado" class="result-list" aria-live="polite"></ul>
```

## Exemplo de Código JavaScript
```javascript
function adicionarAmigo() {
    const inputNome = document.getElementById('amigo');
    const nome = inputNome.value.trim();
  
    if (nome === '') {
        alert('Por favor, insira um nome válido.');
        return;
    }

    amigos.push(nome);
    inputNome.value = '';
    mostrarNomesDosAmigos();
}
```

---

## Tecnologias Utilizadas

- **HTML**: Estrutura da aplicação.
- **CSS**: Estilização visual (não incluído no exemplo acima).
- **JavaScript**: Lógica e funcionalidades dinâmicas.

---

## Melhorias Futuras

- Implementar a opção de remover amigos da lista.
- Permitir salvar a lista localmente usando `localStorage`.
- Adicionar animações para feedback visual ao adicionar nomes ou sortear.

---

## Autor
Este projeto foi criado como um exemplo prático de funcionalidades básicas em JavaScript. Sinta-se à vontade para melhorar e personalizar!

