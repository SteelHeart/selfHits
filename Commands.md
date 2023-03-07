## Switch vers la base de données active
```
use('SelfHits')
```

## Création des collections
```
db.createCollection('albums')
```

```
db.createCollection('artists')
```

```
db.createCollection('permissions')
```

```
db.createCollection('playlists')
```

```
db.createCollection('roles')
```

```
db.createCollection('songs')
```

```
db.createCollection('tags')
```

```
db.createCollection('users')
```

### Insertion des données

```
db.roles.insert([
  { "name": "Admin", "slug": "admin"},
  { "name": "User", "slug": "user"}
])
```

```
db.permissions.insert([
  {"name": "Create Album", "slug": "created-album", "roles": [ObjectId("64061c4c1f567840c6d0143c")] },
  {"name": "Update Album", "slug": "update-album", "roles": [ObjectId("64061c4c1f567840c6d0143c")] },
  {"name": "Delete Album", "slug": "delete-album", "roles": [ObjectId("64061c4c1f567840c6d0143c")] },
  {"name": "Create Playlist", "slug": "create-playlist", "roles": [ObjectId("64061c4c1f567840c6d0143c"), ObjectId("64061c4c1f567840c6d0143d")] },
  {"name": "Update Playlist", "slug": "update-playlist", "roles": [ObjectId("64061c4c1f567840c6d0143c"), ObjectId("64061c4c1f567840c6d0143d")] },
  {"name": "Delete Playlist", "slug": "delete-playlist", "roles": [ObjectId("64061c4c1f567840c6d0143c"), ObjectId("64061c4c1f567840c6d0143d")] },
])
```

```
db.users.insert([
  {
    "username": "Steelheart",
    "email": "hello@gmail.com",
    "password": "640#61c4c1@fR56s784T0cq6dD0s1f43d",
    "registered_at": new Date(),
    "photo": "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.recia.fr%2Fdefault-avatar-300x300%2F&psig=AOvVaw1Hw8OW-VYNSM7u8s5nURZ3&ust=1678209924999000&source=images&cd=vfe&ved=0CBAQjRxqFwoTCNCW-qXpx_0CFQAAAAAdAAAAABAJ",
    "updated_at": "",
    "role_id": ObjectId('64061c4c1f567840c6d0143c'),
    "playlists": [],
    "bookmarks": [] 
  },

  {
    "username": "King Delano",
    "email": "king@gmail.com",
    "password": "640#61c4c1@fR56s784T0cq6dD0s1f43d",
    "registered_at": new Date(),
    "photo": "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.recia.fr%2Fdefault-avatar-300x300%2F&psig=AOvVaw1Hw8OW-VYNSM7u8s5nURZ3&ust=1678209924999000&source=images&cd=vfe&ved=0CBAQjRxqFwoTCNCW-qXpx_0CFQAAAAAdAAAAABAJ",
    "updated_at": "",
    "role_id": ObjectId('64061c4c1f567840c6d0143c'),
    "playlists": [],
    "bookmarks": [] 
  },

  {
    "username": "Boss Rama",
    "email": "boss@gmail.com",
    "password": "640#61c4c1@fR56s784T0cq6dD0s1f43d",
    "registered_at": new Date(),
    "photo": "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.recia.fr%2Fdefault-avatar-300x300%2F&psig=AOvVaw1Hw8OW-VYNSM7u8s5nURZ3&ust=1678209924999000&source=images&cd=vfe&ved=0CBAQjRxqFwoTCNCW-qXpx_0CFQAAAAAdAAAAABAJ",
    "updated_at": "",
    "role_id": ObjectId('64061c4c1f567840c6d0143d'),
    "playlists": [],
    "bookmarks": [] 
  },

  {
    "username": "Pape DeluxRama",
    "email": "deluxe@gmail.com",
    "password": "640#61c4c1@fR56s784T0cq6dD0s1f43d",
    "registered_at": new Date(),
    "photo": "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.recia.fr%2Fdefault-avatar-300x300%2F&psig=AOvVaw1Hw8OW-VYNSM7u8s5nURZ3&ust=1678209924999000&source=images&cd=vfe&ved=0CBAQjRxqFwoTCNCW-qXpx_0CFQAAAAAdAAAAABAJ",
    "updated_at": "",
    "role_id": ObjectId('64061c4c1f567840c6d0143d'),
    "playlists": [],
    "bookmarks": [] 
  }
])
```

```
db.tags.insert([
  {"name": "Gospel", "slug": "gospel" },
  {"name": "Groove", "slug": "groove" },
  {"name": "Rap", "slug": "rap" },
  {"name": "Rock and roll", "slug": "rock-and-roll" },
  {"name": "Punk", "slug": "punk" },
  {"name": "Folk", "slug": "folk" },
  {"name": "Hip-Hop", "slug": "hip-hop" }
])
```

