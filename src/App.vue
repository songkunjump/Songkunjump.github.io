<template>
  <div class="main-wrapper">
    <nav class="navbar navbar-expand-lg navbar-dark k-primary fixed-top" id="sideNav">
      <a class="navbar-brand js-scroll-trigger" href="#about">
        <span class="d-block d-lg-none">Start Bootstrap</span>
        <span class="d-none d-lg-block">
          <img class="img-fluid mx-auto" src="./assets/profile.jpg" alt="">
        </span>
      </a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#about">About</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#experience">Experience</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#education">Education</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#skills">Skills</a>
          </li>
    
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#awards">Awards</a>
          </li>
        </ul>
      </div>
    </nav>

    <div class="container-fluid p-0">

      <section class="resume-section p-3 p-lg-5 d-flex d-column" id="about">
        <div class="my-auto">
          <h1 class="mb-0">{{ name }}
            <span class="b-primary">{{ surname }}</span>
          </h1>
          <div class="subheading mb-5">{{ address }}
            <a class='b-primary' href="mailto:name@email.com">{{ email }}</a>
          </div>
          <p class="mb-5">{{ aboutMe }}</p>
          <ul class="list-inline list-social-icons mb-0">
            <li class="list-inline-item">
              <a href="#">
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle fa-stack-2x"></i>
                  <i class="fa fa-facebook fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
            <li class="list-inline-item">
              <a href="#">
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle fa-stack-2x"></i>
                  <i class="fa fa-twitter fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
            <li class="list-inline-item">
              <a href="#">
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle fa-stack-2x"></i>
                  <i class="fa fa-linkedin fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
            <li class="list-inline-item">
              <a href="#">
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle fa-stack-2x"></i>
                  <i class="fa fa-github fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
          </ul>
        </div>
      </section>

      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="experience">
        <div class="my-auto">
          <h2 class="mb-5">Experience</h2>

          <div class="resume-item d-flex flex-column flex-md-row mb-5" v-for="(job, index) in experience" :key=index>
            <div class="resume-content mr-auto">
              <h3 class="mb-0">{{ job.position }}</h3>
              <div class="subheading mb-3">{{ job.company }}</div>
              
              <p v-for="(descripe,index) in job.description" :key=index>{{ descripe }}</p>
            </div>
            <div class="resume-date text-md-right">
              <span class="text-primary">{{ job.startDate }} - {{ job.endDate }}</span>
            </div>
          </div>

        </div>

      </section>

      <section class="resume-section p-3 p-lg-5 flex-column" id="education">
        <div class="my-auto">
          <h2 class="mb-5">Education</h2>

          <div class="resume-item d-flex flex-column flex-md-row mb-5">
            <div class="resume-content mr-auto">
              <h3 class="mb-0">Tulane University</h3>
              <div class="subheading mb-3">Bachelor of Science</div>
              <div>Chemical Engineering</div>
              <p>GPA: 3.85</p>
            </div>
            <div class="resume-date text-md-right">
              <span class="text-primary">August 2017 - December 2020</span>
            </div>
          </div>

          <div class="resume-item d-flex flex-column flex-md-row">
            <div class="resume-content mr-auto">
              <h3 class="mb-0">Bangkok Christian International School</h3>
              <p>GPA: 3.75</p>
            </div>
            <div class="resume-date text-md-right">
              <span class="text-primary">August 2011 - May 2017</span>
            </div>
          </div>

        </div>
      </section>

      <section class="resume-section p-3 p-lg-5" id="skills">
        <div class="my-auto">
          <h2 class="mb-5">Skills</h2>

          <div class="subheading mb-3">Programming Languages &amp; Tools</div>
          <ul class="list-inline list-icons">
            <li class="list-inline-item">
              <i class="devicons devicons-html5"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-css3"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-javascript"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-python"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-sass"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-java"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-bootstrap"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-c++"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-docker"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-git"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-npm"></i>
            </li>
          </ul>

          <div class="subheading mb-3">Relevant skills</div>
          <ul class="fa-ul mb-0">
            <li>
              <i class="fa-li fa fa-check"></i>
              Data Structure</li>
            <li>
              <i class="fa-li fa fa-check"></i>
              Algorithm</li>
            <li>
              <i class="fa-li fa fa-check"></i>
              Machine learning</li>
      
          </ul>
          <div class="subheading mb-3 mt-5">Proficient Software skills</div>
          <div>Python, Numpy, Pandas, Git</div>
          
        </div>
      </section>


      <section class="resume-section p-3 p-lg-5" id="awards">
        <div class="my-auto">
          <h2 class="mb-5">Awards &amp; Certifications</h2>
          <ul class="fa-ul mb-0">
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              CELT Faculty Mentored Undergraduate Research Award                                                               </li>
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              ACSM Personal Trainer Certification
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              Undergraduate Chevron Award
            </li>
            
          </ul>
        </div>
      </section>

    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      title: 'My portfolio',
      name: 'Jump',
      surname: 'Viriyavaree',
      address: '2127 Broadway Street New Orleans, LA 70118',
      email: 'songkunjump@gmail.com',
      aboutMe: 'I am a junior majoring in Engineering at Tulane University, and I am interested in pursuing a career as an software engineer. Currently, I am working as a research assistant in a high performance computing project. In addition, I am also a personal trainer.',
      experience: [
        {
          position: 'Undergraduate Research Assistant, Montemore Lab',                                         
          company: 'Chemical and Biomolecular Engineering Department, Tulane University',
          description: ['•	Write scripts that used NumPy, gnuplotlib, and Matplotlib to create visual models for more than several hundred directories',
          '•	Created Python and Linux scripts to optimize job submission process to super-computer, saving graduate students approximately an hour per submission',
          '•	 Scripted Python software tools to download and organize data from more than 2000 webpages—used by machine learning to replace traditional DFT models for catalyst research',
          '•  Supported 7+ research members by maintaining and improving software library to respond to changes and research requirements'],
          startDate: 'May 2019 ',
          endDate: 'Present'
        },
        {
          position: 'Web Developer Internship ',
          company: 'Backyard Co., Ltd',
          description: ['•	Created a login API for a government news sentimental analytical website using Docker, Flask, Postgres Database, and Cosmic Python principles.',
          '•	Used Vue.js to create user-interface that connects to the API and demonstrates sentimental analysis results and the news content.',
          '•	Designed websites crawlers for more than 10 news websites  for news sentimental analysis. '],
          startDate: 'May 2020',
          endDate: 'August 2020'
        },
        
        {
          position: 'Undergraduate Research Assistant, Pesika Lab',
          company: 'Chemical and Biomolecular Engineering Department, Tulane University',
          description: ['•	Designed gecko feet inspired adhesive pads using Fusion 360 program',
          '•	Created 3D printed wafer holder to reduce set up time for wafer coating process'],
          startDate: 'July 2010',
          endDate: 'December 2011'
        },
        
      ]
    }
  },
  mounted () {
    const $ = this.jquery
    this.$nextTick(() => {
      // our custom jQuery code goes here
      $('a.js-scroll-trigger[href*="#"]:not([href="#"])').click(function () {
        if (location.pathname.replace(/^\//, '') === this.pathname.replace(/^\//, '') && location.hostname === this.hostname) {
          var target = $(this.hash)
          target = target.length ? target : $('[name=' + this.hash.slice(1) + ']')
          if (target.length) {
            $('html, body').animate({
              scrollTop: (target.offset().top)
            }, 1000, 'easeInOutExpo')
            return false
          }
        }
      })
      // Closes responsive menu when a scroll trigger link is clicked
      $('.js-scroll-trigger').click(function () {
        $('.navbar-collapse').collapse('hide')
      })
      // Activate scrollspy to add active class to navbar items on scroll
      $('body').scrollspy({
        target: '#sideNav'
      })
    })
  }
}
</script>

