This is a set of Drush commands (for Drush 8.x) for generating code with the
Drupal Code Builder library.

## Installation

1. Place this folder somewhere where Drush will locate it as a command. (See
  http://docs.drush.org/en/8.x/commands/#create-commandfiledrushinc for
  possible locations.)
2. Do `composer require drupal-code-builder/drupal-code-builder` in the Drush
  installation folder.
3. Do `drush cc drush` to rebuild Drush's cache of commands.
4. Do `drush mb-download` in your Drupal site. This detects hooks, services, and
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