<script>
    let blogs = [
      {
        author: "NintenGunner",
        profilePic: "blogger pfps/nintengunner.jpg",
        bio: "Website Maintainer, Graphic Designer",
        posts: [
          {
            title: "Sand Box?",
            date: "Jul 23, 2023",
            content: `You know, it always feels funny whenever somebody acknowledges Ricochet in a big way. And when I mean that, I mean as in "somebody remaking Ricochet in s&box's developer preview". No, seriously.
              <br><br>
              <img src="ricochet sbox.png" alt="Ricochet in s&box"><br><br>
              I played it for a bit, and it feels... imperfect. Of course, s&box is still in heavy development, so of course the recreation inside of it would feel imperfect. But still, some of the items are solid black, like the powerups or the decap disc, and the triple shot goes out to the sides instead of being a shotgun spread. The models ARE correct, though. 
              <br><br>
              Physics is a little off, too. I couldn't do the airstrafing or strafewalking that I usually could, or at least I wasn't able to make effective use of it. But either way, it's still a neat curiosity... and somehow deader than the actual Ricochet. I'll blame that on it being in s&box, though, as it isn't exactly big for... obvious reasons.`,
          },
          {
            title: "So It Begins",
            date: "Jan 7, 2023",
            content: `Well, here we are. As of writing this, it's day 2 since we've begun work on this project, and very high strides have been made. 
              <br><br>
              I almost find it funny about how I ended up lucky enough to hop onto Ricochet when Dog set up that server. But I'd say that it was the greatest coincidence I've been a part of. Ricochet is easily one of my new favorites ever since I started playing it this week. Of course, we all know the meme that Ricochet is the worst Valve game and that it's dead, and while that may be partially true, I've grown immediately fond of how oddly fun Ricochet is. Everyone else on the project has too.
              <br><br>
              And being able to help run a fansite for Ricochet that's tied to a server is one of the most exciting things I've ever done in regards to Valve stuff. I sincerely hope that this whole project gets somewhere, and that some interest in Ricochet will come to fruition, because we sure as hell are interested in Ricochet.
              <br><br>
              If you wanna join the server, check it out <a href="steam://connect/69.4.239.4:27015">here.</a>
              <br><br>
              And while you're at it, check out the <a href="manual">manual</a> I wrote for this site.
              <br><br>
              Thanks for checking this place out.`,
          },
        ],
      },
      {
        author: "ReactedDrop",
        profilePic: "blogger pfps/reacteddrop.jpg",
        bio: "Graphic Designer",
        posts: [
          {
            title: "Lorem Ipsum",
            date: "Feb 16, 2025",
            content: `I am making up words. I'm sorry.`,
          },
        ],
      },
      {
        author: "ImGreenOnline",
        profilePic: "blogger pfps/imgreenonline.jpg",
        bio: "Server Hoster",
        posts: [
          {
            title: "First Impressions of Ricochet Revival",
            date: "Feb 16, 2025",
            content: `I titled it this because I like the strokes, and yk, first impressions of earth.`,
          },
        ],
      },
      {
        author: "The Basic Dog",
        profilePic: "blogger pfps/thebasicdog.jpg",
        bio: "Owner of the Server, Creator of Ricochet Revival",
        posts: [
          {
            title: "Ricochet For all",
            date: "Feb 16, 2025",
            content: `That's what i think basic dog thought when making ricochet revival`,
          },
        ],
      },
    ];
  
    let visibleAuthor = null;
  
    function toggleAuthorPosts(author) {
      visibleAuthor = visibleAuthor === author ? null : author;
    }
  </script>
  
  <main>
    <h1><img src="ricosite blog.png" alt="Ricochet Revival Blog" /></h1>
  
    {#each blogs as blog}
      <section>
        <div class="profile" on:click={() => toggleAuthorPosts(blog.author)}>
          <img
            src={blog.profilePic}
            alt="{blog.author} profile"
            width="60"
            height="60"
          />
          <div>
            <h2>{blog.author}</h2>
            <p>{blog.bio}</p>
          </div>
        </div>
  
        {#if visibleAuthor === blog.author}
          {#each blog.posts as post}
            <div class="post">
              <h3>{post.title}</h3>
              <span>{post.date}</span>
              <div class="content">{@html post.content}</div>
            </div>
          {/each}
        {/if}
      </section>
    {/each}
  
    <div class="footer-message">
      <p>Click on the author's name to view their posts</p>
    </div>
  
    <a href="/" class="back-link">
      <img
        src="arrowanim.gif"
        style="transform: scaleX(-1);"
        height="20"
        alt="Back to Homepage"
      />
      <img src="main.png" height="32" alt="Main Icon" />
    </a>
  </main>
  
  <style>
    main {
      max-width: 900px;
      margin: 20px auto;
      padding: 20px;
      background-color: #000;
      border-radius: 8px;
    }
  
    h1 {
      color: #f0ad4e;
      text-align: center;
      margin-bottom: 30px;
    }
  
    h1 img {
      max-width: 100%;
      height: auto;
      display: block;
      margin: 0 auto;
    }
  
    .profile {
      display: flex;
      align-items: center;
      margin-bottom: 30px;
      cursor: pointer;
    }
  
    .profile img {
      border-radius: 50%;
      margin-right: 15px;
    }
  
    .profile div {
      display: flex;
      flex-direction: column;
    }
  
    .profile h2 {
      color: #f0ad4e;
      margin: 0;
      font-size: 1.4em;
      text-align: left;
    }
  
    .profile p {
      color: #fff;
      margin-top: 5px;
      font-size: 1em;
      text-align: left;
    }
  
    .post {
      background-color: #000;
      margin-bottom: 20px;
      padding: 15px;
      border-radius: 5px;
    }
  
    .post h3 {
      margin-top: 0;
    }
  
    .content {
      font-size: 1.1em;
      margin-top: 10px;
    }
  
    .back-link {
      display: block;
      text-align: center;
      margin-top: 40px;
    }
  
    a {
      color: #f0ad4e;
      text-decoration: none;
    }
  
    a:hover {
      text-decoration: underline;
    }
  
    @media (max-width: 600px) {
      h1 {
        font-size: 1.5em;
      }
  
      h1 img {
        max-width: 90%;
        margin: 0 auto;
      }
  
      .content {
        font-size: 1em;
      }
  
      .profile h2 {
        font-size: 1.2em;
      }
    }
  </style>
  