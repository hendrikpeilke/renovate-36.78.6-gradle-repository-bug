This repository demonstrates a bug for renovate docker image, version 36.78.6.
To reproduce, scan this repository in debug mode 
(onboarding is ok, so no renovate config is needed).
In the log output you can see, that renovate tries to search for
`com.some:dependency-in-not-working-repository` inside `https://some.working.repository.com`
but not inside `https://some.not.working.repository.com/`.
Gradle would interpret that correctly.

This is only a minimal example to show a renovate bug, 
it is not a valid gradle project.