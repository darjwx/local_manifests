Manifests
=========

Local manifests xml files for my supported roms

Basic knowledge
---------------
As wikipedia says, Extensible Markup Language (XML) (the language of the local_manifests) is a markup language that defines a set of rules for encoding documents in  a format which is both human-readable and machine-readable. It is defined by the W3C's XML 1.0 Specification and by several other related specifications, all of    which are free open standards. 
And also is the main tool of the rom porter.

Here are some explanations about the parts of a manifest in an android rom:

**<?xml version="1.0" encoding="UTF-8"?>** : define the version and the type of encoding. You dont have to edit it normally so leave it stay.

**<manifest></manifest>** the start and the end of the manifest

**<remote/>** : Its used to define the atributes of the repos, and to make simpler the document. It has some parts: name (the name that will call it, like a id. If the repo has that id will use some atributes), fetch (the url of the github/bitbucket/gitlab... repositories/organizations such as omnirom or CyanogenMod) review (the gerrit of the organization such as review.cyanogenmod.org. Not needed in most of the cases) sync-c (cores. Optional) and sync-j (number of jobs. Optional). Take in consideration that the remote flag is optional and sometimes can cause conflicts with the main xml of the rom.

**<!-- -->** A comment. The lines inside it are not part of the code.

**<project/>** The repos we want to sync. Has also some parts: name (name of the repo. Full name in normal cases but if you have a remote defined you dont have to put "organizationName/..."), path (the route where the repo will be downloaded), remote (the web where is the repo: github, gitlab... Here also can be the name of yor remote.), groups and revision (branch you want)


There are some others but that are the main ones. Feel free to use my manifests, to take them as a guide or to adapt it to other devices.

*#RomPortersFTW*
 




