<!DOCTYPE html>
<html>
  <head>
    <title>Real Estate Contact Form</title>
    <link href="https://fonts.googleapis.com/css?family=Roboto:300,400,500,700" rel="stylesheet">
    <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.5.0/css/all.css" integrity="sha384-B4dIYHKNBt8Bc12p+WXckhzcICo0wtJAoU8YZTY5qE0Id1GSseTk6S+L3BlXeVIU" crossorigin="anonymous">
    <style>
      html, body {
      min-height: 100%;
      }
      body, div, form, input, select, p { 
      padding: 0;
      margin: 0;
      outline: none;
      font-family: Roboto, Arial, sans-serif;
      font-size: 14px;
      color: #666;
      line-height: 22px;
      }
      h1 {
      position: absolute;
      margin: 0;
      font-size: 36px;
      color: #fff;
      z-index: 2;
      }
      span.required {
      color: red;
      }
      .testbox {
      display: flex;
      justify-content: center;
      align-items: center;
      height: inherit;
      padding: 20px;
      }
      form {
      width: 100%;
      padding: 20px;
      border-radius: 6px;
      background: #fff;
      box-shadow: 0 0 30px 0 #095484; 
      }
      .banner {
      position: relative;
      height: 180px;
      background-image: url("https://media.gettyimages.com/photos/empty-wood-table-top-on-blur-abstract-green-from-garden-and-house-picture-id928765222?b=1&k=6&m=928765222&s=612x612&w=0&h=bQ1mTUf7CudU0-wTVHu972Oqh7-quxBx3_t1b1q_yiY=");  
      background-size: cover;
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      }
      .banner::after {
      content: "";
      background-color: rgba(0, 0, 0, 0.4); 
      position: absolute;
      width: 100%;
      height: 100%;
      }
      p.top-info {
      margin: 10px 0;
      }
      input, select {
      margin-bottom: 10px;
      border: 1px solid #ccc;
      border-radius: 3px;
      }
      input {
      width: calc(100% - 10px);
      padding: 5px;
      }
      select {
      width: 100%;
      padding: 7px 0;
      background: transparent;
      }
      .item:hover p, .question:hover p, .question label:hover, input:hover::placeholder {
      color: #095484;
      }
      .item input:hover, .item select:hover {
      border: 1px solid transparent;
      box-shadow: 0 0 5px 0 #095484;
      color: #095484;
      }
      .item {
      position: relative;
      margin: 10px 0;
      }
      .question input {
      width: auto;
      margin: 0;
      border-radius: 50%;
      }
      .question input, .question span {
      vertical-align: middle;
      }
      .question label {
      display: inline-block;
      margin: 5px 20px 15px 0;
      }
      .btn-block {
      margin-top: 10px;
      text-align: center;
      }
      button {
      width: 150px;
      padding: 10px;
      border: none;
      border-radius: 5px; 
      background: #095484;
      font-size: 16px;
      color: #fff;
      cursor: pointer;
      }
      button:hover {
      background: #0666a3;
      }
      @media (min-width: 568px) {
      .name-item, .city-item {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      }
      .name-item input, .city-item input {
      width: calc(50% - 20px);
      }
      .city-item select {
      width: calc(50% - 8px);
      }
      }
    </style>
  </head>
  <body>
    <div class="testbox">
      <form action="/">
        <div class="banner">
          <h1>Contact Form</h1>
        </div>
        <p class="top-info">Looking to buy or sell a home? We will connect you directly to a realtor in your city.</p>
        <div class="item">
          <p>Name<span class="required">*</span></p>
          <div class="name-item">
            <input type="text" name="name" placeholder="First" required/>
            <input type="text" name="name" placeholder="Last" required/>
          </div>
           <div class="item">
          <p>Email<span class="required">*</span></p>
            <input type="text" name="name" required/>
          </div>
          <div class="item">
          <p>Phone<span class="required">*</span></p>
            <input type="text" name="name" required/>
        </div>
          </div>
        <div class="question">
          <p>Pre-approved mortgage?<span class="required">*</span></p>
          <div class="question-answer">
            <label><input type="radio" value="none" name="mortgage" required/> <span>Yes</span></label>
            <label><input type="radio" value="none" name="mortgage" required/> <span>No</span></label>
          </div>
        </div>
        <div class="question">
          <p>Bedroom requirement<span class="required">*</span></p>
          <div class="question-answer">
            <label><input type="radio" value="none" name="Bedroom Requirement" required/> <span>1</span></label>
            <label><input type="radio" value="none" name="Bedroom Requirement" required/> <span>2</span></label>
            <label><input type="radio" value="none" name="Bedroom Requirement" required/> <span>3</span></label>
            <label><input type="radio" value="none" name="Bedroom Requirement" required/> <span>4+</span></label>
          </div>
          <style>
.yui3-button {
    margin:10px 0px 10px 0px;
    color: #fff;
    background-color: #3476b7;
}
</style>

<div id="demo" class="yui3-skin-sam yui3-g"> <!-- You need this skin class -->

  <div id="leftcolumn" class="yui3-u">
     <!-- Container for the calendar -->
     <div id="mycalendar"></div>
  </div>
  <div id="rightcolumn" class="yui3-u">
   <div id="links" style="padding-left:20px;">
      <!-- The buttons are created simply by assigning the correct CSS class -->
      <button id="togglePrevMonth" class="yui3-button">Toggle Previous Month's Dates</button><br>
      <button id="toggleNextMonth" class="yui3-button">Toggle Next Month's Dates</button><br>
      Selected date: <span id="selecteddate"></span>
   </div>
  </div>
</div>

<script type="text/javascript">
YUI().use('calendar', 'datatype-date', 'cssbutton',  function(Y) {

    // Create a new instance of calendar, placing it in
    // #mycalendar container, setting its width to 340px,
    // the flags for showing previous and next month's
    // dates in available empty cells to true, and setting
    // the date to today's date.
    var calendar = new Y.Calendar({
      contentBox: "#mycalendar",
      width:'340px',
      showPrevMonth: true,
      showNextMonth: true,
      date: new Date()}).render();

    // Get a reference to Y.DataType.Date
    var dtdate = Y.DataType.Date;

    // Listen to calendar's selectionChange event.
    calendar.on("selectionChange", function (ev) {

      // Get the date from the list of selected
      // dates returned with the event (since only
      // single selection is enabled by default,
      // we expect there to be only one date)
      var newDate = ev.newSelection[0];

      // Format the date and output it to a DOM
      // element.
      Y.one("#selecteddate").setHTML(dtdate.format(newDate));
    });


    // When the 'Show Previous Month' link is clicked,
    // modify the showPrevMonth property to show or hide
    // previous month's dates
    Y.one("#togglePrevMonth").on('click', function (ev) {
      ev.preventDefault();
      calendar.set('showPrevMonth', !(calendar.get("showPrevMonth")));
    });

    // When the 'Show Next Month' link is clicked,
    // modify the showNextMonth property to show or hide
    // next month's dates
    Y.one("#toggleNextMonth").on('click', function (ev) {
      ev.preventDefault();
      calendar.set('showNextMonth', !(calendar.get("showNextMonth")));
    });
});
</script>
        </div>
        <div class="btn-block">
          <button type="submit" href="/">Apply</button>
        </div>
      </form>
    </div>
  </body>
</html>
