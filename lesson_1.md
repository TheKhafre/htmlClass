
-------------------CSS------------------------

There are 3 methods of writing a CSS for your HTML project:
1. Inline CSS: This is written directly inside the html tag of the element we want to style. e.g:
    <p style="font-weight: bold; font-family: arial;">Hello World</p>

2. Internal CSS: an internal CSS is written in the head section of an HTML file. The CSS is enclosed within the style tag. e.g:
```html
    <style>
        p {
            background-color: red;
            font-size: 20px
        }

        div {
            border: 1px;
            background-color: yellow;
        }
    </style>
```

3. External CSS: This is an advance CSS writing style, where the CSS for an HTML project is written in another file entirely for clean organizaton and ease of debugging.

the format for styling an HTML entity is:
```html
    selector {
        property: value;
        property: value;
    }
```

A selector is a naming convention for styling an HTML entity. There are 3 types of selectors:
1. Type selector
    A type selector uses the html tag directly to target an html entity for styling. e.g p, div, a, header, span, img, input...
```html
        div {
            property: value;
        }
```

2. Class selector
    A class helps us group html entities to style for a focused styling regardless of the tag frequency. To use the class selector to target an html entity in css, we precede the class name with a dot. e.g suppose we have an html entity with the class name insider, to style it in css, we say:
```html
        .insider {
            property: value;
        }
```
________________________________________________________________________________________

## New (04-12-2024)

The last time saw us touched a few points in the introduction to CSS. However, we only spoke about two of the 3 selectors in HTML i.e the type selector and the class selector. Today, let's take a dive into more concepts in CSS starting from the third selector we didn't talk about last week; Id selector.

The id Selector:
This selector is one of the most powerful selector in HTML with the high priority used both for CSS and JavaScript. However, in case that explanation sounds a bit confusing here is what i meant by that. Suppose we have a Div that we target, and inside this div, we have two other tags, let's call them p and a. with ID selector, we can overwrite any default attribute that might be set for this div. In this manner, even if there was a previous styling that targeted the div with type selector or class selector, the id selector has the highest precedence and will override any styling from the type and class selector.

If you follow the code below for example, you'll notice even though the #testId styling came before the .testclass and after the div type selector, the #testId styling still took the precedence and the background color was violet. This is to prove that regardless of the id styling in CSS, it will always take precedence above all other selector.
```html
    <style>
        div {
                background-color: royalblue;
            }

        #testId {
            background-color: violet;
        }

        .testClass {
            background-color: yellow;
        }

        .hello {
            font-style: oblique;
        }
        .hi {
            font-style: italic;
        }
        
    </style>

    <div class="testClass" id="testId">
        <a href="#" download="true">
            <p>
                hi! This is me
                <img src="me.jpg" alt="yes, thats a picture of me!" width="300px">
            </p>
        </a>
    </div>
```

Styling texts in CSS
HTML being the building block of any website is composed of more than 80% texts with the others being imgs, inputs, and some other minor parts that come together to form the full website. However, as a result of this, the text styling is also one of the concepts that receives most attention when styling a webpage. 

some of the most common text styling includes:
- Font Family
- Font Size
- Font Weight
- Font Style
- Color
- Decoration
- Transformation
- Alignment
However, even though there are many other stylings that can be applied to text, the ones mentioned above takes the most shine. Hence, let's try to understand the meaning of each of those text styling terminologies.

### Font Family:
This is the styling that introduces the category and type of font we want to use. an example of this is selecting from the two prominent font types: Serif and San Serif fonts. To add the font family to a text in css, we need to add the property "font-family" and in front of this property is where we need to add the font we want to use as a value e.g
```html
	p {
		font-family: Tahoma;
	}
```
There are many ways we can get the font for our project, the most common is through the built-in fonts on our computer system. This includes arial, helvetical, Tahoma etc. However, the issue here is that these fonts are not generic and fonts found on one computer might not be on another which could cause quite an issue, especially since we want everyone all over the world to be able to use our website and have the same experience. To resolve this issue, we usually employ the tactic of loading our font from an online source. This is a bit of an advance concept though, so let's stick with using the font on our laptop for now. We'll talk better about loading fonts from online source later when we get to talking about external links.

### Font Size
The other property we need to talk about is the font-size. This determines how big or small our text appears and to load the font size we use "font-size" as our attribute and how big we want it to be as our value. Here is an example"
```html	
	p {
		font-size: 20px;
	}
```

How big or small your text is dependent on two factors, what do you want it to represent e.g the call to action, the main heading, the paragraph text and so on. the other factor is what screen you want it to be displayed on. Hence, while 100px might look okay on the screen of a desktop, a mobile phone users might need to adjust their phone screen before they can read it. That's why responsive design is all the rage out there in the programming world because you don't want to the mobile phone users to have a good experience at the expense of a desktop user and vice versa.

Thank God that you can always play around with the font size of a text regardless of the tag. For example, you can decide you want the font size of you H1 to be 65px on phone and 120px on desktop, the font-size property is there for you to make all the adjustments you need and want.

### Font Weight
you might be curious why some text on a website are bold and the others are not even when all the texts have been written with the p tag. This is all thanks to the font-weight property. This property help us adjust the appearance (otherwise known as the text weight) of our text. The threshold usually goes from 100 to 900 in most cases with 100 being a thinly appeared text, while 900 is a very boldly written text.

To change the default font weight of your text with css, we use the "font-weight" and add the value between 100 to 900 depending on how thing or bold we want our text to appear. However, it must be mentioned though that the normal font weight is usually around 300 to 400, with 400 being the most favoured figure. To use this in a code example, the CSS will look as follows:
```html
	p{
		font-weight: 700;
	}
```
By the way, here is another thing that you need to know, on most IDE and some online sourced fonts, the font weight has scaled the usual number specification and uses the natural English like "normal", "bold", "thin" etc. So, when choosing this format as your preferred way to specify your font weight, there is nothing much to add than simply changing the figure to the preferred keyword e.g
```html
	p {
		font-weight: bold;
	}
```
However, while this keywords are usually the same across fonts, some fonts have extra keywords such as "semi bold" "black" and so on. You can easily find the keyword on the page of any fonts with any of these extra keywords.

### Font Style
While we've spoken about the size, family, and weight attribute of a font, there is one important in the variant we can't skip, and this is the font style property. This is almost similar to the font weight but works differently in that they both determine the appearance of the text.

The font style property has value that include "normal", "italics", and "oblique". The oblique font is actually very confusing in that it looks very much like the italics so we will just ignore it and talk about the normal and italic style instead.

The default style for any text you create as a paragraph text is normal. However, special situation calls for extra styling in situations where we don't want to use the html emphasis or italics tags, we have the font-style attribute to the rescue.

To use the font style in our css, we simply introduce the "font-style" as our property and the style we want to use whether "normal", "oblique", or "italics" as our value. e.g:
```html
	p {
		font-style: italics;
	}
```
It is actually a bit redundant to add the "normal" value to the font-style property because even when you don't add it, the text is naturally in the "normal" state. It's just like saying your name everytime you meet your friends, it's awkward and unnecessary right? that's the exact way it feels when you add normal as the value.

Let's end here today, we'll pick it up from the colors when we continue tomorrow. please go over the document carefully and practice every examples in it, don' worry, you can't break anything.
PS: i deliberately left the first part of the document so that you can start from a part that help you connect the dots.