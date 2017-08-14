
# Change logs for Rudder 4.2.\* versions

Rudder 4.2 is currently the developement version of Rudder.
You can test it using development builds, but not use it in production.

**Main new features in Rudder 4.2:**

**Installing, upgrading and testing**

  - Install docs:
    https://www.rudder-project.org/doc-4.2/_install_rudder_server.html
  - Upgrade docs:
    https://www.rudder-project.org/doc-4.2/_upgrade_rudder.html
  - Download links: https://www.rudder-project.org/site/get-rudder/downloads/

We also recommend using the [Rudder
Vagrant](https://github.com/Normation/rudder-vagrant) config if you want
a quick and easy way to get an installation for testing.

**Operating systems supported**

This version provides packages for these operating systems:

  - Rudder server and Rudder relay: **Debian 7, Debian 8, RHEL/CentOS 6, RHEL/CentOS 7
    (64 bits), SLES 11, SLES 12, Ubuntu 14.04, Ubuntu 16.04**
  - Rudder agent: all of the above plus **Debian 5, Debian 6,
    RHEL/CentOS 3, RHEL/CentOS 5, CentOS 7 (32 bits), Fedora 18, SLES
    10, SLES 12, Ubuntu 10.04, Ubuntu 12.04, Ubuntu 12.10**
  - Rudder agent (binary packages available from
    ([Normation](http://www.normation.com)): **Windows Server 2008R2-2016,
    AIX 5-6-7**

## <a name="4.2.0.beta3" > </a> Rudder 4.2.0.beta3 (2017-08-08)

### Changes

#### Architecture - Internal libs

  - Upgrade to Scala 2.12.3 to improve compilation time
    ([\#11192](https://www.rudder-project.org/redmine/issues/11192))

#### Documentation

  - Update screenshot for interface usage page 
    ([\#11143](https://www.rudder-project.org/redmine/issues/11143))
  - Adapt run schedule documentation and add screenshots
    ([\#11139](https://www.rudder-project.org/redmine/issues/11139))
  - Add diagram and screenshots in documentation
    ([\#11137](https://www.rudder-project.org/redmine/issues/11137))
  - Compliance logfile parsing regex
    ([\#11107](https://www.rudder-project.org/redmine/issues/11107))
  - Warn on risk of updating file format
    ([\#11155](https://www.rudder-project.org/redmine/issues/11155))

#### Miscellaneous

  - filetemplate technique posthook
    ([\#11142](https://www.rudder-project.org/redmine/issues/11142))

#### Techniques

  - Create a file template technique
    ([\#9078](https://www.rudder-project.org/redmine/issues/9078))

### Bug fixes

#### Web - Nodes & inventories

  - Fixed: Add a post-node-acceptance hook
    ([\#11191](https://www.rudder-project.org/redmine/issues/11191))
  - Fixed: When we manage a Windows 2016, we don't have the proper Windows version displayed
    ([\#11172](https://www.rudder-project.org/redmine/issues/11172))

#### Web - Config management

  - Fixed: Typo in unauthorized acces message
    ([\#11182](https://www.rudder-project.org/redmine/issues/11182))
  - Fixed: Cannot add a directive with a " in its name in Rule
    ([\#10754](https://www.rudder-project.org/redmine/issues/10754))

#### Documentation

  - Fixed: Typo in rudder-setup usage in documentation
    ([\#11136](https://www.rudder-project.org/redmine/issues/11136))
  - Fixed: Wrong doc for restore of Rudder ldap on 4.1
    ([\#11127](https://www.rudder-project.org/redmine/issues/11127))

#### Miscellaneous

  - Fixed: Error when trying to remove a node
    ([\#11171](https://www.rudder-project.org/redmine/issues/11171))
  - Fixed: Unrecognized Windows agent version in webapp
    ([\#11186](https://www.rudder-project.org/redmine/issues/11186))

#### Packaging

  - Fixed: /var/rudder/share is not readable by rudder-policy-reader
    ([\#11176](https://www.rudder-project.org/redmine/issues/11176))

#### Initial promises & sys tech

  - Fixed: Check permissions on /var/rudder files, particularly modified-files
    ([\#11110](https://www.rudder-project.org/redmine/issues/11110))
  - Fixed: Wrong stderr / stdout redirection of logs from rudder agent check in 4.1
    ([\#11044](https://www.rudder-project.org/redmine/issues/11044))

#### Security

  - Fixed: JSESSION cookie should be "secure"
    ([\#11159](https://www.rudder-project.org/redmine/issues/11159))

#### Techniques

  - Fixed: No new line between two certificates in ca.cert, breaking apache when there is more than one node with a certificate
    ([\#11151](https://www.rudder-project.org/redmine/issues/11151))


## Rudder 4.2.0.beta2 (2017-07-12)

### Changes

#### System integration

  - Use uuid to authenticate windows agents
    ([\#11033](https://www.rudder-project.org/redmine/issues/11033))

#### Architecture - Refactoring

  - Move out dsc code into the plugin part
    ([\#11072](https://www.rudder-project.org/redmine/issues/11072))

#### Web - Compliance & node report

  - We are identifying agent runs based on hasPolicyServer-*, which is inefficient, and invalid
    ([\#11027](https://www.rudder-project.org/redmine/issues/11027))

### Bug fixes

#### Web - UI & UX

  - Fixed: In Directive details, tags input is broken on Iceweasel
    ([\#11118](https://www.rudder-project.org/redmine/issues/11118))
  - Fixed: Wrong XML identation in event log
    ([\#10951](https://www.rudder-project.org/redmine/issues/10951))
  - Fixed: Wrong XML identation in event log
    ([\#10951](https://www.rudder-project.org/redmine/issues/10951))
  - Fixed: Keep (open/folded) menu state in cache
    ([\#10955](https://www.rudder-project.org/redmine/issues/10955))
  - Fixed: Add a margin between the filters and the table in Technical logs tab
    ([\#11083](https://www.rudder-project.org/redmine/issues/11083))
  - Fixed: Repaired does not appear as yellow anymore
    ([\#11028](https://www.rudder-project.org/redmine/issues/11028))

#### Web - Config management

  - Fixed: Missing included list of ps1 in rudder-directive.ps1
    ([\#11076](https://www.rudder-project.org/redmine/issues/11076))

#### Miscellaneous

  - Fixed: Generated technique name for dsc technique in rudder-directives.ps1 contains forbiden chars
    ([\#11071](https://www.rudder-project.org/redmine/issues/11071))

#### Agent

  - Fixed: rudder agent update -q bad exit code
    ([\#11047](https://www.rudder-project.org/redmine/issues/11047))

#### Packaging

  - Fixed: When upgrading 4.2 server, system techniques from plugin are purged
    ([\#11045](https://www.rudder-project.org/redmine/issues/11045))
  - Fixed: if plugin is broken, we cannot upgrade it
    ([\#11064](https://www.rudder-project.org/redmine/issues/11064))
  - Fixed: When installing Rudder-Webapp, postinst script runs rudder-upgrade before initializing the git, and it can fail
    ([\#10990](https://www.rudder-project.org/redmine/issues/10990))
  - Fixed: Do not show instructions for rudder-node-to-relay on root setup
    ([\#10859](https://www.rudder-project.org/redmine/issues/10859))
  - Fixed: ca.cert file is empty, prevent apache2 to start
    ([\#11114](https://www.rudder-project.org/redmine/issues/11114))

#### Techniques

  - Fixed: Directive: Services Management doesn't support AIX
    ([\#8752](https://www.rudder-project.org/redmine/issues/8752))


## Rudder 4.2.0.beta1 (2017-06-26)

### Changes

#### Web - Nodes & inventories

  - Add option in search engine to search for DSC agent
    ([\#10911](https://www.rudder-project.org/redmine/issues/10911))
  - Display rudder-agent dsc version on Dashboard
    ([\#10836](https://www.rudder-project.org/redmine/issues/10836))
  - Adapt inventory processor so it can read agent certificate
    ([\#10879](https://www.rudder-project.org/redmine/issues/10879))
  - Parse AGENT_KEY instead of CFENGINE_KEY in inventory
    ([\#10824](https://www.rudder-project.org/redmine/issues/10824))
  - Parse and store agent type: dsc
    ([\#10738](https://www.rudder-project.org/redmine/issues/10738))

#### Web - Config management

  - Create system variables for apache authentication
    ([\#10927](https://www.rudder-project.org/redmine/issues/10927))
  - Add system groups/rules/directives for windows dsc agent
    ([\#10953](https://www.rudder-project.org/redmine/issues/10953))
  - Generate a "rudder.json" file containting system variables
    ([\#10936](https://www.rudder-project.org/redmine/issues/10936))
  - Select system techniques and generate correct policies based on agent type
    ([\#10823](https://www.rudder-project.org/redmine/issues/10823))
  - Zip promises post generation for dsc agent
    ([\#10905](https://www.rudder-project.org/redmine/issues/10905))

#### Packaging

  - Add ssl based authentication to policies
    ([\#10958](https://www.rudder-project.org/redmine/issues/10958))
  - /var/rudder/share must be readable by rudder-policy-reader
    ([\#10885](https://www.rudder-project.org/redmine/issues/10885))
  - Rename technique editor hooks to have a better way to organize them and create reload hook
    ([\#10843](https://www.rudder-project.org/redmine/issues/10843))

#### Initial promises & sys tech

  - Accept logs reports which don't start by "R: "
    ([\#10829](https://www.rudder-project.org/redmine/issues/10829))

#### Architecture - Dependencies

  - Bad version in pom.xml for 4.2
    ([\#10975](https://www.rudder-project.org/redmine/issues/10975))

#### Architecture - Refactoring

  - Normalize agent names (cfengine-community, cfengine-nova, dsc)
    ([\#10931](https://www.rudder-project.org/redmine/issues/10931))

#### Server components

  - Share promises for windows agents in https
    ([\#10776](https://www.rudder-project.org/redmine/issues/10776))

### Bug fixes

#### Web - Config management

  - Fixed: Generation error "bad algorithm" with DSC nodes
    ([\#11014](https://www.rudder-project.org/redmine/issues/11014))
  - Fixed: Bad query for all-dsc-node
    ([\#10996](https://www.rudder-project.org/redmine/issues/10996))
  - Fixed: Audit only flag does not take parameter rudder-directives.ps1
    ([\#10974](https://www.rudder-project.org/redmine/issues/10974))
  - Fixed: Unhelpful error message when applying a tehcnique with invalid agent type to a node
    ([\#10969](https://www.rudder-project.org/redmine/issues/10969))
  - Fixed: Audit only flag does not take parameter rudder-directives.ps1
    ([\#10974](https://www.rudder-project.org/redmine/issues/10974))
  - Fixed: Unhelpful error message when applying a tehcnique with invalid agent type to a node
    ([\#10969](https://www.rudder-project.org/redmine/issues/10969))

#### Web - Nodes & inventories

  - Fixed: Invalid agent name for dsc agent
    ([\#10909](https://www.rudder-project.org/redmine/issues/10909))

#### Documentation

  - Fixed: Style broken in documention: upgrade_from_rudder_3_1_3_2_or_4_0
    ([\#11002](https://www.rudder-project.org/redmine/issues/11002))

#### Miscellaneous

  - Fixed: Invalid name for dsc agent type in hooks
    ([\#11001](https://www.rudder-project.org/redmine/issues/11001))
  - Fixed: Error in template
    ([\#11004](https://www.rudder-project.org/redmine/issues/11004))
  - Fixed: Error at node list display/deployement status on fresh Rudder 4.2 install
    ([\#10994](https://www.rudder-project.org/redmine/issues/10994))
  - Fixed: webapp can't start after upgrade to 4.2
    ([\#10986](https://www.rudder-project.org/redmine/issues/10986))

#### Packaging

  - Fixed: SSLUserName should be in directory specific configuration in apache
    ([\#11009](https://www.rudder-project.org/redmine/issues/11009))
  - Fixed: Missing configuration file for Apache2 when installing 4.2
    ([\#10989](https://www.rudder-project.org/redmine/issues/10989))

#### Initial promises & sys tech

  - Fixed: nodeslist.json is not generated into the right file
    ([\#11007](https://www.rudder-project.org/redmine/issues/11007))
  - Fixed: Missing template distributePolicy/1.0,apache_acl during generation
    ([\#10997](https://www.rudder-project.org/redmine/issues/10997))

#### System integration

  - Fixed: Bad semantic for system error on hooks
    ([\#11010](https://www.rudder-project.org/redmine/issues/11010))

### Release notes

This software is in beta status and has several known bugs
(particularly [\#11027](https://www.rudder-project.org/redmine/issues/11027), [\#10961](https://www.rudder-project.org/redmine/issues/10961), [\#10990](https://www.rudder-project.org/redmine/issues/10990) and [\#11051](https://www.rudder-project.org/redmine/issues/11051)).
You should hence not use it in production.
However, we do encourage testing, and welcome all and any
feedback\!

To be able to finish the installation (on ubuntu), after `apt-get install rudder-server-root` fails, you will need to:

- workaround #10990

```
cd /var/rudder/configuration-repository/
git init
git add .
git commit -q -m "initial commit"
```

- workaround #11051

```
touch /opt/rudder/etc/rudder-share-acl-24.conf /opt/rudder/etc/rudder-share-acl.conf
cp /opt/rudder/etc/ssl/rudder.crt /opt/rudder/etc/ssl/ca.cert
```

- finish installation:

```
apt-get install -f
```

- reset git repos (because it is in a bad state)

```
cd /var/rudder/configuration-repository/
rm -rf .git
git init
git add .
git commit -q -m "initial commit"
```