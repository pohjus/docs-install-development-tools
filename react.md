# React Tools

Install

- [VS Code](https://code.visualstudio.com)
- [Node.js](https://nodejs.org/en) (LTS Version)

Test that tools work! - see below!

## ⚠️ Test Node.js

Create a text file called `index.js` with the content of:

    console.log("hello world")

Run the app using node (in command line)

    node index.js

It should output

    hello world

Example workflow in macOS terminal:

![](images/node.gif)

Example in Windows environment with VS Code and MS DOS:

![](images/node-windows.png)

## ⚠️ Test React

React apps have been implemented using `create-react-app` tool. **As of 2025, create-react-app (CRA) is largely deprecated** and no longer the recommended tool for new React projects. The React ecosystem has evolved significantly, and there are now more modern, efficient, and actively maintained alternatives.

But most of "legacy" React projects are built using this tool.

In React training you can choose your tool of choice, but all assignments are tested with [`vite`](https://vite.dev) and all demonstrations are also done with this tool.

So you can for example use

- CRA
- Vite
- Next.js

But as said, Vite is recommendation.

### Vite

Test that vite works:

    npm create vite@latest vite-app

Choose

- React
- JavaScript + SWC

And then

    cd vite-app
    npm install
    npm run dev

See how to use Vite:

![](images/vite.gif)

And then you can open `http://localhost:5173/` in browser:

![](images/vite-running.png)

### CRA

If you want to use CRA, then test that it works:

    npx create-react-app myapp
    cd myapp
    npm start

It should start a browser window:

![](images/cra.png)

### Next.js?

Next.js is a React framework that provides server-side rendering (SSR), static site generation (SSG), API routes, and optimized performance features for modern web applications.

It is built and maintained by Vercel and has become the go-to framework for building scalable, production-ready applications with React.

By default, Next.js has better support for SSR.

Next.js has native support for SSR and integrates tightly with React Server Components (RSC), making it the most optimized solution for full-stack React applications. **Next.js support SSR features introduced in React 19**.

In Vite, you will have to do custom setup.

| Feature                           | Next.js (React 19)                     | Vite (React 19)             |
| --------------------------------- | -------------------------------------- | --------------------------- |
| **Ease of SSR Setup**             | ✅ Built-in                            | ❌ Manual setup needed      |
| **React Server Components (RSC)** | ✅ Fully supported                     | ⚠️ Experimental             |
| **Performance**                   | 🚀 Optimized for production            | ⚡ Super fast dev mode      |
| **Routing**                       | ✅ File-based routing                  | ❌ Uses React Router        |
| **Streaming SSR**                 | ✅ Yes                                 | ⚠️ Limited                  |
| **Edge Function Support**         | ✅ Built-in                            | ❌ Not natively supported   |
| **Best For**                      | Full-stack apps, SSR, hybrid rendering | SPA, MPA, client-heavy apps |

If you want to try out Next.js:

    npx create-next-app@latest my-next-ap

See how to use Next.js:

![](images/nextjs-running.gif)

## ⚠️ Test VS Code

Test that you are able to install VS Code extensions:

- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)

![](images/vs-code-extensions.gif)
