Hello everyone.

I made boilerplate with Next.js and Prisma Postgres that you can use as a base for your own projects.

Don't let simple UI mislead you, this a fairly big project with complete setup for development, testing and production environments with Github Actions CI/CD pipelines. Something like you would find in a small or medium startup. All environments are configured to run either locally or in Docker.

You can run development locally, with VS Code devcontainers or use Gitpod playground if you want to test something really quickly. I suggest you try out devcontainers because it allows you to onboard new team members really quickly, they just need to run the app container. Also all team members have consistent environments so it's much easier to reproduce bugs and debug issues.

It has unit and integration tests for frontend with Jest and React Testing Library for components, hooks and React Query hooks. Also it has unit and integration tests for backend with Jest, Supertest and test database for controllers and services. All tests are configured to run locally, inside Docker and in Github Actions.

Code coverage is also configured and it is around 40%, but important note is that you have configuration and example test for each kind of test, so you can reuse them and use it as reference when you build and test your own features.

It also has end-to-end tests with Cypress also fully configured to run locally, in Docker and in Github Actions.

For production you have local and Docker environments that you can use as staging. But also I made separate repository with real live production environment with Traefik and Docker that you can use to host multiple apps (including this app of course) on any Linux VPS. You just need a Docker image on Dockerhub. For that I set up workflows in Github Actions to build app as Docker image, push it to Dockerhub and deploy it with SSH to your VPS, all that with a single git push.

The app itself is a Next.js app written in Typescript, with custom http/https server, it uses next-auth for login with email/pass, Google and Facebook OAuth. It uses Prisma ORM with User and Post models and Postgres database that runs in Docker. I didn't want to add more models because that would hurt reusability of this as starter project. Seed script with Faker is included. Styling is done with Tailwind and SCSS and uses BEM for naming classes. Support for themes is implemented as Tailwind plugin. For fetching app uses the latest React Query v4. Forms are done with React Hook Form and Zod schemas which are reused on backend too. It uses Suspense and ErrorBoundary for loading and error states. Backend uses Next.js native APIs with next-connect router and Multer for uploads. Also other stuff like ESLint, Prettier, SEO are configured.

It uses all latest versions of packages like React 18.2, Next.js 12.2, React Query 4, React Hook Form 8, Prisma 4, Tailwind 3.1.

Also there is detailed Readme file and entire documentation folder where you can find all tricky parts documented with problems, solutions and links to useful references.

Here are some hints how you can use this:

First, most obvious use it as a base for your own projects. Why would you waste few months struggling with decision fatigue, writing boilerplate code and setting up environments and pipelines when you can install this in 15 minutes and start working on your features immediately. You just need app idea and original design system for styling.

Second, if you still study React you can use it for learning and analyze how things are implemented here. You can tear it a part and reuse already working and tested features. You can reuse configurations. For example you can reuse devcontainers config for any Node.js project.

Third, if you are already proficient with React 18 features you can have look at one open issue and challenge yourself and see if you can fix it. Also there is a Roadmap section in Readme if you want to contribute.

All constructive suggestions how this boilerplate can be improved further are appreciated, feel free to open new issue with bug report or a feature request.

If you use it to build something on top of it don't be shy to send me a message and show me what you did, how it worked for you, and your suggestions what would you do differently in a better way.

All this is completely free, Github repository is in the link bellow. Also I deployed live production demo that you can try out.

Demo link: https://nextjs-prisma-boilerplate.localhost3000.live

Github repository: https://github.com/nemanjam/nextjs-prisma-boilerplate
