# Approach 4: Connect via SSH to the Compute Instance Private IP Address using a SSH Private Key with OCI Cloud Shell

In this approach, we will connect to the Linux instance using the OCI Cloud Shell provided by OCI and connect to the instance using the private IP address.


<img width="2338" height="1710" alt="Access-Manage-Linux-Instance-214" src="https://github.com/user-attachments/assets/5d41159a-82bc-4759-bc3e-a450af8a5252" />

+ Log in to the OCI Console and click on the **OCI Cloud Shell** icon to open the Cloud Shell console.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-215" src="https://github.com/user-attachments/assets/cf909d3a-b200-4c83-b584-00c1b5e2dbe7" />

+ Click **Cloud Shell**.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-216" src="https://github.com/user-attachments/assets/1544ff1e-90c8-40e0-8920-cd6f59c91040" />

Make sure that the Cloud Shell window opens.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-217" src="https://github.com/user-attachments/assets/4a1448ff-a6e7-4f52-b7a3-e4b034793547" />

+ Enter 'N' to skip the tutorial for now.

<img width="1515" height="824" alt="Access-Manage-Linux-Instance-218" src="https://github.com/user-attachments/assets/a54a9634-6007-420a-84d2-092a6aab54cc" />

In order to connect to the Linux instance using the private IP address, it is important that the Cloud Shell gets access to the same subnet as where the Linux instance is connected to.

We can do this by **plugging** the Cloud Shell into the same VCN and subnet where the Linux instance also resides. By default the network is set to **Public**, but we are going to change this by creating a new private network on the fly.

+ Click **Network** and select **Private network definition list**.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-219" src="https://github.com/user-attachments/assets/83c39210-2a69-4198-b716-b9c0a850f01f" />

+ Click **Create private network definition**.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-220" src="https://github.com/user-attachments/assets/ed529a62-e5c0-4813-8b75-6e303cfa3708" />

+ In Create private network definition, enter the following information.

1. Enter a Name.
2. Select the corresponding VCN where the Linux instance resides in.
3. Select the Subnet where the Linux instance resides in.
4. Select Use active network to activate the private network right away.
5. Click Create.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-221" src="https://github.com/user-attachments/assets/c4fbff03-386d-4be0-8d12-735131a3a198" />

+ Notice that the status of the network will change to the newly created private network with Connecting. This will take a few seconds to complete.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-222" src="https://github.com/user-attachments/assets/9ee4581e-8ff1-49bd-af40-52195d799f3b" />

1. Private network is connected.
2. Click Close to close the private network definition list.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-223" src="https://github.com/user-attachments/assets/5910d702-70c4-4f1f-8c51-9206847b7f1e" />

1. Run the `ls-l` command and see that we do not have the private key in the home folder.
2. To upload the private key, click the wheel.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-224" src="https://github.com/user-attachments/assets/9ab843b1-8350-4cea-8d6f-2edb82b0f154" />

1. Click **Upload**.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-225" src="https://github.com/user-attachments/assets/df274513-79c3-4a19-84d9-b84bf85129e2" />

1. Click **Select from your computer**.
2. Click **Upload**.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-226" src="https://github.com/user-attachments/assets/366f4081-3761-4910-b54a-f3b2ff209e44" />

1. Select the private key from the local computer.
2. Click Open.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-227" src="https://github.com/user-attachments/assets/351d265a-f91b-42de-b28a-67ff215d68f9" />

1. Review the key selected in the previous step.
2. Click Upload.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-228" src="https://github.com/user-attachments/assets/8711acec-1a73-447b-8258-f0099aad5cfc" />

1. Make sure the upload is completed.
2. Click Hide.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-229" src="https://github.com/user-attachments/assets/17dab586-7354-4909-b5d6-2cddfece4430" />

+ Run the `ls-l` command to check the private key.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-230" src="https://github.com/user-attachments/assets/cfcbd425-4249-455c-b2e5-7752bfeab820" />

1. Restrict permissions of the private key and make sure the access is restricted before it can be used.
2. Connect to the instance using the SSH command and specify the private key.
3. Run the following command to verify the IP address.
4. Verify the IP address.
5. Minimize the Cloud Shell console.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-231" src="https://github.com/user-attachments/assets/97d0141a-b9eb-4086-9ed6-14f5617bb096" />

+ Cloud Shell console is minimized. Click **Restore** to restore the Cloud Shell console.

<img width="1514" height="824" alt="Access-Manage-Linux-Instance-232" src="https://github.com/user-attachments/assets/10feb71e-fe6e-4393-9939-b067f88343cb" />

+ Review the restored Cloud Shell console. Click **X** to close the Cloud Shell window.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-233" src="https://github.com/user-attachments/assets/c8c522b1-be72-4cf5-bf0a-2a448a2d4731" />

+ Click **Exit** to close the Cloud Shell window.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-234" src="https://github.com/user-attachments/assets/ec34df13-28e7-406e-8e14-8cdf6c50c7a6" />

Now, we are back in the instance overview.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-235" src="https://github.com/user-attachments/assets/059dcd6d-a19d-4ff5-84af-ed6107ae0107" />

---
