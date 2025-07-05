<template>
  <div class="app">
    <!-- Navigation -->
    <nav class="navbar">
      <div class="nav-container">
        <h1 class="logo">🤔 이마누엘 칸트</h1>
        <ul class="nav-menu">
          <li><a href="#home" @click="currentPage = 'about'" :class="{active: currentPage === 'about'}">철학자 소개</a></li>
          <li><a href="#philosophy" @click="currentPage = 'philosophy'" :class="{active: currentPage === 'philosophy'}">주요 사상</a></li>
        </ul>
      </div>
    </nav>

    <!-- Main Content -->
    <main class="main-content">
      
      <!-- About Page -->
      <div v-if="currentPage === 'about'" class="page about-page">
        <div class="hero">
          <div class="hero-content">
            <h1 class="hero-title">이마누엘 칸트</h1>
            <p class="hero-subtitle">Immanuel Kant (1724-1804)</p>
            <p class="hero-description">"근대 철학의 정점이자 현대 철학의 출발점"</p>
          </div>
          <div class="hero-quote">
            <blockquote>
              "내 마음을 채우고 있는 것은 두 가지요, <br>
              밤하늘에 반짝이는 별과 내 마음 속 도덕률이지."
            </blockquote>
            <cite>- 칸트 묘비명</cite>
          </div>
        </div>

        <div class="biography">
          <h2>📚 생애와 업적</h2>
          <div class="timeline">
            <div class="timeline-item">
              <div class="year">1724</div>
              <div class="content">
                <h4>쾨니히스베르크 탄생</h4>
                <p>프로이센 왕국(현재 러시아 칼리닌그라드)에서 마구사의 아들로 태어남</p>
              </div>
            </div>
            <div class="timeline-item">
              <div class="year">1740-1755</div>
              <div class="content">
                <h4>대학 시절과 가정교사</h4>
                <p>쾨니히스베르크 대학에서 철학, 수학, 자연과학 공부 후 9년간 가정교사로 생활</p>
              </div>
            </div>
            <div class="timeline-item">
              <div class="year">1770</div>
              <div class="content">
                <h4>정교수 임용</h4>
                <p>46세에 쾨니히스베르크 대학 논리학·형이상학 정교수로 임용</p>
              </div>
            </div>
            <div class="timeline-item">
              <div class="year">1781</div>
              <div class="content">
                <h4>순수이성비판 출간</h4>
                <p>57세에 대작 『순수이성비판』 출간으로 철학계에 혁명을 일으킴</p>
              </div>
            </div>
            <div class="timeline-item">
              <div class="year">1788-1790</div>
              <div class="content">
                <h4>3대 비판서 완성</h4>
                <p>『실천이성비판』(1788), 『판단력비판』(1790) 출간으로 비판철학 체계 완성</p>
              </div>
            </div>
            <div class="timeline-item">
              <div class="year">1804</div>
              <div class="content">
                <h4>영면</h4>
                <p>80세로 세상을 떠나며 "그것으로 좋다(Es ist gut)"라는 말을 남김</p>
              </div>
            </div>
          </div>
        </div>

        <div class="characteristics">
          <h2>🎭 칸트의 특징</h2>
          <div class="feature-grid">
            <div class="feature-card">
              <div class="feature-icon">⏰</div>
              <h3>규칙적인 생활</h3>
              <p>매일 같은 시간에 산책하여 주민들이 시계를 맞출 정도로 정확한 일상</p>
            </div>
            <div class="feature-card">
              <div class="feature-icon">🏠</div>
              <h3>평생 고향 거주</h3>
              <p>태어난 쾨니히스베르크를 단 한 번도 160km 이상 벗어나지 않음</p>
            </div>
            <div class="feature-card">
              <div class="feature-icon">📖</div>
              <h3>독신으로 학문 전념</h3>
              <p>결혼을 두 번 고려했지만 번번이 너무 오래 생각하다가 기회를 놓침</p>
            </div>
            <div class="feature-card">
              <div class="feature-icon">🧠</div>
              <h3>늦은 나이의 대성</h3>
              <p>57세에 첫 대작을 발표하며 철학사에 길이 남을 업적을 쌓음</p>
            </div>
          </div>
        </div>

        <div class="youtube-section">
          <h2>📺 칸트 철학 학습 영상</h2>
          <div class="video-grid">
            <div class="video-card">
              <h4>서울대 김상환 교수 - 왜 칸트인가?</h4>
              <p>서가명강 시리즈로 유명한 칸트 철학 입문 강의</p>
              <a href="https://www.youtube.com/watch?v=5QWVz1hNsAE" target="_blank" class="video-link">📺 강의 보기</a>
            </div>
            <div class="video-card">
              <h4>Philosophy Tube - Kant's Moral Philosophy</h4>
              <p>160만 구독자의 인기 철학 채널, 칸트 윤리학 설명 (영어)</p>
              <a href="https://www.youtube.com/c/PhilosophyTube" target="_blank" class="video-link">📺 채널 보기</a>
            </div>
            <div class="video-card">
              <h4>The School of Life - Kant</h4>
              <p>940만 구독자의 인문학 채널, 칸트 철학 쉬운 설명 (영어)</p>
              <a href="https://www.youtube.com/user/schooloflifechannel" target="_blank" class="video-link">📺 채널 보기</a>
            </div>
          </div>
        </div>

        <button @click="currentPage = 'philosophy'" class="next-button">주요 사상 알아보기 →</button>
      </div>

      <!-- Philosophy Page -->
      <div v-if="currentPage === 'philosophy'" class="page philosophy-page">
        <h1>🎓 칸트의 핵심 철학</h1>
        
        <div class="main-question">
          <h2>인간 이성의 세 가지 근본 질문</h2>
          <div class="questions">
            <div class="question-card">
              <h3>1️⃣ 나는 무엇을 알 수 있는가?</h3>
              <p><strong>→ 순수이성비판</strong> (인식론)</p>
            </div>
            <div class="question-card">
              <h3>2️⃣ 나는 무엇을 해야 하는가?</h3>
              <p><strong>→ 실천이성비판</strong> (윤리학)</p>
            </div>
            <div class="question-card">
              <h3>3️⃣ 나는 무엇을 희망해도 좋은가?</h3>
              <p><strong>→ 판단력비판</strong> (미학, 목적론)</p>
            </div>
          </div>
        </div>

        <div class="critiques">
          <h2>📖 3대 비판서</h2>
          
          <div class="critique-section">
            <h3>🔍 순수이성비판 (1781/1787)</h3>
            <div class="critique-content">
              <h4>코페르니쿠스적 전회</h4>
              <p><strong>기존 생각:</strong> 인간의 인식이 대상에 따라 결정된다</p>
              <p><strong>칸트의 혁명:</strong> 대상이 인간의 인식 형식에 따라 구성된다</p>
              
              <div class="concept-box">
                <h5>🧩 주요 개념</h5>
                <ul>
                  <li><strong>선험적 종합판단:</strong> 경험 이전에 주어지면서도 새로운 지식을 제공</li>
                  <li><strong>물자체:</strong> 인간이 결코 알 수 없는 사물 그 자체</li>
                  <li><strong>현상:</strong> 인간의 인식 형식을 통해 나타나는 사물의 모습</li>
                </ul>
              </div>
            </div>
          </div>

          <div class="critique-section">
            <h3>⚖️ 실천이성비판 (1788)</h3>
            <div class="critique-content">
              <h4>정언명령 (Categorical Imperative)</h4>
              <div class="moral-law">
                <blockquote>
                  "네 의지의 준칙이 언제나 동시에 보편적 입법의 원리가 될 수 있도록 행동하라"
                </blockquote>
              </div>
              
              <div class="concept-box">
                <h5>🎯 실천 예시</h5>
                <ul>
                  <li><strong>거짓말:</strong> 모든 사람이 거짓말한다면 약속 자체가 불가능 → 금지</li>
                  <li><strong>도움:</strong> 모든 사람이 서로 돕는다면 더 나은 세상 → 의무</li>
                  <li><strong>인격 존중:</strong> 사람을 수단이 아닌 목적으로 대우하라</li>
                </ul>
              </div>
            </div>
          </div>

          <div class="critique-section">
            <h3>🎨 판단력비판 (1790)</h3>
            <div class="critique-content">
              <h4>미적 판단과 목적론적 판단</h4>
              <p>자연과 자유, 감성과 이성을 연결하는 다리 역할</p>
              
              <div class="concept-box">
                <h5>🌸 미의 4가지 특징</h5>
                <ul>
                  <li><strong>관심 없는 만족:</strong> 소유욕 없이 순수하게 아름다움을 느낌</li>
                  <li><strong>보편적 타당성:</strong> 주관적이지만 모든 사람이 동의할 수 있음</li>
                  <li><strong>목적 없는 합목적성:</strong> 목적은 없지만 조화로움</li>
                  <li><strong>필연적 만족:</strong> 미는 필연적으로 쾌감을 줌</li>
                </ul>
              </div>
            </div>
          </div>
        </div>

        <div class="modern-relevance">
          <h2>🌍 현대적 의의</h2>
          <div class="relevance-grid">
            <div class="relevance-card">
              <h4>💼 기업 윤리</h4>
              <p>정언명령을 통한 보편적 기업 윤리 기준 제시</p>
            </div>
            <div class="relevance-card">
              <h4>🏛️ 민주주의</h4>
              <p>인간의 존엄성과 자율성을 바탕으로 한 정치 철학</p>
            </div>
            <div class="relevance-card">
              <h4>🤖 AI 윤리</h4>
              <p>인공지능 시대의 인간 중심적 가치 판단 기준</p>
            </div>
            <div class="relevance-card">
              <h4>🧭 비판적 사고</h4>
              <p>무비판적 수용을 거부하고 이성적 판단 강조</p>
            </div>
          </div>
        </div>

        <div class="famous-quotes">
          <h2>💬 칸트의 명언</h2>
          <div class="quotes-grid">
            <blockquote class="quote">
              "무지는 죄가 아니다. 하지만 배우지 않으려는 의지는 죄다."
            </blockquote>
            <blockquote class="quote">
              "계몽이란 인간이 자신이 초래한 미성년 상태에서 벗어나는 것이다."
            </blockquote>
            <blockquote class="quote">
              "행복을 위해 행동하지 말고, 행복할 자격이 있도록 행동하라."
            </blockquote>
          </div>
        </div>

        <button @click="currentPage = 'about'" class="prev-button">← 철학자 소개로 돌아가기</button>
      </div>

    </main>

    <!-- Footer -->
    <footer class="footer">
      <p>Made with Vue.js • 칸트 탄생 300주년 기념 (1724-2024) • "Sapere aude! - 감히 알려고 하라!"</p>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'KantApp',
  data() {
    return {
      currentPage: 'about'
    }
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Noto Serif KR', 'Times New Roman', serif;
  line-height: 1.7;
  color: #2c3e50;
}

