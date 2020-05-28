# How to Contribute

Following are some suggested steps on how to contribute to the open source project

## Step 1: Clone a copy of the project

Open up [https://github.com/tmjeee/fuyuko](https://github.com/tmjeee/fuyuko) in a browser. At the top right corner click fork.

![](.gitbook/assets/image%20%2816%29.png)

This should create a fork.

![](.gitbook/assets/image%20%2815%29%20%281%29.png)

You should now be able to create a clone from the forked repository. The URL for cloning should be at the top right corner of the forked repositry page.

![](.gitbook/assets/image%20%2818%29.png)

Clone the repository using the following command.

```text
$> git clone https://github.com/tmjee/fuyuko.git
```

Set up the upstream remote url

```text
$> git remote add upstream https://github.com/tmjeee/fuyuko.git
```

This will setup the following source

| Source | Description |
| :--- | :--- |
| Origin | Your forked repository |
| upstream | The original repository where your forked from |

## Step 2: Get it setup

Install and setup the application making sure you can run it locally. See [Front End and Back End installation section](developer-guide/untitled/dev-installation.md) for more information about installation.

This would require knowing the branch you want to work on etc. Typically you would want to do the following initially, assuming you are interested in making contributions to v1.0.0-beta branch :-

### Option 1: Simpler option

```text
$> git checkout --track upstream/v1.0.0-beta -b my-awesome-change    #(1)
```

| Indicator | Description |
| :--- | :--- |
| \(1\) | This will create a branch in local called "my-awesome-change" which will contains the changes from upstream's v1.0.0-beta branch |

### Option  2:

```text
$> git checkout --track origin/v1.0.0-beta            # (1)
$> git pull origin v1.0.0-beta                        # (2)
$> git pull upstream v1.0.0-beta                      # (3)
$> git merge upstream/v1.0.0-beta                     # (4)
$> git checkout -b my-awesome-change                  # (5)
```

| Indicator | Description |
| :--- | :--- |
| \(1\) | Checkout origin v1.0.0-beta branch \(this is the v1.0.0-beta branch from your fork\) |
| \(2\) | Pull and merge in all the changes from v1.0.0-beta branch from your fork into your local. This is to make sure your local have the latest from your fork. |
| \(3\) | Pull and merge in all the changes from upstream v1.0.0-beta. Git now have the latest of upstream v1.0.0-beta. |
| \(4\) | Merge upstream v1.0.0-beta into your local v1.0.0-beta |
| \(5\) | Create a local branch callled "my-awesome-change" or whatever of your preference to make your super changes |

## Step 3: Make the Awesome change\(s\) :-\)

Make the changes you need, preferably using an IDE like [WebStorm](https://www.jetbrains.com/webstorm/). 

After all the changes, you would typically do the following

```text
$> git add ....                                    # (1)
$> git commit -m ".... your commit message ...."   # (2)
$> git push origin my-awesome-change               # (3)
```

| Indicator | Description |
| :--- | :--- |
| \(1\) | Add all your changes |
| \(2\) | Commit your changes with message |
| \(3\) | Push your changes into origin \(your fork\) in a branch called "my-awesome-change" or whatever you have named your branch initially |

## Step 4: Create a pull request

Create a pull request in GitHub

![](.gitbook/assets/image%20%2819%29.png)

![](.gitbook/assets/image%20%2821%29.png)

Click on "New pull request" and then select the source and destination for the pull request.

![](.gitbook/assets/image%20%2820%29.png)

When you are happy with the changes, click on "Create pull request" and you are good to go, off for another changes I would imagine. :-\)

