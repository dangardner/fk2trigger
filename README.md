fk2trigger
==========

NAME
       fk2trigger - Convert InnoDB foreign keys to NDB with triggers

SYNOPSIS
       mysqldump <db> | fk2trigger [-e <engine>] [-t <trigger-file>]

DESCRIPTION
       fk2trigger takes output from mysqldump and converts foreign key constraints to triggers which mimic their behaviour. It also converts all table engines to the specified engine.

       This program was written to ease migration from InnoDB to MySQL Cluster.

OPTIONS
       -e engine
            All engine declarations will be replaced by the specified engine.  Defaults to 'NDBCLUSTER'.

       -t trigger-file
            Write triggers to the specified file, for loading on other nodes in the MySQL Cluster. By default, triggers will be output on stdout, after the mysqldump output.

VERSION
       v0.01 - Initial release

AUTHOR
       Dan Gardner (dan /at/ lizearle /dot/ com)

CREDITS
       Released publicly by kind permission of my employer, Liz Earle Beauty Co. Ltd.

COPYRIGHT
       Copyright (C) 2008, Liz Earle Beauty Co. Ltd.

       This work is licensed under the GNU General Public License version 3.  For the full license information, please visit http://www.gnu.org/copyleft/gpl.html
