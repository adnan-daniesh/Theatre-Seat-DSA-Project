# Theatre Seat Allocation

A web app that books theatre seats using **linked lists**.

**Live demo:** _paste your GitHub Pages link here_

## DSA concept: Linked list

The hall has 6 rows (A–F). Each row is its own **singly linked list** of 10 `Seat` nodes. A node stores the seat number, the name of the person who booked it (or `null` if free), and a pointer to the next seat.

| Operation | Use in the app | Time |
|-----------|----------------|------|
| Traverse to a seat | Book or cancel a chosen seat | O(n) |
| Traverse and count a run of free nodes | Auto-allocate seats together | O(n) per row |
| Traverse all nodes | Search bookings by name, draw the hall | O(n) |

Auto-allocation walks each row from the head, counting consecutive free nodes and resetting the count when it hits a booked one, until it finds enough seats together.

## Features
- Click a free seat to book it, click a booked seat to cancel it
- Auto-allocate 1–10 seats together in the first row that fits
- Search bookings by name (matches are highlighted)
- Live counts of total, booked, and free seats
- Operation log

## Run it
Open `index.html` in a browser. No install or build step.

## Tech
HTML, CSS, and vanilla JavaScript in a single file.
