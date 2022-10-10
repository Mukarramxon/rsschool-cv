# MUKARRAMKHON KODIROVA

## Contact Info

#### Email: <m.kodirova@outlook.com>
#### Phone Number: +9998(93)4139959
#### Linked In: <https://www.linkedin.com/in/mukarramkhon-kodirova-460317155/>


## Summary
> A motivative social person who really love software engineering. I always ready to have a meeting and discuss about technologies which can be solution for real life problems. 


## Skills
- Technical
  - HTML/CSS
  - JS
  - OOP
- Project Management
  - Agile
  - Scrum Master
  - Lean
  - Notion
  - Trello 
  - Microsoft Project Quick
- Soft Skills
  - Leadership
  - Negotiation
  - Problem Solving


## Code Examples

Some basic code

```
import React, { useContext, useEffect, useState } from 'react'
import { useHttp } from '../hooks/http.hook'
import { useMessage } from '../hooks/message.hook'
import { AuthContext } from '../context/AuthContext'

export const AuthPage = () => {
    const auth = useContext(AuthContext)
    const message = useMessage()
    const { loading, request, error, clearError } = useHttp()
    const [form, setForm] = useState({
        email: '', password: ''
    })

    useEffect(() => {
        message(error)
        clearError()
    }, [error, message, clearError])

    const changeHandler = event => {
        setForm({ ...form, [event.target.name]: event.target.value })
    }

    const registerHandler = async () => {
        try {
            const data = await request('/api/auth/register', 'POST', { ...form })
            message(data.message)
        } catch (e) { }
    }

    const loginHandler = async () => {
        try {
            const data = await request('/api/auth/login', 'POST', { ...form })
            auth.login(data.token, data.userId)
        } catch (e) { }
    }


    return (
        <div className='row'>
            <div className="col s6 offset-s3">
                <h1>Shorten URL</h1>
                <div className="card blue darken-1">
                    <div className="card-content white-text">
                        <span className="card-title">Authentification</span>
                        <div>
                            <div className='input-field'>
                                <input
                                    placeholder='Enter an email'
                                    id='email'
                                    type="text"
                                    name='email'
                                    className='yellow-input'
                                    value={form.email}
                                    onChange={changeHandler}
                                />
                                <label htmlFor='email'>Email</label>
                            </div>
                            <div className='input-field'>
                                <input
                                    placeholder='Enter a password'
                                    id='password'
                                    type="password"
                                    name='password'
                                    className='yellow-input'
                                    value={form.password}
                                    onChange={changeHandler}
                                />
                                <label htmlFor='password'>Password</label>
                            </div>
                        </div>
                    </div>
                    <div className="card-action">
                        <button
                            className='btn yellow darken-4'
                            style={{ marginRight: 10 }}
                            disabled={loading}
                            onClick={loginHandler}
                        >
                            Log In
                        </button>
                        <button
                            className='btn grey lighten-1 black-text'
                            onClick={registerHandler}
                            disabled={loading}
                        >
                            Sign In
                        </button>
                    </div>
                </div>
            </div>
        </div>
    )
}

```


## Experience 
**[Beautify.uz](www.beautify.uz)** - In this project participated as a Frontend developer (HTML/CSS, JS , VueJS) <br />
**[BiznesRivoj.uz](www.biznesrivoj.uz)** - Managing, testing, teaching personal to manage the site from admin panel, providing the materials to developers, renewing the website of the online business journal.


## Education
**2017-2021** - Bachelor of Science in Information and Communication Engineering, *INHA University in Tashkent*  
**2013-2016** - Foreign Philology(English), *The 2nd lyceum under Machinery Institute*


## Languages

- Uzbek - Native
- English - C1
- Russian - C1
- Italian - A1


