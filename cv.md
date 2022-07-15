# CV

- cv testing, react query, next, react, tailwind, cypress, architectures, databases, devcontainers, traefik, homelab, projects, github actions

- literature sections

---

## Testing

#### React unit and integration testing

- Jest, testing-library/react, testing-library/hooks, msw
- prettier, eslint, typescript
- mock css, images, fixtures

- jest: --projects setup, mocking modules, functions, values, components, spy, monkey patch, coverage
- async testing
- mock http - msw, setup with swr and React Query, wrapper providers, mocking router
- forms - useEvent, fireEvent, accessibility

#### Node.js API testing

- unit - services, controllers, middleware, supertest, pure functions, error responses, prisma
- integration - database, prisma

#### E2E testing - Cypress

- config, automated tool instead of user, black box, prod running app as whole
- docker images, bare, included
- github actions

---

#### React Query

#### Next.js

- next-auth
- docs...

#### React

- React 18
- react hook form

#### Tailwind (CSS)

#### Node.js (Prisma)

- error handling
- middleware for access permissions
- controller - http, separation of concerns
- services - db

#### Devcontainers (Docker)

#### Traefik

#### Github Actions

- running tests, databases, secrets, env vars, building Docker images, deployment with ssh, release semantic versioning

#### Next.js Prisma Boilerplate (Projects)

React landscape changed, once again it made sense to take the most promising libraries from React ecosystem, make a practical project with them, see for myself how they work together in practice and brush up skills with the most up to date knowledge. At present time Next.js is dominant way to work with React, SSR became standard, Prisma is the most interesting ORM in TypeScript world, React Query is high quality library so the choice of libraries wasn't too difficult.

Typically in companies foundation for a project is made by the most experienced developers that need to make correct decisions about software architecture, choice of technologies and libraries, establish best practices for writing reliable, testable and maintainable code, so that project can scale well as it grows in future without risk of becoming unmaintainable at some point. I saw challenge in doing that myself and that's why I chose to make such base boilerplate project.

This time I made complete foundation for a project including multiple development, testing and production environments, scalable components architecture on frontend, separated concerns with middleware, controllers and services on backend, highly customizable styling with theming support, unit and integration tests for both frontend and backend, automatized end-to-end tests, CI/CD pipelines, detailed documentation, heavily relying on Docker containers in every step of the process.

#### Architectures, Databases (Fundamentals)

#### Docker

- env vars, volume permissions for non-root user
- docker-compose.yml extending

write description for sharing project
