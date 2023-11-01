<h1>Configuring Babel</h1>

Check [this](https://github.com/quielLovesLasagna/JavaScript-Modules/blob/main/transpiling-polyfilling.md) before reading the contents below...

***

Parcel actually automatically uses ```Babel``` to transpile our code. Parcel makes some very good default decisions for us. So we will simply just go with these defaults. 

Basically, Bebel works with plugins and presets that can both be configured. A plugin is besically a specific JavaScript feature that we want to transpile/convert (ex: we only want to convert Arrow Functions back to ES5 but leave everything else in ES6). Usually, that does not make a lot of sense because we will want to transpile everything at the same time. So, usually, instead of using single plugins for each of these features, Babel actually uses presets. A present is basically a bunch of plugins bundled together. By default, Parcel is going to use preset. The present will automaticall select which JavaScript features should be compiled based on browser support. Again, that will all happen automatically and out of the box, Babel will convert all features.

  
