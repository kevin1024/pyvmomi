vim.host.DatastoreBrowser.SearchSpec
====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The data object type describes a search for files in one or more datastores. The   properties do not include the starting datastore path because that path is a   separate parameter to the search method.   <p>   A SearchSpec contains the query parameters and some global search modifiers.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| query | [vim.host.DatastoreBrowser.Query](vim.host.DatastoreBrowser.Query.md "vim.host.DatastoreBrowser.Query") | true | None | The set of file types to match, search criteria specific to the file type, and   the amount of detail for a file. These search parameters are specific to a file   type, meaning that they can be specified only if the file type to which they   are associated is in the set. A file type cannot appear more than once in the   set.   <p>   If this query object is not present, then all files providing only file level   details are matched. |
| details | [vim.host.DatastoreBrowser.FileInfo.Details](vim.host.DatastoreBrowser.FileInfo.Details.md "vim.host.DatastoreBrowser.FileInfo.Details") | true | None | This object comprises a set of booleans that describe what details to return   for each file. The file level details apply globally to all matched files. |
| searchCaseInsensitive | bool | true | None | This flag indicates whether or not to search using a case insensitive match on   type. In general the algorithm used to match file types relies on file   extensions. Although the specific file extensions used are encapsulated by this   API, clients are still allowed to modify the filtering behavior.   <p>   By default, the DatastoreBrowser uses a platform-consistent algorithm to   determine if a file is of a type. Specifically on Linux, where case is   important, the search is case sensitive. On Windows, case is not important, so   the search is case insensitive.   <p>   In an environment with heterogenous platforms, being platform-consistent may   not be desirable. As a result, the default behavior can be overridden by   setting this optional flag. |
| matchPattern | string | true | None | Specifies a list of file patterns that must match for a file to be returned.   This search property is a filter that applies globally so that only files   matching the specified patterns are returned, regardless of the other search   parameters. |
| sortFoldersFirst | bool | true | None | By default, files are sorted in alphabetical order regardless of file type. If   this flag is set to "true", folders are placed at the start of the list of   results in alphabetical order. The remaining files follow in alphabetical   order. |


