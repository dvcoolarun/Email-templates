#This Repo Belongs to Basic Email Templates with Best Practices.

** Structure First
-> Build structure of your email first(means in table with borders) so that you can be able to see what you are creating().

** Test often
-> on litmus(putsmail) or mailchimp or email on acid

** Build

Using an XHTML doctype 1.0 Transitional has the fewest headaches.

####<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"

adding the content-type, viewport(with width=device-width, intial scale=1) this is common as Web design.

Email Design is(done in table) Yupp!(div,span, other element not supported)

** for text not use any(text based tags) but place text in its own cell and apply inline styling to that cell.

* Every element in email template can only have one class

** Don't leave any thing to email client specify proper width for better results.(for your main container element always set the size in pixels Able to use percentage inside your containing element)

** if a attriube exist in html use instead in place of css.

** place a centered table of (600) pixels width inside the main container table, 600 pixels is safest maximum for all the clients to better display.

** don't directly placed a table inside table (in chrome in dom rendering) it showing table outside of that particular table place table inside of td tag

** when using padding in email set the value for all four sides otherwise you'll get unpredictable results

** if there is also trouble with padding if (your send platform is strip your css) don't use it all Simply use empty cells to create space .

** in image tag adding display:block (it is a common fix that stops some email clients adding gaps underneath your images)

** align center to "td" tag to center the image.

** Using Percentage when your content that is a specific size suppose your images is of 260px wide with 20px margin(cell) in middle(this will result in 540) & there is padding of 30px for both the side

** insert blank cell with line-height:0 , font-size:0 Add a non-breaking space charater &nbsp; in the margin-cell.

** set vertical alignment to top for both the cells so that they vertically align to top, default verticle alignment is "middle".

** Here we have set the width of the images using HTML at 100% of the column width. This, again, is so that if we make this email responsive, we only have to use media queries to change the width of the parent element. We'll have to override the height in pixels because using style="height: auto" now won’t work in everything, So we’ll set it using pixels. This means we'd have to set height: auto!important on those images using media queries to override the pixel value, but we could do that with a single class. As we set the width as a percentage, we won’t need to override that. The fewer things to override, the better.