# mlrules-weka-package
Maximum Likelihood Rule Ensembles (MLRules) is a new rule induction algorithm for 
solving classification problems via probability estimation. The ensemble is built 
using boosting, by greedily minimizing the negative loglikelihood which results 
in estimating the class conditional probability distribution. The main advantage 
of decision rules is their simplicity and comprehensibility: they are logical 
statements of the form "if condition then decision", which is probably the easiest 
form of model to interpret. On the other hand, by exploiting a powerful statistical 
technique to induce the rules, the final ensemble has very high prediction accuracy. 

Fork of the original code located here:
http://www.cs.put.poznan.pl/wkotlowski/software-mlrules.html

## Citation

```
@article{DemKotSlo08MLRules,
  author    = {Krzysztof Dembczy\'nski and Wojciech Kot{\l}owski and Roman S{\l}owi\'nski},  
  title     = {Maximum likelihood rule ensembles},
  booktitle = {Proceedings of the 25th International Conference on Machine Learning (ICML 2008)},
  year      = {2008}
}
```

## Changes

* Turned into a Weka package
* Uses a seeded random number generator now (superclass: `weka.classifiers.RandomizableClassifier`)


## Releases

* [2023.7.26](https://github.com/fracpete/mlrules-weka-package/releases/download/v2023.7.26/mlrules-2023.7.26.zip)


## Maven

Use the following dependency in your `pom.xml`:

```xml
    <dependency>
      <groupId>com.github.fracpete</groupId>
      <artifactId>mlrules-weka-package</artifactId>
      <version>2023.7.26</version>
      <type>jar</type>
      <exclusions>
        <exclusion>
          <groupId>nz.ac.waikato.cms.weka</groupId>
          <artifactId>weka-dev</artifactId>
        </exclusion>
      </exclusions>
    </dependency>
```


## How to use packages

For more information on how to install the package, see:

https://waikato.github.io/weka-wiki/packages/manager/


