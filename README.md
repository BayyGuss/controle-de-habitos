# Aplicação de Controle de Hábitos

Este projeto é uma aplicação web simples desenvolvida com React puro. Ele permite ao usuário cadastrar hábitos diários, marcar como concluídos e salvar os dados localmente no navegador.

---

## Funcionalidades

- Cadastrar novos hábitos.
- Marcar e desmarcar hábitos como concluídos.
- Remover hábitos da lista.
- Armazenar dados no `localStorage` (persistência entre sessões).
- Interface simples e responsiva.

---

## Tecnologias Utilizadas

- HTML5 – Estrutura semântica da página.
- CSS3 – Estilização básica e responsividade com Flexbox.
- React – Utilizado via CDN para renderização e gerenciamento de estado.
- ReactDOM – Manipulação do DOM virtual.
- Babel – Transpilação de JSX no navegador.
- LocalStorage – Armazenamento de dados no navegador, sem backend.

---

## Estrutura do Projeto

A aplicação está contida em um único arquivo:

```
index.html
```

### Trechos importantes do código:

Importação de bibliotecas via CDN:

```html
<script src="https://unpkg.com/react@18/umd/react.development.js" crossorigin></script>
<script src="https://unpkg.com/react-dom@18/umd/react-dom.development.js" crossorigin></script>
<script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
```

Gerenciamento de hábitos com useState:

```jsx
const [habitos, setHabitos] = useState([]);
const [novoHabito, setNovoHabito] = useState("");
```

Persistência de dados com localStorage:

```jsx
useEffect(() => {
  localStorage.setItem("habitos", JSON.stringify(habitos));
}, [habitos]);
```

---

## Como Executar

1. Clone ou baixe este repositório.
2. Abra o arquivo `index.html` diretamente em qualquer navegador moderno.
3. A aplicação estará pronta para uso.

> Obs.: Não é necessário instalar dependências ou rodar nenhum comando.

---

## Possíveis Melhorias

- Registro de hábitos por data.
- Histórico e gráficos de desempenho.
- Filtro de hábitos concluídos x pendentes.
- Sistema de autenticação para múltiplos usuários.
- Separação em múltiplos componentes React.