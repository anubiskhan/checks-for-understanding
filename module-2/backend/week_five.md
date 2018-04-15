### Week 5 Questions

Re-pull from this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 5 Questions
1. How do we make flash messages display on a page?
  First we assign them to a variable in the controller method, and then we call them in the html. i.e. <%= flash[:success] %>
2. Where is cart information/temporary information usually stored?
  In a PORO.
3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?
  If you had a lot of users it would take up a lot of space. It might be slower for a customer to interact with their cart. We might want it to persist for advanced analytics.
4. What is the purpose of the asset pipeline?
  To shrink and compile our JS and SASS so that the user can actually see what we want them to see, and to see it faster.  
5. Why do we precompile our assets?
  To make sure users are actually getting what we think they are.  
6. What do each of the following tags do?

"```ruby
<%= stylesheet_link_tag "application" %> - produces an HTML tag linking your style sheets to a view
<%= javascript_include_tag "application" %> - produces an HTML tag including some JS in a view
<%= image_tag "rails.png" %> - produces an HTML tag that shows an image in a view
```"

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
  Concise, clear, organized, avoids jargon, provides setup as well as implementation examples, accessible, addresses bugs and glitches. The advantages are people will like you app more, people are more likely to use an app which shows people are maintaining it, general usability.
8. What are the top four accessibility issues that we as developers should be aware of?
  Does the user understand what they are being presented. Are they able to interact with what they have been presented. Does the presentation inform the user how to interact with it. Does the presentation encompass everything it needs to.
9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
  Of a callback. It would likely be found in the Create portion of our CRUD functionality, possibly in update.
10. Given the following object, how would we create a scope for all users who are active?

```ruby
User.create(name: "Happy", active: true)
```
Inside the user class call - scope :active, where(active: true)
11. What is the difference between a scope and a class method?
  scopes 'tell' active record that this is going to be a query method.

### Review Questions:  
12. Given the following hash:  

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```

  12a. How would you add item with id of 48 with a quantity of 4?  
    hash[:cart]['48'] = 4
  12b. How would you increase the quantity of item 29?  
    hash[:cart]['29'] += INTEGER
  12c. How would you find out how many items your user is thinking about purchasing?   
    hash[:cart].values.sum
13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?  
    An objects ability to be used in a variety of situation. It relates to duck typing in that 'if this object walks and talks like a duck it probably is'. Meaning that using an object in one way probably means it is the kind of object it seems to be.
14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  
    string.gsub(/[^0-9]/, '')
    string.insert(6, '.')
    string.insert(3, '.')

### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources
* ---> I was able to answer most questions independently, but utilized outside resources for a few
* I was able to answer a few questions independently, but relied heavily on outside resources

Choose One:
* I feel confident about the content presented this week
* ---> I feel comfortable with the content presented this week
* I feel overwhelmed by the content presented this week
* I feel quite lost by the content presented this week
