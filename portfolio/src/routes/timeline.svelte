<script>
    // Timeline data - easy to edit in one place
    let timelineData = [
      {
        id: "*",
        title: "Introduced to Tech",
        items: [
          "Introduced to gaming console (playstation) on kindergarten",
          "Spent my time playing it"
        ]
      },
      {
        id: "1",
        title: "Elementary School",
        items: [
          "Got a used pc from my uncle, addicted to video games 😭",
          "Love to operate the pc",
          "Learned how to use ms office, photoshop, pencil animation, Corel draw"
        ]
      },
      {
        id: "2",
        title: "Middle School",
        items: [
          "Curious how does HTTP work, I made my first blog with blogspot and wordpress",
          "Made my first app (calculator) with MS Access Visual Basic",
          "Made simple games with gamemaker"
        ]
      },
      {
        id: "3",
        title: "Highschool",
        items: [
          "Learned my first programming language ever! (Turbopascal)",
          "Learned how network works",
          "Learned html, css, js, php",
          "<b>Internship on Elgibor Solution Semarang as a web designer</b>",
          "Started freelance startup wannabe and founded Ubitoes (later renamed as Krotify), Developed various websites including: <a href='suryamediaadvertising.com'><u>suryamediaadvertising.com</u></a>, <a href='istanakeramik.com'><u>istanakeramik.com</u></a>, <a href='adivasa.com'><u>adivasa.com</u></a>"
        ]
      },
      {
        id: "4",
        title: "College",
        items: [
          "Majored in Computer Science, Graduated in 2024 with 3.4 GPA",
          "Built several full-stack web applications",
          "Built ERP for Istana Keramik Purworejo",
          "Participated in coding competitions",
          "Joined <u classname='text-blue-600'><a href='https://grow.google/intl/id_id/bangkit/?tab=machine-learning'>Bangkit Academy led by Google, Goto, Traveloka</a></u> as a Cloud Computing Cohort",
          "Created the beloved <u classname='text-blue-600'><a href='https://github.com/Techwaste'>Techwaste</u>, E-waste management system</a> with teams! (as the infra / devops)",
          "Joined <u classname='text-blue-600'><a href='https://grow.google/intl/id_id/bangkit/?tab=machine-learning'>Bangkit Academy led by Google, Goto, Traveloka</a></u> as a Mobile Developer Cohort Graduated with distinction! Scored top 10% from over thousands cohorts",
          "Created <a href='https://github.com/Animalink'><u>Animalink</u></a>, Moderated animal marketplace (as the mobile developer)",
        ]
      },
      {
        id: "5",
        title: "After College - 2024",
        items: [
            "Became mentor for <a href='https://grow.google/intl/id_id/bangkit/?tab=machine-learning'><u>Bangkit Academy</u> helped Bangkit to achieved 91% graduation rate</a>",
            "Working as a fullstack developer for Corporate Training and Development Department @ PT. Sukanda Djaya - Diamond Group",
            "Created Kahoot uid generator for Diamond Group",
            "Modified E-learning for Diamond Group for better readibility and user experience",
            "Created product knowledge exam system with gamification features such as reward exchange and more. Also created monthly report with charts dashboard for the exam system",
            "Still active freelancing with my beloved <a href='krotify.com'><u>krotify.com</u></a>"

        ]
      }
    ];
  
    // Function to add a new timeline entry
    function addTimelineEntry() {
      const newId = timelineData.length + 1;
      timelineData = [...timelineData, {
        id: newId.toString(),
        title: "New Entry",
        items: ["Add your details here"]
      }];
    }
  </script>
  
  <h1 class="text-5xl text-center mt-10">My Tech Journey</h1>
  <p class="text-center mt-2">How do I know tech?</p>
  
  <div class="flex justify-center items-center p-10 lg:py-10">
    <div class="max-w-2xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="border-l-2 border-gray-300">
        {#each timelineData as entry}
          <div class="mb-8">
            <div class="flex items-center">
              <div class="bg-black w-16 h-8 rounded flex items-center justify-center -ml-4">
                <span class="text-white font-bold">{entry.id}</span>
              </div>
              <h2 class="ml-6 text-lg sm:text-xl font-semibold text-gray-700">{entry.title}</h2>
            </div>
            <div class="ml-20 mt-2">
              <p class="text-gray-600 text-sm sm:text-base">
                {#each entry.items as item}
                  - {@html item}<br>
                {/each}
              </p>
            </div>
          </div>
        {/each}
      </div>
      
         </div>
  </div>