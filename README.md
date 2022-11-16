# AzureAutoTagger

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Famudapalani%2FAzureAutoTagger%2Fmain%2Fazuredeploy.json)

Azure AutoTagger is a lightweight, low-cost serverless solution that can easily be deployed to an Azure subscription. Once deployed Azure AutoTagger monitors for `ResourceWriteSucess` events such as resource group create, vm create and AKS create within the subscription and triggers an Azure Function to automatically apply a `ITGSO_CREATED_TIMESTAMP` and `ITGSO_CREATED_BY` tag.

![autotagger](/images/autotagger.png)

* [**https://cloudlumberjack.com/posts/azureautotagger/**](https://cloudlumberjack.com/posts/azureautotagger/): More details in a blog post describing the solution.

* [**https://github.com/amudapalani/AzureAutoTagger**](https://github.com/amudapalani/AzureAutoTagger): Contains the ARM template code to deploy the infrastructure and role assignments to the subscription

* [**https://github.com/amudapalani/AzureAutoTaggerFunction**](https://github.com/amudapalani/AzureAutoTaggerFunction): Contains the Azure Function PowerShell code

![tagging](/images/tagging-spedup.gif)

## Deployment

> Important: You must have **Owner** permissions on the subscription you intend to deploy this to. The template will create a managed identity and assign it to the `Reader` and `Tag Contributor` roles.

Use the **Deploy to Azure** button to easily deploy this solution in a subscription

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Famudapalani%2FAzureAutoTagger%2Fmain%2Fazuredeploy.json)
