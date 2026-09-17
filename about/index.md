---
layout: page
type: about
title: "Introduction"
---

<style>
.language-switch {
  display: flex;
  justify-content: flex-end;
  gap: 6px;
  margin-bottom: 24px;
}

.language-switch button {
  padding: 5px 12px;
  border: 1px solid #aaa;
  border-radius: 6px;
  background: transparent;
  cursor: pointer;
  font-size: 0.9rem;
}

.language-switch button:hover {
  background: rgba(128, 128, 128, 0.12);
}

.language-switch button.active {
  font-weight: 600;
  border-color: currentColor;
}
</style>

<div class="language-switch">
  <button id="ko-btn" onclick="showLang('ko')">한국어</button>
  <button id="en-btn" onclick="showLang('en')">English</button>
</div>


<div id="lang-ko" markdown="1">

## 소개

안녕하세요, **고승우**입니다.

새로운 것을 배우고 경험하는 것을 좋아합니다.  
여행과 음악을 좋아하고, 수학이나 프로그래밍처럼 생각하면서 문제를 해결하는 일도 즐깁니다.

한국, 캐나다, 브라질에서 생활하고 공부하면서 다양한 문화와 사람들을 경험했습니다.  
요즘은 학생들을 가르치면서 수학과 프로그래밍을 공부하고, 관심이 생기는 여러 가지를 조금씩 만들어 보고 있습니다.

---

<details markdown="1">
<summary><strong>학력</strong></summary>

### University of Waterloo

**Waterloo, Ontario, Canada**

- Mathematics
- 2022.09 -- 2023.04
- 2027.01 복학 예정

</details>

<br>

<details markdown="1">
<summary><strong>교육 경력</strong></summary>

### EMCS (이음학교)

**고등학교 수학·과학 교사**  
수원, 대한민국  
2026.08 -- 현재

- AP Calculus AB
- AP Physics 1
- 한국 고등학교 수학
- 한국 고등학교 과학

### Grace Academy

**영어 강사**  
화성, 대한민국  
2026.07 -- 현재

- 초등학생 및 중학생 영어 수업
- Reading, Writing, Grammar, Vocabulary 및 Communication 중심 수업

### 아소비 책통클럽 S학원

**영어·수학 강사**  
수원, 대한민국  
2026.03 -- 2026.07

### Seed International School

**컴퓨터과학 교사**  
수원, 대한민국  
2026.02 -- 2026.06

- Scratch
- Python
- Computational Thinking
- AI Prompt Writing
- 영어 및 한국어 수업

### Private IELTS Tutor

**개인 과외**  
Toronto, Canada  
2025.04 -- 2025.10

### Private Mathematics Tutor

**개인 과외**  
Toronto, Canada  
2022.01 -- 2023.01

</details>

<br>

<details markdown="1">
<summary><strong>봉사활동</strong></summary>

### 국제통번역자원봉사단

**번역 봉사자**  
2022.06 -- 2022.08

- 한국어와 영어 간 문서 및 교육 자료 번역
- 행사 운영 및 참가자 커뮤니케이션 지원

### 브라질 지역사회 및 동물복지 봉사

브라질 유학 시절 지역사회 봉사 및 동물보호소 지원 활동에 참여했습니다.

</details>

<br>

<details markdown="1">
<summary><strong>군 복무</strong></summary>

### 대한민국 육군

**현역 복무**  
2023.09 -- 2025.03

- 만기 전역

</details>

<br>

<details markdown="1">
<summary><strong>Online Judge Profiles</strong></summary>

{% include judge_profile.html boj_id="kosnoa" codeforces_id="kosnoa" atcoder_id="kosnoa" %}

</details>

</div>


<div id="lang-en" markdown="1" style="display:none;">

## About Me

Hi, I'm **Tommy**.

I enjoy learning new things, traveling, listening to music, and solving problems.  
I've lived and studied in Korea, Canada, and Brazil, which has given me opportunities to experience different cultures and perspectives.

These days, I spend most of my time teaching, studying mathematics and programming, and exploring whatever catches my interest.

---

<details markdown="1">
<summary><strong>Education</strong></summary>

### University of Waterloo

**Waterloo, Ontario, Canada**

- Mathematics
- Sep. 2022 -- Apr. 2023
- Studies to resume Jan. 2027

</details>

<br>

<details markdown="1">
<summary><strong>Teaching Experience</strong></summary>

### EMCS (이음학교)

**High School Mathematics & Science Teacher**  
Suwon, South Korea  
Aug. 2026 -- Present

- AP Calculus AB
- AP Physics 1
- Korean High School Mathematics
- Korean High School Science

### Grace Academy

**English Instructor**  
Hwaseong, South Korea  
Jul. 2026 -- Present

- English instruction for elementary and middle school students
- Reading, writing, grammar, vocabulary, and communication

### 아소비 책통클럽 S학원

**English and Mathematics Instructor**  
Suwon, South Korea  
Mar. 2026 -- Jul. 2026

### Seed International School

**Computer Science Teacher**  
Suwon, South Korea  
Feb. 2026 -- Jun. 2026

- Scratch
- Python
- Computational thinking
- AI prompt writing
- Instruction delivered in English and Korean

### Private IELTS Tutor

**Self-Employed**  
Toronto, Canada  
Apr. 2025 -- Oct. 2025

### Private Mathematics Tutor

**Self-Employed**  
Toronto, Canada  
Jan. 2022 -- Jan. 2023

</details>

<br>

<details markdown="1">
<summary><strong>Volunteer Experience</strong></summary>

### 국제통번역자원봉사단

**Translation Volunteer**  
Jun. 2022 -- Aug. 2022

- Translated documents and educational materials between Korean and English.
- Supported event operations and participant communication.

### Community & Animal Welfare Volunteering

**Brazil**

Participated in community service and animal shelter support activities while studying in Brazil.

</details>

<br>

<details markdown="1">
<summary><strong>Military Service</strong></summary>

### Republic of Korea Army (ROKA)

**Active Duty Military Service**  
Sep. 2023 -- Mar. 2025

- Honorably Discharged

</details>

<br>

<details markdown="1">
<summary><strong>Online Judge Profiles</strong></summary>

{% include judge_profile.html boj_id="kosnoa" codeforces_id="kosnoa" atcoder_id="kosnoa" %}

</details>

</div>


<script>
function showLang(lang) {
  const ko = document.getElementById('lang-ko');
  const en = document.getElementById('lang-en');
  const koBtn = document.getElementById('ko-btn');
  const enBtn = document.getElementById('en-btn');

  ko.style.display = lang === 'ko' ? 'block' : 'none';
  en.style.display = lang === 'en' ? 'block' : 'none';

  koBtn.classList.toggle('active', lang === 'ko');
  enBtn.classList.toggle('active', lang === 'en');

  localStorage.setItem('about-language', lang);
}

document.addEventListener('DOMContentLoaded', function () {
  const savedLang = localStorage.getItem('about-language') || 'ko';
  showLang(savedLang);
});
</script>
