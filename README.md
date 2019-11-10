# Screencast
Desc of Kodstar screencasting framework

# Screencasting Framework #

The following document is a written Desc of Kodstar screencasting framework. It should be used as a reference on the topic.

## Why you should care about screencasting? ##

You're probably aren't going to take the time to read this document if you're not interested, but there are a lot of nice side effects caused by learning how to create quality screencasts.

1. *Communicating more effectively* - At Envy Labs we produce screencasts for our clients all the time.  Whether it's demoing a new feature or for a presentation for an invester, they're often much more effective and pleasent than a phone call or screen sharing. 

2. *To Become a Teacher* - There is no more noble a profession than passing on knowledge.  There is a great deal of knowledge in the world and with the technology we now have available combined with the tools in this screencast, anyone can teach better than 99% of the people out there.

3. *To Make Money Teaching* - If you join the Kodstar screencasting team we'll pay you to create quality casts. At the bottom of this document we'll tell you how to submit an audition video.

4. *To Work with Us* - We're creating a system where you'll work with our team to polish your work and improve your screencasting skills.

### A Side Note on Composition ###

When teaching technology concepts there is always a certain amount of theory.  You might call this, the "Idea" or "Intent" of the code.  On most typical screencasts all that the viewer sees is the instructor's screen.  Thus when theory is discussed many times the listener stops watching and is forced to listen.  This is typically where people start to fall alseep. To combat this, I'm employing two different strategies:

1. **Use of slides** - Slides are the perfect medium for teaching concepts.  In many of my videos I avoid showing desktop all together, since I can focus the user on just the code I'm talking about.

2. **Facetime** - Humans are attracted to faces.  When it comes time to explain an idea or concept, seeing someone's face speaking to them can capture their attention more frequently.  

This tutorial will show how to use both these techniques to create effective educational content.

## Stuff you'll need ##

1. *Webcam or USB Camera* - In order to really be effective at screencasting you need to show yourself, so you need a webcam, or USB camera.  You're going to want to show yourself.  A built in camera is fine, that's what I like to use.

