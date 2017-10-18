# Part 8: Search Blogs
## Goal: Add a search bar that will allow a user to search the blog posts

1. Update the header template to include a search bar with a search icon (use a glyphicon from bootstrap or from font-awesome)
2. Pressing enter, or clicking on the search icon will initiate a search. You can use jQuery to add an event handler for the enter/click
3. On your server, create an endpoint for searching: GET /search?q=searchterm
4. Using the search terms received, search the array of blog posts to find any blog post that contains the searchterm in the title, or the tags. You should have a new array that contains the BlogPosts that were found.
5. Pass the filtered BlogPosts to the blog.ejs template as data. If no blog posts are found, you should display a message “No Blog Posts Found” on the web page
