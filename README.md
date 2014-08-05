cordova-plugin-dbcopy
=====================

Copy SQLite Database from assets(Android) or Resources(iOS) to App Directory

###Note

**Android**

Put your sqlite database in the *assets* directory.                                                                    


**iOS**

Put your database in *Resources* directory and then Add it in to your Xcode Project.
Right Click on the Resources directory, then click Add files.

###Code

**Copy the database**

In your JavaScript or HTML use the following method to copy your database.

```
window.plugins.sqlDB.copy("demo", copySuccess, copyError);

function copySuccess() {
	// open db and run your queries
}

funtion copyError() {
	// db already exists or problem in copying the db file. Check the Log.
}                    
```

**Check if the database exists**

In your JavaScript or HTML use the following method to check if the database exists.
                                                                                    
```
window.plugins.sqlDB.isDatabaseCreated("demo", databaseCreated, databaseNotCreated);

function databaseCreated() {
	// do your stuff if the database is created.
}

funtion databaseNotCreated() {
	// do your stuff if the database is not created.
}
```

