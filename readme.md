# Secure Users 'r' Us

SUrUs is the internet's most frequented username/password security/listing site. Many users have come to depend on our services and as we develop new features and attract new users, we need a way to ensure that nothing that we add breaks the existing functionality which our current users trust.

Your job is to define the RSpec examples which describe the behavior of names of User.

To get started clone, this repo. Before you can write tests, you'll need to set up a database called rspec_user_db and run the schema.rb and seeds.rb files.

In terminal, in the root directory of this project, run `rspec` (or `rspec -f d` to see with a more detailed presentation) and you'll see ten examples of the behavior of names. If you look in the user_spec.rb file, you will see the same descriptions with additional key words.

Back in the terminal, at the bottom of the rspec output the bottom line says 10 examples, 0 failures, 10 pending. This is because when you can declare an example before defining it. When you run the test with the undefined example it won't count as a failure or a pass but rspec will note the number of pending example you have yet to implement.

In user_spec.rb, insert `do...end` block at the end of line seven. Here you define your example. In the block we write the ruby necessary to produce the behavior we want to define followed by our specs or matchers. A spec is made of two parts, an expectation and a matcher.
```ruby
it "#name returns name when set" do
  bob = User.new(name: "Bob", username: "bdylan" )
  expect(bob.name).to eq("Bob")
end  
```
