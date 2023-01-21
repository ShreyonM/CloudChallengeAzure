# CloudChallengeAzure

This is the first time I am using GitHub to showcase my project and document the process so this ReadMe file also stands to prove that I am learning how to work with GitHub and version control. I have already obtained the Azure Fundamentals Certification with a score of 910 so step 1 is already complete.

## Setting Up Visual Studio With Github

On the getting started page, there is an option to open GitHub repository.
After selecting that option I linked my GitHub account with Visual Studio Code.

I made a test demo readme file and tried commiting changes but in order to do that I had to first setup my defalt identity. To do that I looked at the output tab of the console and it told me to run the commands 
```
 git config --global user.email "you@example.com"
 git config --global user.name "Your Name"
```
on the termianl.

After accomplishing that, I was able to commit the changes and successfully committed code from VS Code to GitHub

## Setting Up a Budget on Azure

Currently I have $200 to use during the first month using the free tier and after that since I linked my student email to the account, I received $100 credit for a 12 month period.

I opened the azure portal (https://portal.azure.com/#home) and then used the blade to navigate to **Cost Management + Billing**.

Then I went to the Budgets panel by clicking **Budgets** under **Cost Management**.

I want to crate a Budget for just the first month of use aka a budget of $200

I clicked **Add** then added a unique name to my budget and then set Reset Period to Monthly and then Creation date to the first of January and Expiration date to first of February the same year.
Set the budget threeshold to $200 and clicked **Next**.

I wanted to get alerts at 25%,50%,75% and 90% of the budget used. Since, it is easier to react to unexpected situations if the data shows a trend in that direction, I chose forecasted instad of actual.

Finally I added my email and hit create. Language was set to default.

Now that I had set up a safeguard to protect my expenditure, it was time to get started on the challenge.

## Creating The HTML file And Styling it With CSS

I made a html page with 3 buttons resembling the youtube subscrive button, youtube join button and a tweet button.
The html code is in the repository under buttons.html (https://github.com/ShreyonM/CloudChallengeAzure/blob/main/buttons.html).

## Hosting My Static Website on an Azure Account
***
* First, log into the azure portal (portal.azure.com). 
* Create a storage account
![Screenshot 2023-01-21 at 5 19 52 PM](https://user-images.githubusercontent.com/122833798/213889714-3d89d8fc-94df-4984-8a8c-e482e49506a1.png)

* Search static website on the blade search bar in the storage account                                       
![Screenshot 2023-01-21 at 5 38 29 PM](https://user-images.githubusercontent.com/122833798/213889765-4c1fc7d7-323e-4dcb-922a-4ef577e3622b.png)
* Select "enabled" and add index document name as buttons.html and error document path blank. Hit save. 
This gives us a the primary endpoint. We can use this link to find our static webiste on the public web but on pasting the link you will see an error message
![Screenshot 2023-01-21 at 5 41 49 PM](https://user-images.githubusercontent.com/122833798/213889848-1568527a-8f7d-4ac8-b0dc-e9cbad00b9e0.png)
now we need to uploaad our html file to the blob storage to find buttons.html to host
* Go back to your storage account and click "containers". Here you will see 2 containers created by default when you created the static website. Now add the buttons.html file in the $web container.
![Screenshot 2023-01-21 at 5 45 04 PM](https://user-images.githubusercontent.com/122833798/213889966-78f43b9e-8c4a-43bb-898f-77099b866a08.png)
* Now go back and search the endpoint provided on the browser.
We will get to see our website.
![Screenshot 2023-01-21 at 5 46 57 PM](https://user-images.githubusercontent.com/122833798/213890000-7ebd13c2-c89b-4a66-843a-7f20bc3271e6.png)
* Deployment of static website complete

## Configuring HTTPS Protocol And Domain Name to The Static Website

