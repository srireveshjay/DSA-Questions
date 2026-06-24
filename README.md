# DSA-Questions
A collection of DSA Questions
#To change the password
crypto.subtle.digest('SHA-256', new TextEncoder().encode('YourNewPassword'))
  .then(b => console.log([...new Uint8Array(b)].map(x=>x.toString(16).padStart(2,'0')).join('')))
