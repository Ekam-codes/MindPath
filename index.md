<!DOCTYPE html>  
<html lang="en">  
<head>  
  <meta charset="UTF-8">  
  <meta name="viewport" content="width=device-width, initial-scale=1.0">  
  <title>MindPath - Career & Personality Assessment Hub</title>  
  
  <!-- Google AdSense Code -->  
  <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-7799118836102656"  
     crossorigin="anonymous"></script>  
  
  <!-- Tailwind CSS & Lucide Icons -->  
  <script src="https://cdn.tailwindcss.com"></script>  
  <script src="https://unpkg.com/lucide@latest"></script>  
</head>  
<body class="bg-slate-900 text-slate-100 min-h-screen font-sans flex flex-col justify-between">  
  
  <!-- Header -->  
  <header class="border-b border-slate-800 bg-slate-900/50 backdrop-blur sticky top-0 z-50">  
    <div class="max-w-4xl mx-auto px-4 py-4 flex items-center justify-between">  
      <div class="flex items-center gap-2">  
        <div class="p-2 bg-indigo-600/20 text-indigo-400 rounded-lg">  
          <i data-lucide="compass" class="w-6 h-6"></i>  
        </div>  
        <span class="text-xl font-bold tracking-tight bg-gradient-to-r from-indigo-400 to-violet-400 bg-clip-text text-transparent">MindPath</span>  
      </div>  
      <span class="text-xs font-semibold px-2.5 py-1 bg-indigo-500/10 text-indigo-400 border border-indigo-500/20 rounded-full">Pro Assessment</span>  
    </div>  
  </header>  
  
  <!-- Main Container -->  
  <main class="max-w-4xl mx-auto px-4 py-8 flex-grow w-full">  
      
    <!-- View 1: Hub Home -->  
    <div id="view-home" class="space-y-8">  
      <div class="text-center space-y-4 max-w-2xl mx-auto">  
        <h1 class="text-3xl md:text-5xl font-extrabold tracking-tight text-white">Discover Your Authentic Career & Personality Path</h1>  
        <p class="text-slate-400 text-base md:text-lg">Take our multi-dimensional career assessment powered by global vocational models (RIASEC) to match with diverse modern professions.</p>  
      </div>  
  
      <div class="grid md:grid-cols-2 gap-6 pt-4">  
        <!-- Card 1 -->  
        <div class="bg-slate-800/50 border border-slate-700/50 rounded-2xl p-6 hover:border-indigo-500/50 transition-all group flex flex-col justify-between">  
          <div class="space-y-4">  
            <div class="w-12 h-12 bg-indigo-600/20 text-indigo-400 rounded-xl flex items-center justify-center group-hover:scale-110 transition-transform">  
              <i data-lucide="briefcase" class="w-6 h-6"></i>  
            </div>  
            <h2 class="text-xl font-bold text-white">Full-Spectrum Career Quiz</h2>  
            <p class="text-slate-400 text-sm">Analyze whether you fit best in Business, Healthcare, Creative Media, Engineering, Public Service, Law, or Education.</p>  
          </div>  
          <button onclick="startQuiz('career')" class="mt-6 w-full py-3 bg-indigo-600 hover:bg-indigo-500 text-white font-semibold rounded-xl transition flex items-center justify-center gap-2">  
            Start Career Quiz <i data-lucide="arrow-right" class="w-4 h-4"></i>  
          </button>  
        </div>  
  
        <!-- Card 2 -->  
        <div class="bg-slate-800/50 border border-slate-700/50 rounded-2xl p-6 hover:border-violet-500/50 transition-all group flex flex-col justify-between">  
          <div class="space-y-4">  
            <div class="w-12 h-12 bg-violet-600/20 text-violet-400 rounded-xl flex items-center justify-center group-hover:scale-110 transition-transform">  
              <i data-lucide="user-check" class="w-6 h-6"></i>  
            </div>  
            <h2 class="text-xl font-bold text-white">Work Dynamics Test</h2>  
            <p class="text-slate-400 text-sm">Discover how your thinking style, leadership traits, and stress response impact your work culture ideal.</p>  
          </div>  
          <button onclick="startQuiz('personality')" class="mt-6 w-full py-3 bg-violet-600 hover:bg-violet-500 text-white font-semibold rounded-xl transition flex items-center justify-center gap-2">  
            Start Personality Test <i data-lucide="arrow-right" class="w-4 h-4"></i>  
          </button>  
        </div>  
      </div>  
    </div>  
  
    <!-- View 2: Quiz View -->  
    <div id="view-quiz" class="hidden max-w-2xl mx-auto space-y-6">  
      <div class="flex items-center justify-between text-sm text-slate-400">  
        <span id="quiz-title" class="font-semibold text-indigo-400">Assessment</span>  
        <span id="progress-text">Question 1 of 5</span>  
      </div>  
        
      <!-- Progress Bar -->  
      <div class="w-full bg-slate-800 h-2 rounded-full overflow-hidden">  
        <div id="progress-bar" class="bg-indigo-500 h-full w-0 transition-all duration-300"></div>  
      </div>  
  
      <!-- Question Card -->  
      <div class="bg-slate-800/50 border border-slate-700/50 rounded-2xl p-6 md:p-8 space-y-6">  
        <h3 id="question-text" class="text-xl font-bold text-white">Question goes here?</h3>  
        <div id="options-container" class="space-y-3">  
          <!-- Options dynamically injected -->  
        </div>  
      </div>  
    </div>  
  
    <!-- View 3: Results View -->  
    <div id="view-results" class="hidden max-w-2xl mx-auto text-center space-y-6 bg-slate-800/50 border border-slate-700/50 rounded-2xl p-8">  
      <div class="w-16 h-16 bg-emerald-500/20 text-emerald-400 rounded-2xl flex items-center justify-center mx-auto">  
        <i data-lucide="award" class="w-8 h-8"></i>  
      </div>  
        
      <div class="space-y-2">  
        <span class="text-xs uppercase tracking-widest text-slate-400">Your Recommended Trajectory</span>  
        <h2 id="result-title" class="text-2xl md:text-3xl font-extrabold text-indigo-400">Result Title</h2>  
      </div>  
  
      <p id="result-desc" class="text-slate-300 leading-relaxed text-sm md:text-base">Detailed description of the result profile.</p>  
  
      <div class="pt-4 flex flex-col sm:flex-row gap-4 justify-center">  
        <button onclick="resetApp()" class="py-3 px-6 bg-slate-700 hover:bg-slate-600 text-white font-semibold rounded-xl transition">  
          Take Another Test  
        </button>  
      </div>  
    </div>  
  
  </main>  
  
  <!-- Footer -->  
  <footer class="border-t border-slate-800 py-6 text-center text-xs text-slate-500">  
    <p>© 2026 MindPath Hub. Built by Ekam.</p>  
  </footer>  
  
  <script>  
    lucide.createIcons();  
  
    const quizData = {  
      career: [  
        {  
          q: "When given a blank project, what kind of work excites you most?",  
          options: [  
            { text: "Designing visual layouts, creative media, or writing stories", type: "Creative" },  
            { text: "Building systems, physical equipment, or software architecture", type: "Technical" },  
            { text: "Investigating research, medical science, or analyzing complex data", type: "Scientific" },  
            { text: "Leading team strategy, negotiating deals, or launching businesses", type: "Leadership" },  
            { text: "Teaching, counseling, or directly helping people in need", type: "Social" },  
            { text: "Managing budgets, financial ledgers, operations, or legal policy", type: "Operations" }  
          ]  
        },  
        {  
          q: "Which daily environment feels like the best fit for your energy?",  
          options: [  
            { text: "A creative studio, digital canvas, or production set", type: "Creative" },  
            { text: "An engineering lab, workshop, or tech dev station", type: "Technical" },  
            { text: "A research clinic, healthcare facility, or analytics hub", type: "Scientific" },  
            { text: "A boardroom, corporate office, or fast-paced startup", type: "Leadership" },  
            { text: "A classroom, community center, or therapy environment", type: "Social" },  
            { text: "A structured accounting firm, bank, or management office", type: "Operations" }  
          ]  
        },  
        {  
          q: "What kind of impact do you want your work to have on the world?",  
          options: [  
            { text: "Inspiring people through art, storytelling, and design", type: "Creative" },  
            { text: "Solving complex technical problems and building tools", type: "Technical" },  
            { text: "Advancing human health, science, and discovery", type: "Scientific" },  
            { text: "Growing organizations, generating wealth, and leading teams", type: "Leadership" },  
            { text: "Empowering individuals, mentoring, and building community", type: "Social" },  
            { text: "Ensuring order, compliance, financial accuracy, and efficiency", type: "Operations" }  
          ]  
        }  
      ],  
      personality: [  
        {  
          q: "How do you prefer to approach major choices and work tasks?",  
          options: [  
            { text: "Relying on logic, cold data, and objective analysis", type: "Analytical" },  
            { text: "Trusting human empathy, team consensus, and personal values", type: "Relational" },  
            { text: "Following strict plans, schedules, and organized checklists", type: "Structured" },  
            { text: "Adapting spontaneously as new situations evolve", type: "Adaptable" }  
          ]  
        },  
        {  
          q: "Where do you draw most of your daily focus and motivation?",  
          options: [  
            { text: "Deep, quiet individual work where I can think uninterrupted", type: "Introverted" },  
            { text: "Active team brainstorming, group discussions, and high engagement", type: "Extroverted" }  
          ]  
        }  
      ]  
    };  
  
    const resultDescriptions = {  
      "Creative": "Creative & Media Strategy: You thrive in self-expression, visual arts, and content innovation! Careers like UX/UI Designer, Film Director, Copywriter, Brand Strategist, and Art Director match your visionary style.",  
      "Technical": "Engineering & Technology: You are a system builder! Professions like Full-Stack Developer, Mechanical Engineer, Cybersecurity Analyst, and Robotics Engineer suit your practical, hands-on problem-solving.",  
      "Scientific": "Research & Healthcare: You are driven by curiosity and discovery! Ideal fields include Data Scientist, Medical Practitioner, Biomedical Researcher, Financial Quant, and Environmental Specialist.",  
      "Leadership": "Entrepreneurship & Management: You are a natural driver of growth! High-impact roles like Business Executive, Startup Founder, Marketing Manager, Venture Capitalist, and Sales Director fit your ambition.",  
      "Social": "Education & Human Services: You care deeply about empowering others! Thriving roles include Psychologist, Academic Educator, HR Director, Career Counselor, and Non-Profit Leader.",  
      "Operations": "Finance & Legal Operations: You bring structure, reliability, and precision! Top-fit roles include Chartered Accountant, Financial Analyst, Corporate Lawyer, Operations Director, and Compliance Specialist.",  
      "Analytical": "Data-Driven Thinker: You make decisions based on clear evidence, objective facts, and structured reasoning.",  
      "Relational": "People-Centric Counselor: You bring strong empathy, active listening, and team harmony to every work culture.",  
      "Structured": "Master Organizer: You excel when managing clear guidelines, detailed workflows, and organized timelines.",  
      "Adaptable": "Agile Innovator: You thrive in fast-changing, flexible environments where quick pivot thinking is required.",  
      "Introverted": "Focused Deep-Worker: You produce your best results when given autonomy, quiet focus, and specialized projects.",  
      "Extroverted": "Collaborative Communicator: You energize team culture, public relationships, and group execution."  
    };  
  
    let currentQuizType = '';  
    let currentQuestionIndex = 0;  
    let scores = {};  
  
    function startQuiz(type) {  
      currentQuizType = type;  
      currentQuestionIndex = 0;  
      scores = {};  
  
      document.getElementById('view-home').classList.add('hidden');  
      document.getElementById('view-quiz').classList.remove('hidden');  
      document.getElementById('view-results').classList.add('hidden');  
  
      document.getElementById('quiz-title').innerText = type === 'career' ? 'Full-Spectrum Career Quiz' : 'Work Dynamics Test';  
        
      renderQuestion();  
    }  
  
    function renderQuestion() {  
      const questions = quizData[currentQuizType];  
      const q = questions[currentQuestionIndex];  
  
      document.getElementById('progress-text').innerText = `Question ${currentQuestionIndex + 1} of ${questions.length}`;  
      document.getElementById('progress-bar').style.width = `${((currentQuestionIndex + 1) / questions.length) * 100}%`;  
      document.getElementById('question-text').innerText = q.q;  
  
      const optionsContainer = document.getElementById('options-container');  
      optionsContainer.innerHTML = '';  
  
      q.options.forEach(opt => {  
        const btn = document.createElement('button');  
        btn.className = 'w-full p-4 rounded-xl bg-slate-800 hover:bg-indigo-600/20 border border-slate-700 hover:border-indigo-500/50 text-left text-slate-200 hover:text-white transition flex justify-between items-center group';  
        btn.innerHTML = `<span>${opt.text}</span> <i data-lucide="chevron-right" class="w-4 h-4 text-slate-500 group-hover:text-indigo-400"></i>`;  
        btn.onclick = () => selectOption(opt.type);  
        optionsContainer.appendChild(btn);  
      });  
  
      lucide.createIcons();  
    }  
  
    function selectOption(type) {  
      scores[type] = (scores[type] || 0) + 1;  
      currentQuestionIndex++;  
  
      if (currentQuestionIndex < quizData[currentQuizType].length) {  
        renderQuestion();  
      } else {  
        showResults();  
      }  
    }  
  
    function showResults() {  
      document.getElementById('view-quiz').classList.add('hidden');  
      document.getElementById('view-results').classList.remove('hidden');  
  
      let topResult = Object.keys(scores).reduce((a, b) => scores[a] > scores[b] ? a : b);  
  
      document.getElementById('result-title').innerText = topResult;  
      document.getElementById('result-desc').innerText = resultDescriptions[topResult] || "You possess a balanced set of interests across multiple professional areas!";  
    }  
  
    function resetApp() {  
      document.getElementById('view-results').classList.add('hidden');  
      document.getElementById('view-quiz').classList.add('hidden');  
      document.getElementById('view-home').classList.remove('hidden');  
    }  
  </script>  
</body>  
</html>  
