# SplunkDataCooker
An Splunk app for creating fake logs and data to make easier tests in your local or development environments

## Structure
- Cooker Configuration
Where the configuration Knowledge Objects are allocated
- Cooker Kitchen
Where the final "food" data is created and allocated

## Explanation
Is a data simulator, where you configure the Python Splunk to create log fake data to make quick or/and local tests in your Splunk Environments
This is an example of a "food order"
```
[`{date, %Y-%m-%d %H:%M:%S.%3N}`] `INFO,DEBUG,WARNING,ERROR` - The log corresponds to the following message: Information by the number `{number, 2:90},N/A`
```
The program will produce the same text on log files, but when an `` appears, it means to the interpreter that it is a command to invoke random data
1.- Inside the {} characters means a special command, in this case it will create a timestamp from the moment of the code execution, and opcionally will require the format, by default will impress the UNIX EPOCH timestamp
2.- The second one will choose a random text, each one separated by comma
3.- The third one will invoke the special command "number", to choose a random range of numbers, if one of the numbers is a decimal, it will choose a random floating number, and optionally you can choose the precision by a third argument (0 by default)

## First Learning and Testing

## Designing and Building

## Testing and deploying