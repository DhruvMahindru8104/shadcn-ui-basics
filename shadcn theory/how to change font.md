step 1 - just globals.css mein jao and add 

body {
  font-family: 'Lobster', cursive; # yha pe add kro apne fonts
}

step2 
// _app.js
import Head from 'next/head';
import '../styles/globals.css';

function MyApp({ Component, pageProps }) {
  return (
    <>
      <Head>
        <link # google font add kro yha pr 
          rel="stylesheet"
          href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap"
        />
      </Head>
      <Component {...pageProps} />
    </>
  );
}

export default MyApp;
