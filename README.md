# Roadtrip

Going on US road trip in March, surely needs a site!

## Initial thoughts

### Planning mode

Before the trip invite all of the Internet to help out and plan this up. Deadline some weeks before trip.

* All submissions have to be manually accepted to avoid too crazy stuff which we can't live up to, and avoid spam
* Money collected goes to travel expenses and is given as donation, does not guarantee anything regarding e.g. suggestions. Make this very clear
* Suggestions can be manually flagged as guaranteed to happen, we'll set up some at the beginning to control overall route
* Suggestions can be with or without coordinates; with coordinates are included into route, without coordinates are used to build bucket lists. Suggestions without coordinates can be with or without a state; with state gets added to state bucket list, without added to nation-wide bucket list
* Bucket lists are made up of suggestions without specific coordinates and sorted by weight, with a certain cut off line after a number of entries
* Show big map with current travel route
* Current travel route is calculated by algorithm taking suggestions with coordinates into account, limited by total driving distance cap
* Suggestions carry weight: weight increased with votes, decrease with deviation from original route and cost (inverse of vote money gain). Higher weight is preferred by routing algorithm
* Deviations from original route is the absolute of the difference in total distance between original route and route with suggestion
* When voting you can pay what you want to increase weight of vote, frame this clearly to be a donation not bound to the outcome of the vote
* Only big enough roads as valid route
* Suggestions can be a 'nightly stay-over'
* Probably smart to think of the trip as several small ones between nightly stay-overs to avoid 48 hour driving stretches or similar
* We can't accomodate suggestions that have a special time of day if it isn't real special as it requires planning. We should be able to, when eveything is finalized, to give a date at least.
* If people want to meet up, encourage them to submit an activity rather than we showing up into akward silence. And we insist to learn more about them before we decide to come by

### Travel feed mode

Follow our adventures, updated daily.

### Models

* __Suggestion__: objective:string, info:text, guaranteed:bool, [state:string], [coordinates:string], [stay_over:bool], [cost:int]
