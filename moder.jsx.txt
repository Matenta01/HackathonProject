import React from 'react';
import logo from './University of Surrey logo.png';
import {Outlet, Link} from 'react-router-dom';
import './OG/index.css'

export function Moder(){

    return(
        <>
      <div className='one'>
        <img src={logo} alt="Surrey logo" width={189} height={70} className='left'/>
        <Link to="/" target="_parent"><button type='button' className='logout'>Log Out</button></Link>
        <Link to="/Academic" target="_parent"><button type='button' className='ac'>Be an Academic</button></Link>
        <h1 className='left'>Welcome Moderator</h1>
        <div className="two">
            <table>
                <tr>
                    <td>Academic Marker Name:</td>
                </tr>
                <tr>
                    (// input academic markers assigned to this student)
                </tr>
            </table>
            <label for="stud">Student URN: </label>
            <input list="stud"></input>
            <datalist id="stud">
            (// for loop on student database to return their full names)
            </datalist>
            <form method="post">
            <div class="mark">
                <label for="mrk">Mark: </label>
                <input id="mrk" type="text"></input>
            </div>
            <label>Comment:</label>
            <input type="text" className="comment"></input>
            </form>
        </div>
        <form action="on Submit">
            <button type="button" className='butt'>Submit</button>
            <button type="button" className='butt'>Save</button>
        </form>
      </div>
      <Outlet />
      </>
    );
  }