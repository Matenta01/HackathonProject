import React from 'react';
import {Outlet, Link} from 'react-router-dom';
import './student.css';

export function Student(){
    return(
        <>
    <div>
        
        <div class="sidebar">
            <Link to='/' target='_parent'><i class="fa fa-fw fa-home"></i>Log Out</Link>
        </div>
        <div class="main">
            <h2>Welcome, <span id="studentName"></span></h2>
            <div className="panel">
                <h3>Final Mark: </h3>
                <input type="text" className="comment"></input>
                
            </div>
            <div className='panel'>
                <h3>Comments: </h3>
                <input type="text" className="comment"></input>
            </div>
            <div className='panel'>
                <form id="preferences" method="post">
                    <label for="preferences">Choose your preferences: </label>
                    <select name="preferences[]" id="preferemces" multiple size="4">
                        <option value="preference1">Preference 1</option>
                        <option value="preference2">Preference 2</option>
                        <option value="preference3">Preference 3</option>
                        <option value="preference4">Preference 4</option>
                    </select>
                    <br></br><br></br>
                    <input type="submit" value="submit"/>
                </form>
            </div>
        </div>
    </div>
    <Outlet/>
    </>
    );
}