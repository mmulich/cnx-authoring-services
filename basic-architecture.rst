Basic Architectural System Design
=================================

Facts
-----

- Attempts to upgrade the existing Rhaptos/Connexions code base
  have failed due to lack of resources and time.
- The existing Rhaptos/Connexions code base is tightly coupled with
  itself and the framework it is built on.

Technical Assumptions
---------------------

- Python will be used in all new development.
- CoffeeScript will used when new javascript needs to be written.
- We will standardize on Jinja2 as our templating language.

General overview
----------------

The Connexions project has made the decision to rewrite the
application as multiple components or systems. The reasons for this
decision are not important to the continued design discussion. It is
assummed that this decision was good and we will continue work in this
direction.

The system will be broken into a number of components. The following
two sections illustrate this components in two perspectives: technical
and user.

Technical Components
~~~~~~~~~~~~~~~~~~~~

- Repository of information (A database abstraction)
- System for Authentication/Authorization information (A web service
  used in the authentication and authorization processes)
- Transformation tools (e.g. PDF and EPub generation, thumbnail
  generation, etc.)
- Portal for viewing published work (a website for viewing specific
  versions of published works)
- Various databases to store information (only mentioned because it is
  an integral part of the system)

User Components
~~~~~~~~~~~~~~~

- A creation and editing interface with users can author content.
- A publically (or intranet) viewable space where users can read and
  interact with the content.
- An interface for sampling transformed content (e.g. show me how this
  section would look in the EPub format).
- A trusted location to store authored content.

These components are some but perhaps not all of the components
necessary to complete the entire :term:`publishing cycle`. The users
components do not exactly matchup with the technical components. For
instance, there is no user component that directly refers to where the
published content will live, because the user is not concerned with
this technical detail. They will however see the end result, which is
the web front-end (aka webview) atop the published
repository.

The following are a list of components that have been established by
previous conversations.

Literal Technical Components
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Components that may or may not be directly used are shown in *italic*.

- Database
- Authentication/Authorization database
- Unpublished repository (and editing environment)
- Published repository (or archive)
- Web view
- *Queuing system*
- *Tool jobs*

