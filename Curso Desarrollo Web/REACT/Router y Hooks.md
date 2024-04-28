![[Pasted image 20240424095901.png]]
![[Pasted image 20240424100010.png]]
![[Pasted image 20240424100024.png]]
![[Pasted image 20240424100930.png]]
![[Pasted image 20240424101117.png]]

# Documentacion 
[Home v6.23.0 | React Router](https://reactrouter.com/en/main)

[React Router: Declarative Routing for React.js](https://v5.reactrouter.com/)

---
![[Pasted image 20240424101258.png]]
![[Pasted image 20240424101337.png]]

---
https://reactrouter.com/en/main/start/tutorial
# Como instalar React Router 
# React Router

1. Instalar los modulos de React Router con el comando:

  

```sh

npm install react-router-dom localforage match-sorter sort-by

o solamente

npm install react-router-dom

```

  

2. Revisar que se haya agregados los modulos `node_modules`

3. Crear una `createBrowserRouter` y configurar en `main.jsx`

  

```jsx

import React from 'react'

import ReactDOM from 'react-dom/client'

import App from './App.jsx'

import './index.css'

import { RouterProvider, createBrowserRouter } from 'react-router-dom'

import Astros from './components/Astros/Astros.jsx'

import Login from './components/login/login.jsx'

/* Aquí irán mis Routes definidas de manera individual, definiendo rutas mediante el path asignado y el elemento

* path, hace referencia a la ruta que se escribirá en el buscador del navegador ../path

* element, hace referencia al componente al cual me quiero dirigir (componente completo)

*/

const router = createBrowserRouter([

  {

    path: "/", element: <App />

  },

  {

    path: "/login", element: <Login />

  },

  {

    path: "/astros", element: <Astros />

  },

]);

ReactDOM.createRoot(document.getElementById('root')).render(

  <React.StrictMode>

    <RouterProvider router={ router } />

  </React.StrictMode>,

)

  

```

  

4. Definir los paths y elements que hacen referencia a las rutas

  

```jsx

const router = createBrowserRouter([

  {

    path: "/", element: <App />

  },

  {

    path: "/login", element: <Login />

  },

  {

    path: "/astros", element: <Astros />

  },

]);

  

```

  

5. Los componentes `<Link ></Link>` cumplen la funcion de dirigir a otras rutas, algo parecido a `<a></a>`. Tengo que definir el path al cual hara referencia `to="/path"`
```jsx
<div className='button--container'>

        <Link to="/astros">

        <Button label='Astros' />

        </ Link>

  

        <Link to="/login">

        <Button label='Login' />

        </Link>

      </div>
```

---
![[Pasted image 20240424115711.png]]
Estos 5 archivos trabajamos

---
[https://github.com/mui/material-ui/blob/v5.15.15/docs/data/material/getting-started/templates/sign-in-side/SignInSide.js](https://github.com/mui/material-ui/blob/v5.15.15/docs/data/material/getting-started/templates/sign-in-side/SignInSide.js "https://github.com/mui/material-ui/blob/v5.15.15/docs/data/material/getting-started/templates/sign-in-side/signinside.js")


---

----
![[Pasted image 20240424121138.png]]
![[Pasted image 20240424121143.png]]
![[Pasted image 20240424121534.png]]
![[Pasted image 20240424121539.png]]
![[Pasted image 20240424121651.png]]
![[Pasted image 20240424121704.png]]

![[Pasted image 20240424121758.png]]![[Pasted image 20240424122124.png]]

[https://desarrollofront.medium.com/entendiendo-los-hooks-de-react-c%C3%B3mo-usar-usestate-y-useeffect-en-nuestros-componentes-611b9e826dfa](https://desarrollofront.medium.com/entendiendo-los-hooks-de-react-c%C3%B3mo-usar-usestate-y-useeffect-en-nuestros-componentes-611b9e826dfa "https://desarrollofront.medium.com/entendiendo-los-hooks-de-react-c%c3%b3mo-usar-usestate-y-useeffect-en-nuestros-componentes-611b9e826dfa")

[https://react.dev/reference/react/hooks](https://react.dev/reference/react/hooks "https://react.dev/reference/react/hooks")


---
Todas las dependencias que hemos descargado
MUI

material ui

icons material

REACT ROUTER

react router dom

AXIOS

axios

---
![[Pasted image 20240424153853.png]]