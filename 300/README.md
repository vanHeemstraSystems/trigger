# 300 - Building Our Application

As soon as you create a new project in cloud.trigger.dev, you will be prompted as below to create a new Next.js project:

Browse to: https://cloud.trigger.dev/orgs/van-heemstra-systems-332b/projects/my-first-project-GfYO

## 100 - Get started in 5 minutes

- Use an existing Next.js project: Use Trigger.dev in an existing Next.js project in less than 2 mins.
- ==> **Create a new Next.js project**: This is the quickest way to try out trigger.dev in a new Next.jsproject and takes 5 mins.

1. Create a new Next.js project

```
$ npx create-next-app@latest
```

Trigger.dev works with either the Pages or App Router configuration.

2. Navigate to your new Next.js project

You have now created a new Next.js project (here we have chosen to name the project ```trigger``` and created it in ```containers/app/``` directory). Let's ```cd``` into it using the project name you just provided:

```
$ cd [replace with your project name]
```

3. Run the CLI 'init' command in your new Next.js project.

```
$ npx @trigger.dev/cli@latest init -k tr_dev_eUBm2f3adw3AuI9RXOes -t https://cloud.trigger.dev
```

**NOTE**: the above hash (tr_dev_eUBm2f3adw3AuI9RXOes) is different for each deploy.

You will be prompted as follows:

```
Need to install the following packages:
@trigger.dev/cli@2.0.10
Ok to proceed? (y) y
                                               
 _____       _                           _           
|_   _| ___ |_| ___  ___  ___  ___     _| | ___  _ _ 
  | |  |  _|| || . || . || -_||  _| _ | . || -_|| | |
  |_|  |_|  |_||_  ||_  ||___||_|  |_||___||___| \_/ 
               |___||___|                            

✨ Initializing project in Trigger.dev Cloud
✅ Detected Next.js project
⚠️ You have uncommitted git changes, you may want to commit them before continuing.
✔ Successfully added dependencies to package.json: @trigger.dev/sdk@2.0.10, @trigger.dev/nextjs@2.0.10
✅ Added TRIGGER_API_KEY=tr_dev_********3adw3AuI9RXOes to .env.local
✅ Added TRIGGER_API_URL=https://cloud.trigger.dev to .env.local
📁 Detected use of src directory
✅ Created app route at src/app/api/trigger.ts
✅ Created trigger client at src/trigger.ts
✅ Created example job at src/jobs/examples/examplesFileName
✅ Wrote trigger.dev config to package.json
✅ Successfully initialized Trigger.dev!
Next steps:
   1. Run your Next.js project locally with 'npm run dev'
   2. In a separate terminal, run 'npx @trigger.dev/cli@latest dev' to watch for changes and automatically register Trigger.dev jobs
   3. View your jobs at https://cloud.trigger.dev/orgs/van-heemstra-systems-332b/projects/my-first-project-GfYO
🔗 Head over to our docs at https://trigger.dev/docs to learn more about how to create different kinds of jobs and add integrations.
```

You'll notice a new folder in your project called 'jobs'. We've added a very simple example Job in ```examples.ts``` to help you get started.

4. Run your Next.js app

```
$ npm run dev
```

5. Run the CLI 'dev' command

In a **separate terminal window or tab** run:

```
$ npx @trigger.dev/cli@latest dev
```

If you’re not running on port 3000 you can specify the port by adding ```--port 3001`````` to the end.

You should leave the ```dev`````` command running when you're developing.

You will be prompted as follows:

```
✔️ [trigger.dev] Detected TriggerClient id: my-first-project-GfYO
✔️ [trigger.dev] Found API Key in .env.local file
  [trigger.dev] Looking for Next.js site on port 3000
✔ 🚇 Created tunnel: https://0ed5-35-205-9-163.ngrok.io
✔ [trigger.dev] 🔄 Refreshed my-first-project-GfYO 9:09:55 AM
```

In a preview or browser window you may get the following message:

```
Rejected host "4040-vanheemstrasyst-trigger-yuvini30hnk.ws-eu104.gitpod.io".

If this request should be permitted, please add "4040-vanheemstrasyst-trigger-yuvini30hnk.ws-eu104.gitpod.io" to the "web_allow_hosts" option in your configuration file.
```

This is something to do in your web server. In the meantime you should be able to see your jobs at https://cloud.trigger.dev/orgs/van-heemstra-systems-332b/projects/my-first-project-GfYO

6. Your Job is ready to run! Click it to run it now.

Example Job: a joke with a delay

Click on the above job as listed on https://cloud.trigger.dev/orgs/van-heemstra-systems-332b/projects/my-first-project-GfYO

It will open a window for this particular job.

7. How to run your Job

**Note**: Scheduled Triggers **do not** trigger Jobs in the DEV Environment. When developing locally you should use the [Test feature](https://cloud.trigger.dev/orgs/van-heemstra-systems-332b/projects/my-first-project-GfYO/jobs/example-job/test) to trigger any scheduled Jobs.

There are two ways to run your Job:

- 1. Trigger a test Run: You can perform a Run with any payload you want, or use one of our examples, on the test page. [Test](https://cloud.trigger.dev/orgs/van-heemstra-systems-332b/projects/my-first-project-GfYO/jobs/example-job/test)


- 2. Trigger your Job for real: Performing a real run depends on the type of trigger your Job is using. [How to run a Job](https://trigger.dev/docs/documentation/guides/running-jobs).


When having clicked on [Test](https://cloud.trigger.dev/orgs/van-heemstra-systems-332b/projects/my-first-project-GfYO/jobs/example-job/test) it will bring you to the tab "Test", to follow these steps:

- How to run a test

-- 1. Select an environment: Select the environment you'd like the test to run against. Let's pick "DEV" for now.

-- 2. Write your test payload: Write your own payload specific to your Job. Some Triggers also provide example payloads that you can select from. This will populate the code editor. **Note** In our case there is no payload, so continue to step 3 below.

-- 3. Run your test: When you're happy with the payload, click Run test. [Learn more about running tests.](https://trigger.dev/docs/documentation/guides/testing-jobs)

When having clicked on Run Test you will see the page specific to this run, e.g. https://cloud.trigger.dev/orgs/van-heemstra-systems-332b/projects/my-first-project-GfYO/jobs/example-job/runs/cllnjbjrl0i6plp37pph8qt4z/trigger

You have the option to rerun the job by clicking ```Rerun Job```.