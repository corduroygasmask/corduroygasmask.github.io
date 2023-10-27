# corduroygasmask.github.io
Solutions created by Roger Farley
***
# EZ SHOW HIDE
A show/hide solution for hand-coded HTML email using [Liquid Script](https://shopify.github.io/liquid/)

###Benefits

explain explain explain 

###Implementation

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

# BLOCKS
Tested blocks of HTML code that can be pulled into HTML email for use in many situations.
_work in progress_
