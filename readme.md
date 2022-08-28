# REACT ROUTER

<p align='center'>
<img src='images/router.png'></p>

* __React Router__ adalah sistem library standar yang di bangun di atas React dan di gunakan untuk membuat perutean (sederhannya) Di React Mengunakan React Router.

## INSTALLATION REACT ROUTER

```
npm install react-router-dom@6
```
> Router di install di dalam file React Js
## HOW TO USE REACT ROUTER IN REACT JS

* setelah kita mengetahui cara menginstal sekarang kita akan membahas cara pemakaian React Router ini, pertama setelah menginstal router kalian harus mengimpor react-router di dalam file index.js di dalam folder src dengan mengunakan configurasi di bawah.

```
Configuring Routes
import * as React from "react";
import ReactDOM from "react-dom/client";
import { BrowserRouter } from "react-router-dom";
import "./index.css";
import App from "./App";
import reportWebVitals from "./reportWebVitals";

const root = ReactDOM.createRoot(
  document.getElementById("root")
);
root.render(
  <React.StrictMode>
    <BrowserRouter>
      <App />
    </BrowserRouter>
  </React.StrictMode>
);
```
* Setelah itu kalian bebas menggunakan react di mana saja, contoh buka src/App.js dan ketik default markup dengan menggunakan beberapa route.
```
import * as React from "react";
import { Routes, Route, Link } from "react-router-dom";
import "./App.css";

// import file Home
import Home from './Home';

function App() {
  return (
    <div className="App">
      <h1>Welcome to React Router!</h1>
      <Routes>
        <Route path="/" element={<Home />} />
      </Routes>
    </div>
  );
}
```
> jangan lupa untuk mengimport route dan component yg akan di gunakan.

* masih di dalam folder App.js kalian bisa coba membuat route kalian sendiri.
```
function Home() {
  return (
    <>
      <main>
        <h2>Welcome to the homepage!</h2>
        <p>You can do this, I believe in you.</p>
      </main>
      <nav>
        <Link to="/about">About</Link>
      </nav>
    </>
  );
}
```

* terakhir kalian bisa merunning atau menjalankan dengan mengetik pada terminal dengan command ```npm start```

[Pelajari Selanjutnya Tentang Router ](https://reactrouter.com/en/main)

# REACT REDUX

<p align="center">
<img src="images/Redux.jpg"></P>

* __React Redux__ adalah sebuah state managemen third part atau library di luar dari pada React bahkan dari website tersendiri mengatakan A Predictable state container for Javascript Apps, Redux ini tidak eksklusif unutk React JS saja namun bisa di gunakan untuk project-project lainya misalnya Angular dan lain-lain karna bersifat global. Disamping itu ada state managemen lainnya yang namnya Context yg mana context ini adalah state managemen yg di sediakan secara langsung oleh React JS.

## INSTALLATION REDUX 
 
 * kalian bisa menggunakan ```npm``` maupun ```yarn``` dengan comand sebagai berikut.

 ```
npm install @reduxjs/toolkit react-redux
 ```

 * Kemudian buat sebuah File di dalam src/app/store.js. kemudian import configurStore dari redux.
 ```
import { configureStore } from '@reduxjs/toolkit'

export default configureStore({
  reducer: {},
})
 ```
 * setelah membuat selesai membuat store kita juga bisa memakainya di dalam component dengan cara mengimport ```<Provider> ``` di dalam aplikasi react kita ```src/index.js``` kemudian ketik ```<Provider>``` di dekat ```<app>``` dan ketik juga store sebagai prop.

 ```
import React from 'react'
import ReactDOM from 'react-dom/client'
import './index.css'
import App from './App'
import store from './app/store'
import { Provider } from 'react-redux'

// As of React 18
const root = ReactDOM.createRoot(document.getElementById('root'))

root.render(
  <Provider store={store}>
    <App />
  </Provider>
)
 ```

 [pelajari selanjutnya tentang redux](https://react-redux.js.org/tutorials/quick-start)