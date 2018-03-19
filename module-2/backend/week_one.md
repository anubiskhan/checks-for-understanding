## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.  
GET, POST, PATCH, DELETE, PUT  
2. What is Sinatra?  
A web framework for Ruby  
4. What is MVC?  
Model, view, controller  
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?  
To adhere to RESTful routing.  
6. What types of variables are accessible in our view templates without explicitly passing them?  
instance, class, and global variables  
7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    erb :index
  end
  ```  

Add @count = 1  
8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?  
Add @name = 'Mr. Ed'  
9. What's the purpose of ERB?  
To write HTML with ruby commands in it.  
10. Why do I need a development AND test database?  
For sanitation and to make sure you don't destroy your actual data.  
11. What is CRUD and why is it important?  
Create, Read, Update, and Delete. It is basic functionality that all databases should have.  
12. What does HTTP stand for?  
HyperText Transfer Protocol  
13. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?  
<%= %> and <% %>. The former will print to the page while the latter will not.  
14. What's an ORM?  
Object relational mapping. It allows you to interact with the databases using Objects.  
15. What's the most commonly used ORM in ruby (Sinatra & Rails)?  
ActiveRecord.  
16. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.  

get /restaurants -> takes you to restaurant index  

get /restaurants/new -> takes you to the form to make a new restaurant  

post /restaurants/new -> sends a post command allowing you to actually create a new restaurant  

get /restaurants/edit -> takes you to the form to edit an existing restaurant  

patch /restaurants/edit -> sends a patch command allowing you to actually create a new restaurant  

get /restaurants/view -> takes you to view a specific restaurant  

delete /restaurants/delete ->   sends a delete command allowing you to delete an instance of a restaurant  


17. What's a migration?  
A way in which you can alter the schema for your db.  
18. When you create a migration, does it automatically modify your database?  
No, you need to migrate it first and then seed your database after your schema has been effected by the migration.  
19. How does a model relate to a database?  
A model is the middle-man for your controller and db. It handles the logic portion of your server/db.   
20. What is the difference between `#new` and `#create`?  
With new you need to also save. Create makes a new instance AND saves it.  

### Review Questions:  
21. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  
CSV.foreach('./data/films.csv', OPTIONS) do |film|
  Film.create(film.to_h)
end   
You would also need to create a Film model.  
22. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone'],
  brunch: {cost: $35, supplies: ['mimosa flutes'],
  antiquing: {cost: $200, supplies: ['list of antique stores']
}
```
How would I add 'granola bar' to things you should have when hiking?  
activities[:hiking][:supplies].push('granola bar')  
23. What are the 4 Principles of OOP? Give a one sentence explanation of each.  
Encapsulation -  That the relative properties of an object exist as part of itself. I.e. it creates its own function.  
Abstraction -  The framework of how something should work, without being a specific instance.  
Inheritance - The properties that an object has a result of it's superclasses and ancestors.  
Polymorphism -  An object's ability to change and alter specifics within the scope of its encapsulation.  


### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources
* ---> I was able to answer most questions independently, but utilized outside resources for a few
* I was able to answer a few questions independently, but relied heavily on outside resources

Choose One:
* I feel confident about the content presented this week
* I feel comfortable with the content presented this week
* ---> I feel overwhelmed by the content presented this week
* I feel quite lost by the content presented this week
