import React from 'react'
import './Form.css'
import moderator_image from '../../assets/pexels-andy-barbour-6684373.jpg'
import {Navbar} from '../Navbar/Navbar.jsx'
import {Outlet, Link} from 'react-router-dom'

export function Form() {
  return (
    <>
    <div className='myForm'>
        <Navbar/>
        <div className='body-col1'>
         <form action="onSubmit">
            <label htmlFor="urn">URN:</label>
            <input type="number" id="urn" name="URN" minLength="7" maxLength="7" placeholder='Input URN' required/>
            <label htmlFor="mark">Mark:</label>
            <input type="number" id="mark" name="mark" min="0" max="100" placeholder='Input Mark'/>
            <label htmlFor="comment">Comment</label>
            <textarea name="comment" rows="20" placeholder='Enter comment'></textarea>
            <button type="save" className='btn1'>Save Draft</button>
            <button type="submit" className='btn1'>Submit now</button>
         </form>
        </div>
        <div className='body-col2'>
          <div className="image">
            <img src={moderator_image} alt="" />
            <div className="caption">
            <Link to="/Moderator" target="Moderator"><button id="link">Be A Moderator</button> </Link>
            </div>
          </div>
        </div>
       
      
    </div>
    <Outlet/>
    </>
  )
}

