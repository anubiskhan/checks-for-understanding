## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?  
  Information sent from a server to a client used to identify the client every time it pings the server. It can also store up to 4 mb of relevant data.
2. What’s the difference between a session and a cookie?  
  A session's info lives on the server, a cookie lives on the client. Cookies have expirations, sessions expire when the browser/page is closed.
3. What’s a flash and when do you want to use flashes?
  a flash is temporary bit of data called/shared with a user. Very useful for notifying a user if something went wrong or was submitted properly.
4. Why do people say “HTTP is stateless”?
  HTTP doesn't have any history of what just happened, or who did it.  
5. What’s authentication? Explain.
  Authentication is the practice of using some form of verification to signify that a user is who they say they are.  
6. What’s the difference between authentication and authorization?
  Authorization is the non-user side of things that denotes what a specific, authenticated user is allowed to do. i.e. user vs admin privileges
7. What’s a before filter?
  A before filter is code that lives at the controller level and tells the server to run a method prior to executing an action. i.e. is this a user? is this user an admin?  
8. How do we keep track of a user once they’ve logged in?
  Cookies and sessions.  
9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?  
  Namespacing for when the nested path is not a model object(such as admin status).  Nesting is good for when a model would only live inside another. The difference is model/non-model.  
10. At a high level, what tools can you use to implement authorization? How would you use them?  
  Sessions and cookies to identify who a user is(authenticate them), and once they are in an authenticated session I could use before methods(require admin?/user?) to make sure a user is authorized to take a certain action.
11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
  An enum is a piece of code that basically says "assign these values(typically strings) to these integer values for database purposes(typically starting at 0.)" User level(default, admin) is a data type that would use it. enums are declared at the model level.
12. What are some strategies you can use to keep your views DRY?
  Using partials for forms. before methods(i.e. assigning an instance variable for a controller to use)


### Reviews Questions
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}
]
```
(HASH.sort_by(keys[:holiday][:name])).each do |i|
  print i
end
14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300?
string.to_i

### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources
---> * I was able to answer most questions independently, but utilized outside resources for a few
* I was able to answer a few questions independently, but relied heavily on outside resources

Choose One:
* I feel confident about the content presented this week
---> * I feel comfortable with the content presented this week
* I feel overwhelmed by the content presented this week
* I feel quite lost by the content presented this week
