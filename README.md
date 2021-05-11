# serverless-hol-lab

1. Click the Deploy to Azure button to open the Azure portal:
  <a href ="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Friwasa%2Fserverless-hol-lab%2Fmain%2Fserverless-hol-no-vm.azuredeploy.json" target="_blank" title="Deploy to Azure">
      <img src="http://azuredeploy.net/deploybutton.png"/>
  </a>

2. On the custom deployment screen, the first parameter you need to populate is the `ObjectId` associated with the account you used to log into the Azure portal. To retrieve this, select the **Cloud Shell** icon on the Azure portal toolbar to open an Azure command line interface (CLI) terminal window at the bottom of your open browser window.

   ![The Cloud Shell icon is highlighted on the Azure portal toolbar.](media/azure-toolbar-cloud-shell.png "Azure toolbar")

3. In the PowerShell terminal window that opens in the Azure portal, enter the following command at the prompt:

   ```powershell
   az ad signed-in-user show --query objectId -o tsv
   ```

   ![At the cloud shell prompt, the az ad signed-in-user show command is entered and highlighted.](media/azure-cli-az-ad-signed-in-user-show.png "Azure CLI")

4. Execute the command and copy the output value.

   ![In the cloud shell, the output from the az ad signed-in-user show command is highlighted.](media/azure-cli-az-ad-signed-in-user-show-output.png "Azure CLI")

5. Now, on the custom deployment screen in the Azure portal, enter the following:

   - **Subscription**: Select the subscription you are using for this hands-on lab.
   - **Resource group**: Select the hands-on-lab-SUFFIX resource group from the dropdown list.
   - **Signed In User Object Id**: Paste the value you copied above from the cloud shell terminal command output.
   - **Vm Username**: Accept the default value, **demouser**.
   - **Vm Password**: Accept the default value, **Password.1!!**.

   ![The Custom deployment blade is displayed, and the information above is entered on the Custom deployment blade.](media/azure-custom-deployment.png "Custom deployment blade")

6. Select **Review + create** to review the custom deployment.

   > **Note**: The ARM template will append a hyphen followed by a 13-digit string at the end of resource names. This suffix ensures globally unique names for resources. We will ignore that string when referring to resources throughout the lab.

7. On the Review + create blade, ensure the _Validation passed_ message is displayed and then select **Create** to begin the custom deployment.

   > **Note**: The deployment of the custom ARM template should finish in about 5 minutes.

   ![On the Review + create blade for the custom deployment, the Validation passed message is highlighted, and the Create button is highlighted.](media/azure-custom-deployment-review-create.png "Review + create custom deployment")

8. You can monitor the deployment's progress on the **Deployment** blade that opens when you start the ARM template deployment.





   
Do not click this button unless instructed:

  <a href ="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Friwasa%2Fserverless-hol-lab%2Fmain%2Fserverless-hol.azuredeploy.json" target="_blank" title="Deploy to Azure">
      <img src="http://azuredeploy.net/deploybutton.png"/>
   </a>
