# General Readme

S2N-EasyForms is a laravel / vue package that makes setting up and magaing forms and actions in your laravel applciation simple. All data is edited in the backend and this generates your forms on the front end. For simplicity the forms, fields and settings are loaded in using the JSON format.

## Getting started
---
To ensure PlusTimeIT EasyForms runs without errors there is an initial setup phase that must be completed either through our automatic command or you can do this manually. 

Before either of those options is completed you first must:
- Open up `config/app.php` and add the code below to your `providers` array. 
`PlusTimeIT\EasyForms\App\Providers\EasyForms::class` 
- You should also consider adding the below code to the `alias` array aswell.
`'EasyForms' => PlusTimeIT\EasyForms\App\Providers\EasyForms::class,` 

### --- Automatic setup
- Run the PlusTimeIT EasyForms initiate command
`php artisan SEF:initial-setup` 

### --- Vue Components
Once published the components will be added to your projects `/resources/assets/components/forms`. You only need to import the Vue component `FormLoader` into your `app.js` file.

`import FormLoader from './components/forms/FormLoader.vue';`
`Vue.component( 'form-loader' , FormLoader );`

### --- Forms
There are 2 types of forms you can create with easy forms, input and action. To edit your forms you can find them:
`/resources/data/forms`

Input forms are used for user input forms, like logins, data editing forms.
Action forms are forms that process data but don't require user input, like table data actions, view, edit, delete. 



### ---  Fields
`/resources/data/fields`

### --- Settings
`/resources/data/settings`

