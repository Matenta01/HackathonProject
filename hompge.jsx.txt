import React from 'react';
import logo from './University of Surrey logo.png';
import './OG/index.css';
import { Outlet, Link, Route} from 'react-router-dom';

export function Home(){
    return(
        <>
        
        <div className='center'>
            <img src={logo} alt='surrey logo' width={270} height={100}/>
            <h1>Welcome, who are you signing in as?</h1>
            <br/>
            <Link to='Student' target='_parent'><button type="button">Student</button></Link>
            <br/>
            <Link to='Academic' target='_parent'><button type="button">Academic</button></Link>
            <br/>
            <Link to='Convener' target='_parent'><button type="button">Convener</button></Link>
       </div>
       <Outlet />
       </>
    );
}