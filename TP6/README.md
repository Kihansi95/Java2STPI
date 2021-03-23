# TP6 Documentation

INSA Rennes

## Configuration JavaFX for Eclipse

### To check your current **JDK** and **JRE** version:
* check JDK
```bash
# check JDK
javac -version

# check JRE
java -version

# check where they were installed
# Windows:
where javac
# Linux/Mac:
which javac
```

For JDK > 11.0.0, you need to install [JavaFX](https://openjfx.io/openjfx-docs/#install-javafx)

### Download and install JavaFX

1. After downloaded the link above, create new library in Eclipse:

`Eclipse (-> Window) -> Preferences -> Java -> Build Path -> User LIbraries -> New`

2. Include under existing project:

Right click in `Project -> Build path -> User library -> JavaFX15`

### Set up e(fx)eclipse

Browse and install **e(fx)eclipse** from **Eclipse Marketplace**

### Run configuration

If you encounter following error:
`Error: JavaFX runtime components are missing, and are required to run this application`
   
1. Choose `project -> "Run" (Tab) -> Run Configuration`

2. Add this line to VM Options:
```
--module-path /path/to/JavaFX/lib --add-modules=javafx.controls
```

3. Uncheck the following option: `Use the -XstartOnFirstThread argument when launching with SWT`

