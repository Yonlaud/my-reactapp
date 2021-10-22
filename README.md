import React, { Component } from 'react'
import logo from './logo.svg'
import './App.css'
import NotificationsSwitch from './components/notifications-switch'
import UserSettings from './components/user-settings'

class App extends Component {
  render () {
    return (
      <div className='App'>
        <div className='App-header'>
          <img src={logo} className='App-logo' alt='logo' />
          <h2>Welcome to React</h2>
        </div>
        <p className='App-intro'>
          To get started, I just edited this text in my app.
        </p>

        <hr />
        <NotificationsSwitch />
        <hr />
        <UserSettings />

      </div>
    )
  }
}

export default App
