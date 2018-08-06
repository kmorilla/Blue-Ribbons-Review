# Blue-Ribbons-Review
Blue Ribbons Review is a website that allows sellers to get their products some traction by offering deals on their products to buyers on the Blue Ribbons Review site which encourages users to leave reviews on the products being sold through Amazon. I worked on this project for 2 weeks remotely in a team of 5 members, completing 11 stories and working with Azure, TFS, Slack, and Scrum methodologies. The website was built using ASP.NET MVC and the languages used were CSS, HTML, JavaScript, jQuery, C# and Razor. The website was also built using Bootstrap 3 which made the styling a bit more tedious and challenging. 

## jQuery Datepicker
The assignment for this story was to just add a background color to the datepicker element. As seen in the before image, the datepicker was very ugly and cramped, so I decided to get a little more creative than to just add a background color. By researching online, I was able to learn how to change the design of the datepicker and I altered it to my liking. 
### Before
![datepickerbefore](https://user-images.githubusercontent.com/37521213/43691573-5aa2bd76-98d3-11e8-84b9-d49c029b16bf.jpg)
```
.ui-datepicker {
  width: 200px;
  height: auto;
  padding: 10px;
  background-color: rgba(178,178,178,0.8);
}
.ui-datepicker a {
  text-decoration: none;
}
.ui-datepicker table {
  width: 100%;
}
.ui-datepicker-header {
  font-weight: bold;
}
.ui-datepicker-title {
  text-align: center;
}
.ui-datepicker-prev .ui-datepicker-next {
  display: inline-block;
  width: 30px;
  height: 30px;
  text-align: center;
  cursor: pointer;
}
.ui-datepicker-prev {
  float: left;
}
.ui-datepicker-next {
  float: right;
}
```
### After
![datepickerafter](https://user-images.githubusercontent.com/37521213/43691572-5a8bf618-98d3-11e8-87a0-cd0fb34f01fe.jpg)

## Modal Changes
In the Details partial view, I completed multiple stories editing the modal. The edits include: adding a border around the modal and the image, making the entire text black except the sale price, enlarging the image, and having the buttons to the left and the links to the right.
```
/*-- Border around Modal and Image --*/
div.details-border, img.details-border {
  border: 2px solid black;
  border-radius: 10px;
}
/*-- _Details font color change to black --*/
div.details-color, a.details-color, h3-details-color {
  color: #000 !important;
}
/*-- _Details Image Enlargement and Styling --*/
.now-only-container {
  width: auto;
  height: auto;
  display: inline-block;
}
.now-only-style {
  float: left;
  font-size: 20px;
  font-weight: 600;
}
.now-only-text {
  color: #000;
  padding-right: 10px;
}
.now-only-price {
  color: #4172a8;
}
#item-image {
  max-width: 250px;
  height: auto;
}
/*-- Styling for Buttons --*/
.details-row {
  display: flex;
}
.details-col {
  flex: 1;
  padding: 10px;
}
```
### Output
![modalimg](https://user-images.githubusercontent.com/37521213/43691810-4dbe9fdc-98d6-11e8-91b0-c0cdfd1c4fc4.jpg)

![modalbuttons](https://user-images.githubusercontent.com/37521213/43691809-4da7d860-98d6-11e8-8432-596989a0025e.jpg)

## Popover
This assignment had me change the popover effect from being to wide and have some padding around the text. As you can see in the before image, because we were using Bootstrap 3, the popover defaulted to the default popover effect. After adding the popover jQuery from Bootstrap 4, the popover effect is much cleaner and neat. 
### Before
![popoverbefore](https://user-images.githubusercontent.com/37521213/43691926-c3ee1768-98d7-11e8-8725-ed2545099c21.jpg)
```
$(function () {
  $('[data-toggle="popover"').popover({
    placement: 'right',
    trigger: 'hover'
  });
});
```
### After
![popoverafter](https://user-images.githubusercontent.com/37521213/43691925-c3d5274e-98d7-11e8-844b-0756d3901488.jpg)

## Character Count
This assignment had me move the character count element to be beneath the Review text box. The reason why it was so low was because there was an unused div tag before the character count element. Then, because the character count element was hidden until you typed in the Review text box, when it would be displayed the the items underneath would shift down. To fix this, I gave the character count a small height.  
### Before
![charactercountbefore](https://user-images.githubusercontent.com/37521213/43692101-41d724a2-98d9-11e8-9615-b8a95b0eeace.jpg)
```
.character-box {
  height: 15px;
}
```
### After
![charactercountafter](https://user-images.githubusercontent.com/37521213/43692100-41bff0a2-98d9-11e8-8278-5300cce1df09.jpg

## Wishlist Page
On the Wishlist page, I completed a few stories that included: if there were no items in the Wishlist, it would display the message "You currently have no items in your Wishlist. Check out our products here!"; adding a new column with a link that would take you to see the item on Amazon; and adding a shopping cart icon next to the title. The first story was completed using Razor code with an if else statment where it would check to see if there were any items in the Wishlist, and then display the message or the items. For the second story, I had to add a new column with knockoutjs and target the item's URL with Razor code because it was saved in the database. Because the title in the last story was in a ViewBag, I needed to use JavaScript to add an icon from Font Awesome. The script would target the element of the ViewBag, create a copy of the element after it, and then add the Font Awesome icon class to the new element. 

```
//The if statement for the first story
@if (Model.Wishlists.Count() == 0)
{
  <div class="container">
    <div class="row">
      <h4>You currently have no items in your Wishlist. Check out our products @Html.ActionLink("here!", "Index", "Campaigns")</h4>
    </div>
  </div>
}
else
{
...

//The Amazon link for the second story
<td class="td-valign">
  <a href="@item.Campaign.VendorsPurchaseURL" target="_blank">See on Amazon</a>
</td

//The JavaScript code for the third story
<script>
  var para = document.createElement("h3");
  var element = document.getElementsByTagName("H3")[0];
  element.appendChild(para).className = "fa fa-shopping-cart shopping-cart-margin";
</script>
```
### Story One

### Story Two

### Story Three
