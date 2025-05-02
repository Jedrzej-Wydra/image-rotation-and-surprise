# Machine Learning, Linear Model, Rotating Images, and Remembering the First Faculty
author: Jędrzej Wydra
## History
This project started as a challenge for my students — and for myself. I wanted to show them two things: first, that teaching a computer to do something simple often takes surprising effort; and second, that even a basic linear model isn't just a math exercise — it can do real work, like rotating an image.

Instead of relying on empirical data, I generated synthetic training data analytically. I considered a unit circle and defined a finite, ordered sequence of points 
$(a_1, a_2, ..., a_n)$ evenly spaced along a circular arc corresponding to the desired rotation angle. For each  $i \in {1,…,n−1}$, the training set consisted of input-output pairs $(a_i, a_i+1)$, where $a_i$ was treated as the input and $a_i+1$ as the target output. This construction allowed the model to learn the transformation corresponding to rotation in an elegant, fully controlled way.

The idea worked — the model learned to rotate. But not without surprises. In an earlier attempt, I tried to use two intersecting straight lines to define corresponding point pairs. The result? Instead of learning rotation, the model decided to squash the entire plane into a line. Linear, yes — but not quite what I had in mind.

This little experiment turned out to be a fun detour into the philosophy of modeling — and a reminder that sometimes, the best training data is the one you draw yourself.

## Side Note
I ran the project using the facilities of the faculty I graduated from — my very first one: Faculty of Law and Administration. During my second degree (on Faculty of Mathematics and Computer Science), a professor once asked me how I was coping in such a completely different world. I said I was doing fine, but whenever I visited my first faculty, I felt something different — like a deeper heartbeat, a stronger emotional pull. He smiled and said:
"Jędrzej, studies are like girlfriends — you never forget the first one."
That was Prof. Maciej Kandulski — a truly wonderful person.
