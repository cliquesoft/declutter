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

	Archive data before May 1st 2025 to /mnt/archive:
	     declutter -A '2025-05-01 00:00:01' -a move /mnt/nas /mnt/archive

	Separate live data after May 1st 2025 to /mnt/live:
	     declutter -B '2025-05-01 00:00:01' -a move /mnt/nas /mnt/live

	Deduplicate a single directory, ignorning newer additions
	     declutter -A '2025-05-01 00:00:01' -d delete /home/user/Videos

	Deduplicate two directories moving the duplicates to /opt/dupes
	     declutter -d move /mnt/sda1/files /mnt/sdb1/data /opt/dupes

	Remove empty directories:
	     declutter -e delete /mnt/nas/data

	Delete mismatch data (including hidden) between two drives:
	     declutter -H -m delete /mnt/sdb1 /mnt/sdc1

	Move mismatched (non-hidden) data between two drives to /opt/diff:
	     declutter -m copy /mnt/sdb1 /mnt/sdc1 /opt/diff

	Same as previous line but removing part of the directory structure:
	     declutter -R 'remove/me' -m copy /mnt/sdb1 /mnt/sdc1 /opt/diff

	Same as previous line but adding to the directory structure:
	     declutter -P 'add/me' -m copy /mnt/sdb1 /mnt/sdc1 /opt/diff




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

