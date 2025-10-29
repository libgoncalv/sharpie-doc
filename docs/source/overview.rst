High-level overview
=====

SHARPIE is organized around two main components: the web server and the runner.

Web server
----------------

The web server is serving files to the user as well as interacting with the backend runner. Here, we will only highlight the fonctionnalities but we invite you to have a look at the Django documentation for a better understanding of how it is working. The web server is divided in 4 apps:

* **Home**: the landing page of the platform.
* **Admin**: managing the platform settings, users, and experiments.
* **Accounts**: login in and registering users.
* **Experiments**: participant-facing and backend-facing interface to run experiments.

Runner
----------------

The runner is responsible for managing the execution of experiments. The runner communicates with the web server to provide real-time updates and receive participant inputs. It is designed to be modular and extensible, allowing researchers to easily integrate new environments and algorithms by using simple wrappers. It is divided in several modules:

* **Manager**: intitializing and running environments and AI agents.
* **Experiment**: per experiment wrappers for RL environments and algorithms.
     * Environment: environment wrapper, input mapping and termination condition.
     * Agent: agent(s) wrapper.

Interaction diagram
----------------

The following diagram illustrates the interaction between the web server, runner and participant during an experiment.

.. image:: _static/overview.png
    :width: 600
    :alt: SHARPIE overview diagram