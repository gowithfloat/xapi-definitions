xAPI URI Registry
=================
As Float continues to advance new use cases for the xAPI specification, it occasionally needs to define new identifiers (URIs) to describe custom verbs, activity types, or extensions.

This repository contains the definition for those URIs.

Each URI definition should be submitted to the official [Tin Can Registry](https://registry.tincanapi.com).

Feedback
--------
We welcome feedback on any of our identifiers. Feel free to open an issue to discuss!

Adding a new identifier
----------------
_for Float team members_

1. Determine the URI for the new identifier.

	The URI should follow the format:

		http://xapi.gowithfloat.net/{resource}/{slug}

	`{resource}` should be one of `extension`, `verb`, or `activitytype`.

	`{slug}` should be the specific identifier for this URI.

2. Create a new JSON file in the cooresponding resource folder (e.g. `extension`). The file name should match the slug determined above and have a `.json` file extension. Specify the name and description of the new identifier.

		{
		  "name": {
		    "en-US": "Activity Host"
		  },
		  "description": {
		    "en-US": "An activity extension which allows the host of an activity to store information about itself. This allows other systems to know who is responsible for maintaining an activity. The value of the extension should be a JSON-encoded object containing a `homePage` for the host and a host-specific `id` for the activity."
		  }
		}

3. Submit a pull request.

4. After approval, submit the identifier to the [Tin Can Registry](https://registry.tincanapi.com).
