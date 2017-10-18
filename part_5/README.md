# Part 5: Dynamic Urls and Blog Posts
## Goal: Use EJS to track blog posts on the Web Server and display blogs on their own pages

1. Install EJS on your express server
2. Use app.set to configure express to use EJS
3. Create a views directory for the ejs templates. For each of the templates, you can use the html from your existing HTML pages as as starter code
4. Create an endpoint on your express server three endpoints:
    * GET /blog → Retrieve all blog posts for the blog page
    * GET /blog/:blogid → Retrieve a blog post for an individual blog page
    * POST /blog → Create a new Blog Post
    * DELETE /blog/:blogid → Delete an existing Blog Post
5. Create an ejs template called “blog.ejs”
6. In server.js, create a global variable that will be an array to hold all the blog posts
7. There should also be a constructor for creating new BlogPost objects
8. For the end point GET /blog
    * Pass the blog post array of blog posts as data to the blog.ejs template
    * The blog.ejs template should display a list of all the blogs in the array on a page. Clicking on “Read More” on one of the blog posts will link to an individual page for that blog post
9. For the end point POST /blog
    * Install the npm library called [Body Parser](https://github.com/expressjs/body-parser). Body parser is used as middleware to process post parameters from a request.
        Post parameters can be retrieved from the req.body object in the same way that we use req.query and req.params
    * Retrieve the blog post data from req.body and create a new BlogPost object
        You’ll need to create a blog post id, and create at timestamp for when the BlogPost was created
    * Push the BlogPost object onto the array used to hold all of the BlogPost’s
    * Pass the array of blog posts to the blog.ejs template. Blog Posts should be displayed in order from newest to oldest
10. For the end point DELETE /blog/:blogid
    * This end point will delete the specified blog post with blogid
    * Based on the provided blogid, remove the blog post from the array of blog posts
    * Pass the array of blog posts as data to the blog.ejs template to display the list of blog posts
11. For the end point GET /blog/:blogid
    * Create an ejs template called blog-post.ejs
    * Based on what the provided blogid is, look up the blog post and pass the BlogPost object as data to the blog-post.ejs template
    * Display the contents of the blog post on the page
    * BONUS: At the end of the blog post, there should be “next” and “previous” links that will link to the next blog post (the next oldest blog post) and “previous” links (the next newest blog post)