2. [Screenflow](http://www.telestream.net/screen-flow/overview.htm) or [Camtasia](http://www.techsmith.com/camtasia/) - Both of these products have free trials, but you'll eventually want to buy a copy of one of them for ($99).  I prefer Screenflow at the moment.  However, don't worry about going out and buying it immediately.  If you're trying out for the Kodstar Screencasting team, instead of sending me video you can just zip up your screenflow file (from the trial app) and send that instead of a video file.  

3. *USB Microphone* - Quality audio for screencasts is really important, even more than quality video.  Which is why I recommend getting a USB Microphone if you're really serious about this stuff.  If you want to try out for our Screencasting team though, feel free to skip purchasing one and just use what you have for now.

4. *Patience* - Just like learning a new web framework for creating web applications, please have patience as you work through this framework and create your own screencast for the first time.  Know that there's always room to improve, and anything you submit for the first time, I'll probably have some small revisions needed before it goes live.

## Scripting ##

To create effective screencasts you need to have an effective script or outline of what you want to cover. 

1. **Outlining** - Outlines can be as simple or complex as you need them to be.  Here is an outline of a screencast which  covers how to use the css3button gem.

     > **Assumptions, Problem, & Solution - Keynote slides**

     > 1. This screencast assumes you're familiar with Rails basics.  It's beginner.

     > 2. "So you're working on an application, and it has crappy buttons." Show boring scaffolding.

     > 3. Show css3buttons. "You want pretty buttons like these"

     > 4. "Enter css3buttons gem, created by Nicholas Bruning."  Show github page for css3buttons and give credit to the authors.

     > **Demo - Show some code**

     > 1. Show steps needed to implement css3buttons in a Rails app.

     > 2. WIN

     > **Show advanced usage - Keynote slides**

     > 1. Show different icons, styles, colors, and button groups

     > **Challenge - Keynote Slides**

     > 1. Give the viewers a challenge which uses the buttons.

2. **Figure out all your code** - This is where you figure out all code you're going to show during the screencast along with your base app.  

     A. Find or create a good base app to work with.  I recommend doing is starting either with a empty Rails app with a few scaffolds, or a real basic Rails app like [Nerd Factory](http://github.com/envylabs/NerdFactory). 

     B. Create a copy of your starting point, and label one directory "-before" and one "-after".  This idea came from Ryan Bates's RailsCasts.  His demo app for episode #264 was called "todo"

     ![before and after directories](http://img.skitch.com/20110509-xu3d1j67n4xfn9e6w5wrgbhaar.jpg)

     C. Go through the app in your "-after" directory, making modifications and taking notes as to what you're doing along the way.  Obviously you don't want to demonstrate something too complex.  It's better to show a short entertaining demo than to be completely thorough.  Here is an example for the CSS3Butttons screencast of what my code script looks like as I modified the "demo-after" directory. 
     
     > 1. Inside Gemfile add - 'gem css3buttons'

     > 2. $ bundle

     > 4. $ rails g css3buttons
 
     > 5. $ rails s

     > 5. Place before stylesheet declarations in layout <%= css3buttons_stylesheets %>
            Reason is that it includes a reset stylesheet.  If you don't want to use the reset.. 
            <%= css3buttons_stylesheets :include_reset => false %>

     > 6. /app/views/users/_form.html.erb - line 31 - button_submit_tag

     > 7. /app/views/users/index.html.erb - 
       (on new - line 29)
         button_link_to 
         add_button_link_to  # Talk about resolution... 

     > 8. Then show CSS3 Github Buttons on browser.
       (on edit) 
         pill_button_link_to, pill_button_link_to, pill_button_link_to 
         negative_button_link_to
         edit_button_link_to, remove_negative_button_link_to

     > 9. remove th and tds and do "<%= button_group do %>"

     These notes may not make sense to you, since I gave myself just enough notes so I can reproduce the changes once I start filming the actual screencast.  It's important at this stage to TEST out everything you're going to show so once you start recording, everything will go as planned (with any luck).

3. **Review** - If you'd like feedback from me or the community, this would be the time to do it. Throw your script into an [email](Gregg@EnvyLabs.com) or a [github gist](https://gist.github.com).  This is obviously the best time for feedback, before you started constructing any of the materials for the cast itself.

# Screen Resolution #

Make sure you're creating the screencast at a 1280x720 (720p) resolution. Properly sized text and windows will ensure that your screencast will have high clarity and readability.  You'll have to specifically select this resolution for Keynote slides, which is coming up next.

# Creating your Slides #

I highly recommend Keynote (on OSX) or Powerpoint (on PC) be used to create slides.  They make the job easy and quick.  If you want to create a Kodstar screencast, you'll want to download the Kodstar theme pack and start from there:

[Keynote Theme Deck](http://courseware.codeschool.com/screencasting_framework/codeschool-keynote.zip) | [Powerpoint Theme Deck](http://courseware.codeschool.com/screencasting_framework/codeschool-powerpoint.zip)

If you're not creating a Kodstar screencast, I recommend putting together one that's similar so all your screencasts maintain branding consistancy.  

Up next we'll be walking through the standard slides you'll find in this theme deck, and creating what we need for our first cast, based on the outline we have above.

## Title Slide ##

When the screencast starts, you need a title slide that gives the main topic, author name, and the production company.  Here is the title slide from the theme deck:

![title slide](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/title_slide_default.png)

The "you go here" is where your video goes and where you'll great the people who are watching.

## Table of Contents ##

There are two key ways to keep people's attention with videos:

1. **Set Expectation** - Let people know what you're going to talk about.

2. **Give Checkin Points** - Between each topic let people know where they are, and what your'e going to be talking about next.  If they've started to get distracted, these checkin points give them an opportunity to jump onboard without feeling lost.

Both of these can be done using a table of contents, and in the default theme it looks something like this:

![Table of Contents](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/toc.png)

As you can see the topics we've already covered are faded, the topic we're going to be talking about next is in black/orange, and the topics that we haven't yet talked about are in gray.  Between each topic we'll check-in and show the viewers all we've accomplished and what is next.

## Talking Points, Diagrams, and Images ##

When you're explaining ideas you may need to introduce a topic.  Here's the talking point slide from the theme:

![Talking Point](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/talking_point.png)

When explaining a topic with a tree or hierarchy, it can be quite useful to create a diagram.  Here's the starting point for that:

![Diagram](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/diagram.png)

Sometimes using image can be really useful for getting a point across.  Something like this:

![Image Example](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/image.jpg)

You'll notice at the bottom of this image I've added a link back to the Flickr page where I found it, to stay within my creative common's rights.  You could also save this credit until the end of the video, I've been known to do that at times, ending the video with something that looks like this:

![Credits](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/introduction.jpg)

## Screenshots & Websites ##

Very often it will be useful to take screenshots of tools and websites to place inside the keynote.  This is where something like [Skitch](http://skitch.com/) (if you're on a Mac) or [Jing](http://www.jingproject.com) (if you're on a PC) come in handy.  Simply take the screenshot and drag it into the keynote document.  If you're listing a website, you should probably list the URL along the bottom of the screen.

## Showing Code ##

Often it will be easier to teach code in a slide rather than in the actual code editor, we've provided theme slide for getting started with that as well:

![Code Slide](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/code_slide.png)

As you can see, this provides an easy way to show code on a topic.  Sometimes you may want to show bad code vs good code...   Which is why we've put together some icons for doing so:

![Alerts](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/alerts.png)

You can use these to signify warnings, errors, or just good/bad code.  Here's an example of them in use:

![Alerts Example](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/alerts_example.png)

## Font Size & Color ##

When it comes to regular text font size or code font size, I try to stay above 24pt if at all possible.  I've gone down to 22 or even 20 at times, but it's best to stay at or above 24.  If code doesn't seem to fit, it'd be better to break it up into multiple lines if you can do so in a way to keep it readable, and keep it at 24pt.  You can also show only parts of a file at once.

Textmate makes it easy to automatically get colored code from your text editor into your slides.  Here's how:

1. Make your textmate color theme what ever you wish to import into your slides.

2. Under the Bundle menu item, scroll down to "textmate", and then select "Create HTML From Document"

![Create HTML From Document](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/create_html_from_document.jpg)

You'll notice in the screenshot that I have it bound to option + command + P.  This is not bound by default, I added this after the fact.

3. Under the Window menu item, click on "Show Web Preview".

![Show Web Preview](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/show_web_preview.jpg)

This is bound to control + option + command + P by default.  

4. Copy and paste text from the resulting window which pops up directly into keynote.

There are certainly other ways to do colored code, this is just how I do it.

## Transitions ##

Transitions between slides should not be fancy, I recommend using a 0.50 second dissolve which is what the slide deck has by default.

## Animations ##

I encourage you to learn how to do Keynote / Powerpoint animations, but I'm not going to attempt to describe it here... See the video.

## Exporting ##

So you're done with your slides, and you're ready to export them into your editor (Camtasia or Screenflow).  Here's how you'll want to export, using keynote.

1. Under the Play menu item select "Record Slideshow", and click through all of your slides their transitions and animations.  If you'd like you can talk through them as you go, recording your audio.  However, your official audio for this will be recorded later.

![Record Slideshow](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/record_slideshow.png)

2. Under the File menu item select "Export":

![Keynote Export](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/keynote_exporting.png)

3. Select QuickTime, Playback Users: Recorded Timing, Format: Full Quality Large, and make sure "Include the slideshow recording" is checked.

![quicktime export](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/quicktime_export.png)

4. Save the file to somewhere you'll remember.  Maybe a directory like ~/Documents/Screencasts/Episode_Name/

5. Go create the desktop portion of the screencast, and once ready drag and drop the .MOV file into the editor.

# Recording your Desktop #

To capture really nice desktop screencasts there's a bunch of steps you need to take from the get go.  You've already done the hard part and wrote out the script, here's what else you need to know.

## FYI, Recording Narration Comes Later ##

I know some people like to record their audio at the same time as they're typing things out.  I'm not going to recommend it, so we're not going to teach it here.  Just know that the recording part comes later.

## Setup ##

The following you'll need to do before you start the screencast:

1.  Clean off your desktop.  Any stray pictures you have lying around, kill them.  The obnoxious background you're using, kill it.  

2.  Setup application resolution.  I like to use an application called [XScope](http://iconfactory.com/software/xscope) but I know there are others out there that do the same thing.  Once I startup XScope I click on the Frames icon:

![xScope Frames](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/xscope_frames.jpg)

This will pop up a frame.

![xScope 4by3](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/xscope_4by3.jpg)

You'll then want to drag the icon in the bottom right down until the resolution on the bottom reads 1280, and the resolution on the side reaches 728.

![xScope Drag Me](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/xscope_dragme.jpg)

3. Arrange your text editor so that it is within the 1280x720 box, and the optimal size for screencasting.  You also might want to hide your project drawer in textmate by selecting the View menu item and selecting "Hide Project Drawer" or pressing control + option + command + D.

![xScope hide drawer](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/textmate_hide.jpg)

4. Increase your editor font size to be as big as you can, but not causing the files you're editing to wrap too badly. In textmate hitting command+shift+plus will increase your font.  minus will decrease your font.  

5. If your screencast is going to use the terminal you'll want to fit it inside the 1280x720 box and increase the font size to make it comfortable.  You can use the same command+shift+plus to increase the font size.  If you need two terminal windows where you might be showing console on one and a log in the other you should try to fit one on the top and one on the bottom within the 1280x720 box.

6. Make sure you don't have some obnoxious prompt on your terminal.  I shorten my terminal prompt to nothing by running **export PS1='$ '**.  If you have a nice git prompt that should work fine too.

7. Set a nicer terminal font.  You can set this by going to File => Preferences.  I like using [anonymous pro](http://www.fontsquirrel.com/fonts/Anonymous-Pro) at the moment, but feel free to use whatever looks good.  

8. Turn your terminal opacity off if it's transparent.

9. If you're using a browser window, set your browser window to the 1280x720 resolution.

10. Clean up your browser, remove bookmarks bar or any other plugins which will distract people.

11. Move each of your different windows (browser, editor, terminal) around the screen so they can be panned to during your screencast.  I know it's a little counter intuitive, but this allows for a nice pan everytime you switch into a different context during your screencast.  

![shift windows](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/shift_windows.jpg)

12. Close out xScope if you haven't yet by hitting the X at the top of the box.

13. Hide your operating system dock, so when we're panning around the screen we don't accidentally see it.

![Hide Dock](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/hide_dock.jpg)

14. Startup [Keycastr](http://stephendeken.net/software/keycastr/) which allows people to visualize what you're typing on your keyboard.  This is really useful if you use tons of shortcuts.  Move the Keycastr window to where it needs to be, most likely the top or bottom corner of your editor.

## Rehearsing ##

Now that you have everything setup, you're going to want to do a run through.  Things to keep in mind:

1. Make a copy of your "-before" directory so you have a clean starting point.

2. Put your script on a second monitor, or better yet, print out your script so you have it handy.

3. Try to think about how you're going to narrate the cast later.  Remember, we're not going to record audio until after we have everything put together how we want it.  Talk it through how you're going to do it later.

## Actually Recording ##

So you're ready to actually do it?  Lets jump into some Screenflow basics.  If you're using Camtasia on a PC, don't worry, much of the functionality is VERY similar.  You should be able to figure it out.

1. Check all your windows to make sure everything is reset.  Copy over your "-before" directory so you're starting with a clean slate of your code base if you need to.  Set your browser to a good starting point or blank page.  Clear out your terminal windows (command-k) so they're blank.

2. Startup Screenflow.  If you don't see the configure recording window, you'll want to open it by clicking here:

![Configure Recording](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/configure_recording.png)

3. Record from the right monitor. You'll want to uncheck all of the checkboxes since all you care about is recording your desktop.  If you have two monitors you'll want to select the right one.  

![Record Desktop](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/record_desktop.png)

If you only have one monitor it will already be selected, don't worry about it.

4. Hit record (that big red button).  If this is the first time you're recording, you may want to simply do one or two things then stop the screencast and verify you're recording is working properly.  To stop recording at any time you can either hit shift + command + 2 or just go up to the camera icon in the top right and select stop recording:

![Stop Recording](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/stop_recording.png)

5. Go through your screencast code script.  Don't worry about screw ups or typos (if they're small) these make you look human and most people won't care.  If you hit a major road block or error, feel free to roll back a step and try again.  Don't stop recording, we can edit the screw up out later.

6. Once you're done and you stop recording, a new screencast window should automatically pop up.  **SAVE IT NOW**.  Don't touch it, save it. =)

## Editing your cast ##

1. You probably notice that ScreenFlow is always recording your whole screen.  At some point you may need to change your viewing screen size (how big the screen your editing appears to you).  You can do this by holding command and pressing = or -.  Try it if you haven't.

2. If you exported your video at this point it'd be your entire screen resolution (probably too big).  Remember, our screencast is going to be 1280x720.  So what you'll want to do is **resize the canvas** you're using to be 1280x720:

![Resize Canvas](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/resize_canvas.jpg)

3. Click the video, and drag the screen to where you want the video to start and play through until you need to do one of the following:

4. Cutting out video.  We all make mistakes, bad typos, or had to do a do over.  To delete parts of the video you're basically going to split the clip in two places, delete the video in between the cuts, and drag the other clips together.  To do a split you can select the edit menu and then the "Split Clip" item or better yet, just do **Shift + Command + T**.  Find where you want to cut the clip to, split it there, select (click) the video in between the cuts, hit the delete key, and then drag one part of the video up against the other.  It's as simple as that.  

Fine tuning / cutting too much.  Don't worry if you ever cut too much of the video, it's never actually deleted.  You can undo, or you can also select the edge of a clip and drag it to get what you deleted back:

![Drag Clip](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/stretch_clip.jpg)

5. Moving the window. Obviously as you move from the editor to terminal to browser you're going to need to move the focus of the screen around.  Screenflow makes this pretty easy to do:

> A. Select the point in the timeline of the recording where you'd want the screen to end (when you want the screen to be done panning).  Then click the Add Video Action button, or command + K.

> ![Add Video Action](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/add_video_action.jpg)

> You should see something like below pop into your timeline:

> ![Video Action](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/video_action.jpg)

> If the action looks real small you may want to zoom into it a little more by using the zoom bar in the bottom left of the screen (which you can see in the picture above).  Just drag that to the right to zoom a little.

> B. What this is showing is when on the timeline the video will start moving, and when it will end.  If you want to change where it starts and where it ends, all you have to do is put the cursor immediately after the video action (which it may already be at if you just did this), go up to the video window, and click and drag the window to the new location you want it to end on.  If you click the time cursor to before the action and press the spacebar to play it back, you should see it move from one place to the next.  You can also change the starting point by just selecting before the action and click and move the screen.

> C. The next thing you may want to do is reposition or slow down the action (so it lasts a bit longer).    Once you've done that you can make the video action longer by clicking on the border of the action and dragging it out.  To reposition the action just click on the middle of it and drag left or right.  I recommend making the action at least a second long, if not longer.

> D. Zooming.  There are times when you may want to Pan and Zoom in a video action.  There are a few ways to do this, but I recommend using the Scale slider at the top of the page.  Notice how it's at 100% right now.  This is where you want it ALMOST ALWAYS.  So if you do an action where you zoom in, you should always create another action shortly after where it goes back to 100%.

> ![Zooming Video](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/scaling_video-1.jpg)

6. Freeze Framing.  Sometimes you may have gone too quick, or maybe you want to talk about something between typing two lines of code.  The way to slow things down is to do a freeze frame, which Screenflow makes really easy.  Simply move the timeline to the point you want to freeze on, and select the "Add Freeze Frame" in the Edit menu, or simply press "Shift + Command + F". 

![Freeze Framing](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/freeze_frame.jpg)

You'll notice that this does three things.  It cuts the video in half, moves it apart, and then places a freeze frame in the middle.

![freeze frame view](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/freeze_frame_view.jpg)

To make the freeze frame longer you just need to drag the video clip on the right over then click and drag the right edge of the freeze frame to meet up with the video you moved.  **This technique will be really useful once you add video/audio to your screencast**.  Very often you will want to extend your screencast or even keynote slide, and the way you'll do it is by adding a freeze frame.

7. Doing transitions (AKA Fixing screw ups).  Sometimes you may have two video cuts which don't match up, or maybe you did multiple recordings.  Screenflow makes it easy to do a transition dissolve (also known as a fade) so you can dissolve from one video to the other without it being a hard cut (which can be disorienting).  

Transitions in Screenflow are as easy as overlapping one video on top of another.  If you try dragging a video into another video you'll end up having something that looks like this:

![transition](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/transition.jpg)

You can change the duration of a transition by the amount of overlap between each video.  When it comes time to bring in slides you'll be doing lots of this when transitioning from slides to desktop video and back.

8. Recording again.  Nothing wrong with going back and recording something again if the video didn't work out.  To do that in screenflow, just minimize your current document, record again, and when you stop the recording it will ask you if you want to add the recording to your existing document:

![add to document](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/add_to_document.jpg)

You should then be shown all the media (videos) in your document, and you should be able to drag and drop the new recording into your older timeline:

# Editing it all together #

Now it's time to combine your keynote video with your screenflow document, and get it ready to do the final narration.  Start with your screenflow file:

1. Click on the media icon on the top right part of Screenflow, and drag your keynote quicktime video into it:

![drag video](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/drag_media.jpg)

You'll then want to drag your video into the second line in your timeline above or underneath your desktop screencast.

![both timelines](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/both_timelines.jpg)

2. Pan through your timeline until you get to the part where your live screencast should happen.  Split the video at that point, and create a wide gap in the video where the live demo video might fit.

3. You'll probably want to move around large amounts of video sometimes.  This is one of those times, since we want to move all of our live desktop screencast in the middle of our keynote slides. To do so, you'll want to drag that magnifying glass in the bottom left corner further to the left.  

![skinny timeline](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/skinny_timeline.jpg)

Then select your desktop screencast by dragging a select box around all the video parts.  If you need to select it multiple times you can always hold down the shift key.  Once you have it all selected click the selected video group and move them collectively towards the gap in the keynote video.  Although you may be tempted to move it into the gap between each video DO NOT do this yet.    Eventually you'll put them on the same track and overlap them to make it transition, but things we'll be easier if we do that later. You'll want to keep them on separate tracks for now, although you can line them up so as soon as the keynote ends the desktop screencast begins, and then vise versa at the end.

4. Pat yourself on the back.  The hardest parts are now done!!  All that's left is to follow the directions below to record the video and audio.

# Recording You #

Yes, I do believe every screencast needs a face, and it's not going to be enough to just have audio.  In my opinion it's just not engaging enough.  If you still want to create content, and you're comfortable with someone else narrating your video this is fine.  Edit the video together with your Keynote / Desktop video as well as you can, write good notes, and skip down to the Exporting and Sending your video section down below.  I'd be happy to narrate the video for you, and still give you TONS of credit.

## Using a Camera ##

You don't need a USB camera if your computer comes with a camera built in, that will probably be good enough.  Here's how to setup to record using your desktop camera:

1. Camera positioning is important.  Make sure that you're not looking down or up at your camera, it should be eye level.

2. Lighting is important.  Don't record with back lighting or a window behind you.  Put something interesting behind you, or use a solid color curtain so that it won't distract from the video.

3. Make sure you're using the full frame of the camera, not cutting off your head, not getting too close, or too far away.

4. Use Photo Booth so you can see yourself while you're getting setup or even while you're recording the screencast.

## Getting Good Audio ##

Good audio is more important than good video, believe it or not!  Here's how to do it:

1. Be aware of background noise.  Close the door and turn off the music.

2. Find a good USB microphone (if you can afford one.. if you can't just do the best you can).  Right now I'm recommending the [Yeti](http://www.amazon.com/Blue-Microphones-Yeti-USB-Microphone/dp/B002VA464S) which has lots of nice features and works great.  Make sure if you have a microphone with different settings that you have it recording in a single/front directions.  The way I remember it, is look for the setting that looks like an upside down heart (or a butt).  

3. Setup the microphone so that it's out of picture, but as close to your mouth as possible.  Sounds impossible doesn't it?  It's not.  (see the video).

4. If your microphone has a headphone jack, plug into it so you can figure out the best microphone placement.  If you don't have a microphone with a headphone jack, just plug your headphones into your computer so you can monitor your audio levels.

5. Do a sound test.  I recommend using something like [Audacity](http://audacity.sourceforge.net/), it's free. 

> A. Make sure you have the right microphone selected.  Preferences => Device.. make sure you have the right microphone selected and that you're recording mono.

> B. Record and make sure the audio you're getting isn't too loud.

> ![Too Loud](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/too_loud.jpg)

> Or Too Soft

> ![Too Soft](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/too_soft.jpg)

> It should no smaller than this:

> ![About Right](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/about_right.jpg)

## Rehearsing ##

Before you start recording you'll want to do a dry run to make sure everything makes sense.  To do this, you're just going to play through your screenflow file with photobooth open to make sure you stay centered, and maybe with your headphones on to make sure you're getting good audio.  Here is how I setup my desktop when I rehearsed, and also when I recorded.

![desktop recording](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/rehearsing.jpg)

The reason I put screenflow at the top center of the screen was because my camera was at the top center of the screen.  When I know my face is going to be on the video I wanted to be looking RIGHT at the camera, but if I had to look away to glance at a slide I didn't want it to be too far.  In this case it'd just be a few inches down.

As I rehearsed, I used the space bar to stop the video when I needed to pause on a slide, and then the space bar again to resume.  Although I was tempted to jump in and edit, I knew this was not yet the time for it.

## Recording! ##

I think this is the most fun part, since all the grunt work is out of the way.  When you're ready to record you'll want to select "add additional recording" under the file menu:

![Add Recording](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/add_additional_recording.jpg)

When you do this it will bring up a menu that looks like this:

![Add additional recording](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/add_additional_recording2.jpg)

You'll want to make sure that your proper camera and audio input is selected.  If you're using an USB microphone, make sure it's selected here.

When you're ready take a deep breath, smile, try to be as friendly as possible, and hit the record button.  Once you start recording just hit play on your screenflow document and start narrating.

## Notes on Recording ##

1. When you're doing keynote slides and you're going to put your face on screen make sure you're looking directly at the camera.  People can tell when you read, it's annoying.

2. **Try not to use notes**.  or if you do use notes, just make them reminders so you know what to talk about next.

3. If you screw up a little, keep on going.  Nothing wrong with looking human, and when you make fun of yourself people like you even more.

4. If you screw up badly, don't start over.. Just go to the last place you can cut easily.  If you're on screen explaining an idea then this would be the last time you appeared on screen.  If you're off screen, then you can just pickup the last sentence.  Feel free to roll back the screenflow recording to that point, then hit that spacebar and keep on recording.

5. If you need to take a break for a glass of water, don't forget about the pause button under the camera icon.

![pause button](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/pause.jpg)

6. When you're done recording, go get a beer.  Seriously, you deserve it.. you're in the home stretch.

# Editing it all Together #

Now it's just a matter of editing things together.  It'll probably look something like this:

1. **Adding the facetime video**. You should see new media inside the right tab which shows your camera:

![new recording](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/new_media.jpg)

As you might suspect, you'll want to drag this into your timeline.  It **must be** the top most video timeline in your timeline.  Your timeline should look something like this:

![timeline three videos](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/timeline_three.jpg)

2. **Check your audio / video**.  Play back your audio and video and make sure it's good enough.  Your audio shouldn't be too low, and your video shouldn't be too crappy.

3. **Centering yourself**.  Center yourself in the title theme slide by clicking and dragging it into the center.

![center yourself](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/centered_gregg.jpg)

Depending on what sort of camera you use, you may need to also scale the image down either by using the scale video knob or by holding down the shift key (to lock the aspect ratio) and drag a corner of the facetime video in / out.

4. **Moving your head around**.  You may need to move yourself around the screen, like where I position myself during the table of contents:

![table of contents](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/table_of_contents_vid.jpg)

To do the move from the center of the screen down to the corner (and scale myself down at the same time) I make sure the facetime video is selected and select "Add Video Action" by hitting Command + K.  I can then move my face where I want it to go and scale it properly.

5. **Stretching and shrinking slides**.  Inevitably you'll need to increase or decrease the duration a slide is on the screen, to increase the duration simply use the Freeze Frame technique talked about above (shift + command + F).  To decrease the duration simply split the video (shift + command + T), then drag one of the ends of the videos inward and then drag one back up against the other.

6. **Fading yourself out** - You don't want to be on the screen all the time.  When you have code or syntax you want people to learn, you shouldn't be on the screen.  To fade yourself out you're going to add another Video Action (Command + K) and then set the opacity to zero.

![opacity](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/opacity.jpg)

7. **Fading yourself in** - Do the opposite of step 6.

8. **Making sure you have the right stuff selected**. Inevitably you'll sometimes run into the issue where you try to add an action or split a clip and either it doesn't seem to let you or it selects the wrong clip.  You'll always want to make sure that the video you want to edit is selected with a yellow select box.  If you run into this issue just make sure the right clip is selected.

# Rendering and Sending your Video #

## Exporting ##

1. If you have the demo version of screenflow, go ahead and zip up your screenflow file and skip to the sending section below.

2. Under the file menu select export or just hit command + e

![export](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/export.jpg)

Set the name of the export, along with the locations and all the same settings as you see them below:

![export settings](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/export_settings.jpg)

Go get a beer.  Rendering could take 20 minutes to 3 hours depending on how fast your computer is and how long the video is.

3. Watch the rendered video to make sure it's free of all graphic glitches and it plays smoothly.  Watching it back the first time you will inevitably find things that you hadn't seen before.

## Sending it In ##

If you want to join the Code TV team, (or you're already a member) you'll want to send in your video by posting it privately online.  I usually use [DropBox](http://www.dropbox.com/) for this, by placing the file in my public directory, then right clicking and selecting "copy public link":

![copy public link](http://courseware.codeschool.com.s3.amazonaws.com/screencasting_framework/copy_public_link.jpg)

You'll then have a public link you can send to me to download your cast.  

## Send me an email ##

If you're sending me a screencast to join the Kodstar team please email skuzey@gmail.com with the cast, and be prepared for feedback.  I know it feels like a lot of work when you do these casts, but there are always going to be ways you can improve, don't be discouraged if I send you a list of a few things to improve upon.

If your screencast is good enough and you want to start getting paid to do this stuff, there's not much stopping you.  We'll get you lined up to start producing, and you audition video will be released for free when Code TV goes live, and you'll get credit for your work.  

# Contributing to this Tutorial #

If you'd like to help me improve this tutorial, please fork it, modify it, and do a pull request.  Stuff that would be nice to add:

1. Alternate instructions for Camtasia.
2. Additional features of Screenflow.
3. Keynote Transitions and Animations.
