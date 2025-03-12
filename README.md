This is an example project for custom rules using kantra

## Steps to reproduce

### Installation
1. Download kantra [here](https://github.com/konveyor/kantra/releases)
2. Extract the archive

3. Rename Kantra cli and move it to PATH. 
```bash
 mv darwin-kantra kantra
```

4. Add all the files from the extracted folder into `.kantra` 
```bash
 cd kantra.darwin.arm64/
 mv $HOME/bin/kantra .

```
5. run the analysis (e.g. in ssti dir)
```bash
kantra analyze --input=tests/data/ssti-test-project --output=output --overwrite  --target openjdk17
 --rules rules
```

Now you can open the report from Kantra into the browser e.g. 
file:///somepath/demo-custom-rules/security/output/static-report/index.html#/issues/applications

![output](images/kantra-output-ssti.jpeg)