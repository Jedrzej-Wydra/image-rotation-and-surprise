# Machine Learning, Linear Model, Rotating Images, and Remembering the First Faculty
author: Jędrzej Wydra

## Short summary (1 sentence for a DS recruiter):
Demonstrated that a simple linear regression model can learn controlled 2D geometric transformations (specifically image rotation) using analytically generated training data from unit circle mappings, highlighting the power of linear models in structured tasks.

## Technical summary (2–3 sentences, concise):
Synthetic datasets were generated from ordered points on a unit circle arc to represent rotation as sequential input–output pairs. A standard linear regression model (scikit-learn) successfully learned local rotation mappings, while a naive approach using intersecting lines collapsed the space to a degenerate projection. The experiment leveraged NumPy and matplotlib for data generation and visualization, with model evaluation focused on transformation fidelity rather than standard metrics.

## History
This project started as a challenge for my students — and for myself. I wanted to show them two things: first, that teaching a computer to do something simple often takes surprising effort; and second, that even a basic linear model isn't just a math exercise — it can do real work, like rotating an image.

Instead of relying on empirical data, I generated synthetic training data analytically. I considered a unit circle and defined a finite, ordered sequence of points 
$(a_1, a_2, ..., a_n)$ evenly spaced along a circular arc corresponding to the desired rotation angle. For each  $i \in \lbrace 1, \dots, n-1 \rbrace$, the training set consisted of input-output pairs $(a_i, a_{i+1})$, where $a_i$ was treated as the input and $a_{i+1}$ as the target output. This construction allowed the model to learn the transformation corresponding to rotation in an elegant, fully controlled way.

The idea worked — the model learned to rotate. But not without surprises. In an earlier attempt, I tried to use two intersecting straight lines to define corresponding point pairs. The result? Instead of learning rotation, the model decided to squash the entire plane into a line. Linear, yes — but not quite what I had in mind.

This little experiment turned out to be a fun detour into the philosophy of modeling — and a reminder that sometimes, the best training data is the one you draw yourself.

## Side Note
I ran the project using the facilities of the faculty I graduated from — my very first one: Faculty of Law and Administration. During my second degree (on Faculty of Mathematics and Computer Science), a professor once asked me how I was coping in such a completely different world. I said I was doing fine, but whenever I visited my first faculty, I felt something different — like a deeper heartbeat, a stronger emotional pull. He smiled and said:
"Jędrzej, studies are like girlfriends — you never forget the first one". That was Prof. Maciej Kandulski — a truly wonderful person.
