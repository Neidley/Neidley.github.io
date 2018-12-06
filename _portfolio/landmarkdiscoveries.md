---
layout: post
title: Landmark Discoveries
thumbnail-path: "img/landmarkdiscoveries2.png"
short-description: AWS S3 Buckets for image storage,<br/> Paperclip gem for image upload,<br/> Google Vision API for landmark identification.<br/> Built on Rails.
---

{:.center}
<img src="/img/landmarkdiscoveries2.png" alt="Landmark Discoveries" style="width: 450px;"/>

{:.center}
[VISIT LIVE](https://landmark-discoveries.herokuapp.com/users/sign_up)

#### Landmark Discoveries uses

* _[Google Cloud Vision (GVC) API](https://cloud.google.com/vision/docs/), capable of identifying landmarks
  around the world_
* _[googleauth API](https://developers.google.com/maps/documentation/maps-static/intro), takes the longitude and latitude from the GVC API to show
  location of the landmark on a map_
* _[paperclip](https://github.com/thoughtbot/paperclip) Ruby gem to upload the image_
* _[AWS Buckets](https://aws.amazon.com/sdk-for-ruby/) for image storage_
* _[devise](https://github.com/plataformatec/devise) for authentication and create, read, update, and delete users_
* _[Figaro](https://github.com/laserlemon/figaro) for Heroku deployment configuration_
