### Frequently Asked Questions

Please take a look at this page before directly contacting us. Most questions are already covered here:

<details > 
    <summary>
        Could we observe real time utilization of sybil to gain an intuitive understanding to assist during discussions with hospital IT?
    </summary>
    <br>
    We would be happy to provide a screen capture of using Sybil on an iMac at our lab.
    <br>
    <br>
</details>

<details > 
    <summary>
        What security events are logged for access and for data modifications? Can this information be provided in an audit trail report?
    </summary>
    <br>
    No events were logged when we used Sybil in our lab. This could be implemented via a script, for example in Python.
    <br>
    <br>
</details>

<details > 
    <summary>
        Do you have a network diagram showing the software/hardware components, architecture, and communication and data flow?  
    </summary>
    <br>
    All steps are performed on the machine where Sybil is installed. A more detailed description can be found in the guide we shared previously.
    <br>
    <br>
</details>

<details > 
    <summary>
        Does the software or data need to be backed up or retained for compliance?  
    </summary>
    <br>
    We did not create any back ups when using Sybil at our lab. From our side, no backups or logging are required.
    <br>
    <br>
</details>

<details > 
    <summary>
        How are users’ access permissions assigned and controlled? (Is users’ access to the software role-based.)
    </summary>
    <br>
    Sybil is installed within Docker as a regular application on the machine, therefore each user on the device can access Docker and Sybil.
    <br>
    <br>
</details>

<details > 
    <summary>
        What type of authentication is used for users’ access to the software? (Active directory, application credentials, local user, none, other?)
    </summary>
    <br>
    No authentication was required when we used Sybil at our lab, but this could be implemented.
    <br>
    <br>
</details>

<details > 
    <summary>
        Is any data stored locally on the users’ devices?
    </summary>
    <br>
    Yes, the data analyzed by Sybil and the output are stored on the device where Sybil is installed.
    <br>
    <br>
</details>

<details > 
    <summary>
        Is any data stored or processed outside of Hospital networks?
    </summary>
    <br>
    No data is sent outside the device where Sybil is installed.
    <br>
    <br>
</details>

<details > 
    <summary>
        How is the software patched/updated for vulnerabilities?
    </summary>
    <br>
    Sybil was developed and updated as needed by Dr. Barzilay’s group at MIT.
    <br>
    <br>
</details>

<details > 
    <summary>
        Does the software: process(send/receive), store, access, or display ePHI (patient data) or other data subject to regulation?  
    </summary>
    <br>
    In our lab, we used Sybil to process CT scans containing patient data. It should also be possible to run Sybil on anonymized CT scans from which patient data was removed.
    <br>
    <br>
</details>

<details > 
    <summary>
        If the software does not store patient data, how would we link each data set (CT scan and sybil out)?
    </summary>
    <br>
        If running Sybil on anonymized CT scans, one option would be to replace the accession number with another unique identifier. This could be implemented via a script.
    <br>
    <br>
</details>
