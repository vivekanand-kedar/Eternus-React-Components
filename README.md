# Eternus-React-Components

[![NPM](https://img.shields.io/npm/v/react-select.svg)](https://www.npmjs.com/package/react-bootstrap)


React components inspired by react-bootstrap.

# Availale components

 - Dropdown
 - Login Component
 - File Upload
 - Export to Excel
 

# Install

``` bash
$npm install eternus-react-component
```

# Dropdown

**Usage**

```js
import {Dropdown} from "eternus-react-component";

export default class Sample extends Component {

    optionClicked = () => {
        ...
    }

    render() {
        const options = [
               {
                    optionName :"Action 1",
                    onClick:this.optionClicked,
                    Link :"#/action1",
                    icon :"fa fa-arrow-right"
                },
                {
                    ...
                }
           ];
        return (
            <div>;
                <Dropdown
                    title = "Dropdown"
                    variant = "success"
                    dropDirection = "down"
                    options = {options}
                    error = {true}
                    errorMessage = "error message"
                />
            </div>
        )
    }
}

```

**Props**

Common props you need to specify include:

| **Props** | **Default** | **Type** | **Description** |
| --- | --- | --- | --- |
| title | Dropdown | String | Title for the dropdown  |
| variant | success | String ['primary', 'secondary' , 'success' ,'danger' , 'warning' , 'info' , 'dark' , 'light'] | Color for the dropdown  |
| dropDirection | down | String ['up', 'down', 'left', 'right']  | Determines the direction and location of the Menu in relation to its toggle  |
| options | Empty array | Array of objects | Option menu for dropdown menu items  |
| error | false | Boolean | Allows the user to trigger an error  |
| errorMessage | Empty String | String | Error message to be displayed  |



**Options array object keys**

| **Key** | **Type** | **Default** | **Description** |
| --- | --- | --- | --- |
| optionName  | String |   | Name for menu item |
| onClick  | Function |   | Callback fired when the menu item is clicked |
| Link  | String |   | href link associated with menu item |
| icon  | String |   | Icon to be displayed along with menu item name |
| disabled  | Boolean | false | Disable the menu item, making it unselectable |


# Login

**Usage**

```js

import {Login} from "eternus-react-component";

export default class Sample extends Component {

    onChangeComponent=(e) => {
        ...
    }

    onSubmit =()=>{
        ...
    }

    render() { 
        return (
                <Login
                    title="Login"
                    usernameType="email"
                    usernamePlaceholder="Username" 
                    passwordPlaceholder="Password"
                    buttonTitle="Sign In"
                    onChange={this.onChangeComponent.bind(this)}
                    position="Left"  
                    usernameName="usernameValue"     
                    passwordName="userPasswordValue"   
                    usernameValue={this.state.usernameValue}
                    userPasswordValue={this.state.userPasswordValue}
                    error={false}
                    errorMessage="Invalid username or password"  
                    onSubmit= {this.onSubmit}  
                />
        )
    }
}

```

**Props**

Common props you need to specify include:


| **Props** | **Default** | **Type** | **Description** |
| --- | --- | --- | --- |

| variant             | success      | String ['primary', 'secondary' , 'success' ,'danger'  , 'warning' , 'info' , 'dark' , 'light'] | Color for sign in button                           |
| passwordType        | password     | String[password]                                                                               | Input type for password field                      |
| title               | Login        | String                                                                                         | Title for the login page                           |
| usernameType        | text         | String[email,number,text]                                                                      | Input type for username field                      |
| usernamePlaceholder | Username     | String                                                                                         | Placeholder for username field                     |
| passwordPlaceholder | Password     | String                                                                                         | Placeholder for password field                     |
| buttonTitle         | Sign In      | String                                                                                         | Text for sign in button                            |
| onChange            |              | Function                                                                                       | onChange handler for username and password fields  |
| position            | center       | String[center,left]                                                                            | Position for login page title                      |
| username       | username     | String                                                                                         | Input name for username field                      |
| passwordName        | password     | String                                                                                         | Input name for password field                      |
| usernameValue       | Empty String | String                                                                                         | Value for username field                           |
| userPasswordValue   | Empty String | String                                                                                         | Value for password field                           |
| forgotPasswordLink  |              | String                                                                                         | Redirect link for forgot password                  |
| signUpLink          |              | String                                                                                         | Redirect link for sign up                          |
| error               | false        | Boolean                                                                                        | Trigger error                                      |
| errorMessage        | Empty String | String                                                                                         | Error message to be displayed                      |
| onSubmit            |              | Function                                                                                       | Callback function to submit the login credentials  |
