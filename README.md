vidtomp3-api-parser-android
===========================

vidtomp3.com API XML Parser for Android

How to use this stuff
--------------

##### How to use this parser in your project

* Add Vidtomp3parser.java to your Project
* Send a POST request to http://www.vidtomp3.com/cc/conversioncloud.php and extract *statusurl* from the response
* Write some code:
```java

...
InputStream instream = httpEntity.getContent(); //Get Inputstream from response
Vidtomp3parser parser = new Vidtomp3parser();
HashMap<String, String> data = parser.parse(instream);
```

* Now you can access **_status_**, **_videoid_**, **_file_**, **_downloadurl_** and **_filesize_** tags.

```java

/* Data */
private String title;
private String videoid;
private String mp3url;
private String status;
private String downloadsize;

...

status = data.get("status");
if (status.equals("finished")) {
  videoid = data.get("videoid");
  title = data.get("file");
  mp3url = data.get("downloadurl");
  downloadsize = data.get("filesize");
  }
```

* Done!

Check out my code!
--------------

* Clone this repo below

```sh
https://github.com/ingamedeo/DatabaseTest.git
```

License
----

DWTFYW (Explanation below)


###### Do What the Fuck You Want
