form-saver
==================

Saves form to localStorage of the browser and next time it offers to select the set of that values to be prefilled.

To save form values on form submit:
  
    FormSaver('my-saved-forms','','fill as:');
    
The div with id=aa-fs-my-saved-forms must be present and must be inside the form, you want ot save
Whole form is saved.

If you want to save just some part of the form, add second parameter like this:

     FormSaver('my-saved-forms','.mysubform','fill as:');
     
The complete working example with needed jQuery and deserialize plugin. 

    <!DOCTYPE html>
    <html lang="cs">
    <head>
      <meta charset="UTF-8">
      <title>form-saver</title>
      <link rel=stylesheet type="text/css" href="https://cdn.jsdelivr.net/gh/honzito/form-saver/form-saver.css">
    </head>
    <body>

    <form action="">

      <!-- mandatory div where the options will be presented -->
      <div class=aa-form-saver id=aa-fs-my-saved-forms></div>

        <p><label>First name</label><input type="text" name="first_name"></p>
        <p><label>Last name</label><input type="text" name="last_name"></p>

        <button>Sign up</button>
      </div>
    </form>

    <!-- jQuery and deserialize is needed -->
    <script src="https://cdn.jsdelivr.net/npm/jquery@3.4.1/dist/jquery.min.js" integrity="sha256-CSXorXvZcTkaix6Yvo6HppcZGetbYMGWSFlBw8HfCJo=" crossorigin=anonymous></script>
    <script src="https://cdn.jsdelivr.net/npm/jquery-deserialize@2.0.0-rc1/src/jquery.deserialize.js" integrity="sha256-iQpPGsHQZs7cuArBkNIa6QOJlnnf8A1RBfMLxp/MLVI=" crossorigin=anonymous></script>
    <script src="https://cdn.jsdelivr.net/gh/honzito/form-saver/form-saver.min.js"></script>

    <script> FormSaver('my-saved-forms','','fill as:'); </script>

    </body>
    </html>

