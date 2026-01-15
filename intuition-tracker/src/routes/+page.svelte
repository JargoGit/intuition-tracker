<script>
  const systemStatus = {
    state: "Initialized",
    mode: "Idle",
    lastUpdate: new Date().toLocaleString(),
    signalIntegrity: "Stable",
    notes: "Awaiting input"
  };
</script>

<main>
  <h1>Intuition Tracker</h1>

  <section class="status-panel">
    <div class="row">
      <span class="label">System State</span>
      <span class="value">{systemStatus.state}</span>
    </div>

    <div class="row">
      <span class="label">Mode</span>
      <span class="value">{systemStatus.mode}</span>
    </div>

    <div class="row">
      <span class="label">Signal Integrity</span>
      <span class="value">{systemStatus.signalIntegrity}</span>
    </div>

    <div class="row">
      <span class="label">Last Update</span>
      <span class="value">{systemStatus.lastUpdate}</span>
    </div>

    <div class="row notes">
      <span class="label">Notes</span>
      <span class="value">{systemStatus.notes}</span>
    </div>
  </section>
</main>

<style>
  main {
    font-family: system-ui, -apple-system, BlinkMacSystemFont, sans-serif;
    padding: 2rem;
    max-width: 720px;
  }

  h1 {
    font-size: 1.75rem;
    margin-bottom: 1.5rem;
    font-weight: 600;
  }

  .status-panel {
    border: 1px solid #2a2a2a;
    border-radius: 8px;
    padding: 1.25rem;
    background: rgba(255, 255, 255, 0.02);
  }

  .row {
    display: flex;
    justify-content: space-between;
    padding: 0.4rem 0;
    border-bottom: 1px solid rgba(255, 255, 255, 0.06);
    font-size: 0.95rem;
  }

  .row:last-child {
    border-bottom: none;
  }

  .label {
    opacity: 0.7;
  }

  .value {
    font-weight: 500;
  }

  .notes .value {
    font-style: italic;
    opacity: 0.85;
  }
</style>
