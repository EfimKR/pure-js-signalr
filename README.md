# pure-js-signalr
## SignalR JS Client without any dependencies

Based on [signalr-no-jquery](https://github.com/DVLP/signalr-no-jquery)

This version of signalR client doesn't have any dependencies - just add and use.
Required minimum of jQuery functionality is added locally to signalR.

This package is not meant to be used with ASP.NET Core version of SignalR.

### Usage

// create hub connection
var connection = hubConnection();

connection.qs = { 'version': '1.0' };

connection.url = url;

hubProxy = connection.createHubProxy('hubProxy');

// add event listeners
hubProxy.on('event', function(data) {
    handleEvent(data);
});

// create connection
connection.start()

   .done(function(response){ handleResponse(response) })
    
   .fail(function(error){ handleError(error) });
