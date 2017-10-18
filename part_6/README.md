# Part 6: Partials - Header and Footer
## Goal: Implement common code in reusable ejs template files with html fragments

1. Create a directory in views called ‘partials’. We can put template files in here that we want to reuse in different pages
2. Create two templates in partials, header.ejs, and footer.ejs
3. header.ejs
    * Should contain all of the links/scripts/css that your pages need
    * Should contain the title and nav bar for the site
4. footer.ejs
    * Should contain the footer content
5. Convert any remaining html pages into templates (e.g. index.ejs, about.ejs, contact.ejs)
6. Create end points for each of the other pages on your site (e.g. / → index.ejs, /about → about.ejs, /contact → contact.ejs)
7. Use the HTML content from each of your web pages as starter for the templates
8. Replace all of the duplicate code for the header by moving it to header.ejs and using: <% include header %> in your template files 
9. Do the same for the footer
