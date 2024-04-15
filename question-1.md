# About async and defer on script

1. normal <script> will be have a network blocking
2. property `defer` and `async` in script
3. `async` as it name, this will not blocking the HTML parsing on the browser, like basically in the background will fetch the script, once it done the the script will be run
4. `defer` like `async` but it will be executed at the end while the HTML finished parsed on the browser
5. if we have a property async and defer in the save script tag html, we will using a fallback default from the browser, but the main property will be `defer` first if not fallback to `async`
