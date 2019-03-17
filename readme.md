# Best Practices For Email Templates.

#### Structure First
	* Build structure of your email first(means in table with borders) 
	* So that you can be able to see what you are creating.
	
#### Test Often
	* On "litmus(putsmail)" or "mailchimp" or "email on acid"


#### Use XHTML doctype 1.0 Transitional.

	<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" 	   
        "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">

``` Add the content-type, viewport with(width=device-width, intial scale=1) this is common practice in web development.```

``` Email Design is(done in Tables) Yupp!(div,span,other-elements not supported) ```

``` 
* For Text Based Things not use any(text based tags).
* But Place Text in its own cell and apply inline styling to that cell.
```

``` Every element in email template can only have one class. ```

```
* Don't Leave Any Thing To Email Client 
  Specify Proper Width For Better Results.
  
* For Your Main container Element 
  Always Set The Size In Pixels.
  
* Able To Use Percentage.
  Inside Your Containing Element inside container.

```


``` If a Attriube exist in html, use that instead of css. ```

``` Place a centered table of (600) pixels width inside the main container table, 600 pixels is safest maximum for all the clients to better display. ```

``` Don't directly place a table inside table (In chrome dom rendering(table outside of the container table) by email clients.) * Place table inside of td tag. ```

###### ``` When using padding in email, set the value for all four sides otherwise you'll get unpredictable results. ```

###### ``` If there is also trouble with padding if (your send platform is strip your css) don't use it all Simply use empty cells to create space. ```

###### ``` In image tag adding display:block (it is a common fix that stops some email clients adding gaps underneath your images). ```

###### ``` Use align center property in "td" tag to center the image.```

###### ``` Using Percentage when your content that is a specific size suppose your images is of 260px wide with 20px margin(cell) in middle(this will result in 540) & there is padding of 30px for both the side. ```

###### ``` Insert blank cell with line-height:0,font-size:0 Add a non-breaking space charater &nbsp; in the margin-cell. ```

###### ``` Set vertical alignment to top for both the cells so that they vertically align to top, default verticle alignment is "middle". ```

``` 
* Set the width of the images using HTML at 100% 
  of the column width(to make email responsive).

* We only have to use media queries to 
  change the width of the parent element. 

* We'll have to override the height in pixels 
  because using style="height:auto" 
  won’t work in everything, So set it using pixels. 
  
* This means we'd have to set height:auto! important 
  on those images using media queries to override the pixel values.
  
* But We could do that with a single class. 
  As we set the width in percentage, we won’t need to override that. 
  
  ''' The fewer things to override, the better. ```
```

```

Gmail App for Android never supported the media queries 
However it now scales down your emails by 
reducing the size of outer table 
to fit within the viewable area of the screen.

Whenever you use css rules in the head tag you must use tools to 
convert all the css, into inline at the time of rendering.
(mailchimp or campaign moniter they automatically take care of these step)

You must do this because some clients. 
Such as Gmail, will ignore your style tag contents.

Premailer :- can be used to bring css inline.

(if tool is used, remember to take out your media queries 
Before processing. Than reinsert media queries after processing).

(You must do this because some clients, 
Such as Gmail, will ignore your style tag contents.)
