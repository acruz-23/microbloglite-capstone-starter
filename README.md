# Enjoy the Microblog Project and the MicroblogLite API!

Don't forget to read the [_MicroblogLite_ API docs](https://microbloglite.herokuapp.com/docs/) and experiment with the API in _Postman!_

Practice and experimentation provide experience, and experience provides confidence.

## Collaborators

- Carlos Guardado
- Adan Cruz
- Andrew Muok
- Arondre Shelton

## Code Review

- Carlos: a small piece of code that I enjoyed doing was adding topic options to select from whenever a user is creating a new post. I definitely believe that it would be a cool feature to have in a blogging page, that way the reader can see what type of post it will be by just adding a topic.

- Adan: The toughest part of this project, for me anyways, was dynamically generating a like button, to add and remove likes, for every post on the page. After trying various methods, I finally got it working by setting an onclick event that calls a function to either remove or like a post. Once clicked the button will call a fetch requests and then change the onclick to call the opposing function. For example, if a button is clicked to remove a like that button's properties will change as follows:

 ```
        const clickedBtn = document.querySelector(`button[id='${postId}']`);
        clickedBtn.setAttribute("onclick", `likePost(this.id)`);
        clickedBtn.removeAttribute("class");
        printLikes(postId, clickedBtn);
```
A class is added/removed to visually represent if the post is liked. A function printLikes is also called to get an accurate count of likes.

- Arondre: My main role in this capstone project was CSS. I personally selected and coded various styles for different elements and classes on the Microblog web page, setting the background color, text color, and button styles to create a consistent visual theme using shades of teal and light gray. 
- (Arondre:) Additionally, I added JavaScript code to the posts.js file, which includes a dropdown menu ('sortDropdown') that allows us to sort the posts based on different criteria such as creation date, username, or the number of likes. When the sorting option is changed, the ('getPosts') function is called to retrieve and display the sorted posts. This feature enables us to view posts in a customized order.
 



- Andrew: The code i found the most interesting was figuring out how to see more than the default 100 posts from users on the posts page. As a group, we had a difficult time figuring out how to see more than 100 posts until we realized we had to set the query parameter limit to 2000. 
```
fetch(apiBaseURL + "/api/posts?limit=2000", options)
    .then((response) => response.json())
...
```
## And another section here