.app {
  min-height: 100vh;
  background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
}

/* Navigation */
.navbar {
  background: rgba(44, 62, 80, 0.95);
  backdrop-filter: blur(10px);
  padding: 1rem 0;
  position: sticky;
  top: 0;
  z-index: 100;
  box-shadow: 0 2px 20px rgba(0,0,0,0.1);
}

.nav-container {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 2rem;
}

.logo {
  font-size: 1.8rem;
  font-weight: bold;
  color: #ecf0f1;
}

.nav-menu {
  display: flex;
  list-style: none;
  gap: 3rem;
}

.nav-menu a {
  text-decoration: none;
  color: #bdc3c7;
  font-weight: 500;
  transition: color 0.3s;
  cursor: pointer;
  font-size: 1.1rem;
}

.nav-menu a:hover,
.nav-menu a.active {
  color: #3498db;
}

/* Main Content */
.main-content {
  max-width: 1200px;
  margin: 0 auto;
  padding: 3rem 2rem;
  min-height: calc(100vh - 140px);
}

.page {
  background: white;
  border-radius: 20px;
  padding: 3rem;
  box-shadow: 0 15px 50px rgba(0,0,0,0.1);
  animation: fadeIn 0.6s ease-in;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(30px); }
  to { opacity: 1; transform: translateY(0); }
}

