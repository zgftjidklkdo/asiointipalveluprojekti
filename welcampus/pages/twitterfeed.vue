<template>
  <v-app>
    <v-content>
      <v-container>
        <body>
            <h1>Twitter Feed</h1>
            <a
            class="twitter-timeline"
            data-lang="fi"
            data-width="570"
            data-height="680"
            data-theme="dark"
            data-link-color="#FAB81E"
            href="https://twitter.com/treduofficial?ref_src=twsrc%5Etfw">
            Tweets by treduofficial
            </a>
            <div class="textblock">
                <h2>Privacy Policy</h2>
                <p>
                Personal data that you submit to us (for example, during the process of registration), such as name and E-Mail address or other personal information will not be disclosed to anyone besides you and us.
                </p>
                <p>
                We will not use the data in any way, except to register you here and let you submit posts, comments and such.
                </p>
            </div>
            <div class="textblock">
                <h2>Cookie Policy</h2>
                <p>
                Cookies are small files that contain information about your browsing activity. When you visit our website, we place a cookie on your device. We only place cookies on your device after you clearly agree that we can do that. With cookies we aim to make your experience on our website better.
                </p>
                <p>
                Your login will happen automatically, and you’ll receive suggestions based on your activities. You can disable cookies on your profile settings.
                </p>
            </div>
            <div class="textblock">
                <h2>What does Cookie mean and why are Users warned of them?</h2>
                <p>
                A cookie is a file that a website stores on your computer via your browser, it contains information about your browsing activity. It can be used for many useful things, such as letting you log in quicker.
                </p>
                <p>
                Cookies aren’t malicious by nature, but they can be used in questionable ways, as they store your personal browser activity data. It makes it able for companies to build a profile of your activities and customize their advertisements specifically to you, which can be manipulating.
                </p>
                <p>
                People in the EU are warned of cookies, because of that and the EU also websites that are based here to always get the permission of the user, before placing cookies on their devices.
                </p>
            </div>
        </body>
        <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
      </v-container>
    </v-content>
  </v-app>
</template>

<style>
  body  {
    text-align: center;
  }
  h1 {
    font-size: 1.25in;
    color: #4079d6;
    margin-bottom: 25px;
  }
  .textblock {
    border-radius: 5px;
    background-color: #e8ecf2;
    border-style: groove;
    border-width: 4px;
    margin: 45px 175px 30px 175px;
    padding: 20px 50px 20px 50px;
    height: auto;
  }
  .textblock h2 {
    font-size: 0.35in;
    margin-top: 10;
  }
  .textblock p {
    margin-left: 0.8in;
    margin-right: 0.8in;
  }
</style>

<script>
export default {
  name: 'Twitterfeed',
  data() {
    return {
      //
    }
  }
}
</script>
