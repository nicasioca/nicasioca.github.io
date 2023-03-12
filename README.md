# Code Build Run Docs

> Docs from a software engineer / entrepreneur.

## Running the website locally

To create my documentation site I cloned a working copy of the site repo https://github.com/google/docsy-example, and to run my website locally you can simply clone my repo and follow the simplified steps below.

I installed the required prerequisites below (Go, Node, Git, and Hugo), from the repo root folder, run `hugo server` via npm:

```
npm run build
npm run serve
```

### Install Go language

Hugo's commands for module management require that the Go programming language is installed on your system. Check whether `go` is already installed:

```bash
$ go version
go version go1.18.4 windows/amd64
```

Ensure that you are using version 1.12 or higher.

If the `go` language is not installed on your system yet or if you need to upgrade, go to the [download area](https://go.dev/dl/) of the Go website, choose the installer for your system architecture and execute it. Afterwards, check for a successful installation.

### Install/Upgrade Node.js

To ensure you can properly build your site beyond executing `hugo server`, you must have the [latest long term support (LTS) Version](https://nodejs.org/en/about/releases/) of Node.js.

### Install Git VCS client

Hugo's commands for module management require that the `git` client is installed on your system. Check whether `git` is already present in your system:

```bash
git version
git version 2.37.1.windows.1
```

If no `git` client is installed on your system yet, go to the [Git website](https://git-scm.com/), download the installer for your system architecture and execute it. Afterwards, check for a successful installation.

### Install Hugo

You need a [recent **extended** version](https://github.com/gohugoio/hugo/releases) (we recommend version 0.73.0 or later) of [Hugo](https://gohugo.io/) to do local builds and previews of sites (like this one) that use Docsy. If you install from the release page, make sure to get the `extended` Hugo version, which supports [SCSS](https://sass-lang.com/documentation/file.SCSS_FOR_SASS_USERS.html); you may need to scroll down the list of releases to see it.

For comprehensive Hugo documentation, see [gohugo.io](https://gohugo.io/).

#### As an `npm` module

You can install Hugo as an `npm` module using [`hugo-bin`](https://www.npmjs.com/package/hugo-bin). This adds `hugo-bin` to your `node_modules` folder and adds the dependency to your `package.json` file.  To install the extended version of Hugo:

```bash
npm install hugo-extended --save-dev
```

See the [`hugo-bin` documentation](https://www.npmjs.com/package/hugo-bin) for usage details.

## Running a container locally

You can run docsy-example inside a [Docker](https://docs.docker.com/)
container, the container runs with a volume bound to the `docsy-example`
folder. This approach doesn't require you to install any dependencies other
than [Docker Desktop](https://www.docker.com/products/docker-desktop) on
Windows and Mac, and [Docker Compose](https://docs.docker.com/compose/install/)
on Linux.

1. Build the docker image 

   ```bash
   docker-compose build
   ```

1. Run the built image

   ```bash
   docker-compose up
   ```

   > NOTE: You can run both commands at once with `docker-compose up --build`.

1. Verify that the service is working. 

   Open your web browser and type `http://localhost:1313` in your navigation bar,
   This opens a local instance of the docsy-example homepage. You can now make
   changes to the docsy example and those changes will immediately show up in your
   browser after you save.

### Cleanup

To stop Docker Compose, on your terminal window, press **Ctrl + C**. 

To remove the produced images run:

```console
docker-compose rm
```
For more information see the [Docker Compose
documentation](https://docs.docker.com/compose/gettingstarted/).
