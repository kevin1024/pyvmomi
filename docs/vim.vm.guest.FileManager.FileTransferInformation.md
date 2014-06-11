vim.vm.guest.FileManager.FileTransferInformation
================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


Represents the information about a  <a href="vim.vm.guest.FileManager.md#initiateFileTransferFromGuest">InitiateFileTransferFromGuest</a> operation  of <a href="vim.vm.guest.FileManager.md">GuestFileManager</a> object.  <p>  The user can use the URL provided in url property to transfer  the file from the guest. The user should send a HTTP GET request to the  URL. Entire file content will be returned in the body of the response  message.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| attributes | [vim.vm.guest.FileManager.FileAttributes](vim.vm.guest.FileManager.FileAttributes.md "vim.vm.guest.FileManager.FileAttributes") | None | None | File attributes of the file that is being transferred from the guest. |
| size | long | None | None | Total size of the file in bytes. |
| url | string | None | None | Specifies the URL to which the user has to send HTTP GET request.  Multiple GET requests cannot be sent to the URL simulatenously. URL  will become invalid once a successful GET request is sent.   The host part of the URL is returned as '*' if the hostname to be used  is the name of the server to which the call was made. For example, if  the call is made to esx-svr-1.domain1.com, and the file is available for  download from  http://esx-svr-1.domain1.com/guestFile?id=1&token=1234,  the URL returned may be  http://&#42;/guestFile?id=1&token=1234.  The client replaces the asterisk with the server name on which it  invoked the call. |


