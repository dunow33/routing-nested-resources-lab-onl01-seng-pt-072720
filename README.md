# Nested Resource Routing Lab

## Objectives

1. Write nested routes
2. Filter data sets based on nesting
3. Handle errors in nested routes

## Overview

In this lab, we're going to extend our song library using nested
resources to build new routes for our artists and songs, and then use
the URL helpers in our views to expose these new routes.

We'll also be handling errors when nested resoureces aren't found so
that we can provide a more professional experience to our users.

## Instructions

The base models, controllers, views and other files have been provided. There are tests for the lab in the `spec` directory. You can run tests with the `rspec` command.

Before running the lab, remember to do a `rake db:seed` to set up a
starter song library!

1. Create nested resource routes to show all songs for an artist (`/artists/1/songs`) and individual songs for that artist (`/artists/1/songs/1`). Restrict the nested songs routes to `index` and `show` actions only.
2. Update the artists `index` view to use the new nested resource route
   URL helper in a link to the index of all songs by that artist.
3. Update the artist `show` view to list each song for that artist and use the new nested resource route
   helper in a link to view each song.
4. Update the `songs_controller` to allow `index` and `show` to handle
   for an artist.
a valid song for the artist.
5. In the songs `index` action, if the `Artist` can't be found, redirect to
   the artists index and set a `flash[:alert]` of "Artist not
found".
6. In the artists index view, display the flash alert if it exists.
7. In the songs `show` action, if the song can't be found for a given
   artist, redirect to the artist's songs index and set a
`flash[:alert]` of "Song not found".
8. In the songs index view, display the flash alert if it exists.
9. Make sure all tests pass then party down!

![Party Down](http://i.giphy.com/l41lNRz0uXPQLm0RG.gif)

**Hints**

1. For a refresher on the use of `flash`, see the [ActionController RailsGuide.](http://guides.rubyonrails.org/action_controller_overview.html#the-flash)
2. Remember when filtering nested resources to query for the children
   through the parent, e.g. `@artist.songs.find(...)`

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/routing-nested-resources-lab' title='Objectives'>Objectives</a> on Learn.co and start learning to code for free.</p>
