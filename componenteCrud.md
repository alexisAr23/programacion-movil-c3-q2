[!Captura de pantalla = ![alt](pantallaCrud.png)]

<template>
  <!-- Contenedor Principal -->
  <div id="app">
    <!-- Título de la Tienda -->
    <h1>TIENDA ALEXIS</h1>

    <!-- Componente CRUD para Productos -->
    <CrudSection
      title="Productos"
      :items="productos"
      new-item-placeholder="Añadir nuevo producto"
      @add="addProducto"
      @update="updateProducto"
      @delete="deleteProducto"
    />

    <!-- Componente CRUD para Clientes -->
    <CrudSection
      title="Clientes"
      :items="clientes"
      new-item-placeholder="Añadir nuevo cliente"
      @add="addCliente"
      @update="updateCliente"
      @delete="deleteCliente"
    />

    <!-- Componente CRUD para Número de Teléfono -->
    <CrudSection
      title="Número de Teléfono"
      :items="telefonos"
      new-item-placeholder="Añadir nuevo número de teléfono"
      @add="addTelefono"
      @update="updateTelefono"
      @delete="deleteTelefono"
    />

    <!-- Botón de Finalizar Pedido -->
    <button @click="finalizeOrder" class="btn-finalize">Pedido Realizado</button>
  </div>
</template>

<script>


export default {
  data() {
    return {
      productos: [],
      clientes: [],
      telefonos: [],
      newProducto: "",
      newCliente: "",
      newTelefono: "",
    };
  },
  methods: {
    addProducto() {
      if (this.newProducto.trim()) {
        this.productos.push({ id: Date.now(), name: this.newProducto.trim() });
        this.newProducto = "";
      }
    },
    updateProducto(id, name) {
      const producto = this.productos.find((p) => p.id === id);
      if (producto) producto.name = name;
    },
    deleteProducto(id) {
      this.productos = this.productos.filter((p) => p.id !== id);
    },

    addCliente() {
      if (this.newCliente.trim()) {
        this.clientes.push({ id: Date.now(), name: this.newCliente.trim() });
        this.newCliente = "";
      }
    },
    updateCliente(id, name) {
      const cliente = this.clientes.find((c) => c.id === id);
      if (cliente) cliente.name = name;
    },
    deleteCliente(id) {
      this.clientes = this.clientes.filter((c) => c.id !== id);
    },

    addTelefono() {
      if (this.newTelefono.trim()) {
        this.telefonos.push({ id: Date.now(), number: this.newTelefono.trim() });
        this.newTelefono = "";
      }
    },
    updateTelefono(id, number) {
      const telefono = this.telefonos.find((t) => t.id === id);
      if (telefono) telefono.number = number;
    },
    deleteTelefono(id) {
      this.telefonos = this.telefonos.filter((t) => t.id !== id);
    },

    finalizeOrder() {
      alert("¡Pedido realizado con éxito!");
    },
  },
};
</script>