/* About Page */
.hero {
  text-align: center;
  margin-bottom: 4rem;
  padding: 3rem 0;
}

.hero-title {
  font-size: 4rem;
  margin-bottom: 1rem;
  background: linear-gradient(135deg, #2c3e50, #3498db);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  font-weight: 300;
}

.hero-subtitle {
  font-size: 1.5rem;
  color: #7f8c8d;
  margin-bottom: 1rem;
  font-style: italic;
}

.hero-description {
  font-size: 1.2rem;
  color: #34495e;
  margin-bottom: 2rem;
}

.hero-quote {
  background: #ecf0f1;
  padding: 2rem;
  border-radius: 15px;
  border-left: 5px solid #3498db;
  margin-top: 2rem;
}

.hero-quote blockquote {
  font-size: 1.3rem;
  font-style: italic;
  color: #2c3e50;
  margin-bottom: 1rem;
  line-height: 1.6;
}

.hero-quote cite {
  color: #7f8c8d;
  font-size: 1rem;
}

/* Timeline */
.biography h2 {
  text-align: center;
  margin-bottom: 3rem;
  font-size: 2.5rem;
}

.timeline {
  position: relative;
  padding-left: 2rem;
}

.timeline::before {
  content: '';
  position: absolute;
  left: 0;
  top: 0;
  bottom: 0;
  width: 3px;
  background: #3498db;
}

.timeline-item {
  position: relative;
  margin-bottom: 3rem;
  padding-left: 3rem;
}

.timeline-item::before {
  content: '';
  position: absolute;
  left: -7px;
  top: 5px;
  width: 15px;
  height: 15px;
  border-radius: 50%;
  background: #3498db;
}

.year {
  font-size: 1.2rem;
  font-weight: bold;
  color: #3498db;
  margin-bottom: 0.5rem;
}

.timeline-item h4 {
  color: #2c3e50;
  margin-bottom: 0.5rem;
  font-size: 1.3rem;
}

.timeline-item p {
  color: #7f8c8d;
  line-height: 1.6;
}

/* Feature Grid */
.characteristics {
  margin: 4rem 0;
}

.characteristics h2 {
  text-align: center;
  margin-bottom: 3rem;
  font-size: 2.5rem;
}

.feature-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2rem;
}

