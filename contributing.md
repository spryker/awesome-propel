# Contribution Guidelines
Please ensure your pull request adheres to the following guidelines:

* Please search previous suggestions before making a new one, as yours may be a duplicate.
* Code, comments and documentation need to be in English.
* Libraries that are PHP 7.3+, Composer-installable, PSR compliant, tested and documented are preferred.
* A license file must be in the root directory (usually named `LICENSE`).
* If possible, please publish your library under an open source license (preferably MIT).
* Please make an individual pull request for each suggestion.
* New categories, or improvements to the existing categorisation are welcome.
* Keep descriptions short and simple.
* End all descriptions with a full stop/period.
* Check your spelling and grammar.
* Make sure your text editor is set to remove trailing whitespace.
* Proposed libraries should ideally have 10+ stars.
* Please keep the lists in alphabetical order.

Thank you for your suggestions!

## Tips for creating composer packages

Choose a semantically meaningful name for the package name. This should ideally be prefixed with the dependency, in this case "propel" as the framework. A suffix can also clarify its intension.
The vendor name will usually be your GitHub username.
Do **not** use the Propel namespace (propel) as this is reserved to Propel domain itself.
The convention is to use lowercase letters and dashes as separator.

So if you created a behavior `Logging` with your GitHub account `FooBar`, a good name
would be `foo-bar/propel-logging-behavior`.

You can prefix your namespace and therefore your extension name with your vendor name to make sure there are no collisions with other similar extensions.
This would then be in your composer autoload definition:
```
"FooBar\\PropelLoggingBehavior\\": "src/"
```
GitHub URL would be then `foo-bar/propel-logging-behavior` respectivly.

Make sure those names match to avoid confusion here for users.


## Tips for creating extensions

* Make sure the README or docs contain installation and usage instructions. The more verbose, the better.
* The composer.json contains necessary dependencies including constraints (ideally using [semver](http://semver.org/)).
* The extension contains basic tests (unit, ...) of the functionality provided.
* It should have GithubActions or some CI set up.
* You can add badges under the README h1 header to visually show your tests are green etc.
* Ideally, also check phpstan level 8 on `src/` dir and [prefer-lowest](https://www.dereuromark.de/2019/01/04/test-composer-dependencies-with-prefer-lowest) to ensure a high quality for your extension.
