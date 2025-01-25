<!--
Licensed to the Apache Software Foundation (ASF) under one
or more contributor license agreements.  See the NOTICE file
distributed with this work for additional information
regarding copyright ownership.  The ASF licenses this file
to you under the Apache License, Version 2.0 (the
"License"); you may not use this file except in compliance
with the License.  You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing,
software distributed under the License is distributed on an
"AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
KIND, either express or implied.  See the License for the
specific language governing permissions and limitations
under the License.
-->

<head>
<meta name="author" content="Benjamin Bentmann" />
<title>Source Repository</title>
</head>

# Source Repository

Maven projects use [Git](http://git-scm.com/) to manage their source code:

Instructions on Git use can be found in the online book [Pro Git](http://git-scm.com/book/).
Instructions for using the Apache Software Foundation Git repositories are
at [GitBox - ASF Writable Git Services](https://git-wip-us.apache.org).

## Full Maven Sources

As described in the next paragraphs, Maven full source code is dispatched in more than 100 Git repos: Maven core, but
also plugins or components, skins, a few svn2git read-only mirrors...

To check out full Maven source code easily, we provide a simple way using
additional [Google repo](https://android.googlesource.com/tools/repo) tool and an additional Git repository for tool's
manifest:

| Content                                                                                          |                                                    Repository                                                    |                       Mirror                       |
|:-------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------:|:--------------------------------------------------:|
| Apache Maven [full source code](https://github.com/apache/maven-sources/blob/master/default.xml) | [`https://gitbox.apache.org/repos/asf/maven-sources.git`](https://gitbox.apache.org/repos/asf/maven-sources.git) | [GitHub](https://github.com/apache/maven-sources/) |

1. Install a Git client if needed and the [Google repo](https://android.googlesource.com/tools/repo) tool
   (see [manual install instructions](https://android.googlesource.com/tools/repo#install)).
2. Check out a new repo workspace and prepare master branch:

   ```
   repo init -u https://github.com/apache/maven-sources.git
   repo sync
   repo start master --all
   ```
3. In your IDE, import the projects you're interested in from the repo workspace.
   Or directly build with command line the component you want.

## Maven Sources Overview

<p>
   <object type="image/svg+xml" data="maven-sources/site.svg"/>
</p>
<p>
   <object type="image/svg+xml" data="maven-sources/core.svg"/>
</p>
<p>
   <object type="image/svg+xml" data="maven-sources/plugins.svg"/>
</p>
<p>
   <object type="image/svg+xml" data="maven-sources/doxia.svg"/>
</p>
<p>
   <object type="image/svg+xml" data="maven-sources/misc.svg"/>
</p>
<p>
   <object type="image/svg+xml" data="maven-sources/shared.svg"/>
</p>
<p>
   <object type="image/svg+xml" data="maven-sources/plexus.svg"/>
</p>

Each component has its own Jira project or component for issue tracking: see
the [Issue Management report](/issue-management.html) to get a summary.

## Maven Site

The sources for this site are available in a distinct Git repository:

| Content                |                                                 Repository                                                 | Mirror                                          |                            Issues                             |
|:-----------------------|:----------------------------------------------------------------------------------------------------------:|:------------------------------------------------|:-------------------------------------------------------------:|
| [Apache Maven Site](/) | [`https://gitbox.apache.org/repos/asf/maven-site.git`](https://gitbox.apache.org/repos/asf/maven-site.git) | [GitHub](https://github.com/apache/maven-site/) | [GitHub Issues](https://github.com/apache/maven-site/issues/) |

## Maven Core

The Git repository for [Maven](/ref/current/) contains a master branch which is the current development version.
There is also a branch for maven-2.2.X or maven-3.0.x.
In addition, the [integration tests for the Maven core](/core-its/) have their own repository.

| Content                             | Repository                                                                                                                               |                             Mirror                             |                          Issues                          |
|:------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------:|:--------------------------------------------------------:|
| [Apache Maven](/ref/current/)       | [`https://gitbox.apache.org/repos/asf/maven.git`](https://gitbox.apache.org/repos/asf/maven.git)                                         |           [GitHub](https://github.com/apache/maven/)           | [JIRA MNG](https://issues.apache.org/jira/projects/MNG/) |
| [Apache Maven Core ITs](/core-its/) | [`https://gitbox.apache.org/repos/asf/maven-integration-testing.git`](https://gitbox.apache.org/repos/asf/maven-integration-testing.git) | [GitHub](https://github.com/apache/maven-integration-testing/) |                           N/A                            |

## Other Components

The source repositories for the various plugins are in Git, listed in the documentation of the respective plugin,
reachable via the [plugin index](/plugins/index.html).
There are also many shared components and subsystems with their own source repositories, mainly in Git, some in
Subversion.

### Components in Git

The components in Git are shown in the following table.

| Content                                                                                                                             | Repository                                                                                                                             |                            Mirror                             |                                     Issues                                     |
|:------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| [Apache Maven Archetype](/archetype/)                                                                                               | [`https://gitbox.apache.org/repos/asf/maven-archetype.git`](https://gitbox.apache.org/repos/asf/maven-archetype.git)                   |     [GitHub](https://github.com/apache/maven-archetype/)      |     [JIRA MARCHETYPE](https://issues.apache.org/jira/projects/MARCHETYPE/)     |
| [Apache Maven Archetypes](/archetypes/)                                                                                             | [`https://gitbox.apache.org/repos/asf/maven-archetypes.git`](https://gitbox.apache.org/repos/asf/maven-archetypes.git)                 |     [GitHub](https://github.com/apache/maven-archetypes/)     |    [JIRA MARCHETYPES](https://issues.apache.org/jira/projects/MARCHETYPES)     |
| [Apache Maven Artifact Resolver](/resolver/)                                                                                        | [`https://gitbox.apache.org/repos/asf/maven-resolver.git`](https://gitbox.apache.org/repos/asf/maven-resolver.git)                     |      [GitHub](https://github.com/apache/maven-resolver/)      |      [JIRA MRESOLVER](https://issues.apache.org/jira/projects/MRESOLVER/)      |
| [Apache Maven Artifact Resolver Ant Tasks](/resolver-ant-tasks/)                                                                    | [`https://gitbox.apache.org/repos/asf/maven-resolver-ant-tasks.git`](https://gitbox.apache.org/repos/asf/maven-resolver-ant-tasks.git) | [GitHub](https://github.com/apache/maven-resolver-ant-tasks/) |      [JIRA MRESOLVER](https://issues.apache.org/jira/projects/MRESOLVER/)      |
| [Apache Maven Distribution Checking Tool](https://ci-maven.apache.org/job/Maven/job/maven-box/job/maven-dist-tool/job/master/site/) | [`https://gitbox.apache.org/repos/asf/maven-dist-tool.git`](https://gitbox.apache.org/repos/asf/maven-dist-tool.git)                   |     [GitHub](https://github.com/apache/maven-dist-tool/)      |       [GitHub Issues](https://github.com/apache/maven-dist-tool/issues)        |
| [Apache Maven Enforcer](/enforcer/)                                                                                                 | [`https://gitbox.apache.org/repos/asf/maven-enforcer.git`](https://gitbox.apache.org/repos/asf/maven-enforcer.git)                     |      [GitHub](https://github.com/apache/maven-enforcer/)      |      [JIRA MENFORCER](https://issues.apache.org/jira/projects/MENFORCER/)      |
| [Apache Maven JXR](/jxr/)                                                                                                           | [`https://gitbox.apache.org/repos/asf/maven-jxr.git`](https://gitbox.apache.org/repos/asf/maven-jxr.git)                               |        [GitHub](https://github.com/apache/maven-jxr/)         |            [JIRA JXR](https://issues.apache.org/jira/projects/JXR/)            |
| [Apache Maven Indexer](/maven-indexer/)                                                                                             | [`https://gitbox.apache.org/repos/asf/maven-indexer.git`](https://gitbox.apache.org/repos/asf/maven-indexer.git)                       |      [GitHub](https://github.com/apache/maven-indexer/)       |       [JIRA MINDEXER](https://issues.apache.org/jira/projects/MINDEXER/)       |
| [Apache Maven Plugin Testing](/plugin-testing/)                                                                                     | [`https://gitbox.apache.org/repos/asf/maven-plugin-testing.git`](https://gitbox.apache.org/repos/asf/maven-plugin-testing.git)         |   [GitHub](https://github.com/apache/maven-plugin-testing/)   | [JIRA MPLUGINTESTING](https://issues.apache.org/jira/projects/MPLUGINTESTING/) |
| [Apache Maven Plugin Tools](/plugin-tools/)                                                                                         | [`https://gitbox.apache.org/repos/asf/maven-plugin-tools.git`](https://gitbox.apache.org/repos/asf/maven-plugin-tools.git)             |    [GitHub](https://github.com/apache/maven-plugin-tools/)    |        [JIRA MPLUGIN](https://issues.apache.org/jira/projects/MPLUGIN/)        |
| [Apache Maven Release](/maven-release/) (Release api and plugin)                                                                    | [`https://gitbox.apache.org/repos/asf/maven-release.git`](https://gitbox.apache.org/repos/asf/maven-release.git)                       |      [GitHub](https://github.com/apache/maven-release/)       |       [JIRA MRELEASE](https://issues.apache.org/jira/projects/MRELEASE/)       |
| [Apache Maven SCM](/scm/)                                                                                                           | [`https://gitbox.apache.org/repos/asf/maven-scm.git`](https://gitbox.apache.org/repos/asf/maven-scm.git)                               |        [GitHub](https://github.com/apache/maven-scm/)         |            [JIRA SCM](https://issues.apache.org/jira/projects/SCM/)            |
| [Apache Maven Surefire](/surefire/)                                                                                                 | [`https://gitbox.apache.org/repos/asf/maven-surefire.git`](https://gitbox.apache.org/repos/asf/maven-surefire.git)                     |      [GitHub](https://github.com/apache/maven-surefire/)      |       [JIRA SUREFIRE](https://issues.apache.org/jira/projects/SUREFIRE/)       |
| [Apache Maven Wagon](/wagon/)                                                                                                       | [`https://gitbox.apache.org/repos/asf/maven-wagon.git`](https://gitbox.apache.org/repos/asf/maven-wagon.git)                           |       [GitHub](https://github.com/apache/maven-wagon/)        |          [JIRA WAGON](https://issues.apache.org/jira/projects/WAGON/)          |

#### Plugins

| Content                                                                                 | Repository                                                                                                                                               |                                 Mirror                                 |                                 Issues                                  |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| [Apache Maven ACR Plugin](/plugins/maven-acr-plugin/)                                   | [`https://gitbox.apache.org/repos/asf/maven-acr-plugin.git`](https://gitbox.apache.org/repos/asf/maven-acr-plugin.git)                                   |         [GitHub](https://github.com/apache/maven-acr-plugin/)          |        [JIRA MACR](https://issues.apache.org/jira/projects/MACR)        |
| [Apache Maven Ant Plugin](/plugins/maven-ant-plugin/)                                   | [`https://gitbox.apache.org/repos/asf/maven-ant-plugin.git`](https://gitbox.apache.org/repos/asf/maven-ant-plugin.git)                                   |         [GitHub](https://github.com/apache/maven-ant-plugin/)          |        [JIRA MANT](https://issues.apache.org/jira/projects/MANT)        |
| [Apache Maven AntRun Plugin](/plugins/maven-antrun-plugin/)                             | [`https://gitbox.apache.org/repos/asf/maven-antrun-plugin.git`](https://gitbox.apache.org/repos/asf/maven-antrun-plugin.git)                             |        [GitHub](https://github.com/apache/maven-antrun-plugin/)        |     [JIRA MANTRUN](https://issues.apache.org/jira/projects/MANTRUN)     |
| [Apache Maven Assembly Plugin](/plugins/maven-assembly-plugin/)                         | [`https://gitbox.apache.org/repos/asf/maven-assembly-plugin.git`](https://gitbox.apache.org/repos/asf/maven-assembly-plugin.git)                         |       [GitHub](https://github.com/apache/maven-assembly-plugin/)       |   [JIRA MASSEMBLY](https://issues.apache.org/jira/projects/MASSEMBLY)   |
| [Apache Maven Changelog Plugin](/plugins/maven-changelog-plugin/)                       | [`https://gitbox.apache.org/repos/asf/maven-changelog-plugin.git`](https://gitbox.apache.org/repos/asf/maven-changelog-plugin.git)                       |      [GitHub](https://github.com/apache/maven-changelog-plugin/)       |  [JIRA MCHANGELOG](https://issues.apache.org/jira/projects/MCHANGELOG)  |
| [Apache Maven Changes Plugin](/plugins/maven-changes-plugin/)                           | [`https://gitbox.apache.org/repos/asf/maven-changes-plugin.git`](https://gitbox.apache.org/repos/asf/maven-changes-plugin.git)                           |       [GitHub](https://github.com/apache/maven-changes-plugin/)        |   [JIRA MACHANGES](https://issues.apache.org/jira/projects/MACHANGES)   |
| [Apache Maven Checkstyle Plugin](/plugins/maven-checkstyle-plugin/)                     | [`https://gitbox.apache.org/repos/asf/maven-checkstyle-plugin.git`](https://gitbox.apache.org/repos/asf/maven-checkstyle-plugin.git)                     |      [GitHub](https://github.com/apache/maven-checkstyle-plugin/)      | [JIRA MCHECKSTYLE](https://issues.apache.org/jira/projects/MCHECKSTYLE) |
| [Apache Maven Clean Plugin](/plugins/maven-clean-plugin/)                               | [`https://gitbox.apache.org/repos/asf/maven-clean-plugin.git`](https://gitbox.apache.org/repos/asf/maven-clean-plugin.git)                               |        [GitHub](https://github.com/apache/maven-clean-plugin/)         |      [JIRA MCLEAN](https://issues.apache.org/jira/projects/MCLEAN)      |
| [Apache Maven Compiler Plugin](/plugins/maven-compiler-plugin/)                         | [`https://gitbox.apache.org/repos/asf/maven-compiler-plugin.git`](https://gitbox.apache.org/repos/asf/maven-compiler-plugin.git)                         |       [GitHub](https://github.com/apache/maven-compiler-plugin/)       |   [JIRA MCOMPILER](https://issues.apache.org/jira/projects/MCOMPILER)   |
| [Apache Maven Dependency Plugin](/plugins/maven-dependency-plugin/)                     | [`https://gitbox.apache.org/repos/asf/maven-dependency-plugin.git`](https://gitbox.apache.org/repos/asf/maven-dependency-plugin.git)                     |      [GitHub](https://github.com/apache/maven-dependency-plugin/)      |        [JIRA MDEP](https://issues.apache.org/jira/projects/MDEP)        |
| [Apache Maven Deploy Plugin](/plugins/maven-deploy-plugin/)                             | [`https://gitbox.apache.org/repos/asf/maven-deploy-plugin.git`](https://gitbox.apache.org/repos/asf/maven-deploy-plugin.git)                             |        [GitHub](https://github.com/apache/maven-deploy-plugin/)        |     [JIRA MDEPLOY](https://issues.apache.org/jira/projects/MDEPLOY)     |
| [Apache Maven DOAP Plugin](/plugins/maven-doap-plugin/)                                 | [`https://gitbox.apache.org/repos/asf/maven-doap-plugin.git`](https://gitbox.apache.org/repos/asf/maven-doap-plugin.git)                                 |         [GitHub](https://github.com/apache/maven-doap-plugin/)         |       [JIRA MDOAP](https://issues.apache.org/jira/projects/MDOAP)       |
| [Apache Maven EAR Plugin](/plugins/maven-ear-plugin/)                                   | [`https://gitbox.apache.org/repos/asf/maven-ear-plugin.git`](https://gitbox.apache.org/repos/asf/maven-ear-plugin.git)                                   |         [GitHub](https://github.com/apache/maven-ear-plugin/)          |        [JIRA MEAR](https://issues.apache.org/jira/projects/MEAR)        |
| [Apache Maven EJB Plugin](/plugins/maven-ejb-plugin/)                                   | [`https://gitbox.apache.org/repos/asf/maven-ejb-plugin.git`](https://gitbox.apache.org/repos/asf/maven-ejb-plugin.git)                                   |         [GitHub](https://github.com/apache/maven-ejb-plugin/)          |        [JIRA MEJB](https://issues.apache.org/jira/projects/MEJB)        |
| [Apache Maven GPG Plugin](/plugins/maven-gpg-plugin/)                                   | [`https://gitbox.apache.org/repos/asf/maven-gpg-plugin.git`](https://gitbox.apache.org/repos/asf/maven-gpg-plugin.git)                                   |         [GitHub](https://github.com/apache/maven-gpg-plugin/)          |        [JIRA MGPG](https://issues.apache.org/jira/projects/MGPG)        |
| [Apache Maven Help Plugin](/plugins/maven-help-plugin/)                                 | [`https://gitbox.apache.org/repos/asf/maven-help-plugin.git`](https://gitbox.apache.org/repos/asf/maven-help-plugin.git)                                 |         [GitHub](https://github.com/apache/maven-help-plugin/)         |         [JIRA MPH](https://issues.apache.org/jira/projects/MPH)         |
| [Apache Maven Install Plugin](/plugins/maven-install-plugin/)                           | [`https://gitbox.apache.org/repos/asf/maven-install-plugin.git`](https://gitbox.apache.org/repos/asf/maven-install-plugin.git)                           |       [GitHub](https://github.com/apache/maven-install-plugin/)        |    [JIRA MINSTALL](https://issues.apache.org/jira/projects/MINSTALL)    |
| [Apache Maven Invoker Plugin](/plugins/maven-invoker-plugin/)                           | [`https://gitbox.apache.org/repos/asf/maven-invoker-plugin.git`](https://gitbox.apache.org/repos/asf/maven-invoker-plugin.git)                           |       [GitHub](https://github.com/apache/maven-invoker-plugin/)        |    [JIRA MINVOKER](https://issues.apache.org/jira/projects/MINVOKER)    |
| [Apache Maven JAR Plugin](/plugins/maven-jar-plugin/)                                   | [`https://gitbox.apache.org/repos/asf/maven-jar-plugin.git`](https://gitbox.apache.org/repos/asf/maven-jar-plugin.git)                                   |         [GitHub](https://github.com/apache/maven-jar-plugin/)          |        [JIRA MJAR](https://issues.apache.org/jira/projects/MJAR)        |
| [Apache Maven Jarsigner Plugin](/plugins/maven-jarsigner-plugin/)                       | [`https://gitbox.apache.org/repos/asf/maven-jarsigner-plugin.git`](https://gitbox.apache.org/repos/asf/maven-jarsigner-plugin.git)                       |      [GitHub](https://github.com/apache/maven-jarsigner-plugin/)       |  [JIRA MJARSIGNER](https://issues.apache.org/jira/projects/MJARSIGNER)  |
| [Apache Maven Javadoc Plugin](/plugins/maven-javadoc-plugin/)                           | [`https://gitbox.apache.org/repos/asf/maven-javadoc-plugin.git`](https://gitbox.apache.org/repos/asf/maven-javadoc-plugin.git)                           |       [GitHub](https://github.com/apache/maven-javadoc-plugin/)        |    [JIRA MJAVADOC](https://issues.apache.org/jira/projects/MJAVADOC)    |
| [Apache Maven JDepRScan Plugin](/plugins/maven-jdeprscan-plugin/)                       | [`https://gitbox.apache.org/repos/asf/maven-jdeprscan-plugin.git`](https://gitbox.apache.org/repos/asf/maven-jdeprscan-plugin.git)                       |      [GitHub](https://github.com/apache/maven-jdeprscan-plugin/)       |  [JIRA MJDEPRSCAN](https://issues.apache.org/jira/projects/MJDEPRSCAN)  |
| [Apache Maven JDeps Plugin](/plugins/maven-jdeps-plugin/)                               | [`https://gitbox.apache.org/repos/asf/maven-jdeps-plugin.git`](https://gitbox.apache.org/repos/asf/maven-jdeps-plugin.git)                               |        [GitHub](https://github.com/apache/maven-jdeps-plugin/)         |      [JIRA MJDEPS](https://issues.apache.org/jira/projects/MJDEPS)      |
| [Apache Maven JLink Plugin](/plugins/maven-jlink-plugin/)                               | [`https://gitbox.apache.org/repos/asf/maven-jlink-plugin.git`](https://gitbox.apache.org/repos/asf/maven-jlink-plugin.git)                               |        [GitHub](https://github.com/apache/maven-jlink-plugin/)         |      [JIRA MJLINK](https://issues.apache.org/jira/projects/MJLINK)      |
| [Apache Maven JMod Plugin](/plugins/maven-jmod-plugin/)                                 | [`https://gitbox.apache.org/repos/asf/maven-jmod-plugin.git`](https://gitbox.apache.org/repos/asf/maven-jmod-plugin.git)                                 |         [GitHub](https://github.com/apache/maven-jmod-plugin/)         |       [JIRA MJMOD](https://issues.apache.org/jira/projects/MJMOD)       |
| [Apache Maven Linkcheck Plugin](/plugins/maven-linkcheck-plugin/)                       | [`https://gitbox.apache.org/repos/asf/maven-linkcheck-plugin.git`](https://gitbox.apache.org/repos/asf/maven-linkcheck-plugin.git)                       |      [GitHub](https://github.com/apache/maven-linkcheck-plugin/)       |  [JIRA MLINKCHECK](https://issues.apache.org/jira/projects/MLINKCHECK)  |
| [Apache Maven PDF Plugin](/plugins/maven-pdf-plugin/)                                   | [`https://gitbox.apache.org/repos/asf/maven-pdf-plugin.git`](https://gitbox.apache.org/repos/asf/maven-pdf-plugin.git)                                   |         [GitHub](https://github.com/apache/maven-pdf-plugin/)          |        [JIRA MPDF](https://issues.apache.org/jira/projects/MPDF)        |
| [Apache Maven PMD Plugin](/plugins/maven-pmd-plugin/)                                   | [`https://gitbox.apache.org/repos/asf/maven-pmd-plugin.git`](https://gitbox.apache.org/repos/asf/maven-pmd-plugin.git)                                   |         [GitHub](https://github.com/apache/maven-pmd-plugin/)          |        [JIRA MPMD](https://issues.apache.org/jira/projects/MPMD)        |
| [Apache Maven Project Info Reports Plugin](/plugins/maven-project-info-reports-plugin/) | [`https://gitbox.apache.org/repos/asf/maven-project-info-reports-plugin.git`](https://gitbox.apache.org/repos/asf/maven-project-info-reports-plugin.git) | [GitHub](https://github.com/apache/maven-project-info-reports-plugin/) |        [JIRA MPIR](https://issues.apache.org/jira/projects/MPIR)        |
| [Apache Maven RAR Plugin](/plugins/maven-rar-plugin/)                                   | [`https://gitbox.apache.org/repos/asf/maven-rar-plugin.git`](https://gitbox.apache.org/repos/asf/maven-rar-plugin.git)                                   |         [GitHub](https://github.com/apache/maven-rar-plugin/)          |        [JIRA MRAR](https://issues.apache.org/jira/projects/MRAR)        |
| [Apache Maven Remote Resources Plugin](/plugins/maven-remote-resources-plugin/)         | [`https://gitbox.apache.org/repos/asf/maven-remote-resources-plugin.git`](https://gitbox.apache.org/repos/asf/maven-remote-resources-plugin.git)         |   [GitHub](https://github.com/apache/maven-remote-resources-plugin/)   | [JIRA MRRESOURCES](https://issues.apache.org/jira/projects/MRRESOURCES) |
| [Apache Maven Repository Plugin](/plugins/maven-repository-plugin/)                     | [`https://gitbox.apache.org/repos/asf/maven-repository-plugin.git`](https://gitbox.apache.org/repos/asf/maven-repository-plugin.git)                     |      [GitHub](https://github.com/apache/maven-repository-plugin/)      | [JIRA MREPOSITORY](https://issues.apache.org/jira/projects/MREPOSITORY) |
| [Apache Maven Resources Plugin](/plugins/maven-resources-plugin/)                       | [`https://gitbox.apache.org/repos/asf/maven-resources-plugin.git`](https://gitbox.apache.org/repos/asf/maven-resources-plugin.git)                       |      [GitHub](https://github.com/apache/maven-resources-plugin/)       |  [JIRA MRESOURCES](https://issues.apache.org/jira/projects/MRESOURCES)  |
| [Apache Maven SCM Publish Plugin](/plugins/maven-scm-publish-plugin/)                   | [`https://gitbox.apache.org/repos/asf/maven-scm-publish-plugin.git`](https://gitbox.apache.org/repos/asf/maven-scm-publish-plugin.git)                   |     [GitHub](https://github.com/apache/maven-scm-publish-plugin/)      |         [JIRA SCM](https://issues.apache.org/jira/projects/SCM)         |
| [Apache Maven Scripting Plugin](/plugins/maven-scripting-plugin/)                       | [`https://gitbox.apache.org/repos/asf/maven-scripting-plugin.git`](https://gitbox.apache.org/repos/asf/maven-scripting-plugin.git)                       |      [GitHub](https://github.com/apache/maven-scripting-plugin/)       |  [JIRA MSCRIPTING](https://issues.apache.org/jira/projects/MSCRIPTING)  |
| [Apache Maven Shade Plugin](/plugins/maven-shade-plugin/)                               | [`https://gitbox.apache.org/repos/asf/maven-shade-plugin.git`](https://gitbox.apache.org/repos/asf/maven-shade-plugin.git)                               |        [GitHub](https://github.com/apache/maven-shade-plugin/)         |      [JIRA MSHADE](https://issues.apache.org/jira/projects/MSHADE)      |
| [Apache Maven Site Plugin](/plugins/maven-site-plugin/)                                 | [`https://gitbox.apache.org/repos/asf/maven-site-plugin.git`](https://gitbox.apache.org/repos/asf/maven-site-plugin.git)                                 |         [GitHub](https://github.com/apache/maven-site-plugin/)         |       [JIRA MSITE](https://issues.apache.org/jira/projects/MSITE)       |
| [Apache Maven Source Plugin](/plugins/maven-source-plugin/)                             | [`https://gitbox.apache.org/repos/asf/maven-source-plugin.git`](https://gitbox.apache.org/repos/asf/maven-source-plugin.git)                             |        [GitHub](https://github.com/apache/maven-source-plugin/)        |    [JIRA MSOURCES](https://issues.apache.org/jira/projects/MSOURCES)    |
| [Apache Maven Stage Plugin](/plugins/maven-stage-plugin/)                               | [`https://gitbox.apache.org/repos/asf/maven-stage-plugin.git`](https://gitbox.apache.org/repos/asf/maven-stage-plugin.git)                               |        [GitHub](https://github.com/apache/maven-stage-plugin/)         |      [JIRA MSTAGE](https://issues.apache.org/jira/projects/MSTAGE)      |
| [Apache Maven Toolchains Plugin](/plugins/maven-toolchains-plugin/)                     | [`https://gitbox.apache.org/repos/asf/maven-toolchains-plugin.git`](https://gitbox.apache.org/repos/asf/maven-toolchains-plugin.git)                     |      [GitHub](https://github.com/apache/maven-toolchains-plugin/)      | [JIRA MTOOLCHAINS](https://issues.apache.org/jira/projects/MTOOLCHAINS) |
| [Apache Maven Verifier Plugin](/plugins/maven-verifier-plugin/)                         | [`https://gitbox.apache.org/repos/asf/maven-verifier-plugin.git`](https://gitbox.apache.org/repos/asf/maven-verifier-plugin.git)                         |       [GitHub](https://github.com/apache/maven-verifier-plugin/)       |   [JIRA MVERIFIER](https://issues.apache.org/jira/projects/MVERIFIER)   |
| [Apache Maven WAR Plugin](/plugins/maven-war-plugin/)                                   | [`https://gitbox.apache.org/repos/asf/maven-war-plugin.git`](https://gitbox.apache.org/repos/asf/maven-war-plugin.git)                                   |         [GitHub](https://github.com/apache/maven-war-plugin/)          |        [JIRA MWAR](https://issues.apache.org/jira/projects/MWAR)        |

#### Parent POMs

| Content                                              | Repository                                                                                                                         |                           Mirror                            |                                Issues                                 |
|:-----------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------:|
| [Apache Parent POM](/pom/asf/)                       | [`https://gitbox.apache.org/repos/asf/maven-apache-parent.git`](https://gitbox.apache.org/repos/asf/maven-apache-parent.git)       |  [GitHub](https://github.com/apache/maven-apache-parent/)   | [GitHub Issues](https://github.com/apache/maven-apache-parent/issues) |
| [Apache Maven Parent POMs](/pom/maven/)              | [`https://gitbox.apache.org/repos/asf/maven-parent.git`](https://gitbox.apache.org/repos/asf/maven-parent.git)                     |      [GitHub](https://github.com/apache/maven-parent/)      |    [GitHub Issues](https://github.com/apache/maven-parent/issues)     |
| [Apache Resource Bundles](/apache-resource-bundles/) | [`https://gitbox.apache.org/repos/asf/maven-apache-resources.git`](https://gitbox.apache.org/repos/asf/maven-apache-resources.git) | [GitHub](https://github.com/apache/maven-apache-resources/) |    [JIRA MASFRES](https://issues.apache.org/jira/projects/MASFRES)    |

#### Shared Components

| Content                                                                       | Repository                                                                                                                                       |                               Mirror                               |                               Issues                                |
|:------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| [Apache Maven Archiver](/shared/maven-archiver/)                              | [`https://gitbox.apache.org/repos/asf/maven-archiver.git`](https://gitbox.apache.org/repos/asf/maven-archiver.git)                               |        [GitHub](https://github.com/apache/maven-archiver/)         |   [JIRA MSHARED](https://issues.apache.org/jira/projects/MSHARED)   |
| [Apache Maven Artifact Resolver](/shared/maven-artifact-resolver/)            | [`https://gitbox.apache.org/repos/asf/maven-artifact-resolver.git`](https://gitbox.apache.org/repos/asf/maven-artifact-resolver.git)             |    [GitHub](https://github.com/apache/maven-artifact-resolver/)    | [JIRA MRESOLVER](https://issues.apache.org/jira/projects/MRESOLVER) |
| [Apache Maven Artifact Transfer](/shared/maven-artifact-transfer/)            | [`https://gitbox.apache.org/repos/asf/maven-artifact-transfer.git`](https://gitbox.apache.org/repos/asf/maven-artifact-transfer.git)             |    [GitHub](https://github.com/apache/maven-artifact-transfer/)    |   [JIRA MSHARED](https://issues.apache.org/jira/projects/MSHARED)   |
| [Apache MavenCommon Artifact Filters](/shared/maven-common-artifact-filters/) | [`https://gitbox.apache.org/repos/asf/maven-common-artifact-filters.git`](https://gitbox.apache.org/repos/asf/maven-common-artifact-filters.git) | [GitHub](https://github.com/apache/maven-common-artifact-filters/) |   [JIRA MSHARED](https://issues.apache.org/jira/projects/MSHARED)   |
| [Apache Maven Dependency Analyzer](/shared/maven-dependency-analyzer/)        | [`https://gitbox.apache.org/repos/asf/maven-dependency-analyzer.git`](https://gitbox.apache.org/repos/asf/maven-dependency-analyzer.git)         |   [GitHub](https://github.com/apache/maven-dependency-analyzer/)   |   [JIRA MSHARED](https://issues.apache.org/jira/projects/MSHARED)   |
| [Apache Maven Dependency Tree](/shared/maven-dependency-tree/)                | [`https://gitbox.apache.org/repos/asf/maven-dependency-tree.git`](https://gitbox.apache.org/repos/asf/maven-dependency-tree.git)                 |     [GitHub](https://github.com/apache/maven-dependency-tree/)     |   [JIRA MSHARED](https://issues.apache.org/jira/projects/MSHARED)   |
| [Apache Maven Downloader](/shared/maven-downloader/)                          | [`https://gitbox.apache.org/repos/asf/maven-downloader.git`](https://gitbox.apache.org/repos/asf/maven-downloader.git)                           |       [GitHub](https://github.com/apache/maven-downloader/)        |                                 N/A                                 |
| [Apache Maven Filtering](/shared/maven-filtering/)                            | [`https://gitbox.apache.org/repos/asf/maven-filtering.git`](https://gitbox.apache.org/repos/asf/maven-filtering.git)                             |        [GitHub](https://github.com/apache/maven-filtering/)        |   [JIRA MSHARED](https://issues.apache.org/jira/projects/MSHARED)   |
| [Apache Maven Invoker](/shared/maven-invoker/)                                | [`https://gitbox.apache.org/repos/asf/maven-invoker.git`](https://gitbox.apache.org/repos/asf/maven-invoker.git)                                 |         [GitHub](https://github.com/apache/maven-invoker/)         |   [JIRA MSHARED](https://issues.apache.org/jira/projects/MSHARED)   |
| [Apache Maven Jarsigner](/shared/maven-jarsigner/)                            | [`https://gitbox.apache.org/repos/asf/maven-jarsigner.git`](https://gitbox.apache.org/repos/asf/maven-jarsigner.git)                             |        [GitHub](https://github.com/apache/maven-jarsigner/)        |   [JIRA MSHARED](https://issues.apache.org/jira/projects/MSHARED)   |
| [Apache Maven Mapping](/shared/maven-mapping/)                                | [`https://gitbox.apache.org/repos/asf/maven-mapping.git`](https://gitbox.apache.org/repos/asf/maven-mapping.git)                                 |         [GitHub](https://github.com/apache/maven-mapping/)         |   [JIRA MSHARED](https://issues.apache.org/jira/projects/MSHARED)   |
| [Apache Maven OSGi](/shared/maven-osgi/)                                      | [`https://gitbox.apache.org/repos/asf/maven-osgi.git`](https://gitbox.apache.org/repos/asf/maven-osgi.git)                                       |          [GitHub](https://github.com/apache/maven-osgi/)           |                                 N/A                                 |
| [Apache Maven Project Utils](/shared/maven-project-utils/)                    | [`https://gitbox.apache.org/repos/asf/maven-project-utils.git`](https://gitbox.apache.org/repos/asf/maven-project-utils.git)                     |      [GitHub](https://github.com/apache/maven-project-utils/)      |   [JIRA MSHARED](https://issues.apache.org/jira/projects/MSHARED)   |
| [Apache Maven Reporting API](/shared/maven-reporting-api/)                    | [`https://gitbox.apache.org/repos/asf/maven-reporting-api.git`](https://gitbox.apache.org/repos/asf/maven-reporting-api.git)                     |      [GitHub](https://github.com/apache/maven-reporting-api/)      |   [JIRA MSHARED](https://issues.apache.org/jira/projects/MSHARED)   |
| [Apache Maven Reporting Executor](/shared/maven-reporting-exec/)              | [`https://gitbox.apache.org/repos/asf/maven-reporting-exec.git`](https://gitbox.apache.org/repos/asf/maven-reporting-exec.git)                   |     [GitHub](https://github.com/apache/maven-reporting-exec/)      |   [JIRA MSHARED](https://issues.apache.org/jira/projects/MSHARED)   |
| [Apache Maven Reporting Implementation](/shared/maven-reporting-impl/)        | [`https://gitbox.apache.org/repos/asf/maven-reporting-impl.git`](https://gitbox.apache.org/repos/asf/maven-reporting-impl.git)                   |     [GitHub](https://github.com/apache/maven-reporting-impl/)      |   [JIRA MSHARED](https://issues.apache.org/jira/projects/MSHARED)   |
| [Apache Maven Respository Builder](/shared/maven-repository-builder/)         | [`https://gitbox.apache.org/repos/asf/maven-repository-builder.git`](https://gitbox.apache.org/repos/asf/maven-repository-builder.git)           |   [GitHub](https://github.com/apache/maven-repository-builder/)    |                                 N/A                                 |
| [Apache Maven Runtime](/shared/maven-runtime/)                                | [`https://gitbox.apache.org/repos/asf/maven-runtime.git`](https://gitbox.apache.org/repos/asf/maven-runtime.git)                                 |         [GitHub](https://github.com/apache/maven-runtime/)         |                                 N/A                                 |
| [Apache Maven Script Interpreter](/shared/maven-script-interpreter/)          | [`https://gitbox.apache.org/repos/asf/maven-script-interpreter.git`](https://gitbox.apache.org/repos/asf/maven-script-interpreter.git)           |   [GitHub](https://github.com/apache/maven-script-interpreter/)    |   [JIRA MSHARED](https://issues.apache.org/jira/projects/MSHARED)   |
| [Apache Maven Shared Incremental](/shared/maven-shared-incremental/)          | [`https://gitbox.apache.org/repos/asf/maven-shared-incremental.git`](https://gitbox.apache.org/repos/asf/maven-shared-incremental.git)           |   [GitHub](https://github.com/apache/maven-shared-incremental/)    |   [JIRA MSHARED](https://issues.apache.org/jira/projects/MSHARED)   |
| [Apache Maven Shared IO](/shared/maven-shared-io/)                            | [`https://gitbox.apache.org/repos/asf/maven-shared-io.git`](https://gitbox.apache.org/repos/asf/maven-shared-io.git)                             |        [GitHub](https://github.com/apache/maven-shared-io/)        |   [JIRA MSHARED](https://issues.apache.org/jira/projects/MSHARED)   |
| [Apache Maven Shared Jar](/shared/maven-shared-jar/)                          | [`https://gitbox.apache.org/repos/asf/maven-shared-jar.git`](https://gitbox.apache.org/repos/asf/maven-shared-jar.git)                           |       [GitHub](https://github.com/apache/maven-shared-jar/)        |   [JIRA MSHARED](https://issues.apache.org/jira/projects/MSHARED)   |
| [Apache Maven Shared Resources](/shared/maven-shared-resources/)              | [`https://gitbox.apache.org/repos/asf/maven-shared-resources.git`](https://gitbox.apache.org/repos/asf/maven-shared-resources.git)               |    [GitHub](https://github.com/apache/maven-shared-resources/)     |   [JIRA MSHARED](https://issues.apache.org/jira/projects/MSHARED)   |
| [Apache Maven Shared Utils](/shared/maven-shared-utils/)                      | [`https://gitbox.apache.org/repos/asf/maven-shared-utils.git`](https://gitbox.apache.org/repos/asf/maven-shared-utils.git)                       |      [GitHub](https://github.com/apache/maven-shared-utils/)       |   [JIRA MSHARED](https://issues.apache.org/jira/projects/MSHARED)   |
| [Apache Maven Verifier](/shared/maven-verifier/)                              | [`https://gitbox.apache.org/repos/asf/maven-verifier.git`](https://gitbox.apache.org/repos/asf/maven-verifier.git)                               |        [GitHub](https://github.com/apache/maven-verifier/)         |   [JIRA MSHARED](https://issues.apache.org/jira/projects/MSHARED)   |

#### Shared Components

| Content                                                 | Repository                                                                                                                 |                         Mirror                          |                            Issues                             |
|:--------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------:|:-------------------------------------------------------------:|
| [Apache Maven Default Skin](/skins/maven-default-skin/) | [`https://gitbox.apache.org/repos/asf/maven-default-skin.git`](https://gitbox.apache.org/repos/asf/maven-default-skin.git) | [GitHub](https://github.com/apache/maven-default-skin/) | [JIRA MSKINS](https://issues.apache.org/jira/projects/MSKINS) |
| [Apache Maven Fluido Skin](/skins/maven-fluido-skin/)   | [`https://gitbox.apache.org/repos/asf/maven-fluido-skin.git`](https://gitbox.apache.org/repos/asf/maven-fluido-skin.git)   | [GitHub](https://github.com/apache/maven-fluido-skin/)  | [JIRA MSKINS](https://issues.apache.org/jira/projects/MSKINS) |

#### Components in Subversion

Everything in Subversion can be checked-out from a single entry point, referencing each part through svn:externals
[`https://svn.apache.org/repos/asf/maven/trunks/`](https://svn.apache.org/repos/asf/maven/trunks/).

You can also check out every component separately. The components in Subversion are:

| Content                                                                  | Repository                                                                                                    |                       Mirror                       |
|:-------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|:--------------------------------------------------:|
| Maven Project (mainly KEYS)                                              | [`https://svn.apache.org/viewvc/maven/project`](https://svn.apache.org/repos/asf/maven/project/)              |                                                    |
| Maven Sandbox                                                            | [`https://svn.apache.org/viewvc/maven/sandbox/trunk/`](https://svn.apache.org/repos/asf/maven/sandbox/trunk/) | [GitHub](https://github.com/apache/maven-sandbox/) |
| A variety of other subsystems (including obsolete trees replaced by git) | [`https://svn.apache.org/viewvc/maven/`](https://svn.apache.org/repos/asf/maven/)                             |                                                    |
