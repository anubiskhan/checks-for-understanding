## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?  
  rails new app_name  
2. What do Models generally inherit from in rails?  
  ApplicationRecord  
3. What do Controllers generally inherit from in a rails project?  
  ApplicationController
4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?  
inside the routes config call
  resources :horses, only: [:show]
5. What rake task is useful when looking at routes, and what information does it give you?  
  rake routes. it shows you all of the rails route helper paths based on your resources called in the routes config
6. What is an example of a route helper? When would you use them?
horses_path, which would take you to the index page for your horses model. when passing information from a page through the controller.
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
  #path is relative to the application while #url is absolute
8. What are strong params and why are they necessary?
  Strong params are a security feature that allows you to set only parts of the parameters to be passed through to the controller.  
9. What role does `form_for` play in helping us create our forms?
  It provides us with a set of built-in methods that the form knows to associate with a model.
10. How does `form_for` know where to submit the user's input?
  Based on which view it is completed in
11. Create a form using a `form_for` helper to create a new `Horse`.
  <%= form_for(@horse) do |f| %>
    <%= f.label :name %>
    <%= f.text_area :name %>
    <%= f.label :breed %>
    <%= f.text_area :breed %>
    <%= f.submit %>

  <% end %>
12. Why do we want to validate our models?
  To make sure we have useable information stored in our database.
13. What are the steps of the DNS lookup?
  Browser checks to see if it knows the address, then computer, then local ISP, then root server, then servers for specialized domains. After the name is matched the ip address is passed back to the client.


### Review Questions
14. How would you call the method `prance` from within the method `move` on a `Horse` instance?
  def move
    prance
  end
  (I feel like I am not understanding the question fully)
15. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3?  
height is buried 1 layer deeper. purchased belongs to the furniture hash, while height belongs to the hash that is the value for table:
16. What is inheritance?
The properties, attributes, and methods that an object has access to because it is a descendant of another object.

### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources
--> * I was able to answer most questions independently, but utilized outside resources for a few
* I was able to answer a few questions independently, but relied heavily on outside resources

Choose One:
* I feel confident about the content presented this week
--> * I feel comfortable with the content presented this week
* I feel overwhelmed by the content presented this week
* I feel quite lost by the content presented this week
