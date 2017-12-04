# Operations Logs



Operations logs can be used to exchange information about work procedures or other work-related topics that are not directly related to objects or work orders. This information is related to functional locations. For example, information or instructions can easily be shared among teams working day, evening, and night shifts.



The basic information related to an operations log is the name of the worker creating the log, the date and time the log was created, and the functional location to which the log relates. The sequence for setting up and using operations logs in Enterprise Asset Management is: First you set up the note types to be available on each functional location. Next, you create descriptions, which can also be related to functional locations. Finally, workers can create operations logs in **Operations logs**.





---



### Setup for Operations Logs



There are two setup forms for operations logs, note types and descriptions. Note types may be used to define work teams or other groups of workers to which a note can be created. They could also define different parts of a production site or building. Descriptions could be set up as work shifts or other work teams to which operations logs could be addressed.





#### Create Note Types



1. Click **Enterprise asset management** > **Setup** > **Operations log** > **Note types**.

2. Click **New**.



3. If your company is using only one functional location, you do not need to select a functional location in the **Functional location** field. If you have set up several functional location hierarchies, select the functional location on which you should be able to select the note type.

4. In the **Line number** field, insert a line number indicating the sequence of note types on a functional location.



5. Insert the identification of the note type in the **Note type** field, and the related name in the **Name** field.

6. Select the **Active** check box if the note type should be shown automatically when you create an operations log for the functional location. If you do not select the **Active** check box, it means that the note type is related to the functional location (if you selected one in step 3), but this "inactive" note type will only be shown if the worker creating an operations log manually adds a new note type line in **Operations logs** > the **Notes** FastTab.



7. Click **Save**.



###### NOTE

You can copy a set of note types from one functional location to another by selecting the **Copy** button, selecting the source location in the **From functional location** field, and the destination location in the **To functional location** field. After you have made a copy of the note types, you can edit the **Note type** and **Name** fields, if required.





![Figure 14-01](/Figures/14-01_OperationsLogs_NoteTypes_AX7-01.png)



---



#### Create Descriptions



1. Click **Enterprise asset management** > **Setup** > **Operations log** > **Descriptions**.

2. Click **New**.



3. If your company is using only one functional location, you do not need to select a functional location in the **Functional location** field. If you have set up several functional location hierarchies, select the functional location on which you should be able to select the description.

4. Insert the description in the **Description** field.



5. Click **Save**.



###### NOTE

You can copy a set of operations log descriptions from one functional location to another by selecting the **Copy** button, selecting the source location in the **From functional location** field, and the destination location in the **To functional location** field. After you have made a copy of the descriptions, you can edit the **Description** field, if required.





![Figure 14-02](/Figures/14-02_OperationsLogs_Descriptions_AX7-01.png)





---





### Create an Operations Log



In this section, you will learn how to create an operations log. Also, creating messages for operations logs and search options in operations logs are explained.



1. Click **Enterprise asset management** > **Common** > **Operations logs**.

2. Click **New**, to create a new log.



3. Select your name in the **Worker** field.

4. In the **Functional location** field, select the functional location for which you are creating the operations log.

###### NOTE

If a functional location has been selected as a primary selection for you, that functional location is automatically inserted in the **Functional location** field. You can change that location, if required.



5. In the **Description** field, select the relevant description.

6. Click **OK**.



7. Select the log line in the left-hand side of **Operations logs**. In the **Details** group > **Active requests** and **Active work orders** fields, you will see the number of active requests and active work orders currently related to the functional location. The **New requests** field shows the number of new requests for the functional location, which has been started since the last log entry. The **Ended work orders** field shows the number of work orders for the functional location, which has been ended since the last log entry.

8. If a message is active on the functional location, it is shown on the **Messages** FastTab. Messages can be created by clicking the **Messages** button. Read more about how to create those messages in the sub section below.



9. On the **Notes** FastTab, you create your notes. Click in the **Note** field related to the relevant note type and add your note. You can add notes to all note types displayed in the list.

10. If required, you can add more note lines by clicking the **Add** button on the **Notes** FastTab. Click in the **Note type** field, select the relevant note type, and insert the note in the **Note** field of the note line.

###### NOTE

In the **Note type** field, you may see more note types displayed than are shown on the **Notes** FastTab. That would be the case if you have created note types in **Operations log note types** that are related to the functional location, but you have not selected the **Active** check box for that note type.



11. Click the **Active requests** or **Active work orders** button to see a list of active requests or active work orders related to the functional location.





![Figure 14-03](/Figures/14-03_OperationsLogs_Form_AX7-01.png)



---



#### Create a Message for Operations Logs



You can create messages to be shown on operations logs. The messages can be set up to be active for a specific period, or they can be shown as long as required if no expiration date is inserted.



1. Click **Enterprise asset management** > **Common** > **Operations logs** > **Messages**.

2. Click **New**.



3. In the **Functional location** field, select the functional location related to the message.

4. In the **Valid from** field, select the start date and time for the message to be shown on operations logs created on the selected functional location.



5. In the **Valid to** field, select an end date and time for the message to be shown. You can also leave this field blank, and the message will continue to be shown until you select an expiration date at a later time.

6. Insert the message in the **Message** field.





![Figure 14-04](/Figures/14-04_OperationsLogs_Messages_AX7-01.png)



---



#### Search in Operations Logs



In Dynamics 365 for Finance and Operations there is an Inquiry function, which can be used in many modules to search for information. In **Operations logs**, you can use the Inquiry functionality to search across all operations logs. You can search for text in the notes you have added on the **Notes** FastTab as well as the messages set up on a functional location.



1. In the **Operations logs**, click **Options** tab > **Advanced Filter/Sort**.

2. In the **Inquiry - Operations logs** drop-down, insert your search criteria for the relevant field, for example, you can search on a word or text string in the **Note** field using asterisks. **Example:** Referring to the **Operations logs form** screenshot above, you want to search for all notes referring to note type "Plant 02". In the **Criteria** field for **Note type**, you insert this text string: \*Plant 02\*



3. The asterisks indicate that you search for all the "Plant 02" text combinations that may have text in front or after that text string.

4. Click **OK**. The search results are shown in **Operations logs**.





![Figure 14-05](/Figures/14-05_OperationsLogs_Inquiry_AX7-01.png)



