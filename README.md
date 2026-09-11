# Meco Memory Companion

## Why I made Meco

Meco started with a pretty simple thought. What if someone living with dementia had something that could help them remember the people they meet and the conversations they have?

I didnt want to make another AI chatbot and call it a dementia solution. I wanted to build something that actually focused on memory and the small moments that can easily get forgotten.

For someone with dementia, forgetting a persons name or not remembering a recent conversation can be really frustrating. I wanted Meco to make those moments a little easier by giving the person something familiar to fall back on.

## What Meco does

Meco is basically a memory companion that can remember important people, conversations, visits and little details about a person.

A caregiver can add trusted people and give Meco some information about them. Meco can then use their face and voice to recognise them when they visit and connect them back to memories the patient already has.

The idea is that instead of the patient constantly having to ask who someone is, Meco can help remind them naturally.

## Remembering people

One of the main things I wanted Meco to do was recognise familiar people.

Caregivers can add someone with their name, relationship and a memory cue. They can also add their face and an optional voice sample.

When that person visits, Meco can use the camera to recognise them. I made it check different angles of the persons face instead of just saving one photo because I wanted it to work more like an actual recognition system.

If Meco recognises someone, it can introduce them using the browser voice.

## Remembering conversations

Meco can also listen to visits and turn conversations into transcripts.

The cool part is that it doesnt just turn everything into one huge block of text. It tries to separate the different people speaking, and if a trusted persons voice has been enrolled it can replace the generic speaker label with their actual name.

The transcript can then be used to create a simple visit report with things like what was discussed, important memory cues and things a caregiver might want to follow up on.

## The companion

I also wanted Meco to be useful when nobody was visiting.

The Companion gives the patient someone to talk to between visits. It can use their existing memory cues to bring up familiar topics and reminiscence prompts.

There is also a wellbeing trend and caregiver alerts for conversations that might be worth looking at more closely.

It is not meant to diagnose anything. I wanted it to be more like an extra layer of support for caregivers.

## The journal

Meco has a journal where the patient can write about their day and record their mood.

Over time, those entries can show how their mood has been changing. I liked this idea because not every important part of someones day happens during a conversation with a caregiver.

Sometimes a small journal entry can say a lot.

## Visits and reminders

Caregivers can create visits and reminders inside Meco and even make them repeat every week.

I also connected it with Google Calendar so that changes can move between the two instead of forcing caregivers to update everything twice.

## Making it easier to use

I wanted the patient side of Meco to feel simple and not like some complicated software dashboard.

There is a patient mode with bigger text and larger touch areas so that the important things are easier to find and use.

The caregiver side has more detailed screens for things like people, memories, visits and reports.

## Languages

I wanted Meco to work for families who dont always speak English at home.

The live transcript can optionally be translated into Mandarin, Tamil or Hindi, so conversations dont have to be limited to one language.

## How I built it

I built Meco as a web app using Node, HTML, CSS and JavaScript.

For accounts I used Clerk and for storing the users data I used Appwrite. I also made sure that the important API keys stay on the server rather than being exposed to the browser.

For live transcription I used Deepgram and I added AssemblyAI as a backup for recorded conversations.

For recognising voices I built a small local service using Resemblyzer. For the AI generated visit reports I used Gemini with Groq as a backup.

I also added local fallbacks for some features because I didnt want Meco to completely stop working just because one external AI service went down.

## Some of the harder parts

Honestly, getting all these different parts to work together was probably the hardest part of the project.

It wasnt just about making one AI feature work. I had to get authentication, storage, camera access, microphone recording, transcription, speaker recognition, face recognition, calendars and AI reports to all work together without exposing sensitive information.

The live transcription was especially interesting because the audio has to move through the server while the conversation is happening and then come back as text almost immediately.

I also spent a lot of time making sure that things could still work when some of the AI services were unavailable.

## Why I care about the project

The part I like most about Meco is that it is not really about the AI.

The AI is just what makes some of the features possible. The actual point is helping someone hold onto the little things that make people familiar.

A name. A face. A conversation. A memory about something they used to love.

Those things can seem tiny, but when someone is struggling with memory, they can mean a lot.

Thats why I wanted to build Meco.
