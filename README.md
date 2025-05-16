# emojify-pwsh

Emoji on the PowerShell command line :wink:

This is a PowerShell port of the [original emojify script](https://github.com/mrowa44/emojify) by mrowa44.

## Description

emojify-pwsh substitutes emoji aliases (like those used on GitHub) with emoji raw characters in your PowerShell console. It's a fun and expressive way to enhance your command-line experience!

## Installation

1. Download the `emojify-pwsh.ps1` script from this repository.

2. Run the script once to add the `Emojify` function to your PowerShell profile:

```powershell
.\emojify-pwsh.ps1
```

This will make the `Emojify` function available in all future PowerShell sessions.

## Usage

Here's a fun example:

```powershell
PS > Emojify "Hey, I just :raising_hand: you, and this is :scream: , but here's my :calling: , so :telephone_receiver: me, maybe?"
```

Output:
> Hey, I just 🙋 you, and this is 😱 , but here's my 📞 , so 📞 me, maybe?

You can also pipe text into the function:

```powershell
PS > "To :bee: , or not to :bee: : that is the question..." | Emojify
```

Output:
> To 🐝 , or not to 🐝 : that is the question...

Or you could run it through git log with something like:
```sh
PS > git log --oneline --color | Emojify
```
and go from this dull thing:

![before](https://raw.githubusercontent.com/mrowa44/emojify/refs/heads/master/img/before.png)

to this:

![after](https://raw.githubusercontent.com/mrowa44/emojify/refs/heads/master/img/after.png)

To have an alias that does that for you, add something like:
```powershell
function GitLogEmojify { git log --oneline --color | Emojify }
Set-Alias -Name log -Value GitLogEmojify
```

to your `$PROFILE`.

### Options

- `-Help`: Display help information
- `-List`: Show all supported emoji
- `-Version`: Display the version of emojify-pwsh

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

This is a PowerShell port of the original [emojify](https://github.com/mrowa44/emojify) bash script by mrowa44. All credit for the original concept and implementation goes to them.