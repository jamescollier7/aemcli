# AEM COMPONENT CLI 
##### &nbsp;&nbsp;&nbsp;v0.1
-----

### About

AEM Component CLI generates clean scaffold/stubs for new AEM Components using an interactive menu or CLI.

###### &nbsp;&nbsp;Old way of starting an AEM Component:
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1. Copy/paste an old component
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2. Strip out all the unwanted parts
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3. Update parts that are required like __name__, __supertype__, __group__, etc.
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4. Build and find all the references you missed
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5. Debug because you stripped out something important
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;6. Rip hair out, go back to step #1, and repeat everytime you need a new component...

###### &nbsp;&nbsp;New way using **AEM COMPONENT CLI**:
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1. `$ aemcli -p="Geometrixx" -t="My New Component"`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2. Build
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3. Rejoice because everything just works and you can actually start development

### Features:
1. Usage/manual
2. Interactive menu (with additional info/prompts to help newer AEM developers)
3. "Prediction" for __name__, __supertype__, __group__, and __category__ based on the provided _project name_ and _component title_.
4. Correctly stitch all the information together to create all the basic makings of an AEM component -- that when built will be ready for development
&nbsp;
-----
&nbsp;
### Installation:
1. Download the current release of `aemcli.jar`
2. Put the release jar here `/usr/local/aemcli/aemcli.jar`
3. Make sure `/usr/local/bin` is in your environment PATHS by running the command `echo $PATH` (if not there, add it using `export PATH=$PATH:~/usr/local/bin`)
4. Make a new file in `/usr/local/bin` called `aemcli`, and put this bash script in it:

    ```python
    #!/bin/bash
    java -jar /usr/local/aemcli/aemcli.jar "$@"%
    ```
5. Run `reset` in any open shells and then try, `aemcli -help`