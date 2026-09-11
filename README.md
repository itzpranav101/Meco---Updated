# meco

## why i made this

meco started from a pretty simple idea what if someone with dementia had something that could actually help them remember people and conversations. i didnt really want to make another chatbot and just slap an ai label on it. i wanted to build something that could actually be useful in real life and focus on something that people with dementia genuinely struggle with which is remembering the small things. someone visiting you, a conversation you had yesterday or even someone you know but just cant remember the name of. those little things can mean a lot and thats basically where meco came from

## what meco does

meco is a memory companion that helps patients and caregivers keep track of people, memories, conversations, visits and other important things. caregivers can add trusted people and give meco some basic information about them and meco can then use their face and voice to recognise them when they visit. the idea is pretty simple really instead of the patient constantly having to ask who someone is, meco can help remind them

## remembering people

one of the first things i wanted to build was face recognition. caregivers can add someone and capture a few different angles of their face and meco uses those to recognise the person when they appear in patient mode. i made it check multiple frames instead of trusting one random camera frame because that would obviously get pretty messy lol. there is also optional voice recognition so if someone has their voice enrolled meco can try to recognise them while they are talking too

## remembering conversations

meco can listen to conversations during visits and turn them into a transcript. it can also separate different people speaking so you dont just end up with one giant paragraph of text. if meco recognises a trusted persons voice it can replace the speaker label with their name. after the conversation meco can turn everything into a visit report with things like what was talked about, memory cues, important topics and things a caregiver might want to check on later

## the companion

i didnt want meco to only be useful when someone was visiting so i added a companion that lets the patient talk to meco between visits. it can use things already stored in their memories to bring up familiar topics and reminiscence prompts. so if someone has a memory about gardening meco might bring that up naturally during a conversation. there is also a wellbeing trend and caregiver alerts for conversations that might be worth looking at. its not supposed to diagnose anything its just meant to give caregivers another bit of information

## the journal

there is also a journal where patients can write about their day and track their mood. over time this gives them something personal to look back on and gives caregivers another way to understand how things have been going. i actually liked this feature because sometimes the small stuff matters more than one big report

## visits

caregivers can create visits and reminders inside meco and they can also make things repeat every week. i connected google calendar too so changes made in meco can sync with the calendar and changes in the calendar can come back into meco. basically less stuff for caregivers to manually update

## making it easy to use

i didnt want the patient side to look like some massive complicated software dashboard. patient mode is kept pretty simple with bigger text and larger buttons while the caregiver side has more information because thats where things like memories, people, visits and reports need to be managed

## languages

i also wanted meco to work for families that dont always speak english. live conversations can be translated into mandarin, tamil or hindi because obviously not every family is going to sit around speaking english all day

## how i built it

meco is a web app built with node, html, css and javascript. i used clerk for accounts and appwrite for storing data. for live transcription i used deepgram and assemblyai as a backup for recorded conversations. i used resemblyzer for the voice recognition part and for the ai reports i used gemini with groq as a backup. i also made local fallbacks for some of the features because i didnt want the entire app to randomly die if one ai service stopped working

## the hardest part

honestly the hardest part wasnt really one specific feature it was getting everything to work together. camera, microphone, transcription, speaker recognition, face recognition, ai, calendar, authentication and data storage all had to somehow work together without making the app completely painful to use. the live transcription was probably one of the more interesting parts because audio gets streamed through the server while the conversation is happening and the transcript comes back almost immediately. there were definitely a lot of moments where something would randomly break and id sit there wondering why it worked five minutes ago 😭

## why i care about this

the thing i like most about meco is that its not really about the ai. the ai is just what lets me build some of these features. the actual point is helping someone hold onto the little things that make people familiar. a name, a face, a conversation or a memory about something they love. those things might seem small but when someone is struggling with their memory they can mean a lot and thats really why i built meco
