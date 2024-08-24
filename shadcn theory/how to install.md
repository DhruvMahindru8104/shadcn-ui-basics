step 1- install tailwind css in your project
step 2- create jsconfig.json in root directory and add this code
{
  "compilerOptions": {
    "baseUrl": ".",
    "paths": {
      "@/components/*": ["components/*"],
      "@/lib/utils/*": ["lib/utils/*"]
    }
  },
  "include": ["**/*.js", "**/*.jsx", "next-env.d.ts"],
  "exclude": ["node_modules"]
}
step 3 - run npx shadcn-ui@latest init on cmd ( it will install shadcn in your nextjs project)

step4- tailwind.config.js mein 
  content: [
    './pages/**/*.{js,jsx}',
    './components/**/*.{js,jsx}',
    './app/**/*.{js,jsx}',
    './@/**/*.{js,jsx}', # to add tailwind in shadcn ui
  ],


it will create components folder , now we can use this folder whenever we need to use it 