```
db.artists.insert([
  {
    "name": "Elvis Presley", 
    "slug": "elvis-presley", 
    "biography": "Short professional bios are concise paragraphs that summarise a person's professional background.", 
    "country": "", 
    "registered_at": new Date(), 
    "updated_at": "" 
  },

  {
    "name": "Michael Jackson", 
    "slug": "michael-jackson", 
    "biography": "Short professional bios are concise paragraphs that summarise a person's professional background.", 
    "country": "", 
    "registered_at": new Date(), 
    "updated_at": "" 
  },

  {
    "name": "Céline Dion", 
    "slug": "celine-dion", 
    "biography": "Short professional bios are concise paragraphs that summarise a person's professional background.", 
    "country": "", 
    "registered_at": new Date(), 
    "updated_at": "" 
  },

  {
    "name": "Bob Marley", 
    "slug": "bob-marley", 
    "biography": "Short professional bios are concise paragraphs that summarise a person's professional background.", 
    "country": "", 
    "registered_at": new Date(), 
    "updated_at": "" 
  },

  {
    "name": "Stevie Wonder", 
    "slug": "stevie-wonder", 
    "biography": "Short professional bios are concise paragraphs that summarise a person's professional background.", 
    "country": "", 
    "registered_at": new Date(), 
    "updated_at": "" 
  },

  {
    "name": "James Brown", 
    "slug": "james-brown", 
    "biography": "Short professional bios are concise paragraphs that summarise a person's professional background.", 
    "country": "", 
    "registered_at": new Date(), 
    "updated_at": "" 
  }

])
```

```
db.albums.insert([
  {
    "title": "A New Day : Live in Las Vegas	", 
    "slug": "a-new-day-live-in-las-vegas", 
    "description": "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat eaque accusantium magnam quae dolor sit sunt blanditiis, repellendus pariatur doloribus? Asperiores molestiae debitis deserunt quas voluptate alias sint cum reprehenderit.", 
    "year": "2004", 
    "image": "https://www.francebleu.fr/s3/cruiser-production/2017/07/0c3b29c2-d074-4359-b6bf-e90242b9b654/1200x680_un_peu_de_nous1.jpg", 
    "authors": [
      ObjectId('640624601f567840c6d01451')
    ], 
    "tags": [
      ObjectId('640623181f567840c6d01449'),
      ObjectId('640623181f567840c6d0144d'),
    ], 
    "created_at": new Date(), 
    "updated_at": "" 
  },
  {
    "title": "Au cœur du Stade", 
    "slug": "au-cœur-du-stade", 
    "description": "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat eaque accusantium magnam quae dolor sit sunt blanditiis, repellendus pariatur doloribus? Asperiores molestiae debitis deserunt quas voluptate alias sint cum reprehenderit.", 
    "year": "1999", 
    "image": "https://www.francebleu.fr/s3/cruiser-production/2017/07/0c3b29c2-d074-4359-b6bf-e90242b9b654/1200x680_un_peu_de_nous1.jpg", 
    "authors": [
      ObjectId('640624601f567840c6d01451')
    ], 
    "tags": [
      ObjectId('640623181f567840c6d0144d'),
      ObjectId('640623181f567840c6d01449'),
    ], 
    "created_at": new Date(), 
    "updated_at": "" 
  },
  {
    "title": "Du soleil au cœur", 
    "slug": "du-soleil-au-cœur", 
    "description": "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat eaque accusantium magnam quae dolor sit sunt blanditiis, repellendus pariatur doloribus? Asperiores molestiae debitis deserunt quas voluptate alias sint cum reprehenderit.", 
    "year": "1983", 
    "image": "https://www.francebleu.fr/s3/cruiser-production/2017/07/0c3b29c2-d074-4359-b6bf-e90242b9b654/1200x680_un_peu_de_nous1.jpg", 
    "authors": [
      ObjectId('640624601f567840c6d01451')
    ], 
    "tags": [
      ObjectId('640623181f567840c6d01448'),
      ObjectId('640623181f567840c6d01449'),
    ], 
    "created_at": new Date(), 
    "updated_at": "" 
  },

  {
    "title": "Got to Be There", 
    "slug": "got-to-be-there", 
    "description": "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat eaque accusantium magnam quae dolor sit sunt blanditiis, repellendus pariatur doloribus? Asperiores molestiae debitis deserunt quas voluptate alias sint cum reprehenderit.", 
    "year": "1972", 
    "image": "https://www.lalibre.be/resizer/uhhb-M5SxVR4u1laSq-txvZNp4k=/1200x800/filters:format(jpeg):focal(4052x1303:4062x1293)/cloudfront-eu-central-1.images.arcpublishing.com/ipmgroup/OXUVNUJKYZAIZJG4754UBU3MZE.jpg", 
    "authors": [
      ObjectId('640624601f567840c6d01450'),
    ], 
    "tags": [
      ObjectId('6400e04b12c81df5e36fc4e3'),
      ObjectId('640623181f567840c6d0144e'),
    ], 
    "created_at": new Date(), 
    "updated_at": "" 
  },
  {
    "title": "Ben", 
    "slug": "ben", 
    "description": "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat eaque accusantium magnam quae dolor sit sunt blanditiis, repellendus pariatur doloribus? Asperiores molestiae debitis deserunt quas voluptate alias sint cum reprehenderit.", 
    "year": "1972", 
    "image": "https://www.lalibre.be/resizer/uhhb-M5SxVR4u1laSq-txvZNp4k=/1200x800/filters:format(jpeg):focal(4052x1303:4062x1293)/cloudfront-eu-central-1.images.arcpublishing.com/ipmgroup/OXUVNUJKYZAIZJG4754UBU3MZE.jpg", 
    "authors": [
      ObjectId('640624601f567840c6d01450'),
    ], 
    "tags": [
      ObjectId('6400e04b12c81df5e36fc4e3'),
      ObjectId('640623181f567840c6d0144e'),
    ], 
    "created_at": new Date(), 
    "updated_at": "" 
  },
  {
    "title": "Music & Me", 
    "slug": "music-&-me", 
    "description": "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat eaque accusantium magnam quae dolor sit sunt blanditiis, repellendus pariatur doloribus? Asperiores molestiae debitis deserunt quas voluptate alias sint cum reprehenderit.", 
    "year": "1973", 
    "image": "https://www.lalibre.be/resizer/uhhb-M5SxVR4u1laSq-txvZNp4k=/1200x800/filters:format(jpeg):focal(4052x1303:4062x1293)/cloudfront-eu-central-1.images.arcpublishing.com/ipmgroup/OXUVNUJKYZAIZJG4754UBU3MZE.jpg", 
    "authors": [
      ObjectId('640624601f567840c6d01450'),
    ], 
    "tags": [
      ObjectId('6400e04b12c81df5e36fc4e3'),
      ObjectId('640623181f567840c6d0144e'),
    ], 
    "created_at": new Date(), 
    "updated_at": "" 
  }
  
])
```

