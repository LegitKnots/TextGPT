# TextGPT (v1.0.0)


## API Key

Replace `"YOUR_API_KEY"` with your actual OpenAI API Key in the `variables.php` file. This key is essential for making API calls to the OpenAI service. Keep it secure and do not share it publicly.

## Usage

This application is designed to work seamlessly with the Shortcuts application within iPhone (tested in iOS 17). Here's an overview of how the application functions:

1.  An automation is installed on your iPhone and configured to run when specific types of text messages are received, or from specific users (please note that iOS restrictions may require specific sender conditions, such as using a space, to trigger the automation).
    
2.  The automation sends the received text message as input to this API intermediary using a GET variable named "textMessage."
    
3.  The API intermediary processes the text message, sends it to ChatGPT, and retrieves a response.
    
4.  The response from ChatGPT is sent back to your iPhone.
    
5.  Your iPhone determines how to format and style the response based on the "responseType" and sends the "responseContent" to you.
    

Below is an example of a Shortcuts Automation for reference.

## Inputs

-   `textMessage`: This is the actual message that will be sent to the model after some pre-parsing.

Within the `textMessage` variable, you can include special commands to modify how the model responds. These commands are prefixed with "@" and followed by the command name, ending with "@end."

### Example:

Suppose you want to change the style in which the AI responds. In that case, you can add the following command anywhere in the text message:


`@style
Your job is to respond to me using only the word "no."
@end` 

### Usage of Commands:

-   `@style`: This command modifies the style of the AI's response.
-   `@imgSize`: This command changes the size of images generated by OpenAI, affecting the response's network time.



![TextGPTImage](https://raw.githubusercontent.com/AJPNetworks/TextGPT/main/images/01.jpg)
![TextGPTImage](https://raw.githubusercontent.com/AJPNetworks/TextGPT/main/images/02.PNG)
![TextGPTImage](https://raw.githubusercontent.com/AJPNetworks/TextGPT/main/images/03.PNG)
![TextGPTImage](https://raw.githubusercontent.com/AJPNetworks/TextGPT/main/images/04.PNG)
![TextGPTImage](https://raw.githubusercontent.com/AJPNetworks/TextGPT/main/images/05.PNG)
![TextGPTImage](https://raw.githubusercontent.com/AJPNetworks/TextGPT/main/images/06.PNG)