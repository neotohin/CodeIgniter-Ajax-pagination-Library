Greetings!

My name is Sean Patterson, and after using this VERY helpful jQuery Pagination
library for CodeIgniter, I wound up adding a couple updates that I thought would
be helpful for the project.

1. The anchor_class variable has been added to this library, to mirror what is
   available in the original CodeIgniter pagination library. If you need to
   assign a CSS class to all of the links in your pager, simply set the 
   anchor_class variable in your initialization:
   
   $ajax_pagination_config['anchor_class'] = 'page_link';
   
   This will apply the appropriate class to every anchor tag.

2. I've added a variable to optionally hide the "Showing 10 to 20 of 100" text
   that shows up in the pager. I needed this text hidden for my pagers, and
   initially I commented out the code entirely, but thought it would be much
   nicer to add that as an option. To enable/disable the "count" text, use the
   following variable in your initialization:
   
   $ajax_pagination_config['show_count'] = false;
   
   By default this value is set to true if you do not configure it.
   
I hope this helps folks out there. CodeIgniter is a great tool and the AJAX
pagination provided by jQuery in this code has helped me even more!

[:: Sean ::]
[:: http://about.me/dillieo ::]

*** Original README ***

Hi My name is Amzad Hossain Tohin
Blog:  tohin.wordpress.com



How to Use JQuery Pagination: 


The use is same as the built in pagination system with extra config parameter :
	$config['div'] = '#content'; /* Here #content is the CSS selector for target DIV */
	$config['js_rebind'] = "alert('it works !!'); "; /* if you want to bind extra js code */
    $config['additional_param'] = 'serialize_form()'; /* If you are using ajax pagination with Search */
    

Requirements: Make sure you have added the Jquery.js file on top of the view file. 

Put "Jquery_pagination.php" file in you application/library folder.

Don't forget to use : $this->jquery_pagination->  instead of $this->pagination



/* Include Searching with Ajax Pagniation */

1. You have a form with id 'myform' before pagination. Which holds input, textarea, selectbox etc for filtering. 
2. Create a function in view file as : 

<script type="text/javascript">
	function serialize_form() {
    	return $('#myform').serialize();
    }
</script>

3. Now add another parameter in Config of jquery pagination:
	$config['additional_param']  = 'serialize_form()';
    
4. Now you will receive filtering datas as POST in your pagination function in controller. 



Original Post Link : http://tohin.wordpress.com/2008/08/12/codeigniter-ajax-pagination/
Example Post Link : http://tohin.wordpress.com/2008/10/07/codeigniter-ajax-pagination-exampleguideline/
