# jsecommerce

1.)Create Folder Structure
create root folder as jsecommerce
add frontend and backend folder
create src folder in frontend
create index.html with heading jsecommerce in src
run npm init in frontend folder
npm install live-server
add start command as live-server src --verbose
run npm start
check result

2.Design Website
create style.css
link style.css to index.html
create div.grid-container
create header, main and footer
style html, body
style grid-container, header, main and footer

3.Create Static Home Screen
create ul.products
create li
create div.product
add .product-image, .product-name, .product-brand, .product-price
style ul.products and internal divs
duplicate 2 times to show 3 products

4.Render Dynamic Home Screen

create data.js
export an array of 6 products
create screens/HomeScreen.js
export HomeScreen as an object with render() method
implement render()
import data.js
return products mapped to lis inside an ul
create app.js
link it to index.html as module
set main id to main-container
create router() function
set main_container innerHTML to HomeScreen.render()
set load event of window to router() function

5.Build Url Router
create routes as route:screen object for home screen
create utils.js
export parseRequestURL()
set url as hash address split by slash
return resource, id and verb of url
update router()
set request as parseRequestURL()
build parsedUrl and compare with routes
if route exists render it, else render Error404
create screens/Error404.js and render error message

6.Create Node.JS Server
run npm init in root jsamazona folder
npm install express
create server.js
add start command as node backend/server.js
require express
move data.js from frontend to backend
create route for /api/products
return products in data.js
run npm start

7.Load Products From Backend
edit HomeScreen.js
make render async
fetch products from '/api/products' in render()
make router() async and call await HomeScreen.render()
use cors on backend

webpack:To manage js files and merge them inside one single js file to
serve by webserver.
if you use webpack --> In network --> js --> we have only one file.
otherwise we have some many files.
benefits:

---

1.It increase speed
2.npm packages

axios: Its a ajax request tool

8.Add Webpack
cd frontend
npm install -D webpack webpack-cli webpack-dev-server
npm uninstall live-server
"start": "webpack-dev-server --mode development --watch-content-base --open"
move index.html, style.css and images to frontend folder
rename app.js to index.js
update index.html
add <script src="main.js"></script> before
npm start
npm install axios
change fetch to axios in HomeScreen

9.Install Babel For ES6 Syntax
npm install -D babel core, cli, node, preset-env
Create .babelrc and set presets to @babel/preset-env
npm install -D nodemon
set start: nodemon --watch backend --exec babel-node backend/server.js
convert require to import in server.js
npm start

Babel compiler: for converting es6 code in backend to es5 which can
be run on node js.
