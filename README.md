# Chocolatey Package for Rakudo Star

The [Chocolatey package for Rakudo Star](https://chocolatey.org/packages/rakudostar).

Get the latest [Rakudo Star](http://rakudo.org/downloads/star/).
Use the URL to a specific version instead of the "latest" link. The
Chocolatey package uses a checksum, which changes.

Update the release notes in [rakudostar.nuspec](rakudostar/rakudostar.nuspec).

Update the version in  [rakudostar.nuspec](rakudostar/rakudostar.nuspec)
and [Tools/chocolateyInstall.ps1](rakudostar/Tools/chocolateyInstall.ps1).

Add the checksum to [Tool/chocolateyInstall.ps1](rakudostar/chocolateyInstall.ps1)

	certUtil -hashfile pathToFileToCheck [HashAlgorithm]

Pack the distro:

	choco pack

Push the distro:

	choco push

You may need to set your [API key](https://github.com/chocolatey/choco/wiki/CommandsApiKey) first:

	choco apikey -k <your key here> -s https://chocolatey.org/