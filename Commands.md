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
db.users.insert([
  {
    "username": "Steelheart",
    "email": "hello@gmail.com",
    "password": "640#61c4c1@fR56s784T0cq6dD0s1f43d",
    "registered_at": new Date(),
    "photo": "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.recia.fr%2Fdefault-avatar-300x300%2F&psig=AOvVaw1Hw8OW-VYNSM7u8s5nURZ3&ust=1678209924999000&source=images&cd=vfe&ved=0CBAQjRxqFwoTCNCW-qXpx_0CFQAAAAAdAAAAABAJ",
    "updated_at": "",
    "role": "admin",
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
    "role": "user",
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
    "role": "user",
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
    "role": "user",
    "playlists": [],
    "bookmarks": [] 
  }
])
```

```
db.tags.insert([
  {"name": "Gospel", ref: 1,  "slug": "gospel" },
  {"name": "Groove", ref: 2,  "slug": "groove" },
  {"name": "Rap", ref: 3,  "slug": "rap" },
  {"name": "Rock and roll", ref: 4,  "slug": "rock-and-roll" },
  {"name": "Punk", ref: 5,  "slug": "punk" },
  {"name": "Folk", ref: 6,  "slug": "folk" },
  {"name": "Hip-Hop", ref: 7,  "slug": "hip-hop" }
])
```

```
db.artists.insert([
  {
    "name": "Elvis Presley", 
    "ref": 1,
    "slug": "elvis-presley", 
    "biography": "Short professional bios are concise paragraphs that summarise a person's professional background.", 
    "country": "", 
    "registered_at": new Date(), 
    "updated_at": "" 
  },

  {
    "name": "Michael Jackson", 
    "ref": 2,
    "slug": "michael-jackson", 
    "biography": "Short professional bios are concise paragraphs that summarise a person's professional background.", 
    "country": "", 
    "registered_at": new Date(), 
    "updated_at": "" 
  },

  {
    "name": "Céline Dion", 
    "ref": 1,
    "slug": "celine-dion", 
    "biography": "Short professional bios are concise paragraphs that summarise a person's professional background.", 
    "country": "", 
    "registered_at": new Date(), 
    "updated_at": "" 
  },

  {
    "name": "Bob Marley", 
    "ref": 3,
    "slug": "bob-marley", 
    "biography": "Short professional bios are concise paragraphs that summarise a person's professional background.", 
    "country": "", 
    "registered_at": new Date(), 
    "updated_at": "" 
  },

  {
    "name": "Stevie Wonder", 
    "ref": 4,
    "slug": "stevie-wonder", 
    "biography": "Short professional bios are concise paragraphs that summarise a person's professional background.", 
    "country": "", 
    "registered_at": new Date(), 
    "updated_at": "" 
  },

  {
    "name": "James Brown", 
    "ref": 5,
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
    "ref": 1,
    "description": "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat eaque accusantium magnam quae dolor sit sunt blanditiis, repellendus pariatur doloribus? Asperiores molestiae debitis deserunt quas voluptate alias sint cum reprehenderit.", 
    "year": "2004", 
    "image": "https://www.francebleu.fr/s3/cruiser-production/2017/07/0c3b29c2-d074-4359-b6bf-e90242b9b654/1200x680_un_peu_de_nous1.jpg", 
    "authors": [
      {"ref": 1},
      {"ref": 2}
    ], 
    "tags": [
      {ref: 2},
      {ref: 4},
      {ref: 7},
    ], 
    "created_at": new Date(), 
    "updated_at": "" 
  },
  {
    "title": "Au cœur du Stade", 
    "slug": "au-cœur-du-stade", 
    "ref": 2,
    "description": "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat eaque accusantium magnam quae dolor sit sunt blanditiis, repellendus pariatur doloribus? Asperiores molestiae debitis deserunt quas voluptate alias sint cum reprehenderit.", 
    "year": "1999", 
    "image": "https://www.francebleu.fr/s3/cruiser-production/2017/07/0c3b29c2-d074-4359-b6bf-e90242b9b654/1200x680_un_peu_de_nous1.jpg", 
    "authors": [
      {"ref": 4},
      {"ref": 2}
    ], 
    "tags": [
      {ref: 1},
      {ref: 4},
      {ref: 9},
    ], 
    "created_at": new Date(), 
    "updated_at": "" 
  },
  {
    "title": "Du soleil au cœur", 
    "slug": "du-soleil-au-cœur", 
    "ref": 3,
    "description": "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat eaque accusantium magnam quae dolor sit sunt blanditiis, repellendus pariatur doloribus? Asperiores molestiae debitis deserunt quas voluptate alias sint cum reprehenderit.", 
    "year": "1983", 
    "image": "https://www.francebleu.fr/s3/cruiser-production/2017/07/0c3b29c2-d074-4359-b6bf-e90242b9b654/1200x680_un_peu_de_nous1.jpg", 
    "authors": [
      {"ref": 1},
      {"ref": 5}
    ], 
    "tags": [
      {ref: 11},
      {ref: 4},
      {ref: 6},
    ], 
    "created_at": new Date(), 
    "updated_at": "" 
  },

  {
    "title": "Got to Be There", 
    "slug": "got-to-be-there", 
    "ref": 4,
    "description": "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat eaque accusantium magnam quae dolor sit sunt blanditiis, repellendus pariatur doloribus? Asperiores molestiae debitis deserunt quas voluptate alias sint cum reprehenderit.", 
    "year": "1972", 
    "image": "https://www.lalibre.be/resizer/uhhb-M5SxVR4u1laSq-txvZNp4k=/1200x800/filters:format(jpeg):focal(4052x1303:4062x1293)/cloudfront-eu-central-1.images.arcpublishing.com/ipmgroup/OXUVNUJKYZAIZJG4754UBU3MZE.jpg", 
    "authors": [
      {"ref": 4},
      {"ref": 1}
    ], 
    "tags": [
      {ref: 10},
      {ref: 3},
      {ref: 7},
    ], 
    "created_at": new Date(), 
    "updated_at": "" 
  },
  {
    "title": "Ben", 
    "slug": "ben", 
    "ref": 5,
    "description": "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat eaque accusantium magnam quae dolor sit sunt blanditiis, repellendus pariatur doloribus? Asperiores molestiae debitis deserunt quas voluptate alias sint cum reprehenderit.", 
    "year": "1972", 
    "image": "https://www.lalibre.be/resizer/uhhb-M5SxVR4u1laSq-txvZNp4k=/1200x800/filters:format(jpeg):focal(4052x1303:4062x1293)/cloudfront-eu-central-1.images.arcpublishing.com/ipmgroup/OXUVNUJKYZAIZJG4754UBU3MZE.jpg", 
    "authors": [
      {"ref": 3},
      {"ref": 5}
    ], 
    "tags": [
      {ref: 7},
      {ref: 4},
      {ref: 11},
    ], 
    "created_at": new Date(), 
    "updated_at": "" 
  },
  {
    "title": "Music & Me", 
    "slug": "music-&-me", 
    "ref": 6,
    "description": "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat eaque accusantium magnam quae dolor sit sunt blanditiis, repellendus pariatur doloribus? Asperiores molestiae debitis deserunt quas voluptate alias sint cum reprehenderit.", 
    "year": "1973", 
    "image": "https://www.lalibre.be/resizer/uhhb-M5SxVR4u1laSq-txvZNp4k=/1200x800/filters:format(jpeg):focal(4052x1303:4062x1293)/cloudfront-eu-central-1.images.arcpublishing.com/ipmgroup/OXUVNUJKYZAIZJG4754UBU3MZE.jpg", 
    "authors": [
      {"ref": 3},
      {"ref": 2}
    ], 
    "tags": [
      {ref: 3},
      {ref: 8},
      {ref: 13},
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
    "read_time": 15, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New independant single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "3 min", 
    "size": "3.2", 
    "read_time": 15, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New independant single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "3 min", 
    "size": "3.2", 
    "read_time": 15, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },
  
  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 15, 
    "album_id": {ref: 6}, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 15, 
    "album_id": {ref: 8}, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 15, 
    "album_id": {ref: 3}, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 15, 
    "album_id": {ref: 4}, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 15, 
    "album_id": {ref: 1}, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 15, 
    "album_id": {ref: 7}, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 15, 
    "album_id": {ref: 8}, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 15, 
    "album_id": {ref: 9}, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 15, 
    "album_id": {ref: 5}, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 15, 
    "album_id": {ref: 12}, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },
  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 15, 
    "album_id": {ref: 4}, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 201, 
    "album_id": {ref: 6}, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 15, 
    "album_id": {ref: 8}, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 807, 
    "album_id": {ref: 1}, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 15, 
    "album_id": {ref: 3}, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 502, 
    "album_id": {ref: 4}, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 15, 
    "album_id": {ref: 2}, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 5, 
    "album_id": {ref: 7}, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 65, 
    "album_id": {ref: 11}, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 15, 
    "album_id": {ref: 10}, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },
  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 415, 
    "album_id": {ref: 6}, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 15, 
    "album_id": {ref: 1}, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 15, 
    "album_id": {ref: 7}, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 15, 
    "album_id": {ref: 8}, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 121, 
    "album_id": {ref: 12}, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 15, 
    "album_id": {ref: 2}, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 12, 
    "album_id": {ref: 3}, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 15, 
    "album_id": {ref: 7}, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 25, 
    "album_id": {ref: 7}, 
    "registerd_at": new Date(), 
    "registerd_by": "" 
  },

  {
    "title": "New single", 
    "url": "https://www.rireetchansons.fr/podcasts/lappel-trop-con/augmentation-fromagere-l-appel-trop-con-de-rire-chansons-1", 
    "duration": "4 min", 
    "size": "3.6", 
    "read_time": 105, 
    "album_id": {ref: 7}, 
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

- Liste des albums avec leurs authors et categories (tags) associées :
```
db.albums.aggregate([
  {
    $lookup: {
      from: "artists",
      "let": {"uid": "$ref"},
      pipeline: [
        {
          "$match": {
            "$expr": {
              "$in": ["$$uid", "$authors.ref"],  
            },
          },
        },
      ],
      as: "registered_albums"
    }
  }
])
```

- Liste des abonnés (sans les administrateurs)
```
db.users.find({ "role": "user") })
```

- Création de playlist pour un utilisateur
```
db.playlists.insertOne({
  "name": "Mes Favoris Rock",
  "slug": "mes-favoris-rock",
  "user_id": ObjectId('640622721f567840c6d01446'),
  "albums": [
    {ref: 2},
    {ref: 4},
    {ref: 7}, 
  ]
})
```

- Mise à jour de playlist dont l'id vaut : 
```
db.playlists.updateOne({ 
  "_id": ObjectId('64074d9b1f567840c6d014c8') 
  }, 
  { 
    $push :{ "albums": {ref: 7} } 
  })
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
db.songs.find().projection({"_id": 0, "title": 1, "read_time": 1}).sort({ "read_time": -1}).limit(10)
```

-	Requête de lecture étoile : Recherche d’albums et/ou de titres spécifiques
```
db.songs.find().limit(10)
```
