# Coding challenge: Your barkeeper's API

You will create an application that serves cocktail recipes using a REST API.

# Specs

## Model

The cocktail or recipe needs at least the following properties:
- id
- name
- ingredients
  - measure
- image(-link)
  - renditions (original, thumbnail)
- instructions
- creationDate
- updateDate

How you model the data is up to you.

## APIs
Expected is an application that provides at least two APIs:

`GET /cocktails`
Returns a list of all cocktails in JSON format. Minimum Properties served: `id, name, alcoholic|non-alcoholic`

`GET /cocktails/:id`
Returns a single cocktail with all it's properties

## Storage layer

Persistence over restarts of the application is not a requirement. But the service should be able to serve cocktails 
right after startup.

Tip:
Frameworks like spring-boot allow to configure an in-memory database.  

### Bootstrap cocktails
 
To have some data to start with create an automated bootstrap task that runs on first startup and fetches some example cocktails
from a 3rd party service like [TheCocktailDB](https://www.thecocktaildb.com). You can also read it from a local JSON file.

## Tests

Create an e2e-test for the project. Create a test that executes an HTTP Get call towards one of the endpoints and verifies 
the returned JSON.
If you can provide a meaningful unit-test that's a bonus.

# Deliverables

- All code is checked into git with meaningful commits.
- Everything needed to get started is documented in a README.md file.
- CI/CD: Create a job that builds your project and runs your tests.
  - Tip: Use Github and GH actions (free tier).

# Evaluation criteria and time

The challenge is meant to give us a feel for how you work and to serve as a starting point for a follow-up discussion.

Your time is precious, we don't want you to spend too much time. It should be doable in 2-4h given the right approach and tools. 
Speed is not a criterion. Shortcuts are fine, document what you left out.

# Contact

We're here to help and answer questions so do not hesitate to ping us, either using the emails from the first interview round or devs@cwire.com.