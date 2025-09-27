<script setup lang="ts">
useSeoMeta({
  title: 'World Wide Bank - Decentralized P2P Banking Protocol',
  description: 'Open source, uncensorable peer-to-peer economic system. Community-controlled banking that blends communist principles with capitalist incentives. No central control, fully transparent.',
  ogTitle: 'World Wide Bank - Decentralized P2P Banking Protocol',
  ogDescription: 'Build your own community bank with our open source protocol. Resist financial censorship with true P2P economics.',
  ogUrl: 'https://github.com/World-Wide-Bank-WWB/World-Wide-Bank-P2P-World-Banking/blob/master/Whitepaper/whitepaper.pdf',
  twitterCard: 'summary_large_image',
  keywords: 'p2p banking, decentralized finance, open source bank, community economics, uncensorable money, mutual aid protocol'
})

const activeSection = ref('introduction');

const sections = {
  introduction: {
    title: 'Introduction',
    content: 'World Wide Bank Protocol - Decentralized P2P Economic Cooperation'
  },
  problem: {
    title: 'The Problem', 
    content: 'Why we need uncensorable financial systems'
  },
  solution: {
    title: 'Our Solution',
    content: 'How WWB solves financial censorship'
  },
  technology: {
    title: 'Technology',
    content: 'P2P architecture and implementation'
  },
  economics: {
    title: 'Economics', 
    content: 'Shared pool model and incentives'
  },
  gettingStarted: {
    title: 'Get Started',
    content: 'How to deploy your own community bank'
  }
};
</script>

