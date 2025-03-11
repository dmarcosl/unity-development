# Cloud Build

Unity Cloud Build is a continuous integration service the projects that helps you save time by automating the process of creating builds on Unity servers.

It helps you catch problems sooner, share builds with collaborators and iterate versions of your development more rapidly.

In order to make builds, you have to:

1. Host your project in a Version Control System, the supported are:
    * Unity Collaborate
    * Git
    * SVN
    * Mercurial
    * Perforce
2. Enable access to the VCS by setting a RSA key or typing credentials
3. Choose Platform
    * iOS
    * Android
    * Windows desktop
    * Mac OS desktop
    * Linux desktop
    * WebGL
    * Unity Web Player (5.3 and below)
4. Target setup, like git branch, Unity Version and Auto-build option
5. Set credentials, like Android sign key

You can

* View build history
* Add collaborators
* Watch stats (logs, build health, etc)
* Change the configuration, like the repository url or the branch
* Get notifications by Webhooks or Slack