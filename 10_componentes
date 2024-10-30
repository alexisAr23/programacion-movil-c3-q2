                <!-- Component 1: Button -->
        <ion-button @click="showAlert">Click Me</ion-button>

        <!-- Component 2: Input Field -->
        <ion-item>
          <ion-label position="floating">Enter Text</ion-label>
          <ion-input v-model="inputValue"></ion-input>
        </ion-item>

        <!-- Component 3: Card -->
        <ion-card>
          <ion-card-header>
            <ion-card-title>Card Title</ion-card-title>
            <ion-card-subtitle>Card Subtitle</ion-card-subtitle>
          </ion-card-header>
          <ion-card-content>
            {{ cardContent }}
          </ion-card-content>
        </ion-card>

        <!-- Component 4: Toggle -->
        <ion-item>
          <ion-label>Toggle</ion-label>
          <ion-toggle v-model="isChecked"></ion-toggle>
        </ion-item>

        <!-- Component 5: List -->
        <ion-list>
          <ion-item v-for="(item, index) in items" :key="index">{{ item }}</ion-item>
        </ion-list>

        <!-- Component 6: Modal Button -->
        <ion-button @click="openModal">Open Modal</ion-button>

        <!-- Component 7: Range Slider -->
        <ion-item>
          <ion-label>Volume</ion-label>
          <ion-range v-model="rangeValue" min="0" max="100"></ion-range>
        </ion-item>

        <!-- Component 8: Select Dropdown -->
        <ion-item>
          <ion-label>Select Option</ion-label>
          <ion-select v-model="selectedOption" ok-text="Okay" cancel-text="Dismiss">
            <ion-select-option v-for="option in options" :key="option">{{ option }}</ion-select-option>
          </ion-select>
        </ion-item>

        <!-- Component 9: Progress Bar -->
        <ion-progress-bar :value="progress / 100"></ion-progress-bar>
        <p>Progress: {{ progress }}%</p>

        <!-- Component 10: Checkbox -->
        <ion-item>
          <ion-label>Agree to terms</ion-label>
          <ion-checkbox v-model="agreed"></ion-checkbox>
        </ion-item>
      </div>
    </ion-content>
  </ion-page>
</template>

<script setup lang="ts">
import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar, IonButton, IonItem, IonLabel, IonInput, IonCard, IonCardHeader, IonCardTitle, IonCardSubtitle, IonCardContent, IonToggle, IonList, IonRange, IonSelect, IonSelectOption, IonProgressBar, IonCheckbox } from '@ionic/vue';
import { ref } from 'vue';

// Component variables
const inputValue = ref('');
const cardContent = ref('This is an example of a card with Ionic components.');
const isChecked = ref(false);
const items = ref(['Item 1', 'Item 2', 'Item 3']);
const rangeValue = ref(50);
const selectedOption = ref('');
const options = ['Option 1', 'Option 2', 'Option 3'];
const progress = ref(70);
const agreed = ref(false);

// Button Alert
const showAlert = () => {
  alert('Button clicked!');
};

// Modal functionality
const openModal = () => {
  alert('This is a modal placeholder');
};
</script>

<style scoped>
#container {
  text-align: center;
  
  position: absolute;
  left: 0;
  right: 0;
  top: 50%;
  transform: translateY(-50%);
}

#container strong {
  font-size: 20px;
  line-height: 26px;
}

#container p {
  font-size: 16px;
  line-height: 22px;
  color: #8c8c8c;
  margin: 0;
}

#container a {
  text-decoration: none;
}
</style>