<template>
  <div class="whitepaper-container">
    <header class="header">
      <h1>World Wide Bank Protocol</h1>
      <p class="subtitle">Open Source Decentralized Banking Infrastructure</p>
      <p class="meta-description">Build community-controlled, uncensorable financial systems with our P2P protocol. No central authority, fully transparent, voluntary participation.</p>
    </header>

    <nav class="navigation">
      <button 
        v-for="(section, key) in sections" 
        :key="key"
        @click="activeSection = key"
        :class="{ active: activeSection === key }"
      >
        {{ section.title }}
      </button>
    </nav>

    <main class="content">
      <!-- Introduction Section -->
      <section v-if="activeSection === 'introduction'" class="section">
        <h2>What is World Wide Bank?</h2>
        <p>World Wide Bank (WWB) is an <strong>open-source protocol</strong> for creating decentralized, peer-to-peer banking systems that cannot be shut down by any government or corporation. It enables communities to build their own financial infrastructure based on mutual aid and voluntary cooperation.</p>
        
        <div class="feature-grid">
          <div class="feature">
            <h3>🛡️ Uncensorable</h3>
            <p>True P2P architecture with no central points of failure. Operates across borders without permission.</p>
          </div>
          <div class="feature">
            <h3>🔓 Open Source</h3>
            <p>Every line of code is publicly auditable. No hidden mechanisms or backdoors.</p>
          </div>
          <div class="feature">
            <h3>🌍 Borderless</h3>
            <p>Mesh network of interconnected instances that transcend geographical boundaries.</p>
          </div>
          <div class="feature">
            <h3>⚖️ Community Governed</h3>
            <p>Rules are encoded in transparent code, not dictated by central authorities.</p>
          </div>
        </div>

        <h3>Core Philosophy</h3>
        <p>WWB blends the best of communist principles (from each according to ability, to each according to need) with capitalist incentives (voluntary participation, contribution-based rewards). This creates a circular economy where wealth circulates rather than accumulates.</p>
      </section>

      <!-- Problem Section -->
      <section v-else-if="activeSection === 'problem'" class="section">
        <h2>The Problem: Centralized Financial Control</h2>
        
        <div class="problem-list">
          <div class="problem-item">
            <h3>🚫 Financial Surveillance</h3>
            <p>Governments and corporations track every transaction, creating permanent financial records that can be used for control.</p>
          </div>
          <div class="problem-item">
            <h3>💸 Wealth Inequality</h3>
            <p>Traditional banking systems favor those who already have wealth, creating ever-widening gaps between rich and poor.</p>
          </div>
          <div class="problem-item">
            <h3>🌐 Cross-Border Barriers</h3>
            <p>Moving money across borders is slow, expensive, and subject to arbitrary restrictions and sanctions.</p>
          </div>
          <div class="problem-item">
            <h3>⚡ Single Points of Failure</h3>
            <p>Centralized systems can be shut down, frozen, or controlled by governments during crises or political unrest.</p>
          </div>
        </div>

        <h3>Why This Matters Now</h3>
        <p>With the rise of Central Bank Digital Currencies (CBDCs) and increasing financial surveillance, the need for decentralized, citizen-controlled alternatives has never been more urgent. WWB provides a viable path toward economic sovereignty.</p>
      </section>

      <!-- Solution Section -->
      <section v-else-if="activeSection === 'solution'" class="section">
        <h2>Our Solution: True P2P Economics</h2>
        
        <div class="solution-steps">
          <div class="step">
            <span class="step-number">1</span>
            <div>
              <h3>Decentralized Network</h3>
              <p>Every participant runs equal software, communicating directly in a mesh network. No central servers to target or shut down.</p>
            </div>
          </div>
          <div class="step">
            <span class="step-number">2</span>
            <div>
              <h3>Shared Resource Pools</h3>
              <p>Communities create shared pools where participants can deposit and withdraw according to transparent, code-enforced rules.</p>
            </div>
          </div>
          <div class="step">
            <span class="step-number">3</span>
            <div>
              <h3>Voluntary Participation</h3>
              <p>No one is forced to participate. Those who join do so because they believe in the community's rules and values.</p>
            </div>
          </div>
          <div class="step">
            <span class="step-number">4</span>
            <div>
              <h3>Transparent Governance</h3>
              <p>All rules are publicly auditable code. Changes require community consensus through software updates.</p>
            </div>
          </div>
        </div>

        <h3>Mathematical Uncensorability</h3>
        <p>WWB achieves true resistance through its P2P architecture. The system can continue operating even if 90% of nodes are taken offline, automatically routing around censorship attempts.</p>
      </section>

      <!-- Technology Section -->
      <section v-else-if="activeSection === 'technology'" class="section">
        <h2>Technical Architecture</h2>
        
        <div class="architecture">
          <div class="arch-layer">
            <h3>🌐 Network Layer</h3>
            <p><strong>Mesh topology</strong> with multiple transport protocols (HTTP, WebSockets, Tor support). Each node maintains connections to several peers for redundancy.</p>
            <code>Node A ↔ Node B ↔ Node C ↔ Node D</code>
          </div>
          
          <div class="arch-layer">
            <h3>🔗 Consensus Mechanism</h3>
            <p><strong>Rule-based validation</strong> where each node independently verifies transactions against community-defined rules encoded in smart contracts.</p>
            <code>validateTransaction(tx) → Boolean</code>
          </div>
          
          <div class="arch-layer">
            <h3>💰 Economic Layer</h3>
            <p><strong>Shared pool mathematics</strong> with contribution-based access controls and voluntary reciprocity mechanisms.</p>
            <code>WithdrawalLimit = f(Contribution, PoolSize, CommunityRules)</code>
          </div>
        </div>

        <h3>Key Technical Features</h3>
        <ul>
          <li><strong>No Single Point of Failure:</strong> Operates without central servers</li>
          <li><strong>Cross-Platform:</strong> Runs on desktop, mobile, and embedded devices</li>
          <li><strong>Privacy Options:</strong> Supports Tor and other anonymity networks</li>
          <li><strong>Federation Ready:</strong> Multiple instances can interoperate securely</li>
        </ul>
      </section>

      <!-- Economics Section -->
      <section v-else-if="activeSection === 'economics'" class="section">
        <h2>Economic Model: Circular Wealth</h2>
        
        <div class="economic-principles">
          <div class="principle">
            <h3>💎 Shared Pool Foundation</h3>
            <p>The core economic unit is the shared pool where participants voluntarily deposit resources that become available to community members in need.</p>
            <code>Pool(t) = Pool(t-1) + Deposits - Withdrawals</code>
          </div>
          
          <div class="principle">
            <h3>📊 Contribution Scoring</h3>
            <p>Participants earn trust and access privileges through demonstrated commitment to the community, creating natural incentives for cooperation.</p>
            <code>Access = Base + (Contribution × TrustMultiplier)</code>
          </div>
          
          <div class="principle">
            <h3>🔄 Voluntary Reciprocity</h3>
            <p>No mandatory repayment schedules or interest charges. The system encourages voluntary giving through social capital and long-term benefits.</p>
          </div>
        </div>

        <h3>Anti-Fragile Design</h3>
        <p>Unlike traditional systems that collapse under stress, WWB becomes stronger through challenges. Attempted exploitation leads to improved rule sets that benefit the entire community.</p>
      </section>

      <!-- Getting Started Section -->
      <section v-else-if="activeSection === 'gettingStarted'" class="section">
        <h2>Start Your Community Bank</h2>
        
        <div class="getting-started-steps">
          <div class="step-card">
            <h3>1. Read the Whitepaper</h3>
            <p>Understand the full protocol specification and economic model before deploying.</p>
            <a href="https://github.com/World-Wide-Bank-WWB/World-Wide-Bank-P2P-World-Banking/blob/master/Whitepaper/whitepaper.pdf" target="_blank" rel="noopener noreferrer">
                <button class="doc-button">📄 Download Full Whitepaper (PDF)</button>
            </a>
          </div>
          
          <div class="step-card">
            <h3>2. Deploy Your Instance</h3>
            <p>Use our Docker templates to launch your own WWB node in minutes.</p>
            <code>docker-compose up -d</code>
          </div>
          
          <div class="step-card">
            <h3>3. Customize Rules</h3>
            <p>Adapt the open source code to your community's specific needs and values.</p>
            <code>// config/rules.js - Modify community parameters</code>
          </div>
          
          <div class="step-card">
            <h3>4. Invite Participants</h3>
            <p>Grow your community and start building economic resilience together.</p>
          </div>
        </div>

        <h3>Community Resources</h3>
        <div class="resource-links">
          <a href="#" class="resource-link">📚 Protocol Documentation</a>
          <a href="#" class="resource-link">🛠️ Developer Guide</a>
          <a href="#" class="resource-link">💬 Community Forum</a>
          <a href="#" class="resource-link">🐛 Issue Tracker</a>
        </div>
      </section>
    </main>

    <footer class="footer">
      <div class="footer-content">
        <div class="footer-section">
          <h4>World Wide Bank Protocol</h4>
          <p>Open source decentralized banking infrastructure for community economic sovereignty.</p>
        </div>
        
        <div class="footer-section">
          <h4>Resources</h4>
          <div class="footer-links">
            <a href="https://github.com/World-Wide-Bank-WWB/World-Wide-Bank-P2P-World-Banking/blob/master/Whitepaper/whitepaper.pdf" class="footer-link">📄 Whitepaper</a>
            <a href="https://github.com/World-Wide-Bank-WWB/World-Wide-Bank-P2P-World-Banking/" class="footer-link">💻 GitHub Repository</a>
            <a href="https://github.com/orgs/World-Wide-Bank-WWB/projects/1" class="footer-link">👥 Community Chat / Project Board</a>
            <a href="https://github.com/World-Wide-Bank-WWB/World-Wide-Bank-P2P-World-Banking/blob/master/readme.md" class="footer-link">🔧 Developer Docs</a>
          </div>
        </div>
        
        <div class="footer-section">
          <h4>Principles</h4>
          <p>Decentralization • Transparency • Voluntary Cooperation • Economic Freedom</p>
        </div>
      </div>
      
      <div class="footer-bottom">
        <p>World Wide Bank Protocol - Open Source Software - Build Economic Freedom</p>
      </div>
    </footer>
  </div>
