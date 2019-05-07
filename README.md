# ![LOGO](logo.png) Fisheye Crucible **flow**ground Connector

## Description

A generated **flow**ground connector for the Fisheye Crucible API (version 1.0.0).

Generated from: https://api.apis.guru/v2/specs/fecru.local/1.0.0/swagger.json<br/>
Generated at: 2019-05-07T17:40:42+03:00

## API Description



## Authorization

This API does not require authorization.

## Actions

### Retrieve a page of groups.

#### Input Parameters
* `prefix` - _optional_ - filter groups by name prefix

### Creates a new user group.

### Deletes a group by name

#### Input Parameters
* `name` - _required_ - group name

### Retrieve a group by name.

#### Input Parameters
* `name` - _required_ - group name

### Updates an existing group.

#### Input Parameters
* `name` - _required_ - group name

### Removes user from group

#### Input Parameters
* `name` - _required_ - group name

### Lists group's user names

#### Input Parameters
* `name` - _required_ - group name

### Adds user to group

#### Input Parameters
* `name` - _required_ - group name

### Retrieve a page of permission schemes.

#### Input Parameters
* `name` - _optional_ - permission scheme name part filter, case insensitive, optional

### Creates a new permission scheme. The new permission scheme is blank or can be created from another existing permission scheme.

#### Input Parameters
* `copyFrom` - _optional_ - if set, the new permission scheme will be a copy of permissionSchemeName

### Deletes a permission scheme by name

#### Input Parameters
* `name` - _required_ - permission scheme name

### Retrieve a permission scheme by name

#### Input Parameters
* `name` - _required_ - permission scheme name

### Updates an existing permission scheme.

#### Input Parameters
* `name` - _required_ - permission scheme name

### Removes anonymous-user permission [action name] from given permission scheme

#### Input Parameters
* `name` - _required_ - permission scheme name

### Retrieve a page of anonymous users permissions [action name] for given permission scheme.

#### Input Parameters
* `action` - _optional_ - action name

### Add anonymous-user permission [action name] to given permission scheme<br/>
>  List of available action names:

#### Input Parameters
* `name` - _required_ - permission scheme name

### Removes group permission [group name, action name] from given permission scheme

#### Input Parameters
* `name` - _required_ - permission scheme name

### Retrieve a page of group permissions [group name, action name] for given permission scheme.

#### Input Parameters
* `name` - _optional_ - group name
* `action` - _optional_ - action name

### Add group permission [group name, action name] to given permission scheme<br/>
>  List of available action names:

#### Input Parameters
* `name` - _required_ - permission scheme name

### Removes logged-in-users permission [action name] from given permission scheme

#### Input Parameters
* `name` - _required_ - permission scheme name

### Retrieve a page of logged in users permissions [action name] for given permission scheme.

#### Input Parameters
* `action` - _optional_ - action name

### Add logged-in-users permission [action name] to given permission scheme<br/>
>  List of available action names:

#### Input Parameters
* `name` - _required_ - permission scheme name

### Retrieve a page of projects for given permission scheme.

#### Input Parameters
* `name` - _required_ - permission scheme name

### Removes review-role permission [role name, action name] from given permission scheme

#### Input Parameters
* `name` - _required_ - permission scheme name

### Retrieve a page of review-roles permissions [role name, action name] for given permission scheme.

#### Input Parameters
* `name` - _optional_ - role name
* `action` - _optional_ - action name

### Add review-role permission [role name, action name] to given permission scheme<br/>
>  List of available action names:<br/>
>  <br/>
> <br/>
>  List of available role names:

#### Input Parameters
* `name` - _required_ - permission scheme name

### Removes user permission [username, action name] from given permission scheme

#### Input Parameters
* `name` - _required_ - permission scheme name

### Retrieve a page of user permissions [username, action name] for given permission scheme.

#### Input Parameters
* `name` - _optional_ - permission scheme name
* `action` - _optional_ - action name

### Add user permission [username, action name] to given permission scheme<br/>
>  List of available action names:

#### Input Parameters
* `name` - _required_ - permission scheme name

### Retrieve a page of projects.

#### Input Parameters
* `name` - _optional_ - project's name part filter, optional
* `key` - _optional_ - project's key part filter, optional
* `defaultRepositoryName` - _optional_ - project's default repository key part filter, optional
* `permissionSchemeName` - _optional_ - project's permission scheme pare name filter, optional

### Creates a new project.

### Deletes a project by key (including all reviews in this project).<br/>
>  Use <br/>
>  to move reviews to another project.

#### Input Parameters
* `deleteProjectReviews` - _optional_ - if true deletes reviews in project

### Retrieve a project by key.

#### Input Parameters
* `key` - _required_ - project key

### Updates an existing project.

#### Input Parameters
* `key` - _required_ - project key

### Delete group from project's allowed reviewer group list

#### Input Parameters
* `key` - _required_ - project key

