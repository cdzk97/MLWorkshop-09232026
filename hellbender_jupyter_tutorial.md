# Running the ML Workshop on Hellbender with Jupyter Notebook

This guide explains how to launch the workshop Jupyter notebooks on the **Hellbender HPC cluster** using the University of Missouri **OnDemand Remote Resources** interface.

> **Important:** Jupyter Notebook must be launched through the OnDemand Remote Resources system for this workshop. Do not attempt to launch Jupyter directly from the Hellbender login node or from a manually requested compute-node session.

---

## Step 1 — Clone the Workshop Repository onto Hellbender

Before launching Jupyter, make sure the workshop GitHub repository has been cloned into your **Hellbender data directory**.

The repository directory should be named:

```text
MLWorkshop-09232026
```

From your Hellbender terminal, navigate to your data directory and clone the repository if you have not already done so:

```bash
git clone https://github.com/YOUR-USERNAME/MLWorkshop-09232026.git
```

After cloning, verify that the repository exists:

```bash
ls
```

You should see:

```text
MLWorkshop-09232026
```

If you cloned the repository earlier, you can enter the directory and retrieve any updates before the workshop:

```bash
cd MLWorkshop-09232026
git pull
```

---

## Step 2 — Open Hellbender OnDemand

Open an **Incognito/Private browser window**.

Navigate to the University of Missouri OnDemand Remote Resources page:

https://ondemand.rnet.missouri.edu/pun/sys/dashboard

Using an Incognito/Private window is recommended to help avoid authentication conflicts with other University of Missouri accounts or existing browser sessions.

---

## Step 3 — Log In

Log in using your University of Missouri **PawPrint SSO credentials**.

These are the same credentials used to log into Hellbender.

Complete Duo or any other required authentication prompts.

After successfully logging in, you should be taken to the Hellbender OnDemand dashboard.

---

## Step 4 — Request a Jupyter Notebook Session

From the OnDemand dashboard, select the **Jupyter Notebook** application.

Request the following resources for the workshop:

| Setting           | Value                 |
| ----------------- | --------------------- |
| Nodes             | `1`                   |
| CPUs              | `8`                   |
| Partition/Queue   | `General`             |
| Runtime           | `2 hours`             |
| Working Directory | `MLWorkshop-09232026` |

The requested resources should be sufficient for the workshop exercises.

> **Note:** The number of requested CPUs may be adjusted depending on the final workshop notebooks and computational requirements.

### Working Directory

Make sure the **Working Directory** points to the cloned workshop repository:

```text
MLWorkshop-09232026
```

This allows the Jupyter session to open directly in the directory containing the workshop notebooks and supporting files.

After confirming the settings, submit the request.

---

## Step 5 — Launch Jupyter Notebook

After submitting the request, OnDemand will queue the job.

The session may initially show a status such as:

```text
Queued
```

Once Hellbender allocates the requested resources, the status will change to indicate that the session is running.

Open the running session and select the option to **launch Jupyter Notebook**.

Once Jupyter opens, navigate to the workshop notebook for the PyTorch portion of the session.

Open the appropriate `.ipynb` file.

---

## Step 6 — Select the Python 3 Kernel

After opening the PyTorch notebook, make sure the notebook is using the:

```text
Python 3
```

kernel.

If prompted to select a kernel, choose **Python 3**.

If a different kernel is already selected, use the Jupyter kernel menu to change it to **Python 3**.

You are now ready to begin the workshop.

---

# Workshop Workflow

The complete setup process is:

```text
Clone repository onto Hellbender
        ↓
Open OnDemand Remote Resources
        ↓
Log in with PawPrint SSO
        ↓
Launch Jupyter Notebook application
        ↓
Request 1 node / 8 CPUs / General / 2 hours
        ↓
Set working directory to MLWorkshop-09232026
        ↓
Wait for session to start
        ↓
Launch Jupyter Notebook
        ↓
Open the PyTorch notebook
        ↓
Select the Python 3 kernel
        ↓
Begin the workshop
```

---

## Troubleshooting

### The repository does not appear in Jupyter

Make sure the repository was cloned into your Hellbender data directory **before** requesting the Jupyter session.

From a Hellbender terminal, confirm that the directory exists:

```bash
ls
```

You should see:

```text
MLWorkshop-09232026
```

---

### My Jupyter session is still queued

The job is waiting for Hellbender to allocate the requested resources.

Keep the OnDemand page open and wait for the session status to change from **Queued** to **Running**.

---

### Jupyter opened in the wrong directory

Check that the **Working Directory** was set to the location of:

```text
MLWorkshop-09232026
```

when requesting the Jupyter Notebook session.

If necessary, end the session and request a new one using the correct working directory.

---

### I cannot find the Python 3 kernel

Do not continue with a different kernel unless instructed during the workshop.

Let one of the workshop instructors know so that the environment can be checked.

---

## Important Reminder

Do **not** launch Jupyter Notebook directly from the Hellbender login node.

For this workshop, Jupyter Notebook should be launched exclusively through the **Hellbender OnDemand Remote Resources** interface using the procedure described above.
