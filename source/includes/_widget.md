#Widget

Although the Swyfft API provides control and flexibility, it also comes "with some assembly required". If what you want is a simple way to show an address box on your web page, the Swyfft Widget may be closer to what you need. With two lines of code, you can add a widget to your website that will look something like this:

![Widget Sample](Widget.png)

The way you do this is very simple. You decide where on your web page you want the Swyfft widget to appear, and place an HTML element there with an appropriately styled height and width. (We recommend at least 500 pixels high and 500 pixels wide.)

```javascript
    <script type="text/javascript" src="//swyfft.com/Widgets/Dist/widgets.bundle.js"></script>
    <script type="text/javascript">
        swyfft.widgets.addressWidget.show('#PutYourTargetElementIdHere', 'PutYourApiKeyHere', SetToTrueToOpenQuoteOnNewTab);
    </script>
```
Then add the javascript to the right to your page:

(Obviously, replacing the `#PutYourTargetElementIdHere`, `PutYourApiKeyHere` and `SetToTrueToOpenQuoteOnNewTab` with the appropriate element id, API key and boolean value.)

You can see an example of how to do it on the `~/Swyfft.ApiDemo.Web/Views/Home/Widget.cshtml` page in the [Swyfft API Demo project](https://bitbucket.org/swyfft/swyfftapidemo/overview).

If you need to override any of the CSS styling, you can do that by overriding the styles defined in the widget's (automatically loaded) stylesheet.