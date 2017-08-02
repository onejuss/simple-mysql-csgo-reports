# simple-mysql-csgo-reports


As the title says, this plugin allows players made reports on players that behave bad, this is my first plugin ever, so mods please check the SP file..

How it works
Simple in game chat you type !report the menu with players will pop up, you choose the player and he's steam_id will be stored to your database in column reported, in column reporter you can find steam_id of the player who made report

Creating table to store data

CREATE TABLE `sm_report` (
`id` int(64) NOT NULL AUTO_INCREMENT,
`reported` varchar(32) DEFAULT '',
`reporter` varchar(32) DEFAULT '',
`reason` text,
`date` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
PRIMARY KEY (`id`)
) ENGINE=MyISAM AUTO_INCREMENT=29 DEFAULT CHARSET=utf8;

In yourSourcemod/configs/databases.cfg
Don't forget to add your credentials 
"default"
{
"driver"	"default"
"host"	"localhost"
"database"	"your_database"
"user"	"your_login"
"pass"	"your_password"
//"timeout"	"0"
"port"	"3306"
}
