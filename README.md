# [PREAMBLE]

	Thanks for taking interest in declutter! This project enables a Linux
	administrator to perform several tasks with user-generated data which
	includes: archiving, cleaning mismatched, deduplicating, removal of
	empty directories.




# [FOR THE IMPATIENT]

	To Install:
		1. cd /path/to/declutter
		2. sudo cp ./declutter /bin

	To Use:
		1. declutter --help




# [USEFUL FEATURES]

	Being a single file usually does not include a rich feature set, but
	this script was able to pack quite a bit in! Here's a short list of
	some rather robust actions that can be performed:

		o Archive data using before or after dates
		o Clean mismatched data between directories or drives
		o Deduplicate data between one or two directories
		o Remove empty directories
		o Each action can ignore files by date specifications
		o Hidden directories and files can optionally be included
		o Dryruns can test results before implementation
		o Each action can move or delete data matching criteria
		o Directory paths can be manipulated when moving data




# [EXAMPLE ACTIONS]

	Install a package:
	     pax -i nano[.i32.bin.soft]

	Install packages from a file:
	     pax -i /path/to/package.list

	Install a specific version:
	     pax -i -V 1.2.3 nano[.i32.bin.soft]

	Make a package for distribution:
	     pax -m nano /path/to/package[/source]

	Only download a package from the repo:
	     pax -d nano[.i32.bin.soft]

	Update a package without optional restore point:
	     pax -i -R none nano[.i32.bin.soft]

	Unload a package:
	     pax -u unload nano[.i32.bin.soft]

	Uninstall a package:
	     pax -u delete nano[.i32.bin.soft]

	Uninstall a package, purging configs too:
	     pax -u purge nano[.i32.bin.soft]




# [FUTURE DEV TIMELINE]

	Since we are working with several many projects (13 on github alone),
	we are going to provide an anticipated timeline of releases using
	internal staff. Obviously outside contribution will advance these
	forecasted dates.

	2025 Oct - update pax; modify to work with (TC) TinyCore Linux
	2026 Jan - package dittodata for (TC) TinyCore Linux
	2026 Feb - completion of ModuleMaker for webWorks
	2026 Apr - migration of existing webWorks modules using ModuleMaker
	         - migration of Tracker into webWorks and deprecation of
	           of standalone project
	2026 May - update paged to 2018 code base from ACME
	         - apply any patches for bug fixes to existing projects
	2026 Jun - update web.libs for dittodata and web.de
	2026 Aug - move code from web.de into cli.de and update the former
	           to use the latter via XML communication
	2026     - rest of 2026 tbd

