<style>
  .rm-wrap { max-width: 640px; padding: 2rem 0; font-family: var(--font-mono); }
  .rm-h1 { font-size: 22px; font-weight: 500; color: var(--color-text-primary); margin: 0 0 0.5rem; }
  .rm-tagline { font-size: 14px; color: var(--color-text-secondary); margin: 0 0 1.5rem; line-height: 1.6; }
  .rm-h2 { font-size: 15px; font-weight: 500; color: var(--color-text-primary); margin: 1.5rem 0 0.5rem; border-bottom: 0.5px solid var(--color-border-tertiary); padding-bottom: 4px; }
  .rm-badge { display: inline-block; font-size: 12px; padding: 3px 10px; border-radius: 999px; margin-right: 6px; margin-bottom: 6px; font-family: var(--font-mono); }
  .b-py { background: var(--color-background-info); color: var(--color-text-info); }
  .b-nb { background: var(--color-background-warning); color: var(--color-text-warning); }
  .b-gh { background: var(--color-background-secondary); color: var(--color-text-secondary); border: 0.5px solid var(--color-border-secondary); }
  .rm-code { background: var(--color-background-secondary); border: 0.5px solid var(--color-border-tertiary); border-radius: var(--border-radius-md); padding: 0.75rem 1rem; font-size: 13px; color: var(--color-text-primary); margin: 0.5rem 0 1rem; white-space: pre; overflow-x: auto; }
  .rm-ul { margin: 0; padding-left: 1.25rem; }
  .rm-ul li { font-size: 14px; color: var(--color-text-primary); margin-bottom: 6px; line-height: 1.6; }
  .rm-ul li span { color: var(--color-text-secondary); }
  .rm-insight { background: var(--color-background-secondary); border-left: 2px solid var(--color-border-info); border-radius: 0; padding: 0.6rem 1rem; margin-bottom: 8px; font-size: 13px; color: var(--color-text-primary); line-height: 1.6; }
  .rm-insight strong { color: var(--color-text-info); font-weight: 500; }
  .anno { font-size: 11px; color: var(--color-text-secondary); background: var(--color-background-warning); border: 0.5px solid var(--color-border-tertiary); border-radius: var(--border-radius-md); padding: 2px 8px; margin-left: 8px; font-family: var(--font-sans); vertical-align: middle; }
</style>

<div class="rm-wrap">
  <h2 class="rm-h1">Review Sentiment Analyzer <span class="anno">✓ what it is</span></h2>
  <p class="rm-tagline">NLP pipeline that classifies 23,000+ women's clothing reviews as Positive, Negative, or Neutral — then surfaces which product categories and keywords drive each sentiment. <span class="anno">✓ one sentence, concrete number</span></p>

  <div>
    <span class="rm-badge b-py">Python</span>
    <span class="rm-badge b-nb">Jupyter</span>
    <span class="rm-badge b-gh">TextBlob / VADER</span>
    <span class="rm-badge b-gh">Pandas</span>
    <span class="rm-badge b-gh">Matplotlib</span>
    <span class="anno" style="font-family:var(--font-sans)">✓ stack visible immediately</span>
  </div>

  <div class="rm-h2">What it does</div>
  <ul class="rm-ul">
    <li>Cleans and normalizes review text <span>(lowercase, punctuation removal)</span></li>
    <li>Scores each review with VADER compound sentiment → labels it Positive / Negative / Neutral</li>
    <li>Aggregates scores by product department and class to rank best and worst performers</li>
    <li>Generates keyword word clouds and frequency charts for each sentiment bucket</li>
  </ul>
  <p style="font-size:13px;color:var(--color-text-secondary);margin-top:6px;">Dataset: <a href="https://www.kaggle.com/" style="color:var(--color-text-info)">Women's Clothing E-Commerce Reviews</a> via Kaggle</p>

  <div class="rm-h2">Setup</div>
  <div class="rm-code">pip install pandas textblob matplotlib</div>
  <p style="font-size:13px;color:var(--color-text-secondary);margin-top:-4px;">Open <code style="font-size:12px;">notebooks/</code> and run cells top to bottom.</p>

  <div class="rm-h2">Key findings <span class="anno" style="font-family:var(--font-sans)">✓ results, not consulting slides</span></div>
  <div class="rm-insight"><strong>Trend dept. has 15.5% negative rate</strong> vs. 8–10% elsewhere — sizing inconsistencies appear as the main driver.</div>
  <div class="rm-insight"><strong>81% of reviews are positive.</strong> Top keywords: "love", "perfect fit", "flattering", "great".</div>
  <div class="rm-insight"><strong>Dresses flagged for "small" / "fabric"</strong> are strong discontinuation candidates based on recurring negative terms.</div>
</div>