</template>

<style scoped>
.whitepaper-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 2rem;
  font-family: system-ui, sans-serif;
  line-height: 1.6;
}

.header {
  text-align: center;
  margin-bottom: 3rem;
  padding-bottom: 2rem;
  border-bottom: 1px solid #e1e8ed;
}

.header h1 {
  font-size: 3.5rem;
  margin: 0;
  color: #2c3e50;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.subtitle {
  font-size: 1.4rem;
  color: #7f8c8d;
  margin: 1rem 0;
}

.meta-description {
  font-size: 1.1rem;
  color: #5d6d7e;
  max-width: 800px;
  margin: 1rem auto;
  line-height: 1.8;
}

.navigation {
  display: flex;
  gap: 0.5rem;
  margin-bottom: 3rem;
  flex-wrap: wrap;
  justify-content: center;
}

.navigation button {
  padding: 1rem 2rem;
  border: 2px solid #3498db;
  background: white;
  color: #3498db;
  border-radius: 25px;
  cursor: pointer;
  transition: all 0.3s ease;
  font-weight: 600;
}

.navigation button.active,
.navigation button:hover {
  background: #3498db;
  color: white;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(52, 152, 219, 0.3);
}

.content {
  min-height: 600px;
}

.section h2 {
  color: #2c3e50;
  border-bottom: 3px solid #3498db;
  padding-bottom: 0.5rem;
  margin-bottom: 2rem;
}

