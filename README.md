<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>손지호 · 건축감리 전문가</title>
<style>
  :root {
    --paper: #f2efe6;
    --paper-alt: #eae5d7;
    --ink: #23241f;
    --ink-soft: #57584e;
    --line: #cfc6ac;
    --navy: #29455a;
    --navy-soft: #4c6d80;
    --rust: #a24a2a;
  }

  @media (prefers-color-scheme: dark) {
    :root {
      --paper: #16191a;
      --paper-alt: #1d2123;
      --ink: #e9e5d8;
      --ink-soft: #a9a89b;
      --line: #3a3d38;
      --navy: #8fb3c4;
      --navy-soft: #6f92a3;
      --rust: #d1774f;
    }
  }
  :root[data-theme="dark"] {
    --paper: #16191a;
    --paper-alt: #1d2123;
    --ink: #e9e5d8;
    --ink-soft: #a9a89b;
    --line: #3a3d38;
    --navy: #8fb3c4;
    --navy-soft: #6f92a3;
    --rust: #d1774f;
  }
  :root[data-theme="light"] {
    --paper: #f2efe6;
    --paper-alt: #eae5d7;
    --ink: #23241f;
    --ink-soft: #57584e;
    --line: #cfc6ac;
    --navy: #29455a;
    --navy-soft: #4c6d80;
    --rust: #a24a2a;
  }

  * { box-sizing: border-box; }

  body {
    margin: 0;
    background: var(--paper);
    color: var(--ink);
    font-family: "Malgun Gothic", "맑은 고딕", "Segoe UI", -apple-system, sans-serif;
    line-height: 1.65;
    -webkit-font-smoothing: antialiased;
  }

  .sheet {
    max-width: 780px;
    margin: 0 auto;
    padding: 56px 28px 96px;
  }

  /* ---------- title block ---------- */
  .titleblock {
    border: 1px solid var(--line);
    padding: 32px 32px 24px;
    position: relative;
    margin-bottom: 44px;
  }
  .titleblock::before,
  .titleblock::after,
  .corner-tl, .corner-br {
    content: "";
    position: absolute;
    width: 10px;
    height: 10px;
    border-color: var(--navy);
    border-style: solid;
  }
  .titleblock::before {
    top: -1px; left: -1px;
    border-width: 2px 0 0 2px;
  }
  .titleblock::after {
    bottom: -1px; right: -1px;
    border-width: 0 2px 2px 0;
  }

  .eyebrow {
    font-size: 12px;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--navy);
    font-weight: 700;
    margin: 0 0 10px;
  }

  h1 {
    font-family: "Segoe UI", "Malgun Gothic", sans-serif;
    font-size: clamp(32px, 6vw, 44px);
    font-weight: 700;
    letter-spacing: 0.01em;
    margin: 0 0 6px;
    text-wrap: balance;
  }

  .role {
    font-size: 16px;
    color: var(--ink-soft);
    margin: 0 0 20px;
  }

  .meta-row {
    display: flex;
    flex-wrap: wrap;
    gap: 8px 10px;
    border-top: 1px solid var(--line);
    padding-top: 16px;
  }
  .meta-tag {
    font-size: 12.5px;
    padding: 4px 10px;
    border: 1px solid var(--line);
    color: var(--ink-soft);
    letter-spacing: 0.02em;
  }

  /* ---------- sections ---------- */
  section { margin-bottom: 52px; }

  .section-head {
    display: flex;
    align-items: baseline;
    gap: 12px;
    margin-bottom: 22px;
  }
  .section-num {
    font-size: 13px;
    color: var(--navy);
    font-weight: 700;
    letter-spacing: 0.05em;
    font-variant-numeric: tabular-nums;
  }
  .section-head h2 {
    font-size: 20px;
    font-weight: 700;
    margin: 0;
    letter-spacing: 0.01em;
  }
  .section-rule {
    flex: 1;
    height: 1px;
    background: var(--line);
    align-self: center;
  }

  /* ---------- intro panel ---------- */
  .intro-panel {
    background: var(--paper-alt);
    border-left: 3px solid var(--rust);
    padding: 26px 28px;
  }
  .intro-panel p {
    font-family: "Batang", "바탕", "Malgun Gothic", serif;
    font-size: 16px;
    margin: 0 0 16px;
    color: var(--ink);
  }
  .intro-panel p:last-child { margin-bottom: 0; }

  /* ---------- timeline ---------- */
  .timeline {
    position: relative;
    border-left: 2px solid var(--line);
    margin-left: 6px;
    padding-left: 28px;
  }
  .tl-item {
    position: relative;
    padding-bottom: 28px;
  }
  .tl-item:last-child { padding-bottom: 0; }
  .tl-item::before {
    content: "";
    position: absolute;
    left: -33px;
    top: 4px;
    width: 8px;
    height: 8px;
    background: var(--navy);
    border-radius: 50%;
  }
  .tl-item.current::before {
    background: var(--rust);
  }
  .tl-period {
    font-size: 12.5px;
    color: var(--navy-soft);
    font-weight: 700;
    letter-spacing: 0.03em;
    font-variant-numeric: tabular-nums;
    margin-bottom: 4px;
  }
  .tl-project {
    font-size: 15.5px;
    font-weight: 700;
    margin-bottom: 3px;
  }
  .tl-company {
    font-size: 13.5px;
    color: var(--ink-soft);
  }
  .tl-role {
    display: inline-block;
    margin-top: 6px;
    font-size: 12px;
    color: var(--navy);
    border: 1px solid var(--line);
    padding: 2px 8px;
  }

  /* ---------- two-col grid ---------- */
  .grid-2 {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 32px;
  }
  @media (max-width: 560px) {
    .grid-2 { grid-template-columns: 1fr; }
  }

  .cred {
    border-top: 1px solid var(--line);
    padding-top: 14px;
    margin-bottom: 18px;
  }
  .cred:last-child { margin-bottom: 0; }
  .cred-title { font-weight: 700; font-size: 14.5px; margin-bottom: 2px; }
  .cred-sub { font-size: 13px; color: var(--ink-soft); }
  .cred-date {
    font-size: 12px;
    color: var(--navy-soft);
    font-variant-numeric: tabular-nums;
  }

  /* ---------- skills ---------- */
  .skill-row {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px 0;
    border-bottom: 1px solid var(--line);
    font-size: 14px;
    gap: 16px;
  }
  .skill-row:last-child { border-bottom: none; }
  .skill-name { font-weight: 700; white-space: nowrap; }
  .skill-note { color: var(--ink-soft); font-size: 13px; text-align: right; }

  footer {
    margin-top: 60px;
    padding-top: 20px;
    border-top: 1px solid var(--line);
    font-size: 12px;
    color: var(--ink-soft);
    text-align: center;
    letter-spacing: 0.04em;
  }