.feature-card {
  text-align: center;
  padding: 2.5rem;
  background: #f8f9fa;
  border-radius: 15px;
  transition: transform 0.3s, box-shadow 0.3s;
  border: 1px solid #ecf0f1;
}

.feature-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 20px 40px rgba(0,0,0,0.1);
}

.feature-icon {
  font-size: 4rem;
  margin-bottom: 1.5rem;
}

.feature-card h3 {
  color: #2c3e50;
  margin-bottom: 1rem;
  font-size: 1.4rem;
}

.feature-card p {
  color: #7f8c8d;
  line-height: 1.6;
}

/* YouTube Section */
.youtube-section {
  margin: 4rem 0;
}

.youtube-section h2 {
  text-align: center;
  margin-bottom: 3rem;
  font-size: 2.5rem;
}

.video-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
}

.video-card {
  background: #f8f9fa;
  padding: 2rem;
  border-radius: 15px;
  border-left: 4px solid #e74c3c;
}

.video-card h4 {
  color: #2c3e50;
  margin-bottom: 1rem;
  font-size: 1.3rem;
}

.video-card p {
  color: #7f8c8d;
  margin-bottom: 1.5rem;
  line-height: 1.6;
}

.video-link {
  display: inline-block;
  background: #e74c3c;
  color: white;
  padding: 0.8rem 1.5rem;
  border-radius: 8px;
  text-decoration: none;
  transition: background 0.3s;
}

.video-link:hover {
  background: #c0392b;
}

/* Philosophy Page */
.main-question {
  margin-bottom: 4rem;
}

.main-question h2 {
  text-align: center;
  margin-bottom: 2rem;
  font-size: 2.5rem;
  color: #2c3e50;
}

