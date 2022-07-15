<!-- ![nextjs-prisma-boilerplate logo](readme-assets/banner.png) -->

<!-- <p align="center">
  <a href="https://badge.fury.io/js/electron-markdownify">
    <img src="https://badge.fury.io/js/electron-markdownify.svg"
         alt="Gitter">
  </a>
</p> -->

![GitHub Workflow Status](https://img.shields.io/github/workflow/status/nemanjam/nextjs-prisma-boilerplate/Run%20unit,%20integration%20and%20e2e%20tests?label=tests&logo=jest)
![GitHub Workflow Status](https://img.shields.io/github/workflow/status/nemanjam/nextjs-prisma-boilerplate/Run%20unit,%20integration%20and%20e2e%20tests?label=tests&logo=cypress)
![GitHub Workflow Status](https://img.shields.io/github/workflow/status/nemanjam/nextjs-prisma-boilerplate/Build%20and%20push%20Docker%20image?label=build%20docker%20image&logo=docker)
![Docker Image Size (tag)](https://img.shields.io/docker/image-size/nemanjamitic/nextjs-prisma-boilerplate/latest?logo=docker)
![GitHub Workflow Status](https://img.shields.io/github/workflow/status/nemanjam/nextjs-prisma-boilerplate/Deploy%20to%20VPS?label=deployment%20live&logo=ubuntu)
![GitHub](https://img.shields.io/github/license/nemanjam/nextjs-prisma-boilerplate)

#### Mobile screen:

<p>
    <img width="150px" src="docs/readme-assets/mobile-screens/Screenshot1.png">
    <img width="150px" src="docs/readme-assets/mobile-screens/Screenshot2.png">
    <img width="150px" src="docs/readme-assets/mobile-screens/Screenshot3.png">
    <img width="150px" src="docs/readme-assets/mobile-screens/Screenshot4.png">
    <img width="150px" src="docs/readme-assets/mobile-screens/Screenshot5.png">
</p>
<p>
    <img width="150px" src="docs/readme-assets/mobile-screens/Screenshot6.png">
    <img width="150px" src="docs/readme-assets/mobile-screens/Screenshot7.png">
    <img width="150px" src="docs/readme-assets/mobile-screens/Screenshot8.png">
    <img width="150px" src="docs/readme-assets/mobile-screens/Screenshot9.png">
    <img width="150px" src="docs/readme-assets/mobile-screens/Screenshot10.png">
</p>
<p>
    <img width="150px" src="docs/readme-assets/mobile-screens/Screenshot11.png">
    <img width="150px" src="docs/readme-assets/mobile-screens/Screenshot12.png">
    <img width="150px" src="docs/readme-assets/mobile-screens/Screenshot13.png">
    <img width="150px" src="docs/readme-assets/mobile-screens/Screenshot14.png">
    <img width="150px" src="docs/readme-assets/mobile-screens/Screenshot15.png">
</p>

Here you can find all fundamental decisions for an app already made for you:

- **frontend architecture** - pages, layouts, views, components, hooks, authentication, styling, theming, data fetching, state management, error handling, forms and validation
- **backend architecture** - controller and service layers, interaction with database, authentication, error handling in both API and getServerSideProps, validation, file uploads and serving
-
- **test configuration** -

## Features backup

#### Frontend:

- authentication with `next-auth` and Facebook, Google and Credentials providers
- decoupled routing and display logic with separate `pages` and `views` folders
- reusable per-page layouts
- styling with TailwindCSS and SCSS in separate `.scss` files so JSX is nice and clean
- classes named following BEM convention
- fully responsive design on mobile
- naturally handled specificity, not a single `!important` statement in entire code
- support for themes, implemented as Tailwind plugin
- current theme is persisted in local storage using `next-themes`
- Typescript with enabled `strict` and `strictNullChecks` options
- all Request/Response models types defined in a single place and reused in both client and API
- all routes and redirects defined in a single place as constants
- error handling for queries done with ErrorBoundary
- loading state done with Suspense
- authenticated user passed from root via context and available synchronously
- images loaded using Next.js Image component with custom loader
- data fetching and server state implemented with React Query and custom hooks
- initial query data passed from `getServerSideProps` using Hydrate provider
- paginated queries for both posts and users
- custom error pages (404 and 500)
- basic SEO setup using custom `Head` component
- forms done with React Hook Form
- validation with Zod schemas reused on both client and server
- image uploads with React Dropzone

#### Backend:

- custom server with both `http` and `https` servers and static folder for serving files at runtime
- Prisma ORM with Postgres database for managing data
- seed script used for development, integration and e2e testing
- Prisma exclude utilities for omitting private fields from API responses
- Prisma schema with User and Post models
- decoupled controller and service layers for clear reasoning and easy testing
- `next-connect` API handlers with clean middleware syntax
- global error handlers for both API and `getServerSideProps` with custom error class
- request body, query and params validated with Zod schemas (reused on client)
- private API routes protected with auth and admin middleware
- upload images with Multer
- API with CRUD operations on User and Post models
- full Postgres text search for getUsers and getPosts services

<!-- lighthouse score screenshot -->

#### Testing:

- Jest and `testing-library/react` for unit and integration tests
- React unit tests for components and hooks
- React integration tests for views
- unit tests for React Query hooks
- API responses for client tests mocked with Mock Service Worker handlers
- test wrappers for components and hooks for mocking auth user, session, router providers
- new QueryClient instance per each test to ensure isolated tests with React Query
- Blob polyfill for mocking images in client tests
- load test environment variables in Jest from `.env.test*` files
- `jest-preview` configured for visual debugging client tests
- unit tests for API controllers with Supertest client and mocked services
- API services unit tests with mocked Prisma client singleton instance
- integration tests (controller + service) per API handler with Supertest client and test database
- separate Jest projects for client, server unit and server integration tests
- all tests are configured to be executed locally, in Docker and in Github Actions
- code coverage configuration that includes all Jest tests
- code coverage currently: statements 43%, branches 47%, functions 39%, lines 43%
- main goal was to have configuration and example for every **kind** of test (client, server, unit, integration, components, hooks, controllers, services)
- Cypress end-to-end tests with configured ESLint and Typescript
- example e2e tests for Home page, main navigation, edit user and post and register new user
- `testing-library/cypress` is used for querying elements in Cypress tests
- Cypress task to seed and teardown test database
- Cypress commands to filter errors, seed and login as admin
- custom Docker image with Cypress installed on top of official base image
- `docker-compose.e2e.yml` with production built app, configured test database and Cypress containers with `.env.test*` files
- Cypress is configured to run locally, in Docker and in Github Actions

#### Development environment:

#### CI/CD:

#### Deployment:

#### Docs:

#### Philosophy:

#### Motivation:

There is a lot of talk, and buzz around JavaScript frameworks, a lot of theory, tutorials, opinions... but lets actually take what we read in documentations and check how it works in practice and see if we can build something useful and meaningful with it.

Full stack boilerplate with Next.js, Prisma, Tailwind, TypeScript, Docker, Postgres, documentation, frontend and backend unit and integration tests with Jest, Cypress end-to-end tests, Github Actions CI/CD workflows, and production deployment with Traefik and Docker.
