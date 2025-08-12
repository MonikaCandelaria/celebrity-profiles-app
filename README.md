import React, { useState } from 'react';

export default function Login() {
  const [username, setUsername] = useState('');
  const [password, setPassword] = useState('');

  const handleSubmit = (e) => {
    e.preventDefault();
    if (username === 'admin' && password === '1234') {
      alert('Login successful!');
    } else {
      alert('Invalid username or password');
    }
  };

  return (
    <div style={{ padding: '2rem' }}>
      <h1>Login</h1>
      <form onSubmit={handleSubmit}>
        <div>
          <label>Username: </label>
          <input value={username} onChange={(e) => setUsername(e.target.value)} />
        </div>
        <div style={{ marginTop: '1rem' }}>
          <label>Password: </label>
          <input type="password" value={password} onChange={(e) => setPassword(e.target.value)} />
        </div>
        <button style={{ marginTop: '1rem' }} type="submit">Login</button>
      </form>
    </div>
  );
}
