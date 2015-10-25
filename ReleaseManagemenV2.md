# Releasing TextBE V2 #

  * [All development happens on mainline](http://svnbook.red-bean.com/en/1.7/svn.branchmerge.commonpatterns.html). There is no branching except for releases
  * The svn has a multi-project structure
  * There is a /p2 directory that contains the P2 repos

  1. Create a branch of the module with the Release number (RN). This number is the version number of the parent POM.
    1. For feature builds, this will determine the version number of the repository
    1. For product builds, this will determine the version number of the repository and product
  1. [Lock](http://svnbook.red-bean.com/en/1.7/svn.ref.svn.c.lock.html) the main line
  1. Set the new version on the main line. The version numbering follows the even odd winding rule, due to the -SNAPSHOT inconsistency between MAVEN/TYCHO and OSGI. _Note: This should be revised for Tycho/Reproducible Version Qualifiers_
    1. Release versions are even
    1. Working versions are odd-SNAPSHOT (tycho) / odd.qualifier (osgi)
    1. **Either** Use the interactive [Tycho Set Version](http://www.eclipse.org/tycho/sitedocs/tycho-release/tycho-versions-plugin/set-version-mojo.html) Mojo to set the version from the parent project for all children,
    1. **or** Set the OSGI versions by hand, then use the interactive [Tycho Update POM](http://www.eclipse.org/tycho/sitedocs/tycho-release/tycho-versions-plugin/update-pom-mojo.html) Mojo to make the POM version match the OSGI version.
  1. Unlock the main line
  1. Switch to the branch
  1. Set the version number on
    1. plugins (major, minor, micro)
    1. Even versions for release, odd versions for snapshot/build qualifier
    1. Features versions compute as upper limit of contained plugin versions
    1. maven build
      1. maven parent pom version is the release version
      1. repository version is identical to the parent pom version
      1. other versions are independent
  1. builds should use -Dtycho.localArtifacts=ignore to ensure insulation
  1. Run the build, verify results by testing (staging ok)
  1. Check-in the branch.
  1. Clean and check out again.
  1. tag the build (move branch from branches to tags)
  1. Check the repository created into P2/RN