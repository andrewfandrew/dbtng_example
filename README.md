# dbtng_example
### Hacking the drupal 8 dbtng_example custom module
- The master branch is a copy of the Drupal 8 examples project module
- Checkout the other branches to see my hacks

## Branches
### age-valid

 This adds further validation to the update form. It prevents negative integers for age. 
 
 As an alternative you can add 'unsigned' => TRUE, to the database schema in the .install file
 but that has the unexpected effect of allowing positive integers greater than 127 for age forcing
 you to validate it in the form instead. 
 
 The reason for this is that when using the MySQL 'TINYINT' datatype if it is made 'unsigned'
 then this frees up bits and increases the range of values from roughly 0.5 x 256 to 1 x 256.

 

