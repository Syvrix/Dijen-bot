# Dijen-bot
## Introduction
Bot for jensen

This bot is made for Jensen Yrkeshögskola.
Discord is used as main communication tool between students and educators/teachers majority of the time.

The goal of this bot is to get News published and post them in a channel designated for it.
Additonally for specific purposes, it will also be able to create events in a discord server.
- Events has the benefits to:
    People to show they are interested to attend
    How plan on attending many.
    Notify the users interested in the event when it starts.
    Dedicate a channel in discord where it takes place.
    Can work as a calendar for specific events etc.

###########################################################################################
## Functions
### Core functions
get_groups
    # Gets all the groups the user has access to.

get_group_cat_content
get_group_cat_news
get_group_cat_channels
get_group_cat_personel

#### group page formating
    # This containts the functions to process and read all the category group channels

    ## content ##
    # This is the content of the course, lessons etc.
    ## News ##
    # This is where news are published

    ## about ## 

    # NOT IN DEVELOPMENT #
    ## channels ##
    ## personel ##
get_content # Gets the content page, NOT YET NEEDED

Read_page_post
    # Formats and read the article webpage to compose it to a passable format.
    Gets a link,

###########################################################################################
## Discord Bot
### News
- Gets news from jesen when one is published.
Get_news
    # Navigates to a specific course, and the news section "Course > News"
    Gets all news posts
        See if any news posts are created
            If new post is found
                Add to buffer to make news post.
            else: exit


### Events
- Skapar event I klass discorden.
	Loggar in på Jensen vid <,event create>
	Skapa event <,event create LÄNK>
		exempel: ,event create https://jenseneducation.learnpoint.se/Id=4376&ItemId=13729
		Hämtar följande från länken
			Titel
			Datum, tid
                if no time found
                    Set default time to 09:00 AM
                if no date found
                    Set default date to tomorrow
                    
			innehåll
	<,event start ID>                               Startar ett event 
	<,event stop ID>                                Avslutar ett event
	<,event remove ID>                              Tar bort ett event
	<,event time ID 'new_timestart new_timeend'>    Ändrar tid på ett event
	<,event date ID 'new_date'>                     Ändrar datum på ett event

OPS botten både startar & avslutar eventet automatiskt efter datan som hämtas på Jensen sidan. vid event create kommandot. Resterande kommandon finns bara för manuell hantering om man skulle vilja.
###########################################################################################