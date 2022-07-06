<p align="center"><img src="docs/readme-assets/banner-1280x640-200kb.png"></p>

# Next.js Prisma Boilerplate

<!-- logo, badges, gif, description, mobile screenshots -->

[![tests](https://github.com/nemanjam/nextjs-prisma-boilerplate/actions/workflows/tests.yml/badge.svg)](https://github.com/nemanjam/nextjs-prisma-boilerplate/actions/workflows/tests.yml)
[![docker build](https://github.com/nemanjam/nextjs-prisma-boilerplate/actions/workflows/build-docker-image.yml/badge.svg)](https://github.com/nemanjam/nextjs-prisma-boilerplate/actions/workflows/build-docker-image.yml)
[![deploy](https://github.com/nemanjam/nextjs-prisma-boilerplate/actions/workflows/deploy.yml/badge.svg)](https://github.com/nemanjam/nextjs-prisma-boilerplate/actions/workflows/deploy.yml)
![Docker Image Size (tag)](https://img.shields.io/docker/image-size/nemanjamitic/nextjs-prisma-boilerplate/latest?logo=docker)
![GitHub](https://img.shields.io/github/license/nemanjam/nextjs-prisma-boilerplate)

This is full stack boilerplate built around latest Next.js stack. It is composed of the best practices described in official docs combined with my decisions derived from my own experience and knowledge that I have gathered from working with other people.

Don't spend next 3 months making architectural decisions, choosing libraries, setting up development environment and CI/CD pipelines, writing boilerplate code, _instead install this boilerplate in 15 minutes and start working on your features **today**._

## Demo

 <!-- live, Gitpod playground -->

## Screenshots

#### Desktop screen:

https://user-images.githubusercontent.com/9990165/177367837-a2692e5d-b694-454e-806d-21e806465836.mp4

## Features

#### Frontend:

- authentication with `next-auth` and Facebook, Google and Credentials providers
- decoupled routing and display logic with separate `pages` and `views` folders
- reusable per-page layouts
- styling with TailwindCSS and SCSS in separate `.scss` files so JSX is nice and clean
- classes named following BEM convention
- support for themes, implemented as Tailwind plugin
- Typescript with enabled `strict` and `strictNullChecks` options
- all Request/Response models types defined in a single place and reused in both client and API

#### Backend:

- custom server with both `http` and `https` servers and static folder for serving files at runtime
- Prisma ORM with Postgres database for managing data
- seed script used for development, integration and e2e testing
- decoupled controller and service layers for clear reasoning and easier testing
- `next-connect` API handlers with clean middleware syntax
- global error handlers for both API and `getServerSideProps`
- request body, query and params validated with Zod schemas (reused on client)
- private API routes protected with auth and admin middleware
- upload images with Multer

#### Testing:

#### Development environment:

#### Deployment:

#### Philosophy:

#### Motivation:

There is a lot of talk, and buzz around JavaScript frameworks, a lot of theory, tutorials, opinions... but lets actually take what we read in documentations and check how it works in practice and see if we can build something useful and meaningful with it.

## How you can use this

## Tech stack

## Docs

## Table of contents

## Installation (Dev environments)

- local, Docker, devcontainers, Gitpod

## Next.js (frontend)

## next-auth

## Next.js (api)

## Database (Prisma)

## Data fetching (React Query)

## Forms

## Styling (TailwindCSS)

## Themes

## Testing

### Testing (frontend)

### Testing (api)

### Testing (coverage)

## E2E testing (Cypress)

## Docker

## Postgres

## CI/CD (Github Actions)

## Deployment (Traefik)

## Known issues

## References

## Contributing

## License
