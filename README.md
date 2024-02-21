# SE111_202420

//view this element via its var name using console.log
        console.log(body)

        //accessing attributes (properties) of stored HTML elements
        console.log(`The body's ID is: ${body.id}`)

        body.id = `bodyId`

        console.log(body)
        console.log(`The body's ID is: ${body.id}`)

        //all elements with open and close tags have a .innerHTML attribute (property)

        //select and store the h2 that says "Hello" (id="hello")
        var hello = document.querySelector(`#hello`)
        console.log(hello)

        //change the hello id to goodbye;  change the content to read goodbye as well 
        hello.id = `goodbye`
        console.log(`The h2's ID is: ${hello.id}`)

        //hello.innerHTML = `goodbye`
        //instead of REPLACING hello with goodbye, ADD & goodbye to the h2
        hello.innerHTML += ` & Goodbye`
        //hello.innerHTML = hello.innerHTML + ` & Goodbye`
        //total = total + 1 ; total += 1

        //EVENT LISTENERS -------- 
        //we add event listeners to elements so they "listen" for an action to take place and then run a function/process

        //select the element first:
        document.querySelector(`#enter-button`).addEventListener(`click`, formConfirm)

        //build the function - this will take place EVERY time the button is clicked
        function formConfirm()
        {

            //access a global value inside of the function
            //console.log(hello)

            //using a local variable - ONLY ACCESSIBLE IN THE FUNCTION
            var fname = document.getElementById(`first`).value
            //above same as below
            //var fname = document.querySelector(`#first`)

            var lname = document.getElementById(`last`).value
            var age = document.getElementById(`age`).value    






            console.log(fname, lname, age) //once .value is added, we can see JUST what was entered into the text fields

            var fullName = fname + ` ` + lname

            alert(`Hello there, ${fullName}!`)





            






            var info = document.querySelector(`#info`)

            info.style.color = `blue`

            //add to the info div's innerHTML
            info.innerHTML += `<h4>Name:</h4>`
            info.innerHTML += `<p>`
            info.innerHTML += fullName
            info.innerHTML += `</p>`

            //conditionals in JS-------------------
            age = Number(age) //casts age as a Number type (instead of string)
            var activity = ``

            //age filter - "for fun activities"
            if (age >= 21)
            {
                activity += 'Drink!'
            }
            if (age >= 18)
            {
                activity += `Vote!`
            }
            if (age >= 16)
            {
                activity += `Drive!`
            }
            else
            {
                activity = `Too young for fun :[`
            }


            info.innerHTML += `<br><br>`
            info.innerHTML += `<h2> ${activity} </h2`


        }//formConfirm() CLOSE