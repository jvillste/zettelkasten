`{:tags [] :draft true}`

# Backlog

The minimum viable backlog application. Similar to PivotalTracker.

## Features

* Server based for multiple user access
* A secret URL for each backlog
  * No accounts needed
  * Just open the browser to an Url backlog.local/some-random-text-here to make a new backlog or to open an existing one
* Available hours for each day
* Each task has estimated size in hours
* Velocity is estimated on two week average completed hours per available hours
* The tool calculates estimated completion date for each task based on available hours and velocity.
* Calculated total estimated work after each task in the backlog to show how far we can get to the backlog with the current budget
* Tasks are either completed or incomplete. Their completion date is saved. This is used for velocity calculation.
* Tasks can have tags that indigate their state before they are complete.
* Plain text export for email reporting
* Task reordering with drag and drop
* Filtering with tags and free text search
* Task description and ID copying to clip board with a single click for easy referencing in emails

