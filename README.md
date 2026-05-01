# kosotns.github.io
+
<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>МОТИВАЦИЯ УЧЕНИЯ: чек-лист осмысления темы</title>
<style>
  @import url('https://cdn.fontsource.org/fontsource/inter.css');

  *, *::before, *::after {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  :root {
    --bg-page: #F5F3EF;
    --accent-blue: #1A3A4A;
    --accent-blue-hover: #234B60;
    --accent-green: #2B5C6F;
    --accent-orange: #E8A735;
    --accent-orange-hover: #D49628;
    --card-bg: #FFFFFF;
    --text-primary: #2C2C2C;
    --text-secondary: #4A5568;
    --text-muted: #718096;
    --border-light: #E2DDD5;
    --checked-bg: #E8F5E9;
    --shadow-sm: 0 1px 3px rgba(0,0,0,0.06), 0 1px 2px rgba(0,0,0,0.04);
    --shadow-md: 0 4px 6px rgba(0,0,0,0.07), 0 2px 4px rgba(0,0,0,0.04);
    --shadow-lg: 0 10px 25px rgba(0,0,0,0.08), 0 4px 10px rgba(0,0,0,0.04);
    --radius: 12px;
    --radius-sm: 8px;
    --transition: 0.25s cubic-bezier(0.4, 0, 0.2, 1);
  }

  body {
    font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    background-color: var(--bg-page);
    color: var(--text-primary);
    line-height: 1.6;
    min-height: 100vh;
    padding: 24px 16px 60px;
  }

  .container {
    max-width: 780px;
    margin: 0 auto;
  }

  /* HEADER */
  .header {
    text-align: center;
    margin-bottom: 40px;
    padding: 36px 28px;
    background: linear-gradient(135deg, var(--accent-blue) 0%, var(--accent-green) 100%);
    border-radius: var(--radius);
    color: #fff;
    box-shadow: var(--shadow-lg);
  }

  .header-icon {
    width: 52px;
    height: 52px;
    margin: 0 auto 16px;
    background: rgba(255,255,255,0.15);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .header h1 {
    font-size: 1.6rem;
    font-weight: 700;
    letter-spacing: -0.02em;
    margin-bottom: 8px;
    line-height: 1.3;
  }

  .header p {
    font-size: 0.95rem;
    opacity: 0.88;
    max-width: 500px;
    margin: 0 auto;
  }

  /* PROGRESS BAR */
  .progress-bar-container {
    margin-bottom: 32px;
    background: var(--card-bg);
    border-radius: var(--radius);
    padding: 20px 24px;
    box-shadow: var(--shadow-sm);
    position: sticky;
    top: 12px;
    z-index: 50;
    border: 1px solid var(--border-light);
  }

  .progress-info {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 10px;
  }

  .progress-label {
    font-size: 0.85rem;
    font-weight: 600;
    color: var(--text-secondary);
  }

  .progress-count {
    font-size: 0.85rem;
    font-weight: 700;
    color: var(--accent-blue);
  }

  .progress-track {
    width: 100%;
    height: 8px;
    background: #E8E5DF;
    border-radius: 99px;
    overflow: hidden;
  }

  .progress-fill {
    height: 100%;
    width: 0%;
    background: linear-gradient(90deg, var(--accent-orange), #F0B34B);
    border-radius: 99px;
    transition: width 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  }

  /* BLOCKS */
  .block {
    background: var(--card-bg);
    border-radius: var(--radius);
    margin-bottom: 20px;
    box-shadow: var(--shadow-sm);
    overflow: hidden;
    border: 1px solid var(--border-light);
    transition: box-shadow var(--transition);
  }

  .block:hover {
    box-shadow: var(--shadow-md);
  }

  .block-header {
    padding: 20px 24px 16px;
    border-bottom: 1px solid var(--border-light);
    display: flex;
    align-items: center;
    gap: 14px;
  }

  .block-number {
    width: 38px;
    height: 38px;
    border-radius: 50%;
    background: var(--accent-blue);
    color: #fff;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: 700;
    font-size: 0.9rem;
    flex-shrink: 0;
  }

  .block-title {
    font-size: 1.05rem;
    font-weight: 700;
    color: var(--accent-blue);
    line-height: 1.35;
  }

  .block-body {
    padding: 8px 24px 20px;
  }

  /* CHECKBOXES */
  .checkbox-item {
    display: flex;
    align-items: flex-start;
    gap: 14px;
    padding: 14px 16px;
    margin: 4px 0;
    border-radius: var(--radius-sm);
    cursor: pointer;
    transition: background var(--transition), transform 0.15s ease;
    user-select: none;
  }

  .checkbox-item:hover {
    background: #FAF9F7;
  }

  .checkbox-item.checked {
    background: var(--checked-bg);
  }

  .checkbox-item input[type="checkbox"] {
    display: none;
  }

  .custom-checkbox {
    width: 24px;
    height: 24px;
    border: 2px solid #C5C0B8;
    border-radius: 6px;
    flex-shrink: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: all var(--transition);
    margin-top: 1px;
    position: relative;
  }

  .checkbox-item input[type="checkbox"]:checked + .custom-checkbox {
    background: var(--accent-orange);
    border-color: var(--accent-orange);
  }

  .custom-checkbox svg {
    width: 14px;
    height: 14px;
    opacity: 0;
    transform: scale(0.5);
    transition: all 0.2s cubic-bezier(0.4, 0, 0.2, 1);
  }

  .checkbox-item input[type="checkbox"]:checked + .custom-checkbox svg {
    opacity: 1;
    transform: scale(1);
  }

  .checkbox-text {
    font-size: 0.92rem;
    color: var(--text-primary);
    line-height: 1.5;
    transition: color var(--transition);
  }

  .checkbox-item.checked .checkbox-text {
    color: var(--accent-green);
    font-weight: 500;
  }

  /* BUTTONS */
  .actions {
    margin-top: 36px;
    display: flex;
    flex-direction: column;
    gap: 12px;
    align-items: center;
  }

  .btn {
    padding: 16px 36px;
    border: none;
    border-radius: var(--radius-sm);
    font-family: inherit;
    font-size: 1rem;
    font-weight: 600;
    cursor: pointer;
    transition: all var(--transition);
    width: 100%;
    max-width: 420px;
    letter-spacing: 0.01em;
  }

  .btn-primary {
    background: var(--accent-blue);
    color: #fff;
    box-shadow: 0 4px 14px rgba(26, 58, 74, 0.3);
  }

  .btn-primary:hover {
    background: var(--accent-blue-hover);
    transform: translateY(-2px);
    box-shadow: 0 6px 20px rgba(26, 58, 74, 0.35);
  }

  .btn-primary:active {
    transform: translateY(0);
  }

  .btn-secondary {
    background: transparent;
    color: var(--text-muted);
    border: 2px solid var(--border-light);
    padding: 12px 28px;
    font-size: 0.9rem;
  }

  .btn-secondary:hover {
    border-color: var(--text-muted);
    color: var(--text-primary);
  }

  /* RESULT */
  .result-section {
    margin-top: 32px;
    overflow: hidden;
    max-height: 0;
    opacity: 0;
    transition: max-height 0.6s cubic-bezier(0.4, 0, 0.2, 1), opacity 0.4s ease, margin-top 0.4s ease;
  }

  .result-section.visible {
    max-height: 800px;
    opacity: 1;
  }

  .result-card {
    border-radius: var(--radius);
    padding: 32px 28px;
    box-shadow: var(--shadow-lg);
    border-left: 6px solid;
  }

  .result-card.excellent {
    background: linear-gradient(135deg, #E8F5E9 0%, #F1F8E9 100%);
    border-color: #4CAF50;
  }

  .result-card.good {
    background: linear-gradient(135deg, #E3F2FD 0%, #E8F5E9 100%);
    border-color: #2196F3;
  }

  .result-card.medium {
    background: linear-gradient(135deg, #FFF8E1 0%, #FFF3E0 100%);
    border-color: #FF9800;
  }

  .result-card.low {
    background: linear-gradient(135deg, #FFF3E0 0%, #FBE9E7 100%);
    border-color: #FF5722;
  }

  .result-card.very-low {
    background: linear-gradient(135deg, #FBE9E7 0%, #FFEBEE 100%);
    border-color: #D32F2F;
  }

  .result-header {
    display: flex;
    align-items: center;
    gap: 16px;
    margin-bottom: 16px;
  }

  .result-emoji {
    font-size: 2.2rem;
    line-height: 1;
  }

  .result-title {
    font-size: 1.3rem;
    font-weight: 700;
    color: var(--text-primary);
  }

  .result-score {
    font-size: 2.5rem;
    font-weight: 800;
    color: var(--accent-blue);
    margin: 8px 0;
    letter-spacing: -0.03em;
  }

  .result-percent {
    font-size: 1rem;
    color: var(--text-secondary);
    margin-bottom: 16px;
    font-weight: 500;
  }

  .result-text {
    font-size: 0.95rem;
    color: var(--text-secondary);
    line-height: 1.7;
    margin-bottom: 16px;
  }

  .result-blocks-info {
    background: rgba(255,255,255,0.7);
    border-radius: var(--radius-sm);
    padding: 16px 20px;
    margin-top: 16px;
  }

  .result-blocks-info h4 {
    font-size: 0.85rem;
    font-weight: 700;
    color: var(--text-secondary);
    text-transform: uppercase;
    letter-spacing: 0.05em;
    margin-bottom: 10px;
  }

  .block-progress-row {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 8px;
  }

  .block-progress-row:last-child {
    margin-bottom: 0;
  }

  .block-progress-label {
    font-size: 0.82rem;
    color: var(--text-secondary);
    min-width: 60px;
  }

  .block-progress-track {
    flex: 1;
    height: 6px;
    background: rgba(0,0,0,0.08);
    border-radius: 99px;
    overflow: hidden;
  }

  .block-progress-fill {
    height: 100%;
    border-radius: 99px;
    transition: width 0.5s ease;
  }

  .block-progress-count {
    font-size: 0.8rem;
    font-weight: 600;
    color: var(--text-muted);
    min-width: 36px;
    text-align: right;
  }

  /* ANIMATIONS */
  @keyframes fadeInUp {
    from {
      opacity: 0;
      transform: translateY(16px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  .block {
    animation: fadeInUp 0.5s ease backwards;
  }

  .block:nth-child(1) { animation-delay: 0.05s; }
  .block:nth-child(2) { animation-delay: 0.1s; }
  .block:nth-child(3) { animation-delay: 0.15s; }
  .block:nth-child(4) { animation-delay: 0.2s; }
  .block:nth-child(5) { animation-delay: 0.25s; }

  /* RESPONSIVE */
  @media (max-width: 600px) {
    body {
      padding: 12px 10px 48px;
    }

    .header {
      padding: 28px 20px;
    }

    .header h1 {
      font-size: 1.3rem;
    }

    .block-header {
      padding: 16px 18px 12px;
      gap: 12px;
    }

    .block-body {
      padding: 4px 12px 16px;
    }

    .checkbox-item {
      padding: 12px 10px;
      gap: 12px;
    }

    .checkbox-text {
      font-size: 0.88rem;
    }

    .result-card {
      padding: 24px 20px;
    }

    .result-score {
      font-size: 2rem;
    }

    .progress-bar-container {
      top: 6px;
      padding: 14px 18px;
    }
  }

  /* Print styles */
  @media print {
    .progress-bar-container, .actions, .btn { display: none; }
    .block { break-inside: avoid; box-shadow: none; border: 1px solid #ccc; }
  }
</style>
</head>
<body>

<div class="container">

  <!-- HEADER -->
  <header class="header">
    <div class="header-icon">
      <svg width="26" height="26" viewBox="0 0 24 24" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <path d="M22 10v6M2 10l10-5 10 5-10 5z"/>
        <path d="M6 12v5c3 3 9 3 12 0v-5"/>
      </svg>
    </div>
    <h1>МОТИВАЦИЯ УЧЕНИЯ: чек-лист осмысления темы</h1>
    <p>Отметьте галочками то, что для вас верно</p>
  </header>

  <!-- PROGRESS BAR -->
  <div class="progress-bar-container">
    <div class="progress-info">
      <span class="progress-label">Ваш прогресс</span>
      <span class="progress-count" id="progressCount">0 / 22</span>
    </div>
    <div class="progress-track">
      <div class="progress-fill" id="progressFill"></div>
    </div>
  </div>

  <!-- BLOCKS -->
  <div id="blocksContainer">

    <!-- BLOCK 1 -->
    <div class="block" data-block="1">
      <div class="block-header">
        <div class="block-number">1</div>
        <div class="block-title">Я понимаю, что такое учебная мотивация</div>
      </div>
      <div class="block-body">
        <label class="checkbox-item" data-block="1">
          <input type="checkbox" name="q1">
          <span class="custom-checkbox"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></span>
          <span class="checkbox-text">Я могу объяснить своими словами, что такое учебная мотивация</span>
        </label>
        <label class="checkbox-item" data-block="1">
          <input type="checkbox" name="q2">
          <span class="custom-checkbox"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></span>
          <span class="checkbox-text">Я понимаю, что мотивация включает 4 компонента: потребность, смысл, цель, эмоции</span>
        </label>
        <label class="checkbox-item" data-block="1">
          <input type="checkbox" name="q3">
          <span class="custom-checkbox"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></span>
          <span class="checkbox-text">Я различаю внешнюю и внутреннюю мотивацию</span>
        </label>
        <label class="checkbox-item" data-block="1">
          <input type="checkbox" name="q4">
          <span class="custom-checkbox"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></span>
          <span class="checkbox-text">Я понимаю, почему «эффект переподкрепления» опасен</span>
        </label>
      </div>
    </div>

    <!-- BLOCK 2 -->
    <div class="block" data-block="2">
      <div class="block-header">
        <div class="block-number">2</div>
        <div class="block-title">Я разобрался в видах мотивов и их динамике</div>
      </div>
      <div class="block-body">
        <label class="checkbox-item" data-block="2">
          <input type="checkbox" name="q5">
          <span class="custom-checkbox"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></span>
          <span class="checkbox-text">Я могу отличить познавательные мотивы от социальных</span>
        </label>
        <label class="checkbox-item" data-block="2">
          <input type="checkbox" name="q6">
          <span class="custom-checkbox"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></span>
          <span class="checkbox-text">Я могу отличить мотивы избегания неудач от внешних отметочных мотивов</span>
        </label>
        <label class="checkbox-item" data-block="2">
          <input type="checkbox" name="q7">
          <span class="custom-checkbox"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></span>
          <span class="checkbox-text">Я понимаю динамику мотивов от 1–2 к 3–4 классу</span>
        </label>
        <label class="checkbox-item" data-block="2">
          <input type="checkbox" name="q8">
          <span class="custom-checkbox"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></span>
          <span class="checkbox-text">Я знаю риски на каждом этапе (угасание, однообразие, мотивационный вакуум)</span>
        </label>
        <label class="checkbox-item" data-block="2">
          <input type="checkbox" name="q9">
          <span class="custom-checkbox"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></span>
          <span class="checkbox-text">Я понимаю, что такое мотивы самоутверждения и мотивы социального сотрудничества</span>
        </label>
      </div>
    </div>

    <!-- BLOCK 3 -->
    <div class="block" data-block="3">
      <div class="block-header">
        <div class="block-number">3</div>
        <div class="block-title">Я научился применять теории к реальной школе</div>
      </div>
      <div class="block-body">
        <label class="checkbox-item" data-block="3">
          <input type="checkbox" name="q10">
          <span class="custom-checkbox"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></span>
          <span class="checkbox-text">Я понимаю теорию самодетерминации (автономия, компетентность, связанность)</span>
        </label>
        <label class="checkbox-item" data-block="3">
          <input type="checkbox" name="q11">
          <span class="custom-checkbox"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></span>
          <span class="checkbox-text">Я могу объяснить, почему публичное сравнение разрушает мотивацию</span>
        </label>
        <label class="checkbox-item" data-block="3">
          <input type="checkbox" name="q12">
          <span class="custom-checkbox"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></span>
          <span class="checkbox-text">Я отличаю опасную атрибуцию от продуктивной</span>
        </label>
        <label class="checkbox-item" data-block="3">
          <input type="checkbox" name="q13">
          <span class="custom-checkbox"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></span>
          <span class="checkbox-text">Я знаю, почему нельзя говорить «ты неспособен»</span>
        </label>
        <label class="checkbox-item" data-block="3">
          <input type="checkbox" name="q14">
          <span class="custom-checkbox"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></span>
          <span class="checkbox-text">Я понимаю, что такое самоэффективность и её 4 источника</span>
        </label>
      </div>
    </div>

    <!-- BLOCK 4 -->
    <div class="block" data-block="4">
      <div class="block-header">
        <div class="block-number">4</div>
        <div class="block-title">Я могу заметить демотивацию и измерить мотивацию</div>
      </div>
      <div class="block-body">
        <label class="checkbox-item" data-block="4">
          <input type="checkbox" name="q15">
          <span class="custom-checkbox"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></span>
          <span class="checkbox-text">Я знаю, что «лень» часто маскирует низкую самоэффективность</span>
        </label>
        <label class="checkbox-item" data-block="4">
          <input type="checkbox" name="q16">
          <span class="custom-checkbox"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></span>
          <span class="checkbox-text">Я различаю, когда применять «Лесенку побуждений», а когда — «Незаконченные предложения»</span>
        </label>
        <label class="checkbox-item" data-block="4">
          <input type="checkbox" name="q17">
          <span class="custom-checkbox"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></span>
          <span class="checkbox-text">Я могу заполнить шкалу наблюдения за учеником</span>
        </label>
        <label class="checkbox-item" data-block="4">
          <input type="checkbox" name="q18">
          <span class="custom-checkbox"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></span>
          <span class="checkbox-text">Я знаю признаки выученной беспомощности у младшего школьника</span>
        </label>
      </div>
    </div>

    <!-- BLOCK 5 -->
    <div class="block" data-block="5">
      <div class="block-header">
        <div class="block-number">5</div>
        <div class="block-title">Я знаю, что делать (и чего не делать) учителю</div>
      </div>
      <div class="block-body">
        <label class="checkbox-item" data-block="5">
          <input type="checkbox" name="q19">
          <span class="custom-checkbox"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></span>
          <span class="checkbox-text">Я могу назвать 6 условий формирования познавательной мотивации</span>
        </label>
        <label class="checkbox-item" data-block="5">
          <input type="checkbox" name="q20">
          <span class="custom-checkbox"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></span>
          <span class="checkbox-text">Я понимаю, зачем нужно безотметочное обучение в 1 классе</span>
        </label>
        <label class="checkbox-item" data-block="5">
          <input type="checkbox" name="q21">
          <span class="custom-checkbox"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></span>
          <span class="checkbox-text">Я отличаю качественную обратную связь от пустой</span>
        </label>
        <label class="checkbox-item" data-block="5">
          <input type="checkbox" name="q22">
          <span class="custom-checkbox"><svg viewBox="0 0 12 12" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M2 6l3 3 5-6"/></svg></span>
          <span class="checkbox-text">Я могу перечислить типичные ошибки учителя, разрушающие мотивацию</span>
        </label>
      </div>
    </div>

  </div>

  <!-- ACTIONS -->
  <div class="actions">
    <button class="btn btn-primary" id="btnCheck" type="button">Проверить результат и получить рекомендации</button>
  </div>

  <!-- RESULT SECTION -->
  <div class="result-section" id="resultSection">
    <div class="result-card" id="resultCard">
      <div class="result-header">
        <span class="result-emoji" id="resultEmoji"></span>
        <div>
          <div class="result-title" id="resultTitle"></div>
        </div>
      </div>
      <div class="result-score" id="resultScore"></div>
      <div class="result-percent" id="resultPercent"></div>
      <div class="result-text" id="resultText"></div>
      <div class="result-blocks-info" id="resultBlocksInfo"></div>
    </div>
    <div class="actions" style="margin-top: 20px;">
      <button class="btn btn-secondary" id="btnReset" type="button">Очистить всё и пройти заново</button>
    </div>
  </div>

</div>

<script>
(function() {
  'use strict';

  const TOTAL_ITEMS = 22;
  const checkboxes = document.querySelectorAll('.checkbox-item input[type="checkbox"]');
  const progressCount = document.getElementById('progressCount');
  const progressFill = document.getElementById('progressFill');
  const btnCheck = document.getElementById('btnCheck');
  const btnReset = document.getElementById('btnReset');
  const resultSection = document.getElementById('resultSection');
  const resultCard = document.getElementById('resultCard');
  const resultEmoji = document.getElementById('resultEmoji');
  const resultTitle = document.getElementById('resultTitle');
  const resultScore = document.getElementById('resultScore');
  const resultPercent = document.getElementById('resultPercent');
  const resultText = document.getElementById('resultText');
  const resultBlocksInfo = document.getElementById('resultBlocksInfo');

  const blockNames = {
    1: 'Блок 1: Понятие мотивации',
    2: 'Блок 2: Виды мотивов',
    3: 'Блок 3: Теории на практике',
    4: 'Блок 4: Диагностика',
    5: 'Блок 5: Рекомендации учителю'
  };

  const blockTotals = { 1: 4, 2: 5, 3: 5, 4: 4, 5: 4 };

  function updateProgress() {
    let checked = 0;
    checkboxes.forEach(function(cb) {
      if (cb.checked) checked++;
    });
    progressCount.textContent = checked + ' / ' + TOTAL_ITEMS;
    progressFill.style.width = (checked / TOTAL_ITEMS * 100) + '%';
  }

  checkboxes.forEach(function(cb) {
    cb.addEventListener('change', function() {
      var parent = this.closest('.checkbox-item');
      if (this.checked) {
        parent.classList.add('checked');
      } else {
        parent.classList.remove('checked');
      }
      updateProgress();
    });
  });

  btnCheck.addEventListener('click', function() {
    var checked = 0;
    var blockCounts = { 1: 0, 2: 0, 3: 0, 4: 0, 5: 0 };

    checkboxes.forEach(function(cb) {
      if (cb.checked) {
        checked++;
        var block = cb.closest('.checkbox-item').getAttribute('data-block');
        blockCounts[parseInt(block)]++;
      }
    });

    var percent = Math.round(checked / TOTAL_ITEMS * 100);

    var emoji, title, cardClass, text;

    if (checked >= 20) {
      emoji = '🎉';
      title = 'Отлично!';
      cardClass = 'excellent';
      text = 'Вы глубоко и осмысленно усвоили тему. Вы готовы применять эти знания на практике и объяснять их другим. Единственная рекомендация — начните вести дневник наблюдений за мотивацией учеников, это закрепит материал.';
    } else if (checked >= 15) {
      emoji = '👍';
      title = 'Хороший результат';
      cardClass = 'good';
      var weakBlocks = [];
      for (var b = 1; b <= 5; b++) {
        if (blockCounts[b] < blockTotals[b]) {
          weakBlocks.push(b);
        }
      }
      var weakBlockNames = weakBlocks.map(function(b) { return blockNames[b]; });
      text = 'Хороший результат, но есть зоны роста. Рекомендуем перечитать разделы лекции, соответствующие непроверенным утверждениям.';
      if (weakBlocks.indexOf(2) !== -1) text += ' Обратите особое внимание на: различение видов мотивов (Блок 2).';
      if (weakBlocks.indexOf(3) !== -1) text += ' Уделите внимание практическому применению теорий (Блок 3).';
    } else if (checked >= 10) {
      emoji = '📖';
      title = 'Средний уровень';
      cardClass = 'medium';
      text = 'Средний уровень осмысления. Вернитесь к лекции и сосредоточьтесь на этих темах: 1) структура учебной мотивации; 2) отличие внутренней от внешней мотивации; 3) теория атрибуции; 4) условия формирования мотивации. Заполните чек-лист ещё раз после повторного чтения.';
    } else if (checked >= 5) {
      emoji = '🔄';
      title = 'Освоение только начинается';
      cardClass = 'low';
      text = 'Освоение темы только начинается. Вам нужно вернуться к лекции системно. Особое внимание уделите базовым понятиям (Блок 1), классификации мотивов (Блок 2) и практическим рекомендациям (Блок 5). Рекомендуем обсудить материал с преподавателем или в учебной группе.';
    } else {
      emoji = '⚠️';
      title = 'Нужно начать сначала';
      cardClass = 'very-low';
      text = 'Вы почти не отметили утверждений. Скорее всего, вы ещё не прочитали лекцию или не поняли ключевые идеи. Настоятельно рекомендуем: 1) внимательно прочитать всю лекцию; 2) выписать 5 главных тезисов; 3) вернуться к чек-листу.';
    }

    resultEmoji.textContent = emoji;
    resultTitle.textContent = title;
    resultScore.textContent = checked + ' из ' + TOTAL_ITEMS;
    resultPercent.textContent = percent + '%';
    resultText.textContent = text;

    // Build blocks info
    var blocksHtml = '<h4>Прогресс по блокам</h4>';
    var barColors = { 1: '#4CAF50', 2: '#2196F3', 3: '#FF9800', 4: '#9C27B0', 5: '#F44336' };
    for (var b = 1; b <= 5; b++) {
      var pct = Math.round(blockCounts[b] / blockTotals[b] * 100);
      blocksHtml += '<div class="block-progress-row">';
      blocksHtml += '<span class="block-progress-label">Блок ' + b + '</span>';
      blocksHtml += '<div class="block-progress-track"><div class="block-progress-fill" style="width:' + pct + '%;background:' + barColors[b] + '"></div></div>';
      blocksHtml += '<span class="block-progress-count">' + blockCounts[b] + '/' + blockTotals[b] + '</span>';
      blocksHtml += '</div>';
    }
    resultBlocksInfo.innerHTML = blocksHtml;

    resultCard.className = 'result-card ' + cardClass;
    resultSection.classList.add('visible');

    setTimeout(function() {
      resultSection.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
    }, 100);
  });

  btnReset.addEventListener('click', function() {
    checkboxes.forEach(function(cb) {
      cb.checked = false;
      var parent = cb.closest('.checkbox-item');
      parent.classList.remove('checked');
    });
    updateProgress();
    resultSection.classList.remove('visible');
    window.scrollTo({ top: 0, behavior: 'smooth' });
  });

  updateProgress();
})();
</script>

</body>
</html>

