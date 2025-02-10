# Phel Datastar demo

Demonstrates integrating Datastar hypermedia framework (https://data-star.dev/) with Phel which can be a good match.

Vanilla PHP being single threaded and non-async the web UI gets blocked and queues new requests while the SSE response is streaming back as seen in the video below after pressing "Fetch signal" the second time at 00:20.

https://github.com/user-attachments/assets/a3ad3fd8-2e30-462a-99ef-439fb479c566

PHP and Go differences are discussed in Datastar podcast video https://www.youtube.com/watch?v=hUqFY9TQvdM.

The original Phel Web Skeleton README continues, follow it to run this locally.

# Phel Web Skeleton

[Phel](https://phel-lang.org/) is a functional programming language that compiles to PHP.

This repository provides you the basic setup to start coding a website using phel.

## Getting started

### Requirements

Phel requires at least PHP 8.2 and Composer.

#### Locally (no Docker)

1. Ensure you have PHP >=8.2 (Some help about how to install multiple PHP versions locally on [linux](https://github.com/phpbrew/phpbrew) and [Mac](https://github.com/shivammathur/homebrew-php))
1. Ensure you have [composer](https://getcomposer.org/composer-stable.phar)
1. Clone this repo
1. Install the dependencies | `composer install`

#### Using Docker

1. Clone this repo
1. Build the image | `docker-compose up -d --build`
1. Go inside the console | `docker exec -ti -u dev phel_web_skeleton bash`
1. Install the dependencies | `composer install`

### Phel code

1. Write your phel code in `src/`
2. Run your web server with
   - `composer run:dev`: it will recompile the code on every request
   - `composer run:prod`: it will run the same compiled code on every request

### Tests

1. Write your phel tests in `tests/`
1. Execute your tests with `composer test`

## More about starting with phel

Find more information about how to start with phel in [getting started](https://phel-lang.org/documentation/getting-started/).