</style>
</head>
<body>
<div class="sheet">

  <div class="titleblock">
    <p class="eyebrow">Profile · 건축감리 전문가</p>
    <h1>손지호</h1>
    <p class="role">건설사업관리(CM) · 건축감리 전문가 &nbsp;/&nbsp; 건축기사</p>
    <div class="meta-row">
      <span class="meta-tag">감리경력 10년차</span>
      <span class="meta-tag">계명대학교 건축학과</span>
      <span class="meta-tag">건축기사 취득</span>
      <span class="meta-tag">건설사업관리기술인 특급</span>
    </div>
  </div>

  <section>
    <div class="section-head">
      <span class="section-num">01</span>
      <h2>자기소개</h2>
      <span class="section-rule"></span>
    </div>
    <div class="intro-panel">
      <p>
        지난 10여 년간 공동주택, 근린생활시설, 산업단지, 재건축정비사업 등 다양한 현장에서
        건축감리 업무에 집중해 왔습니다. 설계·시공·인허가 등 각 공정 간의 유기적인 협조를
        이끌어내는 데 주력하며 맡은 업무를 성실히 수행해 왔고, 그 과정에서 현장을 다각도로
        조율하고 판단하는 관리자로서의 역량을 꾸준히 쌓아올 수 있었습니다.
      </p>
      <p>
        최근에는 AI 코딩 기술을 도면 검토 과정에 접목하여 검토 효율과 정확도를 높이는 시도를
        이어가고 있으며, 이러한 노력이 실제 직무 성과 향상으로 이어지면서 동료들로부터도
        긍정적인 평가를 받았습니다.
      </p>
      <p>
        현장에서 쌓아온 경험과 새로운 기술에 대한 관심을 바탕으로, 기회가 주어진다면
        귀사에 실질적으로 기여하는 인재가 되도록 노력하겠습니다.
      </p>
    </div>
  </section>

  <section>
    <div class="section-head">
      <span class="section-num">02</span>
      <h2>경력사항</h2>
      <span class="section-rule"></span>
    </div>
    <div class="timeline">

      <div class="tl-item current">
        <div class="tl-period">2026.01 — 현재</div>
        <div class="tl-project">서초 신동아 아파트 주택 재건축정비사업</div>
        <div class="tl-company">㈜신한종합건축사</div>
        <span class="tl-role">감리용역 · 이사</span>
      </div>

      <div class="tl-item">
        <div class="tl-period">2023.12 — 2025.12</div>
        <div class="tl-project">방배5구역 재건축정비사업</div>
        <div class="tl-company">㈜신한종합건축사</div>
        <span class="tl-role">건축감리 · 이사</span>
      </div>

      <div class="tl-item">
        <div class="tl-period">2023.03 — 2023.06</div>
        <div class="tl-project">완주군·완주 진안 천연가스 공급시설 건설공사</div>
        <div class="tl-company">㈜신한종합건축사</div>
        <span class="tl-role">시공단계 감독권한대행 등 건설사업관리 · 이사</span>
      </div>

      <div class="tl-item">
        <div class="tl-period">2021.08 — 2022.11</div>
        <div class="tl-project">금천지식산업센터 신축공사</div>
        <div class="tl-company">우리동인건축사사무소</div>
        <span class="tl-role">건축법 감리 · 단장</span>
      </div>

      <div class="tl-item">
        <div class="tl-period">2020.04 — 2021.04</div>
        <div class="tl-project">수원 인계동 근린생활시설(병원) 신축공사 · 지상14층/지하2층</div>
        <div class="tl-company">㈜성지건축사사무소</div>
        <span class="tl-role">건축감리(건축법) · 부장</span>
      </div>

      <div class="tl-item">
        <div class="tl-period">2019.10 — 2020.04</div>
        <div class="tl-project">수원 권선동 오피스텔 신축공사 · 지상12층/지하1층, 연면적 3,451㎡</div>
        <div class="tl-company">㈜누리마루건축사사무소</div>
        <span class="tl-role">건축감리(건축법) · 부장</span>
      </div>

      <div class="tl-item">
        <div class="tl-period">2018.07 — 2019.09</div>
        <div class="tl-project">㈜에이씨엔 공장신축공사</div>
        <div class="tl-company">㈜누리마루건축사사무소</div>
        <span class="tl-role">건축감리(건축법) · 부장</span>
      </div>

      <div class="tl-item">
        <div class="tl-period">2017.11 — 2018.06</div>
        <div class="tl-project">남양주 묵현5지구 공동주택신축공사</div>
        <div class="tl-company">㈜목양종합건축사사무소</div>
        <span class="tl-role">건축감리 · 차장</span>
      </div>

      <div class="tl-item">
        <div class="tl-period">2014.04 — 2016.09</div>
        <div class="tl-project">하남미사강변도시 A6블럭 공동주택건설공사</div>
        <div class="tl-company">(합)건축사사무소 태백</div>
        <span class="tl-role">건축감리 · 과장</span>
      </div>

    </div>
  </section>

  <section>
    <div class="section-head">
      <span class="section-num">03</span>
      <h2>학력 및 자격</h2>
      <span class="section-rule"></span>
    </div>
    <div class="grid-2">
      <div>
        <div class="cred">
          <div class="cred-title">계명대학교 · 건축학과</div>
          <div class="cred-sub">학사 졸업</div>
          <div class="cred-date">1998 — 2005</div>
        </div>
        <div class="cred">
          <div class="cred-title">청구고등학교</div>
          <div class="cred-date">1995 — 1998</div>
        </div>
      </div>
      <div>
        <div class="cred">
          <div class="cred-title">건축기사</div>
          <div class="cred-sub">국가기술자격 취득</div>
          <div class="cred-date">2024.06</div>
        </div>
        <div class="cred">
          <div class="cred-title">건설사업관리기술인 승급 특급 전문교육</div>
          <div class="cred-sub">이수</div>
          <div class="cred-date">2025.02.10 — 2025.03.19</div>
        </div>
      </div>
    </div>
  </section>

  <section>
    <div class="section-head">
      <span class="section-num">04</span>
      <h2>전문 역량</h2>
      <span class="section-rule"></span>
    </div>
    <div>
      <div class="skill-row">
        <span class="skill-name">문서작성 (한글 · 워드)</span>
        <span class="skill-note">상 — 단축키 활용</span>
      </div>
      <div class="skill-row">
        <span class="skill-name">AutoCAD</span>
        <span class="skill-note">중 — 도면 작성 및 편집</span>
      </div>
      <div class="skill-row">
        <span class="skill-name">LISP (AutoCAD 자동화)</span>
        <span class="skill-note">상 — 리습을 활용한 도면 작업 자동화</span>
      </div>
      <div class="skill-row">
        <span class="skill-name">Excel</span>
        <span class="skill-note">중 — 수식 활용</span>
      </div>
      <div class="skill-row">
        <span class="skill-name">PowerPoint</span>
        <span class="skill-note">중 — 표 작성 및 효과 삽입</span>
      </div>
      <div class="skill-row">
        <span class="skill-name">AI 도면 검토</span>
        <span class="skill-note">AI 코딩 기술을 접목한 도면 검토 프로세스 적용</span>
      </div>
    </div>
  </section>

  <footer>SON JIHO — CONSTRUCTION SUPERVISION PROFILE</footer>

</div>
</body>
</html>