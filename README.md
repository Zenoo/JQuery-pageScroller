# pageScroller

Scroll smoothly & easily.

### Doc

* **Installation**

Simply import JQuery & pageScroller into your HTML.
```
<script src="https://code.jquery.com/jquery-3.2.1.min.js" integrity="sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=" crossorigin="anonymous"></script>
<script src="your/Path/js/pageScroller.js" type="text/javascript"></script>	
```
* **How to use**
Select your sections container with a JQuery selector.
```
$('#container').pageScroller();
```
* **Options**
```
{
    travelTime:1000, //travel time
    afterTravelTimeout:1, //length of the pause after each scroll (> 0)
    travelEasing:'swing', //easing type
    startingPage:0, //Index of your starting page (in your container)
    anchors:[], //list of CSS selectors for your custom anchors
    onTrigger : function({nextPage,prevPage}) {}, //Triggers before the scroll starts
    onEnd : function({nextPage,prevPage}) {} //Triggers after the scroll ends
}
```
* **Example**
```
$('#container').pageScroller({
    travelTime:500,
    afterTravelTimeout:50,
    travelEasing:'swing',
    startingPage:0,
    anchors:['.test1','#test2','li.test3>a'],
    onTrigger : function(e) {
        console.log(e);
    },
    onEnd : function(e) {
        console.log(e);
    }
});
```

## Authors

* **Zenoo** - *Initial work* - [Zenoo.fr](http://zenoo.fr)