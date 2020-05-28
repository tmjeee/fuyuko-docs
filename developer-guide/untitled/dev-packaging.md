# Dev - Packaging

To build a package of the software \(zip bundle\), assuming you are in the root/ directory of the source code, run the following :

```text
$> ./build-package.sh
```

{% hint style="info" %}
If build-package.sh is not executable, you might need to run the following, to allow it to be executable.

```text
$> sudo chmod +x ./build-package.sh
```
{% endhint %}

The result will be a a zip file in the format of `fuyuko-<version>.zip`.

