# Basic git hooks for PHP


## Intro

Information about git hooks on the internet is too scattered so I decided to make my own.

IMPORTANT! The hooks are not plug-n-play.
You will still need to adjust them to your environment.
By default all checks are triggered.


## Requirements

- *nix flavour (for *bsd you'll need to adjust the bash path)
- php
- phpunit
- phpcs


## Pre Commit

- only checks indexed files contents
- forbid words like `var_export`, `var_dump`, `print_r` in php files
- enforce a coding standard with PhpCodeSniffer
- check php syntax with `php -l`
- run unit tests with `phpunit`
- forbid `console.*` in js files


## Post Update

- run synchronization scripts like [https://github.com/mrjulio/mysql-revisioning-tool] (@TODO)

## Pre Receive

- (@TODO)

## Credits

- http://stackoverflow.com/users/13923/larryh (Git pre-commit hook : changed/added files)
- https://github.com/s0enke/git-hooks
- http://www.craftitonline.com/2011/08/php-pre-commit-hook/
- http://www.masnun.com/2012/03/18/running-phpunit-on-git-hook.html
- http://stackoverflow.com/questions/2539404/git-pre-receive-hook-to-launch-php-codesniffer
