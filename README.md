# Approach 4: Connect via SSH to the Compute Instance Private IP Address using a SSH Private Key with OCI Cloud Shell

In this approach, we will connect to the Linux instance using the OCI Cloud Shell provided by OCI and connect to the instance using the private IP address.

<img width="2338" height="1710" alt="Access-Manage-Linux-Instance-214" src="https://github.com/user-attachments/assets/f317e1b6-de86-4e30-bc4f-a4d5d9a5beb1" />

+ Log in to the OCI Console and click on the **OCI Cloud Shell** icon to open the Cloud Shell console.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-215" src="https://github.com/user-attachments/assets/d9a43ae5-a46e-453f-a648-29d2c16b3ffa" />

+ Click **Cloud Shell**.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-216" src="https://github.com/user-attachments/assets/16cf2210-9981-44d3-a168-489bba9bf25f" />

Make sure that the Cloud Shell window opens.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-217" src="https://github.com/user-attachments/assets/99d0164c-1fef-4e6d-9f51-bcb54d057224" />

+ Enter 'N' to skip the tutorial for now.

<img width="1515" height="824" alt="Access-Manage-Linux-Instance-218" src="https://github.com/user-attachments/assets/851409ba-9bd6-432b-9631-d12e3e149998" />

In order to connect to the Linux instance using the private IP address, it is important that the Cloud Shell gets access to the same subnet as where the Linux instance is connected to.

We can do this by **plugging** the Cloud Shell into the same VCN and subnet where the Linux instance also resides. By default the network is set to **Public**, but we are going to change this by creating a new private network on the fly.

+ Click **Network** and select **Private network definition list**.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-219" src="https://github.com/user-attachments/assets/d4d7508a-52ab-4d61-b7f5-c96f20b0283b" />

+ Click **Create private network definition**.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-220" src="https://github.com/user-attachments/assets/c85a705f-33b4-44f6-b17d-5c52b18c808b" />

+ In Create private network definition, enter the following information.

1. Enter a Name.
2. Select the corresponding VCN where the Linux instance resides in.
3. Select the Subnet where the Linux instance resides in.
4. Select Use active network to activate the private network right away.
5. Click Create.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-221" src="https://github.com/user-attachments/assets/4f3f962f-c0ee-400e-9ad2-14d573b384ab" />

+ Notice that the status of the network will change to the newly created private network with Connecting. This will take a few seconds to complete.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-222" src="https://github.com/user-attachments/assets/a9d09bef-2102-40da-b452-ae5811541eeb" />

1. Private network is connected.
2. Click Close to close the private network definition list.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-223" src="https://github.com/user-attachments/assets/9774c850-063c-4cee-9030-a20e16f334e1" />

1. Run the `ls-l` command and see that we do not have the private key in the home folder.
2. To upload the private key, click the wheel.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-224" src="https://github.com/user-attachments/assets/eb0002e7-a437-4d6b-801d-f46d920d26df" />

1. Click **Upload**.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-225" src="https://github.com/user-attachments/assets/f5b3bd7a-11ce-42c4-896b-2f8e54c43ad6" />

1. Click **Select from your computer**.
2. Click **Upload**.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-226" src="https://github.com/user-attachments/assets/a24c1ed3-f192-4a18-a398-320b24782d7e" />

1. Select the private key from the local computer.
2. Click Open.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-227" src="https://github.com/user-attachments/assets/a7c7659a-d277-49a9-ae0e-2daff71d0082" />

1. Review the key selected in the previous step.
2. Click Upload.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-228" src="https://github.com/user-attachments/assets/3b5f4ef6-7ef0-4439-9502-f9eddc833c4d" />

1. Make sure the upload is completed.
2. Click Hide.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-229" src="https://github.com/user-attachments/assets/0d42636b-9236-4b56-8adb-636947770af1" />

+ Run the `ls-l` command to check the private key.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-230" src="https://github.com/user-attachments/assets/e71a1534-4141-484b-ab5f-4829e3655c81" />

1. Restrict permissions of the private key and make sure the access is restricted before it can be used.
2. Connect to the instance using the SSH command and specify the private key.
3. Run the following command to verify the IP address.
4. Verify the IP address.
5. Minimize the Cloud Shell console.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-231" src="https://github.com/user-attachments/assets/f07b0e09-d6dd-46b6-b10d-c72ecd4cf024" />

+ Cloud Shell console is minimized. Click **Restore** to restore the Cloud Shell console.

<img width="1514" height="824" alt="Access-Manage-Linux-Instance-232" src="https://github.com/user-attachments/assets/6fc7f196-feca-425a-8191-634f4c8e031f" />

+ Review the restored Cloud Shell console. Click **X** to close the Cloud Shell window.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-233" src="https://github.com/user-attachments/assets/99a3b393-6417-4cd2-b00c-ee6604f85a55" />

+ Click **Exit** to close the Cloud Shell window.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-234" src="https://github.com/user-attachments/assets/b396c9ed-d5c7-4ee6-a18f-c40009261884" />

Now, we are back in the instance overview.

<img width="1512" height="824" alt="Access-Manage-Linux-Instance-235" src="https://github.com/user-attachments/assets/23b39a62-02e5-4036-aefa-efdec6a9fe9d" />

---
