<h1>Bundling with Parcel and NPM scripts</h1>

**Parcel** : is just another tool which is also on NPM. We will use NPM to install it using: ```npm i parcel --save-dev```, this is now be in a different dependency (dev dependency):

 ![Install parcel](./img/install-parcel.png)

```devDependency``` is like a tool that we need to build our application, but it's not a dependency that we actually include in our code. It's simply a tool, that's why it's called devDependency because we can use it to develop our project. So it will appear as a new field in ```package.json```.

![dev dependency](./img/dev-dependency.png)

<h2>Using Parcel</h2>

We cannot use parcel like this: ```parcel index.html```. This does not work with locally installed packages. Our parcel was installed locally (as we did: ```npm i parcel --save-dev```) only on this project, that's why it showed up in ```package.json``` of the project.

To use parcel in the terminal, we have 2 options:

1) Using: ```npx parcel index.html``` the option that we pass into parcel is the entry point. The entry point is ```index.html``` because that's where we include our ```script.js```, so basically the file we want to bundle up. 

![npx](./img/npx.png)

 - After doing that, parcel then also starts a new development server URL:

![development server url](./img/development-server-url.png)

- So basically, besides only bundling, it also does exactly the same job as our live-server.

![parcel live-server](./img/parcel-development-server.png)

- Parcel also created a ```dist``` folder which stands for distrubution because it is essentially gonna be this folder that we will send for production. So basically it's the code in this folder that we will send to our final users.

![dist folder](./img/dist-folder.png)

As you can see above, it created a new index.html and also a bunch of JavaScript files.

