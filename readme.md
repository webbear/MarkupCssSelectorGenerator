#Markup Css Selector Generator 1.01

## Basic Usage

Once installed you can load the module in the template code on demand by using the $module variable:

	$cssClass = $module->get('MarkupCssSelectorGenerator');
	
Simply use it like:

	<html <?php echo $module->get('MarkupCssSelectorGenerator')->render(); ?>>
	
The result could be:
	
	<html class="en about about-me p-1020 t-basic-page s-about safari ipad">
	
The render() method accepts following options array:

* 'customClasses' => 'no-js|my-special-class': *multiple classes separated with pipe (|) you may use this mainly with scripts like modernizr* 
* *'class' => false*: *With class false only the generated classes will be rendered. In this case you'll have to write the class attribute. Default is true.*

Usually I use it like:

	<html <?php echo $module->get('MarkupCssSelectorGenerator')->render($options = array('customClasses'=>'no-js')); ?>>
	
or

	<html class="<?php echo $module->get('MarkupCssSelectorGenerator')->render($options = array('customClasses'=>'no-js', 'class' => false)); ?>">