### Retrieves project's allowed reviewer groups

#### Input Parameters
* `key` - _required_ - project key

### Add group to project's allowed reviewer group list

#### Input Parameters
* `key` - _required_ - project key

### Remove user from project's allowed reviewer users list

#### Input Parameters
* `key` - _required_ - project key

### Retrieves project's allowed reviewer users

#### Input Parameters
* `key` - _required_ - project key

### Add user to project's allowed reviewer users list

#### Input Parameters
* `key` - _required_ - project key

### Delete group from project's default reviewer group list

#### Input Parameters
* `key` - _required_ - project key

### Retrieves project's default reviewer groups

#### Input Parameters
* `key` - _required_ - project key

### Add group to project's default reviewer group list

#### Input Parameters
* `key` - _required_ - project key

### Remove user from project's default reviewer users list

#### Input Parameters
* `key` - _required_ - project key

### Retrieves project's default reviewer users

#### Input Parameters
* `key` - _required_ - project key

### Add user to project's default reviewer users list

#### Input Parameters
* `key` - _required_ - project key

### Move reviews and snippets from source project to destination project

#### Input Parameters
* `sourceProjectKey` - _required_ - project key of reviews and snippets source project
* `destinationProjectKey` - _required_ - project key of reviews and snippets destination project

### Retrieve a page of repositories. Repository properties with default values may not be returned.

#### Input Parameters
* `type` - _optional_ - filter repositories by repository type: svn, git, hg, cvs, p4, ...
* `enabled` - _optional_ - filter repositories by enabled flag
* `started` - _optional_ - filter repositories by started flag

### Creates a repository.

### Adds repository

### Returns information about the status of the repository and the current indexing status

#### Input Parameters
* `repository` - _required_ - the key of the repository

### Deletes repository.<br/>
>  Warning: you can not undo this operation

#### Input Parameters
* `repository` - _required_ - the key of the repository to delete

### Disables repository.

#### Input Parameters
* `repository` - _required_ - the key of the repository to disable

### Enables repository.

#### Input Parameters
* `repository` - _required_ - the key of the repository to enable

### Rebuilds the changeset discussion index for the specified repository. The index is used to display changeset<br/>
>  discussions in activity streams.

#### Input Parameters
* `repository` - _required_ - the key of the repository to perform the operation for

### Re-indexes the linecount data used to generate the LOC graphs. The linecount data will be recalculated in daily<br/>
>  buckets based on the server timezone.

#### Input Parameters
* `repository` - _required_ - the key of the repository to re-index

### Re-indexes all the Crucible revision data (which revisions have been reviewed)

#### Input Parameters
* `synchronous` - _optional_ - if true will wait for the indexing to finish before returning

### Rebuilds the search index data for the given repository. This will rebuild the data used to search by path,<br/>
>  commit message and comitter, also used for activity streams and JIRA integration.

#### Input Parameters
* `repository` - _required_ - the key of the repository to re-index.

### Deletes the existing cache and re-indexes the repository from scratch.<br/>
>  For large or slow repositories this may take some time, during which some functionality will be unavailable.<br/>
>  This action will also restart the repository.

#### Input Parameters
* `clone` - _optional_ - if true and the repository is a dvcs repository (git or mercurial) it will re-clone the repository
 before re-indexing

### Re-scans the repository metadata for SVN and Perforce repositories. Only valid for Perforce and SVN repositories.

#### Input Parameters
* `from` - _optional_ - the revision number to start at
* `to` - _optional_ - the revision number to end at

### Runs an incremental repository index now.  This is the same operation as triggered by scheduled indexing.<br/>
>  Can be called using the REST Api Token to authorize.

#### Input Parameters
* `synchronous` - _optional_ - if true will wait for the indexing to finish before returning

### Scans the whole CVS repository for any changes since the last scan. Only valid for CVS repositories.

#### Input Parameters
* `repository` - _required_ - the key of the repository to scan

### Starts the repository.

#### Input Parameters
* `repository` - _required_ - the key of the repository to start

### Stops the repository. Does not wait for the repository to stop before returning.

#### Input Parameters
* `repository` - _required_ - the key of the repository to stop

### Deletes a repository by key

#### Input Parameters
* `repository` - _required_ - the key of the repository

### Retrieve a repository by key. Repository properties with default values may not be returned.

#### Input Parameters
* `repository` - _required_ - the key of the repository

### Updates an existing repository.

#### Input Parameters
* `repository` - _required_ - the key of the repository

### Runs an full incremental repository index.<br/>
>  For CVS: scans the whole CVS repository for any changes since the last scan.<br/>
>  For other repository types will trigger an incremental index.

#### Input Parameters
* `repository` - _required_ - the key of the repository to scan

### Runs an incremental repository index.  This is the same operation as triggered by scheduled indexing.<br/>
>  Can be called using the REST API Token to authorize.

#### Input Parameters
* `wait` - _optional_ - if true will wait for the indexing to finish before returning

