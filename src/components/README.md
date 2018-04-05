# **Form component Vue.js**

This vue component allows you to build a customizable form for different styles with base in bootstrap

## **Getting Started**

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### **Prerequisites** 

You should download the component from the folder "src/components/form.vue"

### **Installing**
A step by step series of examples that tell you have to get a development env running
1. Paste the component into your components folder.

2. Import with "import formulario from './components/form'" wherever you need to use the component.

3.  Add the component to "Components".

4. Preset an object from this specifing what you need: 
    ```javascript
    info:{
          username: true||false,
          email: true||false,
          tel: true||false,
          pass: true||false,
          time: true||false,
          color: true||false,
          date: true||false,
          isBoostrap: true||false
        },
        usuario: {}
    ```
5. Set at your template:
```
<formulario :info="info" @usuario="printuser"/>
```

6.  Add this method to your methods: 
```javascript
printuser: function(val) {
      this.usuario=val;
        console.log(this.usuario);
    }
```
7. At "usuario" object you will have all the information from the form.

8. To use your own style is only permitted bootstrap, materialize. Adding true or false to isBootstrap var. To add [bootstrap](https://www.bootstrapcdn.com/) or [materialize](http://materializecss.com/getting-started.html) add their cdn's.

## **Demo**
![demostracion](https://gyazo.com/526ff9e5ebc5de891f059611f1185da8.gif)

## **Built with**

* Vue.Js 
* Bootstrap

## **Version** 
BETA v1.00

## **Authors**
* **Eleazar Pérez Arencibia**
* **David González Concepción**
* **Fran González Torres**
* **Christian Perera Duran**

## **License**

Open Source

