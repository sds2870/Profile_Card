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

That completes the HTML file for this tutorial. Next, we shall tackle the CSS. Right of the bat, let's go ahead and import a font style from "fonts.googleapis.com". I will be utilizing the Poppins font, but use whatever you feel comfortable with. The syntax should look like this:

    @import url("http://fonts.googleapis.com/css?family=Poppins:100,200,300,400,500,600,700,800,900");

Now that we have that at the top of our CSS file, we will create our "root" selector (*{}), which will holding our beginning properties of margin(0), padding(0), box-sizing(border-box), and font family("Poppins", sans serif). The root selector should look like so:

    * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Poppins", sans-serif;
    }

Our next selector will focus on the <body> tag of our HTML file. In it, we will define five properties. Our "display" property will be set to 'flex' to employ the flex box feature while "jusitfy-content" will be set to 'center'. Next, we will put the value of 'center' for our "align-items" property followed by '190vh' for our "min-height" property. Finally, we will define our background by using a linear gradient with value for the angle and the two colors that will be used. I've chosen to use a 45-degree angle with my two colors. Once finished, click the "Go Live" icon at the bottom of the VS Code window to see your work in real-time. Your code should resemble this:

    body {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 190vh;
    background: linear-gradient(45deg, #fbda61, #ff5acd);
    }

We're ready to begin working on the card now. First, we need to access the <div> tag with "card" as its class. We do that by saying ".card" followed by the curly braces/brackets. With that selector created, we can add our properties (seven, this time) inside. First, set your "position" property to 'relative'. Next set "width" to '350px' and "height" to '190px'. Create a "background" property and set the color to 'white('#fff')'. Next, we will create a "border-radius" of '20px'. Then, we will employ the box-shadow property with the following value of '0 35px 80px rgba(0,0,0,0.15)'. Finally, we will use the "transition" property, setting the value to '0.5s'. Your syntax should match the following below:

    .card {
    position: relative;
    width: 350px;
    height: 190px;
    background: #fff;
    border-radius: 20px;
    box-shadow: 0 35px 80px rgba(0,0,0,0.15);
    transition: 0.5s;
    }

In CSS, you are able to create selectors that will outrank others due to selector specificity. This will be done with our next selector, which will use the "hover" effect. We do this by creating a new selector that uses the ".card" tag, but adds the "hover" effect via a colon. In this selector, we will only focus on the "height" porperty, making the value '450px'. If done correctly, your selector should look like this:

    .card:hover {
    height: 450px;
    }   

Our next selector will hold eleven properties. This selector will focus on the <div> tag with the "imgBx" class. We set our "position" to 'absolute', "left" to '50%', "top" to '-50%', and our "transform" to 'translateX()' with a value of '-50%'. Your profile card should be exhibiting some character now, but we're not done yet. We want to deal with the properties of "width" and "height", setting their values to '150px' each. For our image box's "background", let's choose the color of white by inputting '#fff' for the value. We will then give our box a "border-radius" of '20px', followed by this value for the "box-shadow" property: '0 15px 50px rgba(0,0,0,0.35)'. I may not have stated this, but the "a" in rgba stands for alpha, and this component's purpose is to determine the transparency of the color created through rgb. Now, all that's left for this <div> is the "overflow", which should be set to 'hidden', and the "transition", which should give a value of '0.5s'. Your code for the imgBx selector should look like this:

    .imgBx {
    position: absolute;
    left: 50%;
    top: -50px;
    transform: translateX(-50%);
    width: 150px;
    height: 150px;
    background: #fff;
    border-radius: 20px;
    box-shadow: 0 15px 50px rgba(0,0,0,0.35);
    overflow: hidden;
    transition: 0.5s;
    }

All right, let's create a new selector, this time combining the "card:hover" with the ".imgBx". Inside of this new selector, we'll just focus on the "width" and "height" properties, giving both a value of '250px'. Make sure that your code resembles the following:

    .card:hover .imgBx {
    width: 250px;
    height: 250px;
    }

Our next target will be the image element within our imgBx tag. Let's create a selector that focuses solely on those two (.imgBx img {}). Inside of the field, we'll set the "position" property to 'absolute' and give the "top" and "left" properties a value of '0'. Then, we will give '100%' for the values of our "width" and "height" properties before finishing things off with the "object-fit" property. This property determines how the contents of a replaced element should be sized in relation to the created box by its used height and width. We'll use 'cover' for the value. Your code should look like this:

    .imgBx img {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    }

Everything should be shaping up nicely as we walk to the finished result. Let's get our card content together. TO do that, we'll create a new selector focusing on the <div> tags containing the classes of "card" and "content". In this selector, we'll set our "position" to 'absolute', with a "height" and "width" of '100%'. Next, we'll give our "display" property the value of 'flex'. Our properties of "justify-content" and "align item" will have the values of 'center' and 'flex-end', respectively. Finally, we will give the value of 'hidden' to our "overflow" property. Everything should look exactly like the following code below:

    .card .content {
    position: absolute;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: flex-end;
    overflow: hidden;
    }

Earlier on, I tocuhed on the concept of selector specificity, but I did not explain why this was important in CSS. In short, if you want to add a particular style element that will always take place once your project is up and running, it's important to make sure that the element in question's specificity ranking is higher so that other styling elements don't override its intended effect. Also, by hovering over the selector name in your CSS file, you'll be able to see the ranking, allowing you to know what selector has a higher/lower specificity ranking in comparison to others. With that being said, let's create a new selector, this time, targeting three classes ("card", "content", and "details"). In the selector field, give your "padding" property a value of '40px'. Then, choose the 'center' value for your "text-align" property. After that, you will have a "width" of '100%' with a "transition" time of '0.5s'. And last, we select 'translateY()', with an inner value of '150px', for our "transform" property. Our coding syntax for this selector should look like this:

    .card .content .details {
    padding: 40px;
    text-align: center;
    width: 100%;
    transition: 0.5s;
    transform: translateY(150px);    
    }

We're on the home-stretch now. Let's create a selector focusing on the card-hover effect along with the "content" and "details" classes. Here, we will only add one property, "transform". The value here will be 'translateY()', but the inner value will be '0px', lie so:

    .card:hover .content .details {
    transform: translateY(0px);
    }

Now, we're heading back to addressing the three classes we've worked with recently; however, we will add the <h2> tag to the mix. In this new selector, let's focus on "font-size"(1.25em), "font-weight"(600), "color"(rebeccapurple/your choice), and "line-height"(1.2em). If you entered everything appropriately, your selector should resemble mine:

    .card .content .details h2 {
    font-size: 1.25em;
    font-weight: 600;
    color: rebeccapurple;
    line-height: 1.2em;
    }

Our next new selector will add "span" to the previous set of classes/tag. In it, we will target the properties of "font-size"(0.75em), "font-weight"(500), and "opacity"(0.5). Your code should look exactly like the following:

    .card .content .details h2 span {
    font-size: 0.75em;
    font-weight: 500;
    opacity: 0.5;
    }

This time around, our new selector will focus on the three aforementioned classes plus one new class, "data". With a specificty ranking of "40", everything we put here will surely appear as it should on-screen. Set your "display" to 'flex' while giving "justify-content" and "margin" values of 'space-between' and '20px 0'. Our code should look like this:

    .card .content .details .data {
    display: flex;
    justify-content: space-between;
    margin: 20px 0;
    }

Can you believe that we're almost through. First, I want to commend you for sticking it out this far. Following a guide to creating a particular product takes time, and you have done well to get to this point. Now, we're going to address our <h3> tag, adding it to the group of four classes to make our new selector. In the field, we will deal with "font-size"(1em), "color"(rebeccapurple/your choice), "line-height"(1.2em), and "font-weight"(600). Your code should look something like this:

    .card .content .details .data h3 {
    font-size: 1em;
    color: rebeccapurple;
    line-height: 1.2em;
    font-weight: 600;
    }

It's time to get our action button working (per say). Here, we will create a selector that addresses the three classes we've been working with ("card", "content", "details") and add the class for our action button to the  mix ("actionBtn"). In the field, we'll set our "display" property to 'flex', "justify-content" to 'space-between', and "gap" to '20px'. The syntax should read as follows:

    .card .content .details .actionBtn {
    display: flex;
    justify-content: space-between;
    gap: 20px;
    }

Our penultimate selector with add the <button> tag to the previous group of classes. Here, we will address nine properties. Our "padding" will have top-bottom and left-right values of '10px' and '30px', with "border-radius" being set to '5px'. Our "border" and "outline" properties will be set to 'none'. Next, set "font-size" to '1em' and "font-weight" to '500'. After that set your "background" for your button to a color of your choosing, but give the "color" property for the text the value of '#fff'. Finally, choose 'pointer' for your "cursor" property. Everything should look like this:

    .card .content .details .actionBtn button {
    padding: 10px 30px;
    border-radius: 5px;
    border: none;
    outline: none;
    font-size: 1em;
    font-weight: 500;
    background: rebeccapurple;
    color: #fff;
    cursor: pointer;
    }

The very last selector for our CSS file will only addressa few properties; however, we will add the "nth-child" syntax to the <button> tag to address the second button in our profile ("Message"). The syntax for that would be this:

    button:nth-child(2)

After creating our selector, let's set our "border" property to the value(s) of '1px', 'solid', and a color of your choosing. Next select a color for the "color" property, which will be for your text. Last, but not least, set the "background" for your button to '#fff'. Your final selector should look like this:

    .card .content .details .actionBtn button:nth-child(2) {
    border: 1px solid rebeccapurple;
    color: rebeccapurple;
    background: #fff;
    }   

And there you have it. You have completed the tutorial for  creating a profile card. Thank you for taking out the time to follow this tutorial. Shout-out to Online Tutorials for providing the video via their Youtube channel. Again, thank you for coming along for the ride. Code on!