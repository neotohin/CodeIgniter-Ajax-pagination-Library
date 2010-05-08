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
