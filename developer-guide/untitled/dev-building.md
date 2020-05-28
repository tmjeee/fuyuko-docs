# Dev - Building and Running

## Checking out the source from Github

```text
$> git clone https://github.com/tmjeee/fuyuko.git
```

## Directory Structure

```text
+ <root>/
   + fe/
      +-          ... content of front end code ...
   + be/
      +-          ... content of back end code ...
   + LICENSE      ... License ...
   + README.md    ... Readme file ...
```

## To build and run the Front End

Assuming we are in `fe/` directory

### Build 

```text
$> npm install   
$> npx ng build --prod
```

### Run

```text
$> npx ng serve  
```

## To build and run the Back End

Assuming we are in `be/` directory

### Build

```text
$> npm install
$> npm run build
```

### Run

```text
$> npm run exec
```



