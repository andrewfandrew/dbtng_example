# dbtng_example
### Hacking the drupal 8 dbtng_example custom module
- The master branch is a copy of the Drupal 8 examples project module
- Checkout the other branches to see my hacks

## Branches
### 'age-valid'

 This adds further validation to the update form. It prevents negative integers for age. 
 
 As an alternative you can add 'unsigned' => TRUE, to the database schema in the .install file
 but that has the unexpected effect of allowing positive integers greater than 127 for age forcing
 you to validate it in the form instead. 
 
 The reason for this is that when using the MySQL 'TINYINT' datatype if it is made 'unsigned'
 then this frees up bits and increases the range of values from roughly 0.5 x 256 to 1 x 256.
 
 #### Tips for form validation
 - Try to restrict values in the schema
 - You can adopt a belt and braces approach by applying the same in the form
 - Form validation is done at the field level and also in the form submit handler
 - Working inside the form layer you have greater control over messages displayed to the user
 
 #### Extending form validation
 - In drupal 8 you can install the symfony derived 'validator' contrib module
 - This enables a library of real-world datatype validators [symfony validator](https://symfony.com/doc/current/validation.html).
 
 

 

