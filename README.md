# mybb-userbars
> Modernized userbars for any MyBB community board.

## Installation
* Step 1: Make a new folder called *assets* within your forum folder.
* Step 2: Insert the *userbars.css* file into the *assets* folder.
* Step 3: Open up the *headerinclude* template in your MyBB templates in the ACP and add the following code:
```
<link href="https://fonts.googleapis.com/css?family=Open+Sans|Roboto" rel="stylesheet"> 
<link href="http://your forum domain/assets/userbars.css" rel="stylesheet"> 
<link href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css" rel="stylesheet" integrity="sha384-wvfXpqpZZVQGK6TAh5PVlGOfQNHSoD2xbE+QkPxCAFlNEevoEH3Sl0sibVcOQVnN" crossorigin="anonymous">
```
* Step 4: Go into your group settings and add the following code to show the Member userbar
  * Pre-defined classes include:
  * .new-member
  * .member
  * .helper (with icon) or .helper2 (no icon)
  * .upgraded (with icon) or .upgraded2 (no icon)
  * .moderator (with icon) or .moderator2 (no icon)
```
<div class="userbar member">
  Member
</div>
```

## Custom userbars (no icon)
* Step 1: Make a new div attached to the *userbar* div:
```
<div class="userbar CUSTOMCLASSNAME">
  Custom userbar
</div>
```
* Step 2: and then style the new div by using the following template and add it to *userbars.css*:
```
.CUSTOMCLASSNAME {
  background: #FFF;         // set a background color
  border: 1px solid #FFF;   // set a border color
}
```

## Custom userbars (with icon)
* Step 1: Make a new div attached to the *userbar* div:
```
<div class="userbar CUSTOMCLASSNAME">
  Custom userbar
</div>
```
* Step 2: and then style the new div by using the following template and add it to *userbars.css*:
```
.CUSTOMCLASSNAME {
  position: relative;       // helper for the :after selector
  background: #FFF;         // set a background color
  border: 1px solid #FFF;   // set a border color
}

.CUSTOMCLASSNAME:after {
  content: '';                      // set icon value (fxxx - example f128 or f01b) from http://fontawesome.io/cheatsheet/.
                                    // !!! always put \ before fxxx - example content: '\f128'; or the icon won't show !!!
  font-family: 'FontAwesome';       // !!! do not change !!!
  position: absolute                // position absolute.
  background: #FFF;                 // set this value as the background of your class.
  border-radius: 20px;              // border-radius of the  circle.
  border: 1px solid #FFF;           // set this value as the border-color of your class.
  border-bottom: 0px                // hide border-bottom.
  width: 22px                       // default value is 22px.
  height: 20px                      // default value is 20px.
  text-align: center                // getting the icon in the center of the circle.
  padding-top: 5px                  // getting the icon in the middle of the circle.
  top: -15px                        // this valie might need some minor change to fit your forum!
  left: 42%                         // this value might need some minor change to fit your forum!
```

## Release History

* v1.02
    * Fixed userbar border to be same size across the browsers.
* v1.01
    * Added *.userbar* class to the css file.
* v1
    * Initial commit

## Meta

Distributed under the GNU General Public License v3.0. See ``LICENSE`` for more information.
