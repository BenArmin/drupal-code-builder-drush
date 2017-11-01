This is a set of Drush commands (for Drush 8.x) for generating code with the
Drupal Code Builder library.

## Installation

There are two ways to install this command:

- Composer installation as a Drush extension
  1. Do `composer require drupal-code-builder/drupal-code-builder-drush:^8.0.0`
    to install this package and its dependencies. You will need your project to
    use drupal-composer/drupal-project, or have your composer.josn configured
    to place Drush extensions into drush/contrib.
- Manual installation as Drush extension
  1. Place this somewhere Drush will locate it as a command, such as
    drush/contrib.
  2. Do `composer require drupal-code-builder/drupal-code-builder` to install
    the Drupal Coder Builder library.

Once this is installed:

1. Do `drush cc drush` to rebuild Drush's cache of commands.
2. Do `drush mb-download` in your Drupal site. This detects hooks, services, and
  plugin types in your Drupal site's codebase and analyses them for use with
  Drupal Code Builder.

## Usage

The following commands are available:

- `drush mb-list`: Lists all the hooks, services, and plugins that Drupal Code
  Builder has detected in your Drupal site's codebase.
- `drush mb-download`: Updates the stored definitions of Drupal hooks, services
  and plugin types.
- `mb-build`: Generates code for a Drupal module. See the command help for more
  detail.

## A note on history

Commits in this repository older than 2017-08-22 are extracted from other
repositories that originally were the home of this command file: the drupal.org
module_builder project, and a drush fork.
They were extracted using git filter-branch, and reconstituted into a single
history with git graft and git filter-branch.
