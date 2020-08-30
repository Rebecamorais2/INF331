
## Modelo para Apresentação do Lab05 - Subcomponentes e Páginas Dinâmicas

### Tarefa 1
![componentes](https://github.com/Rebecamorais2/INF331/blob/master/lab5/images/Model-View-Control-%20Pedido.PNG)
### Tarefa 2

#### HTML
~~~html
<div id="root"></div>
~~~
#### JAVASCRIPT
~~~~ javascript
class Barra extends React.Component {
  render() {
    let resultado = "";
    for (let b = 0; b <= this.props.tamanho; b++)
      resultado += "=";
    return resultado;
  }
}

const elemento = <div>
                   <Barra tamanho="20"/>
                   <h2> Inicio do dia</h2>
                   <Barra tamanho="20"/>
                   <h2>Fim do dia</h2>
                   <Barra tamanho="20"/>
                 </div>
ReactDOM.render(elemento, 
        document.getElementById("root"));
  ~~~~
