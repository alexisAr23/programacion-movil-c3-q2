<ion-page>
  <ion-header :translucent="true">
    <ion-toolbar>
      <ion-title>Presentacion de Semilleros y registros</ion-title>
    </ion-toolbar>
  </ion-header>

  <ion-content :fullscreen="true">
    <ion-header collapse="condense">
      <ion-toolbar>
        <ion-title size="large">Registro</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-list class="expanded-list">
      <ion-item class="expanded-item">
        <ion-select
          label="Semilleros"
          placeholder="Selecciona un Semillero"
          color="danger"
          class="expanded-select"
        >
          <ion-select-option value="Innovacion">Innovacion</ion-select-option>
          <ion-select-option value="Inteligencia Artificial">Inteligencia Artificial</ion-select-option>
          <ion-select-option value="Proteccion Ambiental">Proteccion Ambiental</ion-select-option>
        </ion-select>
      </ion-item>

      <ion-item class="expanded-item">
        <ion-label position="floating">Nombre y Apellido</ion-label>
        <ion-input type="text" class="expanded-input"></ion-input>
      </ion-item>

      <ion-item class="expanded-item">
        <ion-label position="floating">Número de teléfono</ion-label>
        <ion-input type="tel" class="expanded-input"></ion-input>
      </ion-item>

      <ion-item class="expanded-item">
        <ion-select
          label="Semestre al que perteneces"
          label-placement="floating"
          class="expanded-select"
        >
          <ion-select-option value="1-3 Semestre">1-3 Semestre</ion-select-option>
          <ion-select-option value="3-7 Semestre">3-7 Semestre</ion-select-option>
          <ion-select-option value="7-10 Semestre">7-10 Semestre</ion-select-option>
        </ion-select>
      </ion-item>

      <ion-item class="expanded-item">
        <ion-label>Califica tu semillero</ion-label>
        <ion-select class="expanded-select">
          <ion-select-option value="1">1</ion-select-option>
          <ion-select-option value="2">2</ion-select-option>
          <ion-select-option value="3">3</ion-select-option>
          <ion-select-option value="4">4</ion-select-option>
          <ion-select-option value="5">5</ion-select-option>
          <ion-select-option value="6">6</ion-select-option>
          <ion-select-option value="7">7</ion-select-option>
          <ion-select-option value="8">8</ion-select-option>
          <ion-select-option value="9">9</ion-select-option>
          <ion-select-option value="10">10</ion-select-option>
        </ion-select>
      </ion-item>
    </ion-list>

    <div class="button-container">
      <ion-button id="registro-alert" color="danger" expand="block">Registrarse</ion-button>
      <ion-alert
        trigger="registro-alert"
        message="Gracias por registrarse"
        :buttons="alertButtons"
      ></ion-alert>
    </div>
  </ion-content>
</ion-page>
