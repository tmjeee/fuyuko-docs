# Dev - Performing a Release

{% hint style="warning" %}
Outdated information. We have moved to using github actions for doing releases. This page will be updated soon.
{% endhint %}

## Step 1: Perform a FE Docker Release

Run Jenkin's `docker-fuyuko-fe` job

![](../../.gitbook/assets/selection_258.png)

![](../../.gitbook/assets/selection_259.png)

Fill in the `branch` and `docker tag version` and roll the build, typically the `branch` and `docker tag version` will be the same for a release.

## Step 2: Perform a BE Docker Release

Run Jenkin's `docker-fuyuko-be` job.

![](../../.gitbook/assets/selection_260.png)

![](../../.gitbook/assets/selection_261.png)

Fill in the `branch` and `docker tag version` and roll the build, typically the `branch` and `docker tag version` will be the same for a release.

## Step 3: Perform a DB Docker Release

Run Jenkin's `docker-fuyuko-db` job.

![](../../.gitbook/assets/selection_262.png)

![](../../.gitbook/assets/selection_263.png)

Fill in the `branch` and `docker tag version` and roll the build, typically the `branch` and `docker tag version` will be the same for a release.

## Step 4: Perform a Github Release

Run Jenkin's `Github Release` job.

![](../../.gitbook/assets/selection_264.png)

![](../../.gitbook/assets/selection_265.png)

Fill in the `branch`, `version`, `description`, `is draft` and `is prerelease` field and roll the build. Typically `branch` and `version` will be the same for a release. Beta releases will have `is draft` false and `is prerelease` true while a proper release will have both `is draft` and `is prerelease` as false.

## Step 5: Update OW2 Project Page

Update OW2 project page [here](https://projects.ow2.org/view/fuyuko/).

## Step 6: Update Slack \#fuyuko channel with release

Update Slack \#fuyuko channel [here](https://app.slack.com/client/T012LHB2A0M/C013BPQDPNU/details/actions) with release

## Step 7: Merge release branch into master

A manual merge of release branch into master

## Step 8: Create the next release branch from master

Manually create a new release branch from master.

## Step 9: Create new release branch

Create new release branch from master.

## Step 10: Set GitHub default branch to new release branch

Set github default branch to newly created release branch.







