# gitlab-ci
This repo is for learning & actually it just for kubernetes executor.

currently:
add .gitlab.ci.yml
```yaml
include:
  project: 'PatrickPan93/gitlab-ci'
  ref: main
  file: 'templates/java-pipeline.yml'

# could customize your build param here or by default as the undermentioned
variables:
  BUILD_SHELL: 'mvn clean package -DskipTests'
  CACHE_DIR: 'target/'
  BUILD_IMAGE: 'maven:3.8.3-jdk-8'

  TEST_SHELL: 'mvn test'
  JUNIT_REPORT_PATH: 'target/surefire-reports/TEST-*.xml'
  TEST_IMAGE: 'maven:3.8.3-jdk-8'
```
