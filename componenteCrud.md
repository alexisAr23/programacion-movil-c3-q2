# Create the content for the markdown file with CRUD components for Ionic Vue

crud_markdown_content = """
# Ionic Vue CRUD Components

## 1. IonInput (for Create and Update)
This component is used to capture user input when creating or updating a record.

```html
<ion-item>
  <ion-label position="floating">Name</ion-label>
  <ion-input v-model="formData.name" placeholder="Enter name"></ion-input>
</ion-item>

<ion-list>
  <ion-item v-for="(item, index) in items" :key="index">
    <ion-label>{{ item.name }}</ion-label>
    <ion-button @click="editItem(item)">Edit</ion-button>
    <ion-button color="danger" @click="deleteItem(item)">Delete</ion-button>
  </ion-item>
</ion-list>

<ion-button color="danger" @click="deleteItem(item)">
  Delete
</ion-button>
