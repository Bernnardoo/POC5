
# POC - React Native com Next.js

Esta POC tem como objetivo ilustrar conceitos fundamentais de React e Next.js, usando a versão 14 ou superior do Next.js. Vamos abordar:

- Estrutura do projeto
- Criação de componentes simples (sem estado)
- Uso de CSS (global e módulos)

## Estrutura do Projeto

O projeto segue a estrutura padrão do Next.js:

```
my-nextjs-project/
├── components/
│   └── SimpleComponent.js
├── pages/
│   ├── index.js
├── styles/
│   ├── globals.css
│   └── SimpleComponent.module.css
├── package.json
├── README.md
└── next.config.js
```

### Descrição dos Diretórios:

- **components/**: Onde ficam os componentes React reutilizáveis.
- **pages/**: Contém as rotas do Next.js. Cada arquivo dentro deste diretório representa uma página no app.
- **styles/**: Contém o CSS global e os módulos CSS para componentes específicos.

## Conceitos Abordados

### 1. Estrutura de Projeto (Next.js 14 ou superior)
Next.js segue uma estrutura bem organizada que facilita o desenvolvimento de aplicações web, permitindo uma separação clara de responsabilidades entre componentes, páginas, e estilos.

### 2. Criação de Componentes Simples (Sem Estado)
Abaixo, temos um exemplo de um componente simples, `SimpleComponent`, que não possui estado:

```jsx
// components/SimpleComponent.js
import styles from '../styles/SimpleComponent.module.css';

const SimpleComponent = () => {
  return (
    <div className={styles.container}>
      <h1>Hello, Next.js!</h1>
      <p>Este é um componente simples em React.</p>
    </div>
  );
};

export default SimpleComponent;
```

### 3. Uso de CSS Global e CSS Module
- **globals.css**: Define estilos globais aplicados a toda a aplicação.
- **CSS Modules**: Usado para aplicar estilos isolados a componentes específicos. No exemplo acima, o arquivo `SimpleComponent.module.css` é responsável por estilizar o componente `SimpleComponent`.

Exemplo de CSS Global:

```css
/* styles/globals.css */
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background-color: #f0f0f0;
}
```

Exemplo de CSS Module:

```css
/* styles/SimpleComponent.module.css */
.container {
  text-align: center;
  margin-top: 50px;
}

h1 {
  color: #0070f3;
}
```

## Como Rodar o Projeto

1. Clone o repositório:
   ```
   git clone https://github.com/seu-usuario/seu-repo.git
   cd my-nextjs-project
   ```

2. Instale as dependências:
   ```
   npm install
   ```

3. Inicie o servidor de desenvolvimento:
   ```
   npm run dev
   ```

4. Acesse [http://localhost:3000](http://localhost:3000) para visualizar a aplicação.
