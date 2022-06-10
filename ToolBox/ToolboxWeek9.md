# Woche 9 - 04.05.22

##Goodie is in the LiveCoding folder of that week
Dies wäre auch allgemein gesehn ein guter Einsatz um Code besser zu kommentieren.
```javascript

                /**
                 * logs to the console
                 * @function
                 * @template T
                 //* @param { T } x
                 * @return T
                 */
                const id = x => x;

                /**
                 * logs to the console
                 * @function
                 //* @param { !String } message - what to print to the console, mandatory
                 * @return void
                 * @example
                 *      log("Hallo");
                 */

                const log = message => console.log(message);
                log(id("Hi"));
                id(1);
```