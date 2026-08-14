# Mission Reflection

## Which cloud infrastructure component do you think is the most important? Why?

For me it's compute. Storage and networking both matter, but compute is the piece that actually does the work, it's what runs the applications people rely on. Storage just holds data, networking just moves it around, but compute is where everything gets processed. That's also why cloud providers built their entire pricing models around renting out compute power in the first place.

## How does Linux support cloud computing?

Most of the cloud runs on Linux behind the scenes, which I didn't fully appreciate until this lab. It's free, stable, and doesn't need constant restarts, which matters a lot when a provider is managing thousands of servers at once. The commands I used here, like `lscpu` and `free -h`, are the exact same tools real cloud engineers use daily, which made the lab feel a lot more practical than I expected going in.

## Why is technical documentation important before deploying infrastructure?

Because things eventually break, and when they do, someone needs to understand what was built and why without having to guess or reverse-engineer the whole system. I noticed this firsthand during the lab, coming back to an earlier step after a break was a lot easier because I'd already written down what I did and why.

## What new skills did you learn during this laboratory activity?

I got much more comfortable pulling real system information straight from a Linux terminal instead of relying on a graphical interface. I also learned how GitHub handles folders and files through the web browser, including figuring out why some of my files weren't creating folders the way I expected.

## How has your GitHub portfolio improved after completing this mission?

It looks like an actual project now instead of just a README with my name on it. There's real folder structure, real documentation, and a commit history that shows the work being built step by step, which feels a lot closer to what a professional repository should actually look like.
