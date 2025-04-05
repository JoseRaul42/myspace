<script>
  import { Github } from 'lucide-svelte';
  import {Linkedin} from 'lucide-svelte';
  let screenWidth;
  let videoUrl = "https://www.youtube.com/embed/videoseries?si=RTOfLe2PF0c9TXVm&list=PL6DxpDO3tvw2IyiNr0rGwX4hhp5FhJy8a&autoplay=1"; // Replace with your desired YouTube video URL
</script>

<style>
body {
  margin: 0;
  padding: 0;
  overflow-x: hidden; /* Prevent horizontal overflow */
}

.background {
  background-image: url('/giphy.webp'); /* Replace with your animated image */
  background-size: 30%; /* Adjust the size to your desired smaller tile size */
  background-repeat: repeat; /* Tiling effect */
  position: fixed; /* Fix the background so it covers the screen */
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: -1;
  animation: slide 10s linear infinite; /* Adjust the animation as needed */
}

@keyframes slide {
  from {
    background-position: 0 0;
  }
  to {
    background-position: -100% 0;
  }
}



</style>

<div class="background"></div>

<body>
<iframe 
  src={videoUrl} 
  title="YouTube video player" 
  class="youtube-video"
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
  allowfullscreen>
</iframe>

<div class="aboutme">
  <h2 style="font-weight: bold">About Me
    <a href="https://www.linkedin.com/in/jose-valois-29a120213" target="_blank" style="margin-left: 10px; display: inline-flex; align-items: center; text-decoration: none; color: inherit;">
      <span style="display: inline-flex; align-items: center; justify-content: center; width: 50px; height: 50px;  border: 0.1px solid white; border-radius: 9%; background-color: rgba(56, 38, 250, 0.8);">
        <Linkedin size="18" color="white" style="fill: white;"  />
      </span>
    </a>
  </h2>
  <p>Self Taught Developer💻👾💾</p>
  <article class="space-y-12">
    <h5>
      I’m a Full Stack Engineer with expertise in SQL, databases, and developing ETL pipelines. I’ve been programming and bringing my ideas to life through code since 2018.
    </h5>
    <h5>
      Adept at working with SQL, C#, .NET, Powershell, and AzureDevOps. I’ve successfully delivered scalable data solutions and backend software application support. My experience was built delivering complex, data-driven projects where I applied engineering best practices to deliver production-ready implementations and data conversions.
    </h5>
    <h5>
      In my free time, I enjoy exploring use cases for locally hosted LLMs on consumer-grade hardware for edge computing through personal projects, I enjoy discovering new music, and playing Marvel Rivals. I'm actively seeking data-focused engineering or software engineering roles on forward-thinking teams.
    </h5>
  </article>
  
</div>

<div class="projects">
  <h2>
    Github Projects
    <a href="https://github.com/joseraul42" target="_blank" style="margin-left: 10px; display: inline-flex; align-items: center; text-decoration: none; color: inherit;">
      <span style="display: inline-flex; align-items: center; justify-content: center; width: 50px; height: 50px; border-radius: 50%; background-color: #333;">
        <Github size="24" color="white"  />
      </span>
    </a>
  </h2> 
 
  <h3>
    <a href="https://github.com/joseraul42/Aegis" target="_blank" style="text-decoration: none; color: inherit;  ">
      Aegis
      <span style="font-size:1rem; color:cyan  ">
        &larr;  click me 
      </span>
    </a>
  </h3>
  <p style="font-size: 1.4rem;">Working on this project taught me a lot about efficiently parsing JSON from APIs, which was crucial for interpreting data from my local LLM instance. I parsed APIs in OpenAI format to make it possible for my console application to communicate with my local LLM server. I also learned how to optimize LLM performance on my local hardware to speed up query processing. Additionally, setting up and fine-tuning my Snort Intrusion Detection System (IDS) rules helped me reduce false positives. I also used Docker to easily set up a Milvus standalone database to connect with my application. All of these steps were necessary to accomplish my goal of being able to generate real-time reports leveraging AI on Alert Logs files and ask questions about the alert logs in natural language.</p>
      
  <h3>
    <a href="https://github.com/joseraul42/myspace" target="_blank" style="text-decoration: none; color: inherit;">
    MySpace
    <span style="font-size:1rem; color:cyan  ">
      &larr;  click me 
    </span>
    </a>
  </h3>
  <p style="font-size: 1.4rem;">This was a fun weekend project, inspired by my past experiences customizing my Myspace page during an earlier era of social media. I was able to learn a lot about reactive web design. This was developed using Svelte, my preferred front-end framework.</p>
         
  <h3>
    <a href="https://github.com/joseraul42/DataRecovery" target="_blank" style="text-decoration: none; color: inherit;">
    DataRecovery
    <span style="font-size:1rem; color:cyan  ">
      &larr;  click me 
    </span>
    </a>
  </h3>
  <p style="font-size: 1.4rem;">Data Recovery is a Python-based command-line tool designed to recover deleted files from various storage devices. Utilizing byte-level scanning, it identifies files based on their unique signatures, offering a chance to restore files that have been inadvertently deleted or lost.</p>
</div> 
</body>

<footer>
<h1>&copy; Powered by Me</h1>
</footer>
