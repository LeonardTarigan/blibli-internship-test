# Written Test

1. What is a JavaScript Framework and explain about Vue.js as one of the JavaScript Framework!
   
   JavaScript framework is a pre-built structure with functions and features that allows developing dynamic web application easier and more organized, thus increasing efficiency and effectivity.
   
   Vue.js is one of the most popular JavaScript frameworks. It is developed by Evan You and was initially released in 2014. This framework is famous for its simplicity and efficiency in creating dynamic web application. Vue.js is flexible because it allows developers to progressively add new features and tools to existing projects. Like other JS framworks, Vue uses declarative UI where data state can be reactive, so the UI will always be synced with the current state of data.
   
2. What is the use of ellipsis?

    Ellipsis is used to hide the excessive part of a text element. Imagine we have a container 100px wide and a text 200px wide. Initially, the text will be wrapped so it fit the 100px container width. This can result in inconsistency in the number of lines. Ellipsis comes in to play when we need a maximum line to be shown to ensure layout consistency. Let's say we want the maximum number of line is 2. So the text will be fit the width of the container, wrap the words in 2 lines, truncate the remaining words and replacing it with "...".
   
3. Explain animation properties below:
   
   a. @keyframe : used to create a set of animation rule by gradually changing sets of CSS styles, example : 
    ```css
    @keyframes myAnimation {
      0% {
        /* styles at the start of the animation */
      }
      50% {
        /* styles halfway through the animation */
      }
      100% {
        /* styles at the end of the animation */
      }
    }
    ```
   
   b. animation-name : used to specify the name of our @keyframes animation rule
   
   c. animation-duration : used to set the duration of an animation, for example :
   ```css
    .animate-five-secs {
      animation-duration: 5s /* Animation will play five seconds */
    }
    ```
   d. animation-iteration : used to set how many times the animation should be played, for example : 
    ```css
    .animate-five-times {
      animation-iteration-count: 5; /* Animation will play five times */
    }

    .animate-infinite {
      animation-iteration-count: infinitr; /* Animation will play infinitely */
    }
    ```
   
   e. animation-direction : used to define whether an animation should be played in a forward or reverse direction, `normal` plays the animation forward, `reverse` plays the animation backward, `alternate` plays the animation forward and then backward, and `alternate-reverse` plays the animation backward and then forwar

5. Please explain how lazy load works in JavaScript!

    Lazy loading is used to increase the performance of our web application. It works by deferring the loading of certain resources until they are actually needed. The app will only load essential resources in the initial page load.

   The most common example of lazy loading is in image loading. Imagine we have an application like unsplash that displays bunch of images. We can use lazy loading to enhance the initial page load by just loading the images that is visible to the user. The rest of the images will be gradually loaded as the user scrolls down.
   
6. Mention at least 5 git commands and describe each function of them!
   
   a. `git init` : used to initialize new git repository
   
   b. `git clone <repo_url>` : used to copy a remote repository on our local machine
   
   c. `git add <changed_file_1> <changed_file_2> ...` : used to add changes in the staging area, we can use `git add .` to add all files to add all changed files to the staging area
   
   d. `git commit -m <commit_message>` : used to save the changes in staging area to the local repository, we can use the `--amend` flag to combine current staged changes with the previous commit without creating new commit
   
   e. `git push` : used to push the commited changes to the remote repository
