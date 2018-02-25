* Copy all dependencies to F:/localrepo (this repo will be perfectly for `mvn`) 

`mvn -Poffline dependency:go-offline -Dmaven.repo.local=F:/localrepo`

* Accumulate all dependencies (these dependencies will be sufficient for starting with classpath or in IDEs)

`mvn -Poffline dependency:copy-dependencies`

* generate tasks.pdf

`reveal-md lessons.md --css lessons.css --print`

* start presentation

`reveal-md slides.md --theme theme/andrena.css`
