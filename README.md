# 🖥️ CS50 WEB : Final Project - Studynotes

   For the final project of the amazing course **"CS50’s Web Programming with Python and JavaScript"** taught by Brian Yu and provided by Harvard University, I decided to make a project called **Studynotes.**

![homepage](https://user-images.githubusercontent.com/66017329/179422206-aad4ce14-e879-49f0-a818-71aa6d5ce33b.PNG)

   **Studynotes** is a concept of a web application I had in mind at the beginning of the pandemic, where I found my self like many other students stuck at home attending classes online. I searched for a tool where I can take my notes while listening and seeing the lecture, but all the available apps didnt have the option I was looking for, I was constantly ALT-TABing to take my notes, which led to poor concentration during my classes and resulted in a bad performance on my final exams.

   The solution I came up with is to combine my method of note-taking which is inspired by The Cornell Method for note-taking that I use on my text-books and a video frame that contains the lecture or course you wish to attend. For this first version of the application, I used the **YOUTUBE API** to display a youtube video either live or pre-recorded *(but ideally it would be any platform the university is using to broadcast their live classes)* and just under it a place where to take your notes and style it as you wish using the **QuillJS** a rich text editor. And in addition to that, a Calendar section is added to help the user track his deadlines for projects and upcoming exams.

   A note-taking app is definitely not a new or revolutionary idea, but it definitely solved my problem with online classes and I hope it will help other students too, and I will gladly take feedback from users and constantly improve the application. In conclusion, I believe that "Studynotes" is totally distinct in concept from previous projects and it is fairly complex in execution in my opinion, as I have spent months working on this application from learning about UI/UX and TailwindCSS for a better looking and responsive website to researching how to integrate any API to my Django application and keeping everything as secure as possible.

---

![search](https://user-images.githubusercontent.com/66017329/179422281-54ed81d2-7ed8-4f32-a8e0-dce719d803a8.PNG)
![layout](https://user-images.githubusercontent.com/66017329/179422284-24092a78-f30c-4917-8b2f-35fe2f7d3f61.PNG)
![noteview](https://user-images.githubusercontent.com/66017329/179422290-3ae5a2dc-e021-44fb-aa59-6347f5b821f1.PNG)
![notes](https://user-images.githubusercontent.com/66017329/179422291-00b416c4-5f4c-46cb-ade1-49b0bd682340.PNG)

## How to run Studynotes

1. First step is to generate a [Youtube API KEY](https://www.embedplus.com/how-to-create-a-youtube-api-key.aspx) then remplace the **YOUTUBE_API** in settings.py by your own API key :

- When you open **studynotes/setting.py** you should see in the last few lines :

```
import environ
env = environ.Env()

\# reading .env file
environ.Env.read_env()

YOUTUBE_API = env("YTB_API") 
```

- After getting your API KEY, you should delete all the lines from ``import environ`` to ``environ.Env.read_env()`` except the last line where you should replace your API KEY :

``YOUTUBE_API = "YOUR API KEY HERE"``

Then save the file.

2. Now just open up your terminal and run these commands :

```
pip install -r requirements.txt
python manage.py makemigrations
python manage.py migrate
python manage.py runserver
```

📓 And there you go ! Enjoy taking your notes the most optimal way.