### Retrieve repository permissions properties.

#### Input Parameters
* `repository` - _required_ - the key of the repository

### Updates repository permissions properties.<br/>
> <br/>
>  Valid permission settings: any combination of useDefaults, allowAnonymous, allowLoggedIn.

#### Input Parameters
* `repository` - _required_ - the key of the repository

### Delete group from repository allowed groups

#### Input Parameters
* `repository` - _required_ - the key of the repository

### Note: use /rest-service-fecru/admin/repository-permissions/ endpoint for full repository permission administration functionality<br/>
>  Lists groups allowed to access repository.

#### Input Parameters
* `repository` - _required_ - the key of the repository

### Note: use /rest-service-fecru/admin/repository-permissions/ endpoint for full repository permission administration functionality<br/>
>  Adds group to repository allowed groups

#### Input Parameters
* `repository` - _required_ - the key of the repository

### Rebuilds the changeset discussion index for the specified repository. The index is used to display changeset<br/>
>  discussions in activity streams.

#### Input Parameters
* `repository` - _required_ - the key of the repository to perform the operation for

### Re-indexes the linecount data used to generate the LOC graphs. The linecount data will be recalculated in daily<br/>
>  buckets based on the server timezone.

#### Input Parameters
* `repository` - _required_ - the key of the repository to re-index

### Re-indexes all the Crucible revision data (which revisions have been reviewed)

#### Input Parameters
* `repository` - _required_ - the key of the repository to reindex

### Rebuilds the search index data for the given repository. This will rebuild the data used to search by path,<br/>
>  commit message and committer, also used for activity streams and JIRA integration.

#### Input Parameters
* `repository` - _required_ - the key of the repository to re-index.

### Deletes the existing cache and re-indexes the repository from scratch.<br/>
>  For large or slow repositories this may take some time, during which some functionality will be unavailable.<br/>
>  This action will also restart the repository.

#### Input Parameters
* `clone` - _optional_ - if true and the repository is a dvcs repository (git or mercurial) it will re-clone the repository before re-indexing

### Re-scans the repository metadata. Only valid for Perforce and SVN repositories.

#### Input Parameters
* `from` - _optional_ - the revision number to start at
* `to` - _optional_ - the revision number to end at

### Starts repository. Does not wait for the repository to start before returning.

#### Input Parameters
* `repository` - _required_ - the key of the repository to start

### Stops repository. Does not wait for the repository to stop before returning.

#### Input Parameters
* `repository` - _required_ - the key of the repository to stop

### Retrieves repository updates properties.

#### Input Parameters
* `repository` - _required_ - repository key

### updateRepositoryUpdates

#### Input Parameters
* `repository` - _required_ - repository key

### Retrieve default repository permissions properties.

### Updates default repository permissions properties.<br/>
> <br/>
>  Valid permission settings: any combination of allowAnonymous, allowLoggedIn

### Retrieve a page of users.

### Creates a new user. Tries to add the user to fisheye-users and crucible-users groups if those exist.

### Deletes a user by name

#### Input Parameters
* `name` - _required_ - user name

### Retrieve a user by name.

#### Input Parameters
* `name` - _required_ - user name

### Updates an existing user.

#### Input Parameters
* `name` - _required_ - user name

### Removes user from group

#### Input Parameters
* `name` - _required_ - user name

### Lists user's group names

#### Input Parameters
* `name` - _required_ - user name

### Adds user to group

#### Input Parameters
* `name` - _required_ - user name

### Get the user authentication token.

### Returns indexing status of given repository.

#### Input Parameters
* `repository` - _required_ - the key of the repository to get status of

### Get a list of recently visited items for the currently logged in user.

### Get a list of recently visisted items for the currently logged in user, including the detailed entities.

### Get a list of recently visited projects for the currently logged in user.

### Get a list of recently visited projects for the currently logged in Project, including the detailed entities.

### Get a list of recently visited repositories for the currently logged in user.

### Get a list of recently visisted repositories for the currently logged in user, including the detailed entities.

### Get a list of recently visited reviews for the currently logged in user.

### Get a list of recently visited reviews for the currently logged in user, including the detailed entities.

### Get a list of recently visited snippets for the currently logged in user.

### Get a list of recently visited snippets for the currently logged in user, including the detailed entities.

### Get a list of recently visited users for the currently logged in user.

### Get a list of recently visited users for the currently logged in user, including the detailed entities.

### Provides general information about the server's configuration.

### doShareContent

### Using POST method to set a user preference.<br/>
>  If repo is not set, the preference will be recognised as a global preference.

### Getting user's global preference

#### Input Parameters
* `property` - _required_ - the property(preference) name

### Getting user's preference related to a certain repository

#### Input Parameters
* `property` - _required_ - the property(preference) name
* `repository` - _required_ - the key of the repository

## License

**flow**ground :- Telekom iPaaS / fecru-local-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
