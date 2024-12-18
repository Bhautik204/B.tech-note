- React App does not include page routing by default, we need to install a package in order to use routing.
- To install routing package,`npm install react-router-dom`.
- Recommended folder structure,
	- Within the src folder, we’ll create a folder named pages with our component files.
	- src\pages\:
	- Layout.js
	- Home.js
	- About.js  Etc…
- In order to use basic routing we need to import **BrowserRouter**, **Routes** and **Route** from **react-router-dom** package.
```js
index.js
import React from 'react';
import ReactDOM from 'react-dom/client';
import { BrowserRouter, Route, Routes } from 'react-router-dom';

import Layout from './pages/Layout';
import Home from './pages/Home';
import About from './pages/About';
import Contact from './pages/Contact';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
    <BrowserRouter>
        <Routes>
            <Route path='/' element={<Layout />}>
                <Route index element={<Home />}></Route>
                <Route path="about" element={<About />}></Route>
                <Route path="contact" element={<Contact />}></Route>
            </Route>
        </Routes>
    </BrowserRouter>
);
```


#REACT 