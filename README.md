### The goal of this project is to create an infinitely scrolling grid of photos. using the useCallback hook as a ref combined with IntersectionObserver. The starting code for this project contains both a client and an api folder. The api folder contains the code for the fake API we will be using, while the client folder contains the static HTML/CSS files. This API is built on the json-server package, which is a great tool for quickly building fake APIs. Essentially, whenever you make a request to the API it will read/write to the db.json file to get your data.

# API Information

The API has the following endpoints:

- GET /photos?\_page=<page>&\_limit=<limit> - Returns up to <limit> photos starting at <page> page.
- GET /photos-short-list?\_page=<page>&\_limit=<limit> - This is identical to the above endpoint but this endpoint only has 100 photos total so you can more easily test what happens when you reach the end of the list.
  This API also uses the Link HTTP header to give you back the urls to the next, previous, first, and last pages. In our case we really only need the next page url. In order to parse this header we use the parseLinkHeader function in the client folder.

  # Procedures/Instructions

- Create an infinitely scrolling grid of photos using the API.
- The list should not break if there are no more photos to load.
- The list should not break if the user scrolls up and down quickly.
- The list should only load new photos when the user reaches (or gets close to) the bottom of the page.
- Add a simple skeleton loading animation for when the photos are loading.
  
