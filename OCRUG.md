# How to create static website using `blogdown`

##<span style="color:blue">Sat, 7/21/18

- Used *Hugo* Universal theme:

	```R
	devcows/hugo-universal-theme
	```


- After building site:
	
	```r
	 blogdown::serve_site()
	```

	- *Being able to view current state of website on `RStudio` live is very helpful*.

##<span style="color:blue">Sun., 7/22/18

- Create a github `repo` for `OCRUG`:

	- https://github.com/bronze10000/ocrug
	
	- managing git via `Gitkraken`:
	
		- `repo` is 'OCRUG-universal'
	
- connected to Netlify for free static hosting

	- https://stupefied-ptolemy-5c0212.netlify.com/

- Copied and loaded logo
- Copied verbage from current site 



##<span style="color:blue">Thurs., 7/26/18

- When creating a new blog post:
	- Go to: `Addins` / `New Post` /:
		- **Make sure that `subdirectory` is set to `blog`!!!**



##<span style="color:blue">Tues., 7/31/18

- Remove generic posts from directory

- Troubleshoot `domain` redirect

- Write FAQ section


##<span style="color:blue">Tues., 8/14/18

- To start new session:

	- Chose `Recent Projects`

	
##<span style="color:blue">Wed., 8/15/18

- Replace `background-banner``img`:

	- *I stitched together 4 R graphs in `GIMP`.*

		- placed in `/public/img` folder as 'OCRUGbackground.png'

		- **Change specified file:**

		```css
		.home-carousel {
  position: relative;
  background: url('../img/OCRUGbackground.png') center center repeat;
  		```


	
- Reduce the violet `opacity` masking the background-banner img:

	- In `/public/css/style.violet.css`:
	
		```css
		.home-carousel .dark-mask {
		  position: absolute;
		  top: 0;
		  left: 0;
		  width: 100%;
		  height: 100%;
		  background: #986dbd;
		  opacity: 0.6;
		  filter: alpha(opacity=60);
		}
		```
		
###<span style="color:red">*Made a big mistake!  Placed changes in `Public` folder (this will not reflect newly added code; only what is on `Master` branch of github)*


##<span style="color:blue">Thurs., 8/16/18
- R logo is missing from main banner:

	- placed `img` in `/public/img/carousel/RLogo2.png`

- OCRUG logo is missing from header:

	- placed in `/public/OCRUG_logo_small.png`

- Replace banner `img`:

	- placed in `/public/OCRUGbackground.png`
	



##<span style="color:blue">Wed., 8/22/18
- Robert Mohr's suggestions:

	- Main text should read: We have nearly monthly meetings; meetings in not plural currently. 

		- In `data/carousel/customizable.yaml`:

			- change text

	- in the address Irvine, CA should appear on a single line.

		- In `config.toml`:

			```html
		    logo = "img/OCRUG_logo_small.png"
		    logo_small = "img/OCRUG_logo_small.png"
		    address = """<p><strong>PeopleSpace</strong>
		        <br>1691 Kettering Street
		        <br>Irvine, CA
		        <br>
		        <strong>USA</strong>
		      </p>
		      """
		    latitude = "33.698155"
		    longitude = "-117.846824"
		    ```
    
   - The About Us header should be removed, or text should be placed there.  

   		- In `config.toml`:

   			```html
   			# about_us = "<p></p>"
		   # copyright = "Copyright (c) 2015 - 2016, YourCompany; 
		   all rights reserved."
		   ```
		   
		   
##<span style="color:blue">Thurs., 8/23/18
- Remove *lorum ipsum* under `FROM OUR BLOG` heading:

- #####<span style="color:red">How to add images to already published blog posts?

	- By Source (WP:NFCC#4), Fair use, https://en.wikipedia.org/w/index.php?curid=54050994

	- By <span title="must have been published or publicly displayed outside Wikipedia">Source</span> (<a href="//en.wikipedia.org/wiki/Wikipedia:Non-free_content_criteria#4" title="Wikipedia:Non-free content criteria">WP:NFCC#4</a>), <a href="//en.wikipedia.org/wiki/File:IBM_Watson_Logo_2017.png" title="Fair use of copyrighted material in the context of Watson (computer)">Fair use</a>, <a href="https://en.wikipedia.org/w/index.php?curid=54050994">Link</a>


##<span style="color:blue">Mon., 8/27/18
- Remove purple phone & email icon from top left.

	- *deleted `html` in 'text'(betw. quotes) from `config.toml`:*

		```
		# Enable or disable top bar with social icons
[params.topbar]
    enable = true
    text = """
      """
      ```


##<span style="color:blue">Wed., 9/12/18
- Install `OCRUG.ORG` domain on Netlify

	- got help from tech support to accomplish this

- Update files on Netlify

	- *`public/2018` folder was not uploaded to **github**!*
	- * There was '\*' in `.gitignore`*



##<span style="color:blue">Sat., 10/6/18
