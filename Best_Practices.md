# Ascend Project Best Practices and Examples

*   Case sensitivity for images, filenames, file paths, urls, etc. is critical. For example, <code>My_image.jpg</code> is not the same as <code>my_image.jpg</code> and <code>/sites</code> is not the same as <code>/Sites</code>.

*   Image links need an alt text attribute. If you are using markdown the syntax looks like this <code>![alternate text goes here](path/to/your/image.png)</code> and if you are using html the syntax looks like this <code><img src="path/to/image.jpg" alt="alternate text goes here"></code>

*   Never put spaces in filenames, image names or directory names. Using the Finder to create or edit files and directories makes it very easy to make this mistake. Use the command line and use dashes, camelcase or underscores in your file and directory names.

    For example <code>my_file.txt</code> or <code>my-file.txt</code> or <code>myFile.txt</code>

*   The file path for your participant image directory is <code>/participants/location/user/image_dir/image_name.</code> It starts with a forward slash and follows the path from the root Ascend Project directory.

    For example <code> /participants/portland/lisa/images/FromHawthorneBridge.jpg </code> is the file path to my image directory.

*   You may find you want to embed a link to a previous blog post in a different blog post. The path to participant blog posts is a bit different than the path to participant images. The file path for your participant blogs is <code>/participant/location/user/YYYY/MM/DD/blog_title/</code>

    For example <code> /participants/portland/lisa/2014/09/11/push_and_pull/ </code> is the path to one of my Ascend blog posts.

*   Pay attention to spelling. The computer only does what you tell it to do so if you are trying to navigate somewhere or a link you embedded in your blog post claims to be invalid make sure everything is spelled correctly. Close enough won't work. The computer requires the spelling to be exact.

*   Test links in your web browser to make sure they lead to the page you were expecting. If you are still unsure you can always ask another participant to browse to the link on their computer.

*   Make sure your markdown header is formatted correctly and filled out completely. An example of a correctly formatted markdown header looks like:

    <code> 
    ---  
    layout: post  
    title:  "insert title here within quotes"  
    author: author name  
    date:   YYYY-MM-DD  
    categories: participant directory name  
    ---
    </code>
