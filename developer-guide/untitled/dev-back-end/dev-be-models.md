# Dev - BE - models

## Import

### Common models

{% hint style="warning" %}
Do not change **back-end's** `src/model` directory it is being gitignored, change it in **front-end's** `src/model/` directory instead and run **`npm run copy`** in back-end to update it.
{% endhint %}

Common model classes, used by both front-end and back-end, are located in src/model, typically imported as follows :

```text
import { ... } from '<path-to>/src/model';
```

The directory src/model is being gitignored in back-end code. The source of truth is located in front-end src/model directory. Modification should be done in front-end's src/model directory. Running the following will copy and replace the back-end src/model.

```text
$> npm run copy
```

### Server side models

Server side classes, used by back-end only, are located in src/server-side-model, typically imported as follows :

```text
import { ... } from '<path-to>/src/server-side-mode';
```



