#Finding Elements of the page
```
document.getElementsByClassName('img-responsive')
```
Returns an array of elements on the page with the class `img-responive` class
```
document.querySelector('.img-responsive')

>>> <img src=​"img/​coded-homes-logo-sm.png" class=​"img-responsive">​
```
Returns the first child to match the class img-responsive
```
document.querySelectorAll('#example-container li:first-child')
```
-Targets element with id example-container => looks for list items within the elelemtn and returns the first child
-Returns a NodeList in array form.
```
-get all list items within example-container element

items = document.querySelectorAll('#example-container li');

>>> NodeList(6) [li.feature, li.feature, li.feature, li.feature, li.feature, li.feature]

-iterate over all elements using for loop
for(var i=0;i<items.length;i++){
console.log(items[i].innerText);
}

VM1202:2 Luxurious sized master suite
VM1202:2 Oversized walk-in closet
VM1202:2 Frameless Beech cabinetry with concealed hinges
VM1202:2 Elegant slab white quartz countertops with large backsplash
VM1202:2 Dual china sinks with Moen faucets
VM1202:2 Clear frameless shower enclosure

-iterate over all elements using forEach loop
forEach = Array.prototype.forEach;

ƒ forEach() { [native code] }

forEach.call(items, function(item){
	console.log(item.innerText);
})

VM1439:2 Luxurious sized master suite
VM1439:2 Oversized walk-in closet
VM1439:2 Frameless Beech cabinetry with concealed hinges
VM1439:2 Elegant slab white quartz countertops with large backsplash
VM1439:2 Dual china sinks with Moen faucets
VM1439:2 Clear frameless shower enclosures
```
#Working with Live Results
```
- get unordered list element under example-container using querySelector
list =  document.querySelector('#example-container ul')

>>> <ul>​…​</ul>​<li class=​"feature">​Luxurious sized master suite​</li>​<li class=​"feature">​Oversized walk-in closet​</li>​<li class=​"feature">​Frameless Beech cabinetry with concealed hinges​</li>​<li class=​"feature">​Elegant slab white quartz countertops with large backsplash​</li>​<li class=​"feature">​Dual china sinks with Moen faucets​</li>​<li class=​"feature">​Clear frameless shower enclosures​</li>​</ul>​

- get all items on page with class name of feature
items = document.getElementsByClassName('feature')

>>> HTMLCollection(6) [li.feature, li.feature, li.feature, li.feature, li.feature, li.feature]0: li.feature1: li.feature2: li.feature3: li.feature4: li.feature5: li.featurelength: 6__proto__: HTMLCollection

-create a new list item
newitem = document.createElement('LI')

>>> <li>​</li>​

-give the new item a class name
newitem.className = 'feature'

>>> "feature"

- put html text inside the new list item
newitem.innerText = 'Flavoured calistheniks'

>>> "Flavoured calistheniks"

- add the new list item to the exisiting list, you will see the page update and show the newly added element
list.appendChild(newitem)

>>> <li class=​"feature">​Flavoured calistheniks​</li>​

- count number of items in list it will have previous length + 1 
list.length

>>> 7 
```