```
db.songs.insert([
  {
    "title": "New independant single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "3 min", 
    "size": "3.2", 
    "read_time": "15", 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New independant single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "3 min", 
    "size": "3.2", 
    "read_time": "15", 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New independant single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "3 min", 
    "size": "3.2", 
    "read_time": "15", 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },
  
  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d01455'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d01456'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d01457'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d01458'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d01459'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d0145a'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d01455'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d0145a'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d01456'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d01457'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },
  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d01455'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d01456'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d01457'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d01458'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d01459'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d0145a'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d01455'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d0145a'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d01456'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d01457'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },
  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d01455'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d01456'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d01457'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d01458'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d01459'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d0145a'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d01455'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d0145a'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d01456'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": "15", 
    "album_id": ObjectId('6406caff1f567840c6d01457'), 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },
  
])

```

## Exemples de requêtes
- Nombre de titres par albums
```
db.songs.aggregate([
  {
    $group: {
      _id: '$album_id',
      count: { $sum: 1 }
    }
  }
])
```

- Liste des titres indépendants
```
db.songs.find({ album_id: null }).projection({ title: 1 })
```

- Liste des albums
```
db.albums.find()
```

- Liste des artistes avec leurs albums :
```
db.artists.aggregate([
  {
    $lookup: {
      from: "albums",
      localField: "_id",
      foreignField: "authors",
      as: "albums_by_artists"
    }
  }
])
```

- Liste des abonnés (sans les administrateurs)
```
db.users.find({ "role_id": ObjectId('64061c4c1f567840c6d0143d') })
```

- Création de playlist pour un utilisateur
```
db.playlists.insert({
  "name": "Mes Favoris Rock",
  "slug": "mes-favoris-rock",
  "user_id": ObjectId('640622721f567840c6d01446'),
  "albums": [
    ObjectId('6406caff1f567840c6d01455'), 
    ObjectId('6406caff1f567840c6d01459'), 
    ObjectId('6406caff1f567840c6d01458'), 
  ]
})
```

- Mise à jour de playlist dont l'id vaut : 
```
db.playlists.update({ "_id": ObjectId('640730761f567840c6d0147c') }, { $push :{ "albums": ObjectId('6406caff1f567840c6d01456') } })
```

- Liste des playlists d'un utilisateur
```
db.playlists.find({ "user_id": ObjectId('640622721f567840c6d01446') }).pretty()
```

- Liste des albums datant de 2004 (par exemple)
```
db.albums.find({ "year": "2004" })
```

- Top 10 des musiques les plus lues
```
db.songs.find().sort({ "read_time": -1 }).limit(10)
```