.questions {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
}

.question-card {
  background: linear-gradient(135deg, #3498db, #2980b9);
  color: white;
  padding: 2rem;
  border-radius: 15px;
  text-align: center;
}

.question-card h3 {
  margin-bottom: 1rem;
  font-size: 1.4rem;
}

.question-card p {
  font-size: 1.1rem;
}

/* Critiques */
.critiques h2 {
  text-align: center;
  margin-bottom: 3rem;
  font-size: 2.5rem;
}

.critique-section {
  margin-bottom: 3rem;
  background: #f8f9fa;
  padding: 2.5rem;
  border-radius: 15px;
  border-left: 5px solid #9b59b6;
}

.critique-section h3 {
  color: #2c3e50;
  margin-bottom: 1.5rem;
  font-size: 1.8rem;
}

.critique-section h4 {
  color: #8e44ad;
  margin-bottom: 1rem;
  font-size: 1.4rem;
}

.critique-content p {
  margin-bottom: 1rem;
  line-height: 1.6;
}

.moral-law {
  background: white;
  padding: 2rem;
  border-radius: 10px;
  margin: 1.5rem 0;
  border-left: 4px solid #27ae60;
}

.moral-law blockquote {
  font-size: 1.2rem;
  font-style: italic;
  color: #27ae60;
  text-align: center;
}

.concept-box {
  background: white;
  padding: 2rem;
  border-radius: 10px;
  margin-top: 1.5rem;
}

.concept-box h5 {
  color: #2c3e50;
  margin-bottom: 1rem;
  font-size: 1.2rem;
}

.concept-box ul {
  padding-left: 1.5rem;
}

.concept-box li {
  margin-bottom: 0.8rem;
  line-height: 1.6;
}

/* Modern Relevance */
.modern-relevance {
  margin: 4rem 0;
}

.modern-relevance h2 {
  text-align: center;
  margin-bottom: 3rem;
  font-size: 2.5rem;
}

.relevance-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
}

.relevance-card {
  background: linear-gradient(135deg, #f39c12, #e67e22);
  color: white;
  padding: 2rem;
  border-radius: 15px;
  text-align: center;
}

.relevance-card h4 {
  margin-bottom: 1rem;
  font-size: 1.3rem;
}

/* Famous Quotes */
.famous-quotes {
  margin: 4rem 0;
}

.famous-quotes h2 {
  text-align: center;
  margin-bottom: 3rem;
  font-size: 2.5rem;
}

.quotes-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 2rem;
}

.quote {
  background: #ecf0f1;
  padding: 2rem;
  border-radius: 15px;
  font-style: italic;
  font-size: 1.2rem;
  color: #2c3e50;
  border-left: 5px solid #3498db;
  line-height: 1.6;
}

/* Buttons */
.next-button, .prev-button {
  background: linear-gradient(135deg, #3498db, #2980b9);
  color: white;
  border: none;
  padding: 1rem 2rem;
  font-size: 1.2rem;
  border-radius: 10px;
  cursor: pointer;
  transition: transform 0.3s, box-shadow 0.3s;
  margin: 2rem auto;
  display: block;
}

.next-button:hover, .prev-button:hover {
  transform: translateY(-3px);
  box-shadow: 0 10px 30px rgba(52, 152, 219, 0.3);
}

/* Footer */
.footer {
  text-align: center;
  padding: 2rem;
  color: #7f8c8d;
  font-size: 0.95rem;
  background: rgba(236, 240, 241, 0.8);
}

/* Responsive */
@media (max-width: 768px) {
  .nav-container {
    flex-direction: column;
    gap: 1rem;
  }

  .nav-menu {
    gap: 1.5rem;
  }

  .hero-title {
    font-size: 2.5rem;
  }

  .page {
    padding: 2rem 1.5rem;
  }

  .timeline {
    padding-left: 1rem;
  }

  .timeline-item {
    padding-left: 2rem;
  }

  .questions,
  .feature-grid,
  .video-grid,
  .relevance-grid,
  .quotes-grid {
    grid-template-columns: 1fr;
  }
}
</style>