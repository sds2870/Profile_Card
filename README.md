# Profile_Card

Greetings. Today, we will be learning how to create a User Interface (UI) Profile Card utilizing the tutorial seen here: https://www.youtube.com/watch?v=daAVTmsMXeI. 

After creating your HTML and CSS files, the first step, as always, is to set up your HTML tree. After doing so, you can give the document a nice title (I'm using "Profile_Card" as my title). Afterwards, link your CSS file to your HTML using the following <link> tag like so:

    <link rel="stylesheet" href="style.css">

This must be placed above the closing "head" tag (</head>). Once that is completed, we will now create our tags for the body of our HTML tree. First, we will create a "div" tag within the <body> tag that will house everything necessary for our profile card. We will give it a class name so that we can address it in our CSS file. It should look something like this:

    <div class="card">
    </div>

Within this <div> tag, we will create two more <div> tags that will address our information (profile image and content). The following tags should also have classes identifying them properly, like so:

    <div class="imageBX">
    </div>

    <div class="content">
    </div>

Everything else that we will do for our HTML file will be contained in these two <div> tags. For the "imageBx" <div>
tag, we need to use a photo for our profile card. You can create a folder that houses your profile photo. Use the <img> tag to grab the photo from your folder. The code should look something like this:

    <img src="profile photos/Profile_image.jpg" alt="profile_image">

The code seen here should be placed in the aforementioned <div> tag like so:

    <div class="imgBx">
        <img src="profile photos/Profile_image.jpg" alt="profile_image">
    </div>

Notice how the syntax for the image address the folder that houses my image? That's exactly how it should be when you are using images for your web applications. Now, on to the "content" <div> tag. Here, we'll have a bit more code to produce before we can call the HTML file complete. Firstly, we will create another <div> tag inside of the "content" <div> tag and give it a class name ("details", for instance). This particular tag will house a <h2> tag and two more <div> tags with class names of "data" and "actionBtn", respectively. For now, it should look like this:
    
    <div class="content">
        <div class="details">
            <h2></h2>
            <div class="data">
            </div>
            <div class="actionBtn">
            </div>
        </div>
    </div>

Once you have this set-up, you can now address the "details" <div> tag. Inside of your <h2> tag, you can write your name, followed by a <br> tag, which will create a line-break. Right after your <br> tag, create a <span> tag that will house your profile title. The code should look like this:

    <h2>Steven Smith<br><span>Front-End Web Developer</span></h2>

Now, we shall focus on the "data" <div>. Here, create three <h3> tags that will house numerical statistics for the followin categories: Posts, Followers, and Following. You will need to utilize the same <br> tag-<span> tag method employed in the <h2> tag her, also. Your code should resemble this:

    <h3>657<br><span>Posts</span></h3>
    <h3>210k<br><span>Followers</span></h3>
    <h3>173<br><span>Following</span></h3>

Only the <h3> tags should be inside of the "data" <div> tag. Finally, we come to the "actionBtn" <div> tag, which only contains two lines of code inside. These code lines will utilize the <button> tag. Inside of these tags, write the words "Follow" and "Message". The code should look like this:

    <button>Follow</button>
    <button>Message</button>

If you have followed through, your HTML tree should resemble mine:

    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Profile_Card</title>
        <link rel="stylesheet" href="style.css">
    </head>
    <body>
    <div class="card">
        <div class="imgBx">
            <img src="profile photos/Profile_image.jpg" alt="profile_image">
        </div>
        <div class="content">
            <div class="details">
                <h2>Steven Smith<br><span>Front-End Web Developer</span></h2>
                <div class="data">
                    <h3>657<br><span>Posts</span></h3>
                    <h3>210k<br><span>Followers</span></h3>
                    <h3>173<br><span>Following</span></h3>
                </div>
                <div class="actionBtn">
                    <button>Follow</button>
                    <button>Message</button>
                </div>
            </div>
        </div>
    </div>
    </body>
    </html>

That completes the HTML file for this tutorial. Next, we shall tackle the CSS.