# dbtng_example
### Hacking the drupal 8 dbtng_example custom module
- The master branch is a copy of the Drupal 8 examples project module
- Checkout the other branches to see my hacks

## Branches
### age-valid

 This adds further validation to the update form. It prevents negative integers for age. 
 You can try adding 'unsigned' => TRUE, to the database schema in the .install but that
 allows positive integers greater than 127 so if you have to then add custom validation
 to prevent such values since the schema will no longer prevent it.

 

