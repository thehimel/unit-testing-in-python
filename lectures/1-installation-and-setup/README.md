# Installation and Setup

## Running pytest with Docker

- Let's make sure VS Code is set up correctly to run Pytest and Docker. From VS Code, you can open the project
repository. And from here, we've saved our project to the desktop, but for you, if you saved it elsewhere, navigate to
that location. Right here, what I'll do is I'll click that folder and go no further, and we'll double-click and then hit
open. And you can examine the project structure on the left navigation pane, we see our scripts, folder, tests, and then
you'll also notice the Docker file. So let's open this up.
- Now, this Docker file contains a few different things, but let me explain it first. This Docker file will enable us to
run our code within a Docker container, that will act almost like a virtual machine. It will install all the packages we
need and allow your test setup to be just like mine without needing to change your underlying system's configuration. All
the code we execute, occurs in the Docker container. You can think of this script like a recipe for creating our code
environment, called a container.
- For this course, we'll be running Python 3.7, and you'll see here on this file it's using a `test-requirements.txt`.
What it's doing here is it's copying this file into our container, and then it'll run `pip install` over all of those
test requirements. Let's open up that file. Here, we can see it's referencing different libraries that are being
installed. For now, the most important one is Pytest. We're installing it to version 5.2.0.
- As we move further into our testing, we'll explore some of these other packages as they play a role in our testing
workflow. After you've examined these files, let's open our terminal. We can do that by clicking view and then terminal.
And since we've already opened our file, and you see it on the left, the terminal will also go to that location. If that
hasn't happened, you can use `cd` to go to wherever you may have saved that, be that in, you know, downloads, or some
other location.
- Let's build our project and open the container shell, which will let us run commands. We can do so by running the
following. The first one will be `docker-compose build` and what this is doing is it's basically kind of taking that
recipe that we built up in the Docker file and just creating our container environment.
- Now that that's built, we can run our next command, `docker-compose run test sh`. And what this will do, it'll open
the container. From here, we can type `Pytest` and this will run all of our tests. That command ran all of our existing
tests. If we want to run a certain test, we can run this special command. What I'll do here is just cherry-pick a test
that we'll look into a little bit later. So we can use `pytest -k`, which is the keyword argument, and we can run any
test that matches our keyword arguments. So let's say, I think you can see here, we have like a fitness log, so we can
run our fitness log and what Pytest will do, it'll collect all the tests for that certain keyword. If you ever need
help, you can also type `pytest -h`, this will give you information about all the different capabilities Pytest may have
if you have any questions. To exit the shell, on the same line, we can click exit. And we're back into our project
directory.
- Now that we've validated that VS Code is set up, and we can run our Docker commands, we should be good to go.
