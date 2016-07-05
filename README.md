

# Jekyll powered website for projects & events

### To add a project:

For pagination to work, every new project has to be created as a "post". Therefore, every project should be created inside the <b>_posts</b> folder and respect the following guidelines:

- The file is written in markdown (.md)
- The name of the file is preceded by a date in the following format: year-month-day-. You can use the same date as another post. Although it has to be there, this date doesn't affect the rendering, so you could put 01-01-1959, it'd be fine. 
- The name of the file will be used in the url, so keep it short and simple (and of course, no blank spaces, use - to separate words)

For example, a new project could be named: <b>02-07-2016-awesome-project.md</b>

Once you've created a project, before writing its content, you have to specify elements in the YAML front matter. All that means is that you have to give each project its own variables. Layout, title and date are **mandatory** all the other ones are optional, but highly recommended. 
Note: that all the variables have to be placed inside two lines of ---

Check out this example:
<code>

`---`
- **layout: post** --------------------------------------------------<i> this is the same for every project</i>
- **title: "Awesome project with lots of tasks"** -------------------<i> the project's name</i>
- **date: 2016-01-18** ----------------------------------------------<i> the actual day when the project was added</i>
- img: "image-title.jpg" ----------------------------------------<i> Project's image. </i>
- rep: "John Doe" -----------------------------------------------<i> Name of the rep for this project</i>
- rep-img: "name.jpg" -------------------------------------------<i> Rep's image. </i>
- rep-mail: "exemple@mail.com" ----------------------------------<i> Rep's email adress </i>
- socialmatter1: "facebook" -------------------------------------<i> social media's name</i>
- sociallink1: "link-to-social-page.com/"------------------------<i> http adress of the social media's page </i>
- socialtext1: "Check out the facebook page of this project"-----<i> text to be displayed on the social button </i>

`---`

</code>

**How to use these variables:**
 
- **layout:** should always be **post**
- **img:** the project's image has to be placed in the "/img/projets" folder. If the variable doesn't exist or if nothing is specified, an image will be created, basically a rectangle filled with a specific color pattern and the name of the project in the middle. 
- **rep-img:** Has to be placed in the "/img/people" folder and should be **150x150 pixels**. If the variable doesn't exist or if nothing is specified, an auto-fill will be used: placehold.it/150x150.

- **socialmatter#:** will diplay social button(s) on the page. Simply use the official name of the social media. Ex: twitter, facebook, vimeo, youtube etc... For a website, the value should be set to **"home"**. You can specify **up to 6** social medias: socialmatter2, socialmatter3 and so on. The same goes for the sociallink(#) and socialtext(#) variables. **_IMPORTANT!_** no capital letters: instead of ~~Facebook~~ use facebook.


### To add an event (hackathon)

Inside the **_hackathons** folder, create a markdown file (.md), named after the event's title. This name will be used in the page's url.

ex: hackathon6.md

<code>

`---`
- **layout: post-hackathon** ----------------------------------------<i> this is the same for every event</i>
- **title: "Hackathon 6"** ------------------------------------------<i> the event's name</i>
- moment: "11 & 12 November 2016" -------------------------------<i> when the event is happening</i>
- place: "Central Park, NY" -------------------------------------<i> where the event is taking place </i>
- img: "hackathon6.jpg" -----------------------------------------<i> event's image.</i>
- nextevent: "true" ---------------------------------------------<i> write "true" to specify this event is "coming up" </i>
- eventurl: "buy-tickets-here.com" ------------------------------<i> link to register for the event </i>
- notes: "framapad.org" -----------------------------------------<i> link to notes/report (compte-rendu)</i>
- objectif1: "Unite" --------------------------------------------<i> first objective of the event</i>
- objectif2: "Work"----------------------------------------------<i> second objective </i>
- objectif3: "Deploy"--------------------------------------------<i> third objective </i>

`---`

</code>

**important notes on these variables:**
- **layout**: should always be **post-hackathon**
- **img**: the event's image should be placed in the "/img/hackathons" folder
- **nextevent**: Can only be used **ONCE** within all events (will be displayed on homepage). If the variable doesn't exist or if nothing is specified, the homepage will display the most recent event. 
