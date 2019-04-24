# Placeholder

## Challenge

Your challenge is to review a code snippet and improve it. Use the hint tab to access the boilerplate files. Open the file called challenge3.scss.

Is something wrong with this code? How can we improve it? Is something repetitive? Maybe a straightforward placeholder can help us out...

### My thoughts

REMEMBER: Starts with $placeholderName and then extend the placeholder with @extend into a class or a selector (div etc).

A placeholder is lika a bunch of code that's not going to be used immediately, as it is only used when you extend it in a CSS class (@extend).
A placeholder starts with a % (ex. %backgroundImage).
For example we might whant to set some properties for our divs: size, position and repeat. Since we do this in the placeholder we inherit the properties everytime we add a new div and we can for example add a different image to each div but with the same properites.

1)I first put all the code in the placeholder (%background):

%background {
    background {
        size: cover;
        position: center center;
        repeat: no-repeat;
    }
}

2)I then extend the placeholder in the div:

div {
    @extend %background;
}

3)Now that I extended the placeholder into the div, all div's will be compiled with the background properties!

4)I can now add, an image into a class within the div:

.article {
    background-image: url();
}

The class iarticle will now inherit the placeholder properties from the div.

REMEMBER: The placeholder is only compiled when it is used and the container is compiled all the time even if it is not used! Placeholders should be used for code that is intended for reuse.