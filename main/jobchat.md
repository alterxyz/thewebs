---
layout: darkgreen
title: Job Chat
permalink: /jobchat/
---

# Chat with me

<iframe
  src="https://udify.app/chatbot/PgEOgfCdMW6KrNAJ"
  style="width: 80%; height: 80%; min-height: 700px"
  frameborder="0"
  allow="microphone">
</iframe>

<div id="example-container">
    <!-- Initial content here, display simple "hello turnstile" but hidden until turnstile pass -->
    <div style="display: none;">Hello turnstile</div>
</div>

<script src="https://challenges.cloudflare.com/turnstile/v0/api.js?render=explicit"></script>

<script>
// if using synchronous loading, will be called once the DOM is ready
turnstile.ready(function () {
    turnstile.render('#example-container', {
        sitekey: '<0x4AAAAAAAZ8pNrjcHiB7ySq>',
        callback: function(token) {
            console.log(`Challenge Success ${token}`);
        },
    });
});
</script>

[Back to Home](https://youropen.xyz/){: .button}
[My Github](https://about.youropen.xyz){: .button}

[Feedback & Contact with me](https://forms.office.com/r/kv4xuaHxLg){: .button}
[Explore others AI models](https://udify.app/chat/PgEOgfCdMW6KrNAJ){: .button}
