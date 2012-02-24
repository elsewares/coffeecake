#CoffeeCake
##`php app/Console/bake.php --coffeecake`
-----
Bake Coffeescript for your CakePHP app.

`<?php class User extends AppModel {
	var $public $validate = array(
        'username' => array(
            'required' => array(
                'rule' => array('notEmpty'),
                'message' => 'An email address is required.'
            ),
        ),
        'password' => array(
            'required' => array(
                'rule' => array('notEmpty'),
                'message' => 'A password is required.'
            )
        ));
}

?>`

becomes:

`
class User extends Appmodel
	constructor: ->
		super()

	@validate = 	{
			username : ['required', '!null', 'An email address is required'],
			password : ['required', '!null', 'A password is required']			
			}`

