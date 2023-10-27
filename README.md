# corduroygasmask.github.io
Solutions created by Roger Farley
***
# EZ SHOW HIDE
A show/hide solution for hand-coded HTML email using [Liquid Script](https://shopify.github.io/liquid/)

### Benefits

explain explain explain 

### Implementation

To an existing template, add this block to your CSS in the head:

```CSS
.ez_show_hide_mobile { max-height: 0px; font-size: 0; display: none; } 
@media handheld, only screen and (max-width: 649px) {
	.ez_show_hide_mobile { max-height: none!important; display: block!important; max-width: none!important; } 
	.ez_show_hide_desktop { display: none!important; }
	.SetW320 { width: 320px!important; height: auto!important; } 
	.SetW300 { width: 300px!important; height: auto!important; }
}
```
Add this to the beginning of your HTML doc:

```HTML
{% assign ez_show_hide_desktop_start = '<div class="ez_show_hide_desktop">' %}
{% assign ez_show_hide_desktop_end = '</div>' %}
{% assign ez_show_hide_mobile_start = '<***!--***[if !mso]>***--><***div style="display: none;" class="ez_show_hide_mobile"***>' %}
{% assign ez_show_hide_mobile_start = ez_show_hide_mobile_start | replace: '*', '' %}
{% assign ez_show_hide_mobile_end = '</div><***!--<***![endif]--***>' %}
{% assign ez_show_hide_mobile_end = ez_show_hide_mobile_end | replace: '*', '' %}
```
And wrap any desktop/mobile specific code with the variables:
```HTML
{{ez_show_hide_desktop_start}}

	[ DESKTOP ONLY CONTENT ]

{{ez_show_hide_desktop_end}}



{{ez_show_hide_mobile_start}}

	[ MOBILE ONLY CONTENT ]

{{ez_show_hide_mobile_end}}
```



***
***

# BLOCKS
Tested blocks of HTML code that can be pulled into HTML email for use in many situations.
_work in progress_
