import React from 'react'
import './Navbar.css'
import surrey_logo from '../../assets/official logo.png'
import {Outlet, Link} from 'react-router-dom'

export function Navbar(){
    
  return (
    <>
    <nav className= "container">
      <img src={surrey_logo} alt= "" className='logo'/>
      <ul>
        <li><Link to="/" target="_parent"><button className='btn1'>Log Out</button></Link></li>
      </ul>
    </nav>
    <Outlet/>
    </>
  )
  
}



