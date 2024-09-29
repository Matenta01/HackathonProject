import React from 'react';
import ReactDOM from 'react-dom/client';
import reportWebVitals from './reportWebVitals.js';
import {Home} from './hompge.jsx';
import {Moder} from './moder.jsx';
import {Form} from './Components/Form/Form.jsx';
import { BrowserRouter, Routes, Route} from 'react-router-dom';
import {Student} from './student.jsx';
import {Convener} from './convener.jsx';
// all function names must start with a capital letter

const root = ReactDOM.createRoot(document.getElementById('root'));

export default function App(){
  return(
    <React.StrictMode>
  <BrowserRouter>
  <switch>
    <Routes>
      <Route path="/" element={<Home />}/>
      <Route path="Academic" element={<Form />}/>
      <Route path="Moderator" element={<Moder />}/>
      <Route path="Student" element={<Student/>}/>
      <Route path="Convener" element={<Convener/>}/>
    </Routes>
  </switch>
  </BrowserRouter>
  </React.StrictMode>
  );
}

root.render(
  <App/>
);

// If you want to start measuring performance in your app, pass a function
// to log results (for example: reportWebVitals(console.log))
// or send to an analytics endpoint. Learn more: https://bit.ly/CRA-vitals
reportWebVitals();