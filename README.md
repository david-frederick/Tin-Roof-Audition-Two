# Tin-Roof-Audition-Two
This is my response to a problem posed by a interviewer from Tin Roof Software. I was expected to only work on the problem for 1.5 hours.

### This was the problem prompt ###

  Create a Ruby on Rails application for managing photo albums. The data model for these should follow the data formats returned by the /users, /photos, and /albums APIs located at http://jsonplaceholder.typicode.com. The application can be seeded with initial data using those same APIs. 
 
In order of importance, the app should have the following functionality (we don't expect you to be able to complete all of these so don't worry about how far you get). If you get stuck on a specific feature, feel free to skip it and move to the next:
 
1. Data should be loaded from the jsonplaceholder website and stored in a database (sqlite is fine). You can ignore the "company" and "geo" fields of the user model. 
2. App must display a list of users. 
3. Clicking on a user should display the list of albums for that user.
4. The list of albums should show a thumbnail of the album, which is just the first photo's thumbnail.
5. Clicking on an album should show the entire list of photos in the album, using each photo's thumbnail.
6. Clicking on a photo should show the full size photo with the photo's title as a caption.
7. The app should allow for the standard CRUD operations on the albums, photos, and users
8. The app should be styled using bootstrap or any other framework that makes the application look more polished than standard Rails scaffolding. 
9. The app should implement paging for the list of albums or photos (synchronous or asynchronous)
 
Spend at least an hour but no more than one and a half hours to complete as much of this as you can. When finished post on github and send us a link, or zip your code and send it via email. 

### What I did with my hour and a half ###

I spent most of the hour and a half learning how to make proper rake tasks. I have, in the past, simply written local scripts. In this case I wanted to access ActiveRecord (because it made the process of importing the data much cleaner.) Obviously for this to work, I also had to create the associated models and relate them.

See: `lib/tasks/import`.

As my time was coming to a close, I discovered that I was recieving 5000 entries from the photos import. (This, at least on my local machine, was taking a significantly long time.) Given more time I would: 
1. Verify that this is not an error within my code. The api site advertised 200 entries, but the page looks much longer than that.
2. Impliment some kind of batching for this import so that it does not strain memory as much.
(These would be done after accomplishing higher priority items, such as some of the above-listed UI requirements.)
