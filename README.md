# Project 2 - Breaking Bad Characters


<h2>Description</h2>

This project’s goal was to pull data from various APIs to create a character index for the infamous TV-show ‘Breaking Bad’. The final product consists of different functionality, such as the ability to search a character by their name, as well as filtering them by their status (whether they were alive or deceased by the end of the show). When clicking on a character, more information gets displayed, including their in-show nickname, occupation and series appeared in. As an additional feature, a button was introduced to their individual page, that displays a random quote from the respective character.

This project used CSS, JavaScript, React, and elements from react-router-dom, react-bootstrap and Axios.



<h2>Deployment link</h2>

The project was deployed on the netlify app. It can be found in the following link and requires no log in to be used:

https://sweet-puffpuff-02d75b.netlify.app/characters



<h2>Getting Started/Code Installation</h2>

The code can be found on<a href="https://github.com/a-ullmann/breaking-bad"> my personal GitHub page.</a>




<h2>Timeframe & Working Team</h2>

This project was completed within two days in a group of two. It was a pleasure working with Archie Rowan Hamilton. 



<h2>Technologies Used</h2>

<h4>CSS:</h4>
<ul>
  <i>Styling of the individual elements on all pages</i>
Various flex-box elements to position them dynamically
Imported custom font
Conditional colouring of their status
</ul>

<h4>React-Bootstrap:</h4>
Getting first experience with using bootstrap, allowing for a more efficient way of styling. 

<h4>JavaScript & React:</h4>
Axios was used to fetch data from three different APIs
Imported from react, we used useState to track the state of data and useEffect to control the data after a render. This allowed our site to be more responsive and therefore more enjoyable for the user. 
To navigate between our internal pages, we imported Link from react. 

<h4>Other:</h4>
Insomnia was used to inspect the different APIs and gain paths to specific keys. 
Excalidraw.com to draw wireframes and sketch out the project.



<h2>Brief</h2>

Create a functional and interactive app with React using APIs. </br>
​
<h5>The app must:​</h5>
Consume a public API – this could be anything but it must make sense for your project.</br>
Have several components</br>
The app can have a router - with several "pages", this is up to you and if it makes sense for your project.</br>
Include wireframes - that you designed before building the app.</br>
Be deployed online and accessible to the public (hosted on your public github, not GA github!)</br>
​​


<h2>Planning</h2>

As this was my second project, I was prepared to plan more specifically than my first. My partner and I used Excalidraw to wireframe our ideas. We initially had a different API we wanted to work with, but after inspecting it closely, we decided to choose the Breaking Bad APIs as the data from the initial API was not clean enough to fit our goals. The decision making was always split between my partner and I and we worked together throughout the project using live-share in VScode. This created a great dynamic of us working together and splitting the tasks as we go. We defined our MVP as having three different pages; first would be the landing page, which would welcome the user with an eye-catching gif. From there, the user would be able to navigate to the character list. This list would contain all the characters pulled from the API, as well as a search function and a filter function. Once the user clicks on a character, they would be navigated to the individual character page, consisting of useful information of that character. As a target product, we wanted to include a button that displays a random quote of that character, which was pulled from a different endpoint. 



<h2>Build/Code Process</h2>

As initially stated, we worked on this project simultaneously using live-share on VScode. We split up the tasks by pages but at the same time, helping each other if there was a problem. My task was to get started on the landing page and create the character list, while Archie was set on the individual character page. 

To get started, I created a useState as an empty array to have a place to store the characters. Following that, I created a useEffect that would load only on render, to fetch the data from the API with Axios. This was wrapped in a try / catch, which would either result in getting the data, or (catch) show an error message.


Using bootstrap, the function would return a grid-like page with each character being displayed with their image and in-show name, as well as nickname, which can be seen in the screenshot below.


After creating the list, it was time to create a function to filter the characters. Here we stored values in a useState which would then be changed based on the user's decisions. We used a .filter method to filter through the characters and compared with a RegExp test, case insensitive. 




We used an onChange command in combination with our handleChange function to determine the outcome. 



<h2>Challenges</h2>

The biggest challenge by far was to implement the search function. Getting it set up took us a long time as using RegExp was very new to us. After a lot of trial and error, some research and input from our instructor, we managed to successfully implement it. 
Another challenge we came across, seemed like an easy fix but turned out to be more difficult than we thought. When we imported the ‘occupation’ and ‘series appeared in’, it would return the data as a combined string. For example, ‘series appeared in’ would appear as: ‘12345’ instead of ‘1, 2, 3, 4, 5’. This same problem would appear for the characters’ occupation.  In the end we created a work-around of the following: 

This had to be done due to the fact that we could not directly mutate the state of the data. We had to take the individual keys, spread this into a new object, take its values and join them with a comma and a space. This would render every time characters are rendered. 



<h2>Wins</h2>

A win for me was to effectively solve the challenges we encountered during the coding process. I am very glad that I had to work on certain functionalities, such as the search bar, as I am certain that I will reuse this knowledge in multiple projects in the future. Another win for me was to work closely in a team allowing me to learn from my classmates and vice versa. As this was my first time working in a group, it made me realise how much can be learned from other team members. 



<h2>Key Learnings/Takeaways</h2>

A big key takeaway for me is to have learned how to use APIs. in my opinion, it is a very useful ability to have and to work with. It was also a great experience to have worked in a group as it shows the strengths and weaknesses of myself to then use these to my advantage in a professional environment. 



<h2>Bugs</h2>

We encountered several bugs which we did not manage to solve before our deadline. One of these bugs included a false filtering when filtering the two shows. We wanted to have the ability to show characters from Breaking Bad as well as Better Call Saul (the shows are related to each other and share characters). Unfortunately, when filtering for Better Call Saul, only characters who were in Better Call Saul and not in Breaking Bad would show. This due to the key being one string and having both shows in that string. We would have to disassemble this string, create an array of it and then use it for the filtering. This was not possible as we ran out of time. 



<h2>Future Improvements</h2>

Future improvements would include more specific planning. This skill will develop the more projects I am part of as it becomes clearer how the process of completing such projects looks like. Furthermore, splitting the work in a more specific way would also be of great benefit, as it would result in less overlapping work and/or confusion. 



