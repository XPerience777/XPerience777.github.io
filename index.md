---
layout: default
---

# Table of Content

1. Professional Self-Assessment
2. Artifact 1: Final_Cole_Doty 
  - Source Files
  - Enhancement 1: Software Design and Engineering
    - Code Review
    - Narrative
  - Enhancement 2: Algorithms and Data Structures
    - Code Review
    - Narrative
3. Artifact 2: CS360_Weight_Tracker_App
  - Source Files
  - Enhancement 3: Databases
    - Code Review
    - Narrative

# 1. Professional Self-Assessment

I have been getting my bachelor’s degree in computer science since fall of 2019. I went to in person classes at SIUE for 2 years before COVID struck. I had to transition to online remote learning with SNHU for the remaining 2-3 years of my degree before Graduating in the spring of 2024. Thus, taking a total of 5 years to earn my bachelor’s degree in CS. 
While studying CS in university I have learned many core skills that helped me develop in my field. Being able to troubleshoot and research on the fly, how to use proper coding practices to make secure code that’s easy to read, and how to code and develop programs in Java, C++ ,C , and Python with various sub languages along the way. 
I’m looking to enter the workforce searching for an IT based occupation. Some job opportunities I’m looking at currently are software engineering, systems analysis, and networking. I’m fast to learn new techniques and I enjoy working with others in my field so I’m looking forward to the beginning of my carrier where I can begin to train in my field.

# 2. Artifact 1

This artifact was an OpenGL program developed in C++ that renders a 3D scene of my personal desk space. It was my final for my online CS330 course at SNHU back in early 2023. 

I included this artifact because it was left in a state that I knew I could improve greatly within a reasonable amount of time. It also fits 2 of the 3 categorical improvements required for my CS499 capstone project. It also allows me to present my skills in OpenGL and C++ coding while using best coding practices such as proper structure, spelling, commenting, and iterative development.

When I originally submitted the code, it had a very simple scene that was simply floating in a void. I set out to improve this scene by fully modeling a room designed around my current desk workspace setup and layout. I have implemented proper structure, naming, spelling, and commenting in my code to help with the readability and clarity in the code. Over the course of the artifact’s development, I have created many supplementary documents, plans, and code reviews to help with the outside development and understanding of my project. The project uses techniques I’ve learned during my time at SNHU varying from basic C++ coding to the implementation of OpenGL libraries and techniques that build a digital 3D scene. I applied proper computer science practices and standards to all of my code while properly updating the data structures and algorithms such as the stored data for lighting, reflections, textures, and the rendering algorithm updated with a multisampling antialiasing algorithm and FPS counter.

### Source Code
Currently updated version on "Main" branch while original version in on "original 1.0 Version" branch.
**Repository Link:** https://github.com/XPerience777/Final_Cole_Doty

### Enhancement 1: Software Design and Engineering
##### Code Review

https://youtu.be/iWtP-i88p9k

##### Narrative

The original code only has a handful of flat low-resolution textures with lighting that just floated aimlessly to light the scene with no real direction in mind just so it looked vaguely like the source scene. I decided to create custom textures by photographing the object in my room the scene is based off of using my phone. This way the scene could be textured with a one-to-one look to the reference material. 

I then set out to update the lighting to originate from the models that reference the scene’s lamp lighting, so the reflections and lighting direction looked more organic. I added a light for the overhead ceiling lamp, the standing lamp, and a light for the screen and keyboard light. Each has a color and lighting intensity unique to each of them that matches their real-life counterparts. I also softened the reflection intensity for each light individually to show the different diffusion levels through the lamp shades. Lastly, I added multisample x16 anti-aliasing (MSAA) to the rendering algorithm to smooth out the edges of the models to give a smoother and softer look with less pixelization.

### Enhancement 2: Algorithms and Data Structures
##### Code Review

https://youtu.be/xtOr_FlUygw

##### Narrative

