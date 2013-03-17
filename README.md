### [An Open Framework Of Talk Bot]

* Aim to providing an open framework of talk bot
* for using topbot ai, invoking ai.magic(data)

### TODO:

* cache support
* teaching mechanism 
* database building

### PLUGINS

You can easily add more features for topbot with plugins developing.

Each plugin is a python module with two interface 'test' & 'handle' in 'plugins' directory, format as follow:

    def test(data, bot):
        // your code
function 'test' return 'True' handling or 'False' for not handling

    def handle(data, bot):
        // your code

Function 'handle' handles the request and return utf8 encode msg as the response

'data' is a dictionary, contents as follow :

    {
        'from_id'   : identify of sender,
        'to_id'    : identify of reciever,
        'message'    : message content,
    }

`bot` is a bot instance

register your plugin in 'plugins/__init__.py' & add unit test code in directory 'tests'.

### THANKS TO

This project is based on wong2's github repo xiaohuangji-new (https://github.com/wong2/xiaohuangji-new) .