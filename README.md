  MIT License                                                                  

 Copyright (c) [2026] [David Livingston aka Durangod]                          

 Permission is hereby granted, free of charge, to any person obtaining a copy  
 of this software and associated documentation files (the "Software"), to deal 
 in the Software without restriction, including without limitation the rights
 to use, copy, modify, merge, publish, distribute, sublicense, and/or sell     
 copies of the Software, and to permit persons to whom the Software is         
 furnished to do so, subject to the following conditions:                      

 The above copyright notice and this permission notice shall be included in all
 copies or substantial portions of the Software.                               

 THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR    
 IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,      
 FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE   
 AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER        
 LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, 
 OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE 
 SOFTWARE.                                                                     


 OWA Open Web Analytics CUSTOM Dark Chocolate Theme (dark_chocolate) theme by David Livingston (aka durangodave)
 This is a custom theme derived from OWA css files. Remember! Just the changes are posted here not the whole css from the original file 
 at this time we do not have custom icons for themes 
 
 if you need assistance you can reach me at csdurangodaves at outlook dot com
 please be specific (example: OWA dark chocolate theme) with your request as i have many other projects 

 version 1.0 released 11-19-2026 

Dave :)

# OWA-Dark-Chocolate-Theme
This is a custom dark version theme for OWA (Open Web Analytics). Dark and light browns, other misc colors as needed for links and necessities.  It is css mods only at this time.  We do not have custom icons at this time.  If you suffer from eye burn looking at white pages of the default OWA theme, then this dark version is a good option.


To install this theme you simple upload the theme folder and contents to your domain where you want the folder to exist.  I recommend that you place this theme folder one level up from your OWA software install.  This will prevent the theme folders from being over written or destroyed during a OWA update or install.  

Once you have the folder where you want it then go to your OWA domain location and go to 
modules/base/templates/head.php  and copy the following code into the head section.  

IMPORTANT!!  code must be copied to a specific place in the head section.  It must be copied AFTER the default css files are loaded. This will allow our css file values to be present and loaded.  

Here is a visual example using the OWA 1.14.9 version header 

`<?php /** @var \OWA\Core\ViewScope $view */ ?>`
`<!-- HEAD Elements -->`
`<?php if(!empty($view->css)): ?>`
`<?php foreach ($view->css as $cssfile): ?>`
`<LINK REL=StyleSheet HREF="<?php echo $cssfile['url'];?>" TYPE="text/css">`
`<?php endforeach; ?>`
`<?php endif;?>`

"notice above that the default OWA css files load, below that section is where you want to copy our theme code below"
"in the example below i have my OWA installed in example.com/analytics/owa_analytics/"
"to keep the custom theme folders safe from updates or deletion (see text above) i install the custom theme in
example.com/analytics/custom_css/dark_chocolate which is one level above OWA (a good place for it)

`<!-- OWA dark_chocolate custom theme by david livingston -->`
`<!-- mod by dave  -->` 
`<!-- loading custom css files -->`
`<!-- this must remain here AFTER the OWA core css files are loaded -->`
`<link rel="stylesheet" href="https://example.com/analytics/custom_css/dark_chocolate/owa_custom.css" media="screen, projection, tv">`
`<link rel="stylesheet" href="https://example.com/analytics/custom_css/dark_chocolate/owa_reporting_css_combined_custom.css" media="screen, projection, tv">`
`<link rel="stylesheet" href="https://example.com/analytics/custom_css/dark_chocolate/owa_report_custom.css" media="screen, projection, tv">`
`<!-- EMD mod by dave  --> `
`<!-- end OWA dark-chocolate custom theme code -->`

Then refresh your OWA site (you may have to press ctrl-F5 on windows to get a fresh site copy from the server).  

Done!  You should see the new theme.  
