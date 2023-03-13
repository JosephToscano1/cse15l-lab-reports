# How I Am Using What I Learned From This Class

In this lab report I thought that it would be fitting to elaborate on how I have used what I learned 
in cse15L to enable source control and collaboration on a personal project of mine.

This project is a mobile game that I am currently making with a recent alumni at UCSD using GameMakerStudio2, 
this report serves as a reflection of this experience so far, what I have learned, and what I need to know in case I forget
or need to start from scratch for whatever reason.

## 1. Creating The Repository and GameMaker Project 

There are different ways you can create the repo in Git according to your preference, I went with simply creating a repo on GitHub.com

There is only one way to create a GameMaker project which just involves opening GameMakerStudio2 and hitting New Project.

Repo Creation:

<img width="776" alt="image" src="https://user-images.githubusercontent.com/97120058/224610808-f99696b1-95be-45bb-9d72-5c80272ea5eb.png">

Project Creation:

<img width="654" alt="image" src="https://user-images.githubusercontent.com/97120058/224611000-54b6c4b5-9f8e-426a-96d3-47878adbd89d.png">

## 2. Enable Source Control on the GameMaker Project

This step is simple, in your GameMaker Project, navigate to settings. Once in the settings window, there will be a box to check labeled "Enable Source Control."
Check this box.

<img width="484" alt="image" src="https://user-images.githubusercontent.com/97120058/224611336-c5ed2bf5-53b9-462e-aabd-9afe8542f454.png">

Once this is done, hit apply to save your settings.

## 3. Move the GameMaker Project Folder to the Repository

Once your project is created, its contents will be saved in the same location as GameMakerStudio2 in your computer. In order for Github to be able to track
changes made to files in the GameMaker project, it must first be in the repository. Once done, your repository folder should look something like this:

<img width="668" alt="image" src="https://user-images.githubusercontent.com/97120058/224611725-59da5cb8-1367-4b14-837e-2791f1acb79e.png">

## 4. That's it, You're Done!

This will now allow any changes made to the GameMaker project to be tracked by the GitHub repository you made for it. Now, multiple people can collaborate on your game 
by utilizing branches and commits.

## 5. Tips On Collaborative Development

When working on a piece of software with a team, there are a few things to keep in mind. The main branch is one that must be kept sacred, with no bugs being introduced if it can be at all avoided.
If you are working on a new feature, make sure to first fetch and pull the main branch, then make a new branch to test and implement the feature. Once you are finished, 
merge your newly-created branch with main and resolve any conflicts. Never commit directly to main if it can be avoided. Once your branch is safely merged, you may delete it.

Any content that makes your main branch should be ready for realease.


So in summary:

1. Fetch from and push to the remote origin before and after making branches.
2. Never commit directly to main.
3. Always make new branches directly off of main as opposed to off of branches that you made.
4. Do not merge to main if there are bugs.
5. A branch can be deleted once it is added successfully.


## Conclusion

I am very glad to have been able to apply some of the knowledge that I gained in this class to a personal project of mine,
and am happy that I am diving into creating a software project with a team as opposed to on my own. I only hope to learn more in 
the future, and maybe this report taught you something new!



