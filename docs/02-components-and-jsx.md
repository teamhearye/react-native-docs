# Components and JSX

React is pretty great because you build everything using reusable components. What are components? When creating interfaces, we can essentially break down a bunch of design elements into classes or semantic pieces. By defining these components, we can reuse or recycle them in our application => less code => fewer bugs.

Twitter's feed, for example, can be broken down into a multiple, reusable components.
![Twitter][assets/02-components-and-jsx-twitter-example.png]
A React developer would maybe separate the interface into a ProfileView component that displays information about your account, a TweetFeed component that contains a list of tweets from users you follow, as well as Trends and Who to Follow components. These components can also have their own components nested within them. For instance, the TweetFeed could have an individual Tweet component that specifies the structure and behavior of a tweet.

