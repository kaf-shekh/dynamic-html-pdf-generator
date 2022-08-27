we started with convert simple html to pdf 
for that we use <strong>html-pdf</strong> and <strong>fs</strong> library  and now we are going to add one more library for dynamic data binding, <strong>handlebars</strong> 

previuos git repo : <a href="https://github.com/kaf-shekh/html-pdf-generator"></a>

follow below stage:
1. install handlebars library ( npm i handlebars )
2. add library in your index.js file
3. added one const value with my name 
4. in function GeneratePdf we added     
   ``` const template = hbs.compile(htmlContent);

    // it will invoke wherever 'Aname' in html file and return name 
    hbs.registerHelper('Aname',function () {
      return name;
    }) ```

5. And in our htnlodf create function instead of actual html we replace to function on template what we compiled our html
6. in html we put name of our registerHelper name in our case is <i>Aname</i> we add in html in interpolarion (in double curly bracket).
7. we can add multiple registerHelper function  as per requirement can return any thing like checkbox sign images any thing but first we have to convert that in html string (return  '<input type="checkbox"/>' ) like this 
 
 and Done we now run program: node index.js