The original code only has a handful of flat low-resolution textures with lighting that just floated aimlessly to light the scene with no real direction in mind just so it looked vaguely like the source scene. I decided to create custom textures by photographing the object in my room the scene is based off of using my phone. This way the scene could be textured with a one-to-one look to the reference material. I then set out to update the lighting to originate from the models that reference the scene’s lamp lighting, so the reflections and lighting direction looked more organic. I added a light for the overhead ceiling lamp, the standing lamp, and a light for the screen and keyboard light. Each has a color and lighting intensity unique to each of them that matches their real-life counterparts. I also softened the reflection intensity for each light individually to show the different diffusion levels through the lamp shades. Lastly, I added multisample x16 anti-aliasing (MSAA) to the rendering algorithm to smooth out the edges of the models to give a smoother and softer look with less pixelization. I also add a FPS counter for performance clarity.

While implementing these updates I made sure to remove some redundant texture binding to reduce the number of unnecessary operations. I also Standardized the texture size to a maximum of 900px to keep the textures clear without the file being too large and slowing down the rendering algorithm possibly causing any loading problems. In the rendering algorithm I also added multisampling at a x16 multiplier in uRender. At higher multipliers there was little to no visual difference to justify the increased impact to performance so 16 struck the perfect balance of visual fidelity vs performance. I also made sure that the program ran smoothly at a resolution of 1920 x 1080 as that is the industry standard window resolution. I also implemented a V-Sync FPS limit algorithm so the program only has to render so many frames a second equal to your monitor refresh rate, generating a smooth framerate. The window will list the FPS and milliseconds in the Title of the window.

I tried to keep the algorithmic functions in the code as simple and efficient as possible as well. The main rendering loop is a simple recursive algorithm that loops until the window is closed. The time complexity of this main rendering loop is linear due it being a single recursive while loop that only negatively scales its performance based on the input size of the methods called. The only other algorithm present in the program is the flipImageVertically() method the vertically inverts the textures as they are initially loaded and stored in static memory. The algorithm would normally be costly due to its quadratic time complexity (O(n^2)) due to its nested loop, however it actually has very low impact due to only having to quickly run once upon running the program exclusive of the constantly looping rendering algorithm. 



# 3. Artifact 2

This artifact is a weight loss tracker app developed with Android Studio and coded in Java. It was my final for my online CS360 course at SNHU back in early 2023.


### Source Code
Currently updated version on "Main" branch while original version in on "original 1.0 Version" branch.
**Repository Link:** https://github.com/XPerience777/CS360_Weight_Tracker_App

### Enhancement 3: Databases
##### Code Review

https://youtu.be/mSosvgSlPsM

##### Narrative

The original codes authentication was just a simple database that stored the username and password of the user for future logins. I set out to add the option of signing in with Google authentication due to the fact that this app is designed for android so almost every user will have a Google account tied to their device that they can use seamlessly. 

After doing some research on the implementation I began building out the UI first to fit the current layout of my app. I added some dependencies that gave me access to Google operations and visual assets and implemented the buttons first with no functionality tied to them, adding in the functionality as I need to. I then started working on the login by initializing the Google database and enabling internet permissions to the app. When the new button is pressed the built in google authentication on Android is called asking for the user’s login credentials. Upon successful login the weight tracker window swaps in. I also added an onCreate function that lets the user stay signed in upon reentering the app if the user has already successfully signed in. This meant I needed to implement functionality that allowed the user to sign back out in case they didn’t want to remain signed in or wanted to change accounts. I added a button to the apps taskbar that when clicked would sign out the Google account and swap back to the login screen. 

Once the functionality was fully implemented, I needed to set up the Google database account tie in using Google Cloud’s API credential service. What I didn’t realize was that their system has undergone an overhaul recently, so I had to make a few tweaks to my code to have the proper OAuth dependencies that worked with the new system. After some trial and error I found the proper dependencies and everything clicked into place allowing my app to interface with Google account services completing my enhancement 3.

