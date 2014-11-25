emojijs
=======

Emoji Rendering for the web


emojijs is a javascript library that will allow you to easily render emojis on in your webapp. The emojiset used is the [opensource Twitter emojis](https://blog.twitter.com/2014/open-sourcing-twitter-emoji-for-everyone)

What are Emojis?
---------
[Emoji on Wikipedia](http://en.wikipedia.com/wiki/Emoji)  

Emojis are emoticons that are commonly used in text messaging. They are encoded as unicode characters that most fonts can't properly render yet. So unless your on an iOS or Android device you likely won't be able to see very many of them if any. With emojijs you can easily replace the emojis with icons that any browser could render.

How to use
------
Add emoji.js and emoji.css to your project and add the following in the `<head>` section of your project:

    <link rel="stylesheet" href="/path/to/emojijs/emoji.css">
    <script src="text/javascript" href="/path/to/emojijs/emoji.js">

Later in your javascript code you can use the global emoji object to parse emoji into html

    emoji.parseEmoji(emojiString);
    emoji.emojify(element);
    emoji.emojifyWholePage();
    
And if you're using jquery then the jquery plugin will load and you can do the following:

    jQuery("#divWithEmojis").emojify();
    
This will parse the emojis in all text nodes found inside your selected elements.

To emojify the whole page and all changes that happen to it use the following global jQuery function:

    jQuery.emojifyWholePage();

This requires [MutationObservers](https://developer.mozilla.org/en-US/docs/Web/API/MutationObserver) to be supported, you may want to use [this polyfill](https://github.com/Polymer/MutationObservers)
