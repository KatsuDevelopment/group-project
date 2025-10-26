<script setup>
import { reactive } from 'vue';
import { GithubIcon } from 'lucide-vue-next';


const teamMembers = reactive([
  {
    name: 'Supanat Ponkong',
    role: 'Lead Developer',
    githubUsername: 'ItxM3G4RrYz',
    profileUrl: 'https://github.com/ItxM3G4RrYz',
    avatarUrl: 'https://avatars.githubusercontent.com/u/180245470?v=4' // Example generic GitHub avatar
  },
  {
    name: 'Pitchayaphak-Konchom',
    role: '**Blank**',
    githubUsername: 'Pitchayaphak-K',
    profileUrl: 'https://github.com/Pitchayaphak-K',
    avatarUrl: 'https://avatars.githubusercontent.com/u/205885765?v=4' // Example generic GitHub avatar
  },
  {
    name: 'Suchet Boonma',
    role: '**Blank**',
    githubUsername: 'Suchet191',
    profileUrl: 'https://github.com/Suchet191',
    avatarUrl: 'https://avatars.githubusercontent.com/u/205877949?v=4' // Example generic GitHub avatar
  }
]);


</script>

<template>
  <div class="about-view">
    <h1 class="main-title">✨ Our Team ✨</h1>
    <p class="subtitle">This group project is for Vue education.</p>
    
    <div class="team-grid">
      <div v-for="member in teamMembers" :key="member.githubUsername" class="member-card">
        
        <img :src="member.avatarUrl" :alt="`${member.name}'s avatar`" class="profile-avatar">
        
        <div class="member-info">
          <h2 class="member-name">{{ member.name }}</h2>
          <p class="member-role">{{ member.role }}</p>
          
          <a :href="member.profileUrl" target="_blank" rel="noopener noreferrer" class="github-link">
            <GithubIcon class="github-icon" :size="20" />
            <span>@{{ member.githubUsername }}</span>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* Basic styling for the component */
.about-view {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
  font-family: Arial, sans-serif;
}

.main-title {
  text-align: center;
  margin-bottom: 10px;
  color: #333;
}

.subtitle {
  text-align: center;
  margin-bottom: 40px;
  color: #666;
  font-size: 1.1em;
}

/* Team Grid Layout */
.team-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 30px;
}

/* Individual Member Card */
.member-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 25px;
  border: 1px solid #ddd;
  border-radius: 12px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
  transition: transform 0.3s, box-shadow 0.3s;
  background-color: #fff;
}

.member-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 6px 16px rgba(0, 0, 0, 0.1);
}

.profile-avatar {
  width: 120px;
  height: 120px;
  border-radius: 50%;
  object-fit: cover;
  margin-bottom: 15px;
  border: 4px solid #41b883; /* Vue green */
}

.member-info {
  text-align: center;
}

.member-name {
  font-size: 1.5em;
  color: #2c3e50;
  margin-bottom: 5px;
}

.member-role {
  font-size: 1em;
  color: #666;
  margin-bottom: 15px;
}

/* GitHub Link Styling */
.github-link {
  display: inline-flex;
  align-items: center;
  color: #0366d6; /* GitHub blue */
  text-decoration: none;
  font-weight: bold;
  transition: color 0.2s;
}

.github-link:hover {
  color: #00459c;
  text-decoration: underline;
}

.github-icon {
  margin-right: 5px;
  color: #24292e; /* GitHub dark color */
}
</style>