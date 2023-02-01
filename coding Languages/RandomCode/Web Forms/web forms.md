# Web Forms

## store data in Web Forms

1. view state: The view state is a hidden field in the HTML page that stores the state of the page and its controls in a serialized format.**In simple word** to make the data in the page "sticky" when we reload the data  
**To keep in mind** view state is a hidden field if we store a huge amount of data the view state can increase the size of the page, which can impact performance and make it **slower**

2. session: another way to store data in the server site like **view state**,The main difference between them is the scope and lifetime of the data they store:

    * Session: A session is a server-side mechanism for storing user-specific data, such as a user's preferences or login status, for the duration of the user's visit to the website. The data is stored on the server and is accessible to all pages within the website. The data is stored in memory and is lost when the user closes their browser or the session times out.

    * View state: View state is a mechanism for storing the state of a web page and its controls between postBacks. View state is a hidden field in the HTML page that stores the state of the page and its controls in a serialized format. The view state is sent back to the server with each postBack, allowing the server to restore the state of the page and its controls to their previous state. View state is specific to a single web page, and is not accessible to other pages on the website.  
**In simple word** In summary, session is used for storing user-specific data for the duration of the user's visit, while view state is used for storing the state of a single web page between postBacks. Both mechanisms can be used to store state information, and the appropriate choice depends on the specific requirements of the application.

## asp tags vs basic HTML tags

In ASP.NET Web Forms,"asp:" tags like asp:TextBox is a server-side control, while input type="text" tag is a basic HTML input element.

The main difference between the two is that the asp:TextBox control provides additional functionality and features not available with the basic HTML input element. For example:

1. asp:TextBox can be easily accessed and manipulated in code-behind, allowing you to programmatically set its properties, such as its text, font, and color.

2. asp:TextBox can automatically maintain its state across [postBacks](../../../general-Information/Terms.md#postback), meaning that the value entered by the user will be preserved even if the page is reloaded.

3. asp:TextBox can be easily styled using CSS, or can be customized using the built-in ASP.NET validation controls.
