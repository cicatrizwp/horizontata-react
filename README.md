## HorizonTATA

## React Hooks - Intro 

- Abra o arquivo `Apps.tsx` localizado em `/src`;
- Apague o conteúdo da linha 3 até a linha 11;
- Adicione o trecho de código:
```
const App = () => {
  const [count, setCount] = React.useState(0);

  return (
    <div>
      <p>Você clicou {count} vezes</p>
      <button onClick={() => setCount(count + 1)}>
        Clica ai
      </button>
    </div>
  );
}
```
- Faça o teste no navegador;
- Agora faça uma nova alteração no código do `App.tsx`:
```
const App = () => {
  const [count, setCount] = React.useState(0);
  
  React.useEffect(() => {
    document.title = `Você clicou ${count} vezes`;
  });
  
  return (
    <div>
      <p>Você clicou {count} vezes</p>
      <button onClick={() => setCount(count + 1)}>
        Clica ai
      </button>
    </div>
  );
}
```
- Faça o teste no navegador;
- Vamos otimizar nosso último código, adicionando uma condição para o hook `useEffects`:
```
const App = () => {
  const [count, setCount] = React.useState(0);
  
  React.useEffect(() => {
    document.title = `Você clicou ${count} vezes`;
  }, [count]);
  
  return (
    <div>
      <p>Você clicou {count} vezes</p>
      <button onClick={() => setCount(count + 1)}>
        Clica ai
      </button>
    </div>
  );
}
```

Agora você sabe como funcionam os Hooks de `useState`e `useEffect`, os mais importantes para iniciar os estudos e seus projetos!
