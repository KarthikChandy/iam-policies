# AWS IAM Policy Templates

The purpose of this article is to provide suggestions that will help harden security and keep the operating cost low for AWS lab environments.
Additionally, a few baseline AWS IAM templates are also provided.

**NOTE**: Please refer to the Disclaimer for more information.

## Recommended Steps

1. Download and install the **Console Recorder for AWS** tool. Supported platforms are [Firefox](https://addons.mozilla.org/en-US/firefox/addon/console-recorder/) or [Chrome](https://chrome.google.com/webstore/detail/console-recorder-for-aws/ganlhgooidfbijjidcpkeaohjnkeicba?hl=en).
2. Make sure you use an AWS account with unrestricted access to perform the below steps.
3. Click the **Start Recording** button on **Console Recorder for AWS**. </br> ![StartRecording](images/StartRecording.jpg)
4. Start working on the lab and try to stick to the lab instructions.
5. After you conclude the lab, click the **Stop Recording** button on **Console Recorder for AWS**.  </br> ![StopRecording](images/StopRecording.jpg)
6. The **AWS IAM** tab will contain the required policy. </br> ![iampolicy](images/IAM-policy.jpg)
7. Create a new IAM policy using the policy document generated in the earlier step.
8. The policy generated above could serve as an initial starting point to determine the final policy. The generated policy may have a few limitations, as some API actions are not captured.</br> **E.G.**: The policy may capture the *ec2:RunInstances* action. However, how would you specify a list of instance types that should be used? To make it easy to implement these kinds of requirements, explore the additional lab policies included in the sample-policies folder.
9. Customise the final policy as required.
10. Finally, make sure you test your policy before release.