<style>
body {
  font-family: 'Open Sans', serif;
  padding-top: 54px;
  color: #868e96;
}
@media (min-width: 992px) {
  body {
    padding-top: 0;
    padding-left: 17rem;
  }
}
h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: 'Saira Extra Condensed', serif;
  font-weight: 700;
  text-transform: uppercase;
  color: #343a40;
}
h1 {
  font-size: 6rem;
  line-height: 5.5rem;
}
h2 {
  font-size: 3.5rem;
}
.subheading {
  text-transform: uppercase;
  font-weight: 500;
  font-family: 'Saira Extra Condensed', serif;
  font-size: 1.35rem;
}
.list-social-icons a {
  color: #495057;
}
.list-social-icons a:hover {
  color: #BD5D38;
}
.list-social-icons a .fa-lg {
  font-size: 1.75rem;
}
.list-icons {
  font-size: 3rem;
}
.list-icons .list-inline-item i:hover {
  color: #BD5D38;
}
#sideNav .navbar-nav .nav-item .nav-link {
  font-weight: 600;
  text-transform: uppercase;
}
@media (min-width: 992px) {
  #sideNav {
    text-align: center;
    position: fixed;
    top: 0;
    left: 0;
    display: flex;
    flex-direction: column;
    width: 17rem;
    height: 100vh;
  }
  #sideNav .navbar-brand {
    display: flex;
    margin: auto auto 0;
    padding: 0.5rem;
  }
  #sideNav .navbar-brand .img-profile {
    max-width: 10rem;
    max-height: 10rem;
    border: 0.5rem solid rgba(255, 255, 255, 0.2);
  }
  #sideNav .navbar-collapse {
    display: flex;
    align-items: flex-start;
    flex-grow: 0;
    width: 100%;
    margin-bottom: auto;
  }
  #sideNav .navbar-collapse .navbar-nav {
    flex-direction: column;
    width: 100%;
  }
  #sideNav .navbar-collapse .navbar-nav .nav-item {
    display: block;
  }
  #sideNav .navbar-collapse .navbar-nav .nav-item .nav-link {
    display: block;
  }
}
section.resume-section {
  border-bottom: 1px solid #dee2e6;
  padding-top: 5rem !important;
  padding-bottom: 5rem !important;
}
section.resume-section .resume-item .resume-date {
  min-width: none;
}
@media (min-width: 768px) {
  section.resume-section {
    min-height: 100vh;
  }
  section.resume-section .resume-item .resume-date {
    min-width: 18rem;
  }
}
@media (min-width: 992px) {
  section.resume-section {
    padding-top: 3rem !important;
    padding-bottom: 3rem !important;
  }
}

.k-primary {
    background-color: #FFB6C1 !important;
}

.b-primary {
  color: 	#FFB6C1 !important;
}
a {
  color: #FFB6C1 ;
}
a:hover, a:focus, a:active {
  color: #FFB6C1;
}
</style>