# [catenacio21.github.io](https://pueblita01.github.io/catenacio21.github.io/) 
Notas mentales

* Agregando un condicional al setState con BOOLEAN
  
  ```JS
  
   listadoItemsDePedidoElegido = (id) => {
    fetch(`http://localhost:8383/pedido/busqueda/${id}`)
      .then((res) => res.json())
      .then((pedido) =>
        Boolean(pedido)?(
        this.setState({
          pedido: pedido,
          itemsDePedidoElegido: pedido.ItemsPedido,
          itemDePedidoElegido: {},
        })): window.alert("EL pedido no existe o no tiene ItemsPedido")
      );
  };
  
  ```
