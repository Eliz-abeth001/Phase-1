# IT-001 - Computer Running Slowly

1. Identify the Problem

An employee reports that their computer is running slowly when using Teams, Outlook, and a web browser.

2. Establish a Theory of Probable Cause

Possible causes include high memory usage, too many applications or background processes running, high CPU or disk utilisation, or a network-related problem affecting Teams.

3. Test the Theory to Determine the Cause

I would use Task Manager to inspect CPU, memory, disk, and network utilisation. I would also inspect the Processes tab to identify applications and processes consuming significant resources.

The initial investigation showed memory utilisation at approximately 95%. Teams and the browser were using significant amounts of memory, along with other background processes.

I would close unnecessary applications and then recheck resource utilisation. If memory usage decreases but Teams remains slow, I would investigate Teams and the network connection separately.

4. Establish a Plan of Action and Implement the Solution

I would close unnecessary applications that the employee does not currently need and retest the system. If Teams continued to perform poorly, I would investigate the Teams application and check its resource usage. I would also verify that the network connection was functioning normally.

5. Verify Full System Functionality and Implement Preventive Measures

I would reopen and test Teams, Outlook, and the browser and check Task Manager again to confirm that resource utilisation has improved.

Preventive measures could include keeping applications updated, closing unnecessary applications, and monitoring resource usage when performance problems occur.

6. Document Findings, Actions, and Outcomes

The investigation found that memory utilisation was initially high at approximately 95%. After unnecessary applications were closed, memory utilisation decreased to approximately 72%. Teams remained slow, while the network connection was functioning normally and Teams was showing unusually high CPU usage.

The findings directed the investigation toward the Teams application rather than immediately concluding that the workstation required additional hardware.

## 002 - C: Drive Almost Full

1. Identify the Problem

An employee reports that the C: drive is almost full and Windows is displaying low-storage warnings. I would inspect the C: drive to determine its total capacity and the amount of free space remaining.

2. Establish a Theory of Probable Cause

Possible causes include large or unnecessary files, temporary files, installed applications, downloads, Recycle Bin contents, or Windows update files occupying significant storage space.

3. Test the Theory to Determine the Cause

I would use Windows Settings >System > Storage to examine how the storage space is being used. This provides a breakdown of the storage into categories such as temporary files, applications, documents, and other data.

For example, if temporary files were found to be using a significant amount of storage, I would inspect the available temporary files to determine which ones could safely be removed.

4. Establish a Plan of Action and Implement the Solution

I would review the temporary files and remove only unnecessary files that are safe to delete. This would free up storage space without unnecessarily removing important user data or system files.

5. Verify Full System Functionality and Implement Preventive Measures

After removing the unnecessary files, I would check the C: drive again to confirm that the available storage has increased and that the low-storage warning has been resolved.

Preventive measures could include regularly reviewing storage usage, removing unnecessary temporary files, and monitoring the drive before it becomes critically full.

6. Document Findings, Actions, and Outcomes

I would document the original available storage, the files or categories responsible for the storage shortage, the action taken, the amount of storage recovered, and whether the low-storage problem was resolved.

## T-003 - USB Storage Not Appearing in File Explorer

1. Identify the Problem

An employee reports that a USB storage device is connected to the computer but does not appear in File Explorer.

I would first check whether Windows detects the USB device by inspecting Device Manager.

2. Establish a Theory of Probable Cause

If Device Manager detects the USB device without an error, possible causes include the USB not having a drive letter assigned, a partition issue, or a filesystem issue.

3. Test the Theory to Determine the Cause

I would open Disk Management and inspect the USB storage device.

If the USB is detected but does not have a drive letter, this could explain why it is not appearing normally in File Explorer.

4. Establish a Plan of Action and Implement the Solution

I would assign an available drive letter to the USB storage device using Disk Management.

5. Verify Full System Functionality and Implement Preventive Measures

I would open File Explorer and check This PC to confirm that the USB storage device now appears and can be accessed.

If the USB is visible and accessible, the solution has been successful.

6. Document Findings, Actions, and Outcomes

I would document that the USB device was detected by Windows but did not have a drive letter assigned. I would record the drive letter that was assigned and confirm whether the USB became accessible through File Explorer afterward.

## T-004 - Laptop Overheating and Unexpected Shutdown

Issue:
The laptop becomes unusually hot and sometimes shuts itself down.

- Identify the Problem

I would confirm when the overheating and shutdown occur then check whether the issue happens during normal use, when running demanding applications, or after the laptop has been running for a long time.

- Establish a Theory of Probable Cause

Hardware causes:

* Dust or blocked ventilation.
* Faulty cooling fan.
* Poor heat dissipation or degraded thermal paste.
* Battery or power-related hardware problems.

Software causes:

* High CPU usage from applications or background processes.
* Malware or unwanted software.
* Outdated drivers or Windows updates.

- Test the Theory

* Check Task Manager for high CPU, memory, or disk usage.
* Inspect the vents and listen for unusual fan behaviour.
* Run a Windows Security scan.
* Check Windows Update and device drivers.
* Check Event Viewer for errors around the time of the shutdown.

 - Establish a Plan of Action

