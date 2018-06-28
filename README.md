# AEM COMPONENT CLI  &middot; [![GitHub release](https://img.shields.io/badge/version-0.1-lightgrey.svg)](https://github.com/jamescollier7/aemcli/blob/master/aemcli.jar)

-----

### About

AEM Component CLI generates clean scaffold/stubs for new AEM Components using an interactive menu or CLI.

###### &nbsp;&nbsp;Old way of starting an AEM Component:
1. Copy/paste an old component
2. Strip out all the unwanted parts
3. Update parts that are required like __name__, __supertype__, __group__, etc.
4. Build and find all the references you missed
5. Debug because you stripped out something important
6. Rip hair out, go back to step #1, and repeat everytime you need a new component...

###### &nbsp;&nbsp;New way using **AEM COMPONENT CLI**:
1. `$ aemcli -p="Geometrixx" -t="My New Component"`
2. Build
3. Rejoice because everything just works and you can actually start development

### Features:
1. Usage/manual
2. Interactive menu (with additional info/prompts to help newer AEM developers)
3. "Prediction" for __name__, __supertype__, __group__, and __category__ based on the provided _project name_ and _component title_.
4. Correctly stitch all the information together to create all the basic makings of an AEM component -- that when built will be ready for development
&nbsp;
&nbsp;
-----
&nbsp;
### Installation:
1. Download the current release of `aemcli.jar`
2. Put the release jar here `/usr/local/aemcli/aemcli.jar`
3. Make sure `/usr/local/bin` is in your environment PATHS by running the command `echo $PATH` (if not there, add it using `export PATH=$PATH:~/usr/local/bin`)
4. Make a new file in `/usr/local/bin` called `aemcli`, and put this bash script in it:

    ```bash
    #!/bin/bash
    java -jar /usr/local/aemcli/aemcli.jar "$@"%
    ```
5. Run `reset` in any open shells and then try, `aemcli -help`
