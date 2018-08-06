# Blue-Ribbons-Review
Blue Ribbons Review is a website that allows sellers to get their products some traction by offering deals on their products to buyers on the Blue Ribbons Review site which encourages users to leave reviews on the products being sold through Amazon. I worked on this project for 2 weeks remotely in a team of 5 members, completing 11 stories and working with Azure, TFS, Slack, and Scrum methodologies. The website was built using ASP.NET MVC and the languages used were CSS, HTML, JavaScript, jQuery, C# and Razor. 

## jQuery Datepicker
The assignment for this story was to just add a background color to the datepicker element. As seen in the before image, the datepicker was very ugly and cramped, so I decided to get a little more creative than to just add a background color. By researching online, I was able to learn how to change the design of the datepicker and I altered it to my liking. 
### Before
![datepickerbefore](https://user-images.githubusercontent.com/37521213/43691573-5aa2bd76-98d3-11e8-84b9-d49c029b16bf.jpg)
### After
![datepickerafter](https://user-images.githubusercontent.com/37521213/43691572-5a8bf618-98d3-11e8-87a0-cd0fb34f01fe.jpg)
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
