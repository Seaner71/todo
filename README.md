# README

## Todo  application built using rails 

* Ruby Version 2.3.3
* Rails Version 5.1.4

### Applicationfor building out to do list with sub to do items

- Has 2 models *Todo_list* and *Todo_item* 
- allows a user to create todo list with multiple items. a user can "cross off' completed items

### Future enhancements scheduled
 - user authentication
 - adding due dateand calendar functionality
 - testing and tougher validation of models

* DB Schema

```
ActiveRecord::Schema.define(version: 20180124015538) do

  create_table "todo_items", force: :cascade do |t|
    t.string "content"
    t.integer "todo_list_id"
    t.datetime "created_at", null: false
    t.datetime "updated_at", null: false
    t.datetime "completed_at"
    t.index ["todo_list_id"], name: "index_todo_items_on_todo_list_id"
  end

  create_table "todo_lists", force: :cascade do |t|
    t.string "title"
    t.text "description"
    t.datetime "created_at", null: false
    t.datetime "updated_at", null: false
  end

end
```

Run on your computer:

From your project folder, clone the git repository:

    git clone https://github.com/Seaner71/todo.git

Open the project folder:

    cd todo
  
Install all dependencies:

    bundle install
  
Create the database:

    rake db:migrate

Run the application:

    rails server

To see the application in action, open a browser window and navigate to http://localhost:3000.

* ...