If software is causing excessive resource usage, close or remove unnecessary applications and update the system. If overheating appears to be hardware-related, clean the vents and check the cooling fan and thermal system.

- Implement the Solution

Clean blocked ventilation areas, ensure the cooling fan is working, update Windows and drivers, remove unnecessary background processes, and perform a security scan. If the problem continues, escalate the laptop for hardware inspection.

-  Verify Full System Functionality and Apply Preventive Measures

Monitor the laptop’s temperature and performance after the fix. Confirm that it no longer overheats or shuts down unexpectedly. Keep ventilation clear, maintain regular system updates, perform security scans, and avoid running unnecessary resource-intensive applications.

- Conclusion:

Both hardware and software causes should be investigated because overheating can result from poor cooling, excessive system resource usage, malware, or driver and system issues.

## IT-005 - Computer Powers On but Windows Won't Boot

### Logical Troubleshooting Tree

```
flowchart TD
    A[Computer powers on but Windows won't boot] --> B{Correct boot device selected?}

    B -->|No| C[Correct boot order]
    B -->|Yes| D[Check RAM]

    D --> E{RAM okay?}
    E -->|No| F[Test or replace RAM]
    E -->|Yes| G{Is Windows drive detected?}

    G -->|No| H[Restart and check BIOS/UEFI]
    G -->|Yes| I[Check BIOS/UEFI boot settings]

    H --> J{Drive detected in BIOS/UEFI?}
    J -->|No| K[Investigate drive or connection]
    J -->|Yes| I

    I --> L{Boot settings correct?}
    L -->|No| M[Correct boot settings and restart]
    L -->|Yes| N{Does an error message appear?}

    N -->|Yes| O[Identify error and investigate its cause]
    O --> P[Apply appropriate solution]
    P --> Q[Restart and verify Windows boots]

    N -->|No| R[Try Windows Recovery Environment]
    R --> S{Recovery works?}
    S -->|Yes| T[Use recovery tools to troubleshoot Windows]
    S -->|No| U[Investigate deeper hardware or boot issues]

    C --> Q
    F --> Q
    M --> Q
    T --> Q
    ```



Computer powers on but Windows won't boot
                  │
                  ▼
     Is the correct boot device selected?
             /              \
           No                Yes
           │                  │
     Correct boot             ▼
       order             Check RAM
                            │
                       ┌────┴────┐
                     Faulty      OK
                       │          │
                  Test/replace    ▼
                    RAM       Is the Windows
                              drive detected?
                              /          \
                            No            Yes
                            │              │
                     Restart and       Check BIOS/
                     check BIOS/UEFI   UEFI settings
                            │              │
                            ▼         ┌────┴────┐
                     Is the drive    Incorrect  Correct
                     detected?          │         │
                        / \         Correct       ▼
                      No   Yes      settings   Does an error
                      │     │          │       message appear?
                 Investigate  Continue  │       /          \
                 drive/connection      restart  Yes          No
                                               │              │
                                        Identify error    Try Windows
                                        and investigate   Recovery
                                        its cause         Environment
                                               │              │
                                               ▼         ┌────┴────┐
                                         Apply fix     Recovery   Recovery
                                               │         works    fails
                                               ▼           │         │
                                           Restart       Use       Investigate
                                           and verify   recovery   deeper
                                           Windows      tools      hardware/
                                           boots                    boot issues


1. Identify the Problem

The employee reports that the computer powers on, but Windows does not boot successfully.

I would determine where the boot process stops by checking the boot device, memory, storage detection, BIOS/UEFI settings, and the Windows boot process.

2. Establish a Theory of Probable Cause

Possible causes include an incorrect boot device, faulty or improperly detected RAM, a storage drive problem, incorrect BIOS/UEFI boot settings, corrupted Windows boot files, or another Windows operating-system problem.

3. Test the Theory to Determine the Cause

I would first verify that the computer is configured to boot from the correct device. I would then check the RAM and confirm that the storage drive containing Windows is detected.

If the drive is not detected, I would restart the computer and check BIOS/UEFI to determine whether the drive is recognized there.

If the drive is detected, I would check the BIOS/UEFI boot settings. If these settings are correct but Windows still does not boot, I would check whether an error message or Windows Recovery Environment appears.

If an error message appears, I would identify what the error means and investigate its probable cause rather than assuming the cause.

4. Establish a Plan of Action and Implement the Solution

The solution would depend on the results of the investigation. I would correct an incorrect boot configuration, address a RAM problem, investigate a storage or connection problem, or use appropriate Windows recovery tools if the problem is related to the Windows boot process.

5. Verify Full System Functionality and Implement Preventive Measures

After implementing the solution, I would restart the computer and verify that Windows starts successfully and that the system functions normally.

Preventive measures could include maintaining Windows, monitoring storage health, avoiding unnecessary changes to BIOS/UEFI settings, and documenting hardware or software changes.

6. Document Findings, Actions, and Outcomes

I would document the symptoms reported by the employee, the troubleshooting checks performed, the evidence found at each stage, the identified cause, the solution implemented, and the final outcome.

I would also record whether Windows successfully booted after the solution was applied.