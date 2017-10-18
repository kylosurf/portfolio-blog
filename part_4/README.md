# Part 4: Blog Posts
## Goal: The ability to create blog posts and display a list of them on a “Blog” page

1. On your “Blog.html” page, install jQuery.
2. We will use jQuery to set up the basic structure of our blogs and temporarily store them in our web page. Later we will look at how to store blogs more permanently on our server
3. Add a “Create Blog Post” button to your “Blogs.html” page
    * Add a “click” handler using jQuery to the button
    * Clicking on the button should show an input area below with the following fields:
        Title
        Description
        Content
        Header Image (url to an image for now)
        “Create Post” Button
        "Cancel" Button
4. The Cancel Button should:
    * Reset the form
    * Hide the form
5. The “Create Blog Post” 
    * Get the Blog details using jQuery from the Blog Form
    * Use a constructor to create a new Blog object that has the following properties:
        Title, Description, Content, Header Image, Created Date, blog id, tags
    * The new Blog Object should be pushed on to an array. Everytime we create a new Blog post, our array should have a new Blog post object added to it.
    * The new Blog Post object should be used to append the blog content to the end of the list of Blog Posts on the Page. If there are no Blog Posts yet, the Blog page should have a message saying “No Blogs Right Now”.
