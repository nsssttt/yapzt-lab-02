# Lab 02 - Static Analysis and Test Coverage

Run the tests and generate the coverage report consumed by SonarQube.

```sh
python -m pip install coverage radon
python -m coverage run --source=src -m unittest discover -s tests -v
python -m coverage xml
radon cc src -s
radon mi src -s
cloc src tests
```

Run SonarScanner against your own SonarQube server using `sonar-project.properties` and a token supplied through `SONAR_TOKEN`.
