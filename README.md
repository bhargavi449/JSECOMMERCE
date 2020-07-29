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
