How to make a release
=====================

Preparation
-----------

* Change the artifact ID in `pom.xml` to today's date, e.g.:

  ```
  2023.7.26-SNAPSHOT
  ```

* Update the version, date and URL in `Description.props` to reflect new
  version, e.g.:

  ```
  Version=2023.7.26
  Date=2023-07-26
  PackageURL=https://github.com/fracpete/mlrules-weka-package/releases/download/v2023.7.26/mlrules-2023.7.26.zip
  ```

Weka package
------------

* Commit/push all changes

* Run the following command to generate the package archive for version `2023.7.26`:

  ```
  ant -f build_package.xml -Dpackage=mlrules-2023.7.26 clean make_package
  ```

* Create a release tag on github (v2023.7.26)
* add release notes
* upload package archive from `dist`


Maven
-----

* Run the following command to deploy the artifact:

  ```
  mvn release:clean release:prepare release:perform
  ```

* log into https://oss.sonatype.org and close/release artifacts

* After successful deployment, push the changes out:

  ```
  git push
  ````
