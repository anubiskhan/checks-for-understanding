## Week Two - Module 2 Recap

Fork or re-pull this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!).

Note: When you're done, submit a PR.


### Week 2 Questions

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
  ActiveRecord is an ORM that allows us(or programs like rails) to interact with a SQL database.  
2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
  .all, .find, .order. They are provided by the inheritance from ActiveRecord
3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of  Assuming your class only included the code from question 2, how could you find the owner of the same team?
  Team.find(4) and Owner.where(team_id: 4)
4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?
  Team.find(4).owner
5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
  teacher has_many :students, student belongs_to :teacher.
6. Define foreign key, primary key, and schema.
  A primary key is a value in a database entry(traditionally its index integer). A foreign key is a value in a database entry that relates to the primary key in another table. A schema shows the columns that a table(s) has and any primary/foreign key relationships.
7. Describe the relationship between a foreign key on one table and a primary key on another table.
  Represents a one-to-many relationship, where the primary key on one table is related to many entries on the table with the foreign key
8. What are the parts of an HTTP response?
  Verb, Path and Protocol, header, body


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
  rake db:create - creates the db
  rake db:migrate - runs the migration(s) to build out or amend the table(s) in the db
  rake db:seed - populates the db tables using data
3. What two columns does `t.timestamps null: false` create in our database?
created_at and updated_at
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
  one to many.
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
  school has many teachers, teacher belongs to school. (presumably)
6. Give an example of when you might want to store information besides ids on a join table.
  timestamps
7. Describe and diagram the relationship between patients and doctors.
many to many
8. Describe and diagram the relationship between museums and original_paintings.
one to many. painting belongs to museum. Museum has many paintings
9. What could you see in your code that would make you think you might want to create a partial?
  duplicated html text

### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources
* I was able to answer most questions independently, but utilized outside resources for a few
--> * I was able to answer a few questions independently, but relied heavily on outside resources

Choose One:
* I feel confident about the content presented this week
* I feel comfortable with the content presented this week
--> * I feel overwhelmed by the content presented this week
* I feel quite lost by the content presented this week
