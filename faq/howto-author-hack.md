# gHacks - How to Author a gHack

Developing a new gHack is a great way to get your content out to the world. Chances are if you've done workshops or PoCs in the past, you already have the material on which to base a gHack.

## Why gHack?

The gHack "challenge" format is perfect for team-based, hands-on learning experiences.

gHack is all about being "for the people, by the people". This repo was originally created to share real-world hackathons that Google Cloud teams have hosted with their customers. Here are our core principles:
- Anyone can contribute a hack.
- Anyone can use the content to host their own event.
- Anyone can modify the content as needed.
  - Submitting a pull request for modified/improved content is encouraged.
- The content can always be shared with attendees **(Only do this after the event is over!)**

## What Does It Take To Create a gHack?

When you design a gHack, these are the things you should consider:

- [Hack Description](#hack-description) (aka "The One Pager")
- [Challenge Design](#challenge-design)
- [Student Resources](#student-resources)
- [Presentation Lectures](#presentation-lectures) (optional)
- [Coach's Guide](#coaches-guide)
- [Coach Solutions](#coach-solutions)

If you create things in this order, you will be able to flush out a new hack rapidly. 

**HINT:** The Coach's guide and Coach Solutions is the most detail oriented & time consuming item to produce.  Shhh...  don't say we told you this, but hack authors have been known to write the Coach's Guide as a post-mortem from their first run of the hack.

## Hack Description

Why should someone take the time to deliver or participate in your hack?  This is the main question you need to answer in order to define your hack. Every gHack needs to have an executive summary (aka "one pager") that quickly describes your hack to those who will host or attend your hack. Think of this as your marketing pitch. 

**HINT:** The "Hack Description" can serve a dual purpose. If you take the time to write it first, it can be the outline or specification for your hack before you develop the actual content.

The "Hack Description" shall be the README.md that lives in the root of your hack's top level folder.

The "Hack Description" must include the following:

### Hack Title

Give your hack name. Keep it short, but consider giving it a "fun" name that is more than just the name of the technologies that the hack will cover.
  
### Introduction

This is your chance to sell the casual reader on why they should consider your hack. In a paragraph or two, consider answering the following questions:

- What technologies or solutions will it cover? 
- Why are these technologies or solutions important or relevant to the industry?
- What real world scenarios can these technologies or solutions be applied to?

### Learning Objectives

This is where you describe the outcomes a hack attendee should have. Provide a short list of key learnings you expect someone to come away with when they complete this hack.

### Challenges

Every gHack is made up of a collection of technical challenges. For the one pager, you should list out your challenges by name, with no more than a single sentence description for each unless the challenge title is descriptive enough on its own.

For most this page will act as a "Table of Contents" for your hack. We recommend that you create links for each challenge to its respective challenge page.

### Prerequisites

Provide a list of technical prerequisites for your hack here.  List out assumed knowledge attendees should have to be successful with the hack. For example, if the hack is an "Introduction to Kubernetes", the attendee should have a basic understanding of containers.  However, if it is an "Advanced Kubernetes" hack, then the attendee should know the basics of Kubernetes and not ask you what a "pod" or "deployment" is.

Provide a list of tools/software that the attendee needs to install on their machine to complete the hack. 

### Repository Contents (Optional)

While optional, it is a good idea to provide a catalog of the files you are providing with your hack. 

### Contributors

Finally, give yourself and your fellow hack authors some credit. List the names and optionally contact info for all of the authors that have contributed to this hack.

### Hack Description Template

To help you get started, we have provided a sample template for a Hack Description / "one pager" here:
- [Hack Description Template](gH-HackDescription-Template.md). 

Please copy this template into your hack's root folder, rename it to "README.md", and customize it for your hack.

## Challenge Design

Challenges are at the heart of the gHack format. Designing challenges is what a hack author should spend the majority of their time focusing on. 

There are different approaches to designing a hackathon. If you are familiar with the Marvel Comic Universe movies, you know that they follow one of two patterns:
- "Origin Story" - A movie focused on the back story of a SINGLE superhero that lets the audience get to know that character in depth (perhaps with a sidekick character or two included).
- "Avengers Story" - A movie with an ensemble cast of superhero characters working together to solve a mega problem, with each character getting varying amounts of screen time. 

You can use the same patterns when designing a gHack.

- Singleton Hack - A hack designed to give in-depth hands-on experience with a specific technology and maybe a "sidekick technology" or two included.
- Solution Hack - A hack designed to give experience solving a real-world scenario that involves using multiple technologies together for the solution.

Once you have decided what type of hack you want to create, you should follow these guidelines when designing the challenges:

- Include a “Challenge 0” that helps attendees install all of the prerequisites that are required on their computer, environment or GCP account.
- Challenge descriptions should be shorter than this section on how to design challenges. Keep it to a couple of sentences or bullet points stating the goal(s) and perhaps a hint at the skill(s) needed.
- Think through what skills/experience you want attendees to walk away with by completing each challenge
- Challenges should be cumulative, building upon each other and they should:
    - Establish Confidence – Start small and simple (think "Hello World")
    - Build Competence – By having successively more complex challenges.	
- Each challenge should provide educational value.  
    - For example, if an attendee completes only 3 out of 7 challenges, he/she still walks away feeling satisfied that they will have still learned something valuable.
- Take into consideration that a challenge might have more than one way to solve it and that's OK.
- Provide verifiable success criteria for each challenge that lets the coaches and attendees know they have completed it.
- Provide relevant links to learning resources that should lead the attendees toward the knowledge they need to complete the challenge.
- Provide hints for items that could potentially be time consuming to figure out but are of low learning value or relevance to the actual goal of the challenge. **For example:** A command line parameter that is not obvious but would take hours to debug if it were missed.
- Do **NOT** provide a list of step-by-step instructions. These are challenges designed to make the attendees learn by solving problems, not blindly following instructions.

### Challenge Template
To help you get started, we have provided a sample markdown template for a hack Challenge here:
- [Challenge Template](gH-Challenge-Template.md). 

Please copy this template into your hack's `../Student` folder, rename it to "ChallengeXX.md", where "XX" is the challenge number, and customize it for each challenge. 

**NOTE:** In each challenge's markdown file, you should create navigation links to/from the previous & next challenges. Please use relative links (eg. `"/ChallengeXX.md"`) instead of absolute links.

## Student Resources

It is common to provide attendees with resources in order to complete the hack's challenges.  One example is to provide the code for an application that the hack's challenges are based on. Another example might be to provide sample code files, artifacts, or templates that provide guidance for completing the hack's challenges.

If your hack provides attendees with code or resources, they should be included with your hack's contents in the `../Student/Resources` folder.

During a gHack event, it is recommended that you have attendees download any provided resources as a zip file instead of having them clone the entire gHack repo onto their computer.

This has the benefit of not having to direct the attendees to the gHack repo during your hack. Remember, attendees can always find the gHack repo.  However, remind your attendees that they are cheating themselves out of an education if they go foraging around in the gHack repo for the answers.

### Pre-load Resources into Google Chat Space

Our recommended method of providing resource files to attendees is for the gHack event host to pre-load them into the Google Chat space for the gHack event. 

To pre-load resources into the event team, the host should:
1. Create a zip file of everything in the `Student/Resources`.
2. Upload the zip file (or its contents) to the Files tab of the Google Chat space for the gHack event.
3. Direct users to download the resource files from Files tab in the Google Chat space.

## Presentation Lectures

You may be wondering why there is a section called "Presentation Lectures" when the whole point of gHack is to be hands-on and ***NOT*** a "death by Power Point" snoozefest?!  

When you host a gHack event, there is always a kick off meeting where the attendees are welcomed and then introduced to the logistics of the hack. The best way to do that is with a *short* presentation delivered a few slides at a time.

**TODO:** - we need to turn figure out how to share Slides templates since they aren't files?? - Gino
We have provided an Event Kickoff presentation template that you can customize for your hack and use to cover attendee logistics for a gHack event here:
- [Event Kickoff Presentation Template (Virtual)](gH-EventKickoff-Virtual-Template.pptx)
- [Event Kickoff Presentation Template (In-Person)](gH-EventKickoff-InPerson-Template.pptx)

After the kickoff meeting, its up to the hack authors if they want to provide any presentation lectures.  Some hack challenges are easy to jump right into.  Others are more complex and are better preceded by a brief introduction presentation.

It is OK and encouraged to offer a collection of "mini" presentation lectures if necessary for your hack's challenges. If you do provide a presentation lecture, consider these guidelines for each challenge:

- Try to limit the lectures to **5-10 minutes** per challenge.
- Provide a brief overview of the challenge scenario & success criteria
- Provide a brief overview of concepts needed to complete the challenge
- Provide "reference" slides that you might not present, but will have on hand if attendees need additional guidance
- Provide a slide with the challenge description that can be displayed when attendees are working on that challenge

We have more guidance on how and when to deliver mini presentation lectures for your challenges during your event in the [How To Host a gHack](gH-HowToHostAHack.md) guide.

Please publish any presentations in your hack's `../Coach` folder.

## Coaches Guide

Every gHack should come with a Coach's guide. The simple way to think of the Coach's guide is that should be the document with all of "the answers". The reality is, doing so would turn it into a giant step-by-step document loaded with detailed commands, screenshots, and other resources that are certain to be obsolete the minute you publish it. No one wants to maintain a document like that. 

Instead of treating the Coach's guide like a step-by-step document, treat it as the "owner's manual" you would want to provide to future coaches so they can host and deliver your gHack to others. 

The Coach's guide should include the following:

- List of high-level solution steps to each challenge
- List of known blockers (things attendees will get hung up on) and recommended hints for solving them. For example:
    - Resources that will take a long time to deploy in GCP: Go get a coffee.
    - If installing gcloud on Windows, install it in the Windows Subsystem for Linux instead of just Windows itself
    - Permission issues to be aware of, etc
- List of key concepts that should be explained to/understood by attendees before a given challenge (perhaps with a presentation lecture)
- List of reference links/articles/documentation that can be shared when attendees get stuck
- Estimated time it would take an attendee to complete each challenge. This will help coaches track progress against expectation. It should NOT to be shared with attendees.
- Suggested time a coach should wait before helping out if a team is not progressing past known blockers

The Coach's guide should be updated during & post event with key learnings, such as all the gotchas, snags, and other unexpected blockers that your attendees hit.

## Coach Solutions

This is where you put "the answers". There are usually multiple ways to solve a gHack Challenge. The solutions you provide here should be example solutions that represent one way to solve the challenges. The solution resources might include a full working application, configuration files, populated templates, or other resources that can be used to demonstrate how to solve the challenges. 

Examples of Coach Solutions are:
- Prerequisites for the GCP environment if needed. 
    - Example: A VM image with Visual Studio or ML tools pre-installed. 
    - Example: A Terraform template and/or script that builds out an environment that saves time on solving a challenge
- Scripts/templates/etc for some challenges that can be shared with attendees if they get really stuck
    - Example: If challenges 1 through 3 build something (i.e. an ARM template) that is needed for challenge 4, you could “give” a stuck team the template so they could skip to challenge 4.

If your hack provides Coach Solutions with code, templates, etc, it is recommended that you publish those resources as part of your hack's contents in the `../Coach/Solutions` folder.

**NOTE:** This content is NOT intended for hack attendees to see before or during a hack event. The content IS available publicly and thus an attendee can and WILL find it if they are determined enough. It is important to stress to the attendees that they should not cheat themselves out of an education by looking at the solutions.

## Preparing Your Environment

Okay, ready to get started creating your own gHack?

First we create a fork of the main gHack repo and then clone it to disk and create a branch to work in. The instructions below assume you have the git command line on your machine. If you're more comfortable in a GUI git client, you can use that too (we recommend SourceTree).
1. Create a fork of the gHack repo
   - Navigate to the gHack git repo at: <http://github.com/gfilicetti/gHacks>
   - Click the Fork button at the top right of the page and then choose the account you want to create the fork in. 
2. Clone your new fork to your local machine
   - `git clone https://github.com/myname/gHacks.git`
   - `cd gHacks`
3. Create a new branch for your work. It is a best practice to never work directly on the master branch
   - `git branch MyWork`
   - `git checkout MyWork`
4. Add a new folder to the top-level `hacks` root folder. Name your hack something distinctive using snake-case. Eg:
   - `mkdir hacks/century-of-iot`
5. Within your new folder, create the following directory structure:
	- `../Coach`
		- `/Solutions`
	- `../Student`
		- `/Resources`


### Files and Folders
Now that you've created the directory structure above, here is what each of them will contain:
- `../`
	- Hack Description (README.md)
- `../Coach`
	- The Coach's Guide, Lecture presentations, and any supporting files.
	- `/Solutions`
		- Solution code for the coach only. These are the answers and should not be shared with students.
- `../Student`
	- The Challenge markdown files
	- `/Resources` 
		- The code and supporting files the students will need throughout the hack.
