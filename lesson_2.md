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

## New (05-12-2024)
We started a series on styling HTML texts in CSS. This is a crucial first step as already mentioned since text constitutes more than 60% of the building blocks of any website. 

We already spoke about the four important font prefixed css properties yesterday i.e `"Font Family"` `Font Size"` `"Font Weight"` and `"Font Style"`. However, talking about this four properties does not mean those are the only font-prefixed properties in css, but they are the ones you will most likely use in your everyday projects while you might never find yourself using any of the ones not mentioned in this four.

Today, we'll conclude the text styling lesson by talking about the other four important text styling properties i.e:
- Text Color
- Text Decoration
- Text Transformation
- Text Alignment

Without, wasting any more of the precious time, let's get into it.

### Text Color
The flexibiliity to be able change a text color in css is almost one of the best things you can do to a text in css. This is because it give flexibility of design a page with the brand color and in the case of a typographical logo, it makes it easy to design the logo into the HTML without having to bother about the image size. Another important flexibility is how it allows us to chnage thw color of the anchor tag output from the default blue and purple to whichever color we want.

However, putting that aside, folowinf the same format as we did yesterday, to add color to a text we use the property "color". Note the important change here, we used `"color"` not `"text-color"`. So, suppose we have an anchir tag i.e an "a" tag and we want to change their color from the default blue to say something like black, we simply say:
```html
<style>
    a {
        color: black;
    }
</style>
```

The output of the code wil change the color of the link to black instead of the usual blue.

### Text Decoration
In html, the text decoration property deals primarily with lines around texts. this includes underlines, strikethroughs and other lines that appear under, above or through the text.

One of the most prominent hTML entities that makes this property important is the anchor tag. if you have been following the anchor tag well, you'll notice that the color is not the only default property it has, it also has a default underline. with the text-decoration property, we can tell the machine if we want the underline to remain in place or be removed from the tag. 

In most situation and cases, we always opt for removing the underline. Hence, to do so, we simply provide a value of "none" to the text-decoration property under the anchor tag cascade. here is an example in code:

```html
<style>
    a {
        text-decoration: none;
        color: black;
    }
</style>
```

With the example above, we have directly told the machine to remove any text decoration around the link and change the color too to black. 

However, this might make the link end up looking like a regular text which might confuse users. So, a bonus property that might help us in this scenario is to make the cursor change to the hand form when we are on a text that is a link. this helps us tell the user that the link they are currently hovering over is a link. To make cursor turn to hand we use the property "cursor" and suppky it with the value "pointer". Let's add this new property in our example code:

```html
<style>
    a {
        text-decoration: none;
        color: black;
        cursor: pointer;
    }
</style>
```

There are many other ways developers change the appearance of a link to make it obvious to users that the text they are hovering over is a link. Some this known methods include changing the opacity of the text when it is hovered; adding an animation to it; adding a king of decoration only when hovered; and many other ways. This might be out of our current scope, but it is just worth mentioning.


### Text Transformation
Unlike the earlier two properties mentioned, text transformation is not a property you use everyday. This is a property that is used only in special situations and conditions to change the appearance of the text to forms such as title case, uppercase, lowercase etc.

The four important values of text transform includes:
- **Capitalize:** this changes the first letter of each word to uppercase.
```html
<style>
    a {
        text-transform: capitalize;
    }
</style>
```

- **Uppercase:** This change all the characters of the text to capital letters.
```html
<style>
    a {
        text-transform: uppercase;
    }
</style>
```
- **lowercase:** witht the lowercase value, all the characters of the texts are automatically changed to small letters, regardless of the way it was written.
```html
<style>
    a {
        text-transform: lowercase;
    }
</style>
```
- **none:** This is actually a no-brainer because by default, all texts have a default text transformation of none. However, supposing in a situation where we use type selector to change maybe all "p-tags" to Uppercase, the "none" value can help us single out a selected p-tag.

Here is an example:
```html
<style>
    p{
        color: red;
        text-transform: uppercase;
    }

    .special {
        color: black;
        text-transform: none;
    }
</style>

 <div>
    <p>Hello Bola</p>
    <p>Hello Taiwo</p>
    <p class="special">Hello Joseph</p>
    <p>Hello Jamiu</p>
    <p>Hello Malik</p>
</div>
```

if you run this code, you'll realize that all other p tag on the page are all red and in uppercase. However, becuase we have give the p tag with the "special" class a text transform of none, it appears normal and takes ourassigned color of black as well.

### Text Alignment
One of the things you'll have your fair share of struggle with is the alignment of your html entities. However, there is a shortcut to aligning texts on the page; we use the text-align property.

The text align property is a very straight forward and easy property that help you decide easily where you want the text to be placed on the page. it has the following values to help you out:
- **start or left:** By default, the text is aligned on the left of your screen. we call this the start of the screen or you can just say the left part of your screen. 

However, since i already mentioned that the text is naturally aligned to the left, you might not find yourself using this values often. But in the eventuality when it becomes necessary to use, here is how to add it to your code:
```html
<style>
    a {
        text-align: left;
    }
</style>
```

- **end of righr:** Just like you mighht have guessed, this is the direct opposite of the "start or left" value. However, since this alignment is not added to the texts by default, to add it we say:
```html
<style>
    p {
        text-align: right;
    }
</style>
```
This will automatically push all the p texts to the right of the screen.

- **center:** One of the most favoured text alignement value is the "center" which means this is a value you will find yourself using most of the time.

This vakue helps us set the text to the center of the screen, and funny enough, the format of adding it is not too different from the others.
```html
<style>
    div {
        text-align: center;
    }
</style>
```

you'll notice that i have used different tags in the 3 examples i.e a-tag in the first, p-tag in the second, and div in the last example. This is to tell you that the text align property works everywhere there is a text.

Let's end the lesson here today, by the time we meet again next week, we'll be starting with another new concept.
cheers!