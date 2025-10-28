High-level overview
=====

SHARPIE is organized around two main components: the web server and the runner.

Web server
----------------

The web server is serving files to the user as well as interacting with the backend runner. Here, we will only highlight the fonctionnalities but we invite you to have a look at the Django documentation for a better understanding of how it is working. The web server is divided in 4 apps:
* **Home**: the landing page of the platform.
* **Admin**: managing the platform settings, users, and experiments.
* **Accounts**: login in and registering users.
* **Experiments**: participant-facing interface to run experiments.