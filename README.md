# hello-world-v2

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

### Visualizar proyecto en Netlify:
[vue-hello-banco](https://banco-vue-pruebagc.netlify.app/)

### Visualizar proyecto en Host compartido:
[vue-hello-banco](https://vue1.giancode.com/)

Proximamente se estara actualizando este proyecto con mas contenido de vue

Si deseas subir este proyecto en algun servidor:

## Proyecto Vue js en servidor NGINX, ubuntu server
skills: HTML--JAVASCRIPT--VUE JS--GIT/GITHUB--NGINX--NODE JS

```
sudo apt update
sudo apt upgrade
```
### Instalar Node mediante NVM
Referencia: [Cómo instalar Node.js en Ubuntu 20.04](https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-20-04-es)
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.37.2/install.sh | bash
source ~/.bashrc
nvm
nvm list-remote
nvm install node --lts

node --version
```
### NPM Instalación
```
sudo apt install npm
npm --version
```
### Git en linux, mas email y username
```
sudo apt install git
git config --global user.email="tu_email@gmail.com"
git config --global user.name "tu_username"

```
### NGINX instalación
```
sudo apt install nginx
# abrir un navegador y poner dirección ip del servidor, se debe visualizar página de nginx
```
### Clonar este proyecto a tu servidor
```
cd /var/www/html
git clone https://github.com/giancode1/vue-hello-banco.git
```
### Instalar dependencias del proyecto
```
cd vue-hello-banco
npm i
npm run build    #te crea la carpeta dist con el deploy del proyecto
```
### NGINX configuración
```
cd /etc/nginx/sites-available
sudo nano default
# modificar linea a: root /var/www/html/vue-hello-banco/dist
#debajo de server_name; agregar linea: error_page 404 /;
#basicamente esa linea sirve para que las direcciones de vue funcionen bien

sudo nginx -t
sudo service nginx restart
```
### Visualizar proyecto
Asegurarse que nginx esta corriendo
```
sudo service nginx status
```
Finalmente abre una pestaña en un navegador con la dirección ip del servidor

