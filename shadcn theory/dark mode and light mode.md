step 1- tailwind.config.js mein jake
module.exports = {
  darkMode:'media', # ise  media kr do 
  content: [
    './pages/**/*.{js,jsx}',
    './components/**/*.{js,jsx}',
    './app/**/*.{js,jsx}',
    './@/**/*.{js,jsx}',
  ],

step 2 -
_app.js mein jake yeh code add krdo 
 import '../styles/globals.css'
 import { useEffect } from 'react';

 function MyApp({ Component, pageProps }) {
  useEffect(() => {
    const darkMode = window.matchMedia('(prefers-color-scheme: dark)').matches;
    if (darkMode) {
      document.documentElement.classList.add('dark');
    } else {
      document.documentElement.classList.remove('dark');
    }
  }, []);
   return <Component {...pageProps} />
 }
 
 export default MyApp