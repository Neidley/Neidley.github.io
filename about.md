---
layout: page
title: About
permalink: /about/
feature-img: "img/color.png"
---

```ruby
def create
  @post = Post.new(post_params)
  project_id = 'landmarks-183414'
  image_path = @post.image.staged_path
  vision = Google::Cloud::Vision.new project: project_id
  image = vision.image image_path
  image.landmarks.each do |landmark|
    @post.name = landmark.description
        landmark.locations.each do |location|
          @post.location = "#{location.latitude},#{location.longitude}"
        end
  end
```

I left retail to learn Full-Stack Software Development because
I love learning, creating, and analytical thinking.

My past experiences managing a team gave me the invaluable skills of
how to create action plans, identify successful behaviors, and the importance of celebrating small successes everyday.

Everyday I code, I get to learn and create something new everyday and feed my natural curiosity.

I have created 9 projects in the last 9 months since I began this journey.

Most recently using **Google’s Vision API** and **Amazon Web Services**, I created an app called Landmark Discoveries that allows users to identify and save images of landmarks and provides a link to Wikipedia. [Landmark Discoveries](https://landmark-discoveries.herokuapp.com/users/sign_up)

{:.center}
<img src="/img/landmark_discoveries1.png" alt="Landmark Discoveries" style="width: 450px;"/>

I am passionate about continuing to grow into a better developer everyday.

And I couldn't do it without the support of my wife and our two dogs.

{:.center}
![]({{ site.baseurl }}/img/dogs.png)