.section h3 {
  color: #34495e;
  margin: 2rem 0 1rem 0;
}

.feature-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2rem;
  margin: 2rem 0;
}

.feature {
  background: #f8f9fa;
  padding: 2rem;
  border-radius: 12px;
  border-left: 4px solid #3498db;
}

.problem-list, .economic-principles {
  display: grid;
  gap: 1.5rem;
  margin: 2rem 0;
}

.problem-item, .principle {
  background: #f8f9fa;
  padding: 1.5rem;
  border-radius: 8px;
  border-left: 4px solid #e74c3c;
}

.principle {
  border-left-color: #27ae60;
}

.solution-steps, .getting-started-steps {
  display: grid;
  gap: 2rem;
  margin: 2rem 0;
}

.step {
  display: flex;
  align-items: flex-start;
  gap: 1.5rem;
  padding: 1.5rem;
  background: #f8f9fa;
  border-radius: 12px;
}

.step-number {
  background: #3498db;
  color: white;
  width: 3rem;
  height: 3rem;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
  font-size: 1.2rem;
  flex-shrink: 0;
}

.architecture {
  display: grid;
  gap: 1.5rem;
  margin: 2rem 0;
}

.arch-layer {
  background: #f8f9fa;
  padding: 1.5rem;
  border-radius: 8px;
  border-left: 4px solid #9b59b6;
}

.step-card {
  background: #f8f9fa;
  padding: 2rem;
  border-radius: 12px;
  text-align: center;
}

.doc-button {
  background: #27ae60;
  color: white;
  border: none;
  padding: 1rem 2rem;
  border-radius: 8px;
  cursor: pointer;
  font-size: 1.1rem;
  margin-top: 1rem;
}

.resource-links {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 1rem;
  margin: 2rem 0;
}

.resource-link, .footer-link {
  display: block;
  padding: 1rem;
  background: #f8f9fa;
  border-radius: 8px;
  text-decoration: none;
  color: #3498db;
  transition: all 0.3s ease;
}

.resource-link:hover, .footer-link:hover {
  background: #3498db;
  color: white;
  transform: translateX(5px);
}

code {
  background: #2c3e50;
  color: #ecf0f1;
  padding: 0.5rem 1rem;
  border-radius: 4px;
  font-family: 'Courier New', monospace;
  display: block;
  margin: 1rem 0;
  overflow-x: auto;
}

.footer {
  margin-top: 4rem;
  padding-top: 3rem;
  border-top: 1px solid #bdc3c7;
}

.footer-content {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
  margin-bottom: 2rem;
}

.footer-section h4 {
  color: #2c3e50;
  margin-bottom: 1rem;
}

.footer-links {
  display: grid;
  gap: 0.5rem;
}

.footer-bottom {
  text-align: center;
  padding-top: 2rem;
  border-top: 1px solid #bdc3c7;
  color: #7f8c8d;
}

@media (max-width: 768px) {
  .whitepaper-container {
    padding: 1rem;
  }
  
  .header h1 {
    font-size: 2.5rem;
  }
  
  .navigation {
    flex-direction: column;
  }
  
  .feature-grid {
    grid-template-columns: 1fr;
  }
  
  .step {
    flex-direction: column;
    text-align: center;
  }
}

/* SEO enhancements */
.section {
  scroll-margin-top: 2rem;
}

/* Print styles */
@media print {
  .navigation, .footer {
    display: none;
  }
  
  .whitepaper-container {
    max-width: none;
    padding: 0;
  }
}
</style>