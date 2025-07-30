# Share-Capital-Scenarios
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Kaumatua Energy NZ - Capital Raise Dashboard</title>
  <!-- Tailwind CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-50 text-gray-900">
  <div class="max-w-7xl mx-auto py-8 px-4">
    <!-- Header -->
    <header class="mb-8">
      <h1 class="text-3xl font-bold text-blue-900">Kaumatua Energy NZ - Capital Raise Timeline</h1>
      <p class="text-sm text-gray-600">Community-focused energy company providing 30% power bill subsidy to pensioners</p>
      <p class="text-sm text-gray-600">All figures in New Zealand dollars (NZD)</p>
      <p class="text-xs text-gray-500 mt-1">
        💾 <span id="saveStatus">Data automatically saved to browser storage</span>
      </p>
    </header>

    <!-- Business Overview -->
    <section class="mb-10">
      <div class="bg-gradient-to-r from-blue-50 to-green-50 rounded-xl p-6 border-l-4 border-blue-500">
        <h2 class="text-xl font-semibold mb-4 text-blue-900">Business Overview</h2>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
          <div>
            <h3 class="font-medium text-gray-700 mb-2">Revenue Model</h3>
            <ul class="text-sm text-gray-600 space-y-1">
              <li>• Solar energy sales</li>
              <li>• Wholesale market participation</li>
              <li>• Community fund donations</li>
              <li>• Energy consultation services</li>
            </ul>
          </div>
          <div>
            <h3 class="font-medium text-gray-700 mb-2">Key Metrics</h3>
            <ul class="text-sm text-gray-600 space-y-1">
              <li>• <strong>5-Year Revenue CAGR:</strong> 85%</li>
              <li>• <strong>Net Margin (Y5):</strong> 62%</li>
              <li>• <strong>Target Customers:</strong> 1,000 Kaumatua</li>
              <li>• <strong>Payback Period:</strong> 2.5 years</li>
            </ul>
          </div>
          <div>
            <h3 class="font-medium text-gray-700 mb-2">Financial Projections</h3>
            <ul class="text-sm text-gray-600 space-y-1">
              <li>• <strong>2024 Revenue:</strong> $495,529</li>
              <li>• <strong>2025 Revenue:</strong> $1,511,769</li>
              <li>• <strong>2028 Revenue:</strong> $5,780,936</li>
              <li>• <strong>2028 Net Profit:</strong> $3,566,576</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- ===== Founding Shareholders ======================================= -->
    <section aria-labelledby="founders" class="mb-10">
      <h2 id="founders" class="text-xl font-semibold mb-6">Founding shareholders</h2>
      <div class="bg-white rounded-xl shadow p-6">
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6 mb-4">
          <label class="block">
            <span class="block text-sm font-medium mb-1">Founder 1 (%)</span>
            <input type="number" id="founder1Percent" class="w-full px-3 py-2 border rounded-md" value="40" min="0" max="100" step="0.1" />
          </label>
          <label class="block">
            <span class="block text-sm font-medium mb-1">Founder 2 (%)</span>
            <input type="number" id="founder2Percent" class="w-full px-3 py-2 border rounded-md" value="30" min="0" max="100" step="0.1" />
          </label>
          <label class="block">
            <span class="block text-sm font-medium mb-1">Founder 3 (%)</span>
            <input type="number" id="founder3Percent" class="w-full px-3 py-2 border rounded-md" value="20" min="0" max="100" step="0.1" />
          </label>
          <label class="block">
            <span class="block text-sm font-medium mb-1">Founder 4 (%)</span>
            <input type="number" id="founder4Percent" class="w-full px-3 py-2 border rounded-md" value="10" min="0" max="100" step="0.1" />
          </label>
        </div>
        <div class="text-sm text-gray-600">
          <span>Total: <span id="totalFounderPercent" class="font-medium">100.0%</span></span>
          <span id="percentageWarning" class="ml-4 text-red-600 font-medium hidden">⚠️ Total should equal 100%</span>
        </div>
      </div>
    </section>

    <!-- ===== Variable inputs ================================================== -->
    <section aria-labelledby="variables" class="mb-10">
      <h2 id="variables" class="text-xl font-semibold mb-6">Adjust raise variables</h2>
      <!-- Grid wrapper for three raises -->
      <div class="space-y-10">
        <!-- Raise 1 -->
        <div>
          <h3 class="text-lg font-medium mb-4 text-blue-900">1️⃣ Seed Round (2024) - Initial Funding</h3>
          <div class="grid grid-cols-1 sm:grid-cols-3 gap-6">
            <label class="block">
              <span class="block text-sm font-medium mb-1">Capital to raise (NZ$ millions)</span>
              <input type="number" id="amount1" class="w-full px-3 py-2 border rounded-md" value="2.5" min="0.1" step="0.1" />
            </label>
            <label class="block">
              <span class="block text-sm font-medium mb-1">Share price (NZ$)</span>
              <input type="number" id="sharePrice1" class="w-full px-3 py-2 border rounded-md" value="0.50" min="0.01" step="0.01" />
            </label>
            <label class="block">
              <span class="block text-sm font-medium mb-1">Pre‑money valuation (NZ$ millions)</span>
              <input type="number" id="valuation1" class="w-full px-3 py-2 border rounded-md" value="7.5" min="1" step="0.1" />
            </label>
          </div>
          <div class="mt-4 p-4 bg-blue-50 rounded-lg">
            <p class="text-sm text-blue-800"><strong>Use of funds:</strong> Solar panel installation ($1.2M), Company setup ($0.5M), Marketing ($0.3M), Operational reserves ($0.5M)</p>
          </div>
        </div>
        <!-- Raise 2 -->
        <div>
          <h3 class="text-lg font-medium mb-4 text-blue-900">2️⃣ Series A (2025) - Scaling Operations</h3>
          <div class="grid grid-cols-1 sm:grid-cols-3 gap-6">
            <label class="block">
              <span class="block text-sm font-medium mb-1">Capital to raise (NZ$ millions)</span>
              <input type="number" id="amount2" class="w-full px-3 py-2 border rounded-md" value="12" min="0.1" step="0.1" />
            </label>
            <label class="block">
              <span class="block text-sm font-medium mb-1">Share price (NZ$)</span>
              <input type="number" id="sharePrice2" class="w-full px-3 py-2 border rounded-md" value="1.50" min="0.01" step="0.01" />
            </label>
            <label class="block">
              <span class="block text-sm font-medium mb-1">Pre‑money valuation (NZ$ millions)</span>
              <input type="number" id="valuation2" class="w-full px-3 py-2 border rounded-md" value="18" min="1" step="0.1" />
            </label>
          </div>
          <div class="mt-4 p-4 bg-blue-50 rounded-lg">
            <p class="text-sm text-blue-800"><strong>Business context:</strong> Revenue growing to $1.5M, 750 Kaumatua customers, proven business model</p>
          </div>
        </div>
        <!-- Raise 3 -->
        <div>
          <h3 class="text-lg font-medium mb-4 text-blue-900">3️⃣ Series B (2026) - Major Expansion</h3>
          <div class="grid grid-cols-1 sm:grid-cols-3 gap-6">
            <label class="block">
              <span class="block text-sm font-medium mb-1">Capital to raise (NZ$ millions)</span>
              <input type="number" id="amount3" class="w-full px-3 py-2 border rounded-md" value="25" min="0.1" step="0.1" />
            </label>
            <label class="block">
              <span class="block text-sm font-medium mb-1">Share price (NZ$)</span>
              <input type="number" id="sharePrice3" class="w-full px-3 py-2 border rounded-md" value="3.00" min="0.01" step="0.01" />
            </label>
            <label class="block">
              <span class="block text-sm font-medium mb-1">Pre‑money valuation (NZ$ millions)</span>
              <input type="number" id="valuation3" class="w-full px-3 py-2 border rounded-md" value="50" min="1" step="0.1" />
            </label>
          </div>
          <div class="mt-4 p-4 bg-blue-50 rounded-lg">
            <p class="text-sm text-blue-800"><strong>Business context:</strong> Revenue $2.7M, 1,000+ Kaumatua customers, scaling for national expansion</p>
          </div>
        </div>
      </div>
    </section>

    <!-- ===== Snapshots ======================================================== -->
    <section aria-labelledby="snapshots" class="mb-10">
      <h2 id="snapshots" class="text-xl font-semibold mb-6">Capital raise snapshots</h2>
      <div class="space-y-10">
        <!-- Snapshot 1 -->
        <div id="snapshot1" class="bg-white rounded-xl shadow p-6">
          <h3 class="text-lg font-medium mb-4 text-blue-900">After Seed Round (2024)</h3>
          <div class="grid grid-cols-1 sm:grid-cols-4 gap-6 mb-6">
            <div>
              <p class="text-sm text-gray-500">Capital raised</p>
              <p id="capitalRaised1" class="text-2xl font-bold">$2,500,000</p>
            </div>
            <div>
              <p class="text-sm text-gray-500">Shares issued</p>
              <p id="sharesIssued1" class="text-2xl font-bold">5,000,000</p>
            </div>
            <div>
              <p class="text-sm text-gray-500">Post‑money valuation</p>
              <p id="postMoney1" class="text-2xl font-bold">$10,000,000</p>
            </div>
            <div>
              <p class="text-sm text-gray-500">New‑investor ownership</p>
              <p id="investorOwnership1" class="text-2xl font-bold">25%</p>
            </div>
          </div>
          <div class="grid grid-cols-1 sm:grid-cols-2 gap-6 mb-6">
            <div class="bg-green-50 p-4 rounded-lg">
              <h4 class="font-medium text-green-800 mb-2">Financial Projections (2024)</h4>
              <ul class="text-sm text-green-700 space-y-1">
                <li>• Revenue: $495,529</li>
                <li>• Net Profit: $348,281</li>
                <li>• Gross Margin: 100%</li>
                <li>• Target: 500 Kaumatua customers</li>
              </ul>
            </div>
            <div class="bg-blue-50 p-4 rounded-lg">
              <h4 class="font-medium text-blue-800 mb-2">Key Milestones</h4>
              <ul class="text-sm text-blue-700 space-y-1">
                <li>• Solar panel installation complete</li>
                <li>• Community partnerships established</li>
                <li>• First 500 customers onboarded</li>
                <li>• Energy management system operational</li>
              </ul>
            </div>
          </div>
          <div class="border-t pt-4">
            <h4 class="text-md font-medium mb-3">Founder ownership & values</h4>
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-4">
              <div class="bg-blue-50 p-3 rounded-lg">
                <p class="text-sm text-gray-600">Founder 1</p>
                <p id="founder1Ownership1" class="text-lg font-semibold">30.0%</p>
                <p id="founder1Value1" class="text-sm text-green-600 font-medium">$3,000,000</p>
              </div>
              <div class="bg-blue-50 p-3 rounded-lg">
                <p class="text-sm text-gray-600">Founder 2</p>
                <p id="founder2Ownership1" class="text-lg font-semibold">22.5%</p>
                <p id="founder2Value1" class="text-sm text-green-600 font-medium">$2,250,000</p>
              </div>
              <div class="bg-blue-50 p-3 rounded-lg">
                <p class="text-sm text-gray-600">Founder 3</p>
                <p id="founder3Ownership1" class="text-lg font-semibold">15.0%</p>
                <p id="founder3Value1" class="text-sm text-green-600 font-medium">$1,500,000</p>
              </div>
              <div class="bg-blue-50 p-3 rounded-lg">
                <p class="text-sm text-gray-600">Founder 4</p>
                <p id="founder4Ownership1" class="text-lg font-semibold">7.5%</p>
                <p id="founder4Value1" class="text-sm text-green-600 font-medium">$750,000</p>
              </div>
            </div>
          </div>
        </div>
        
        <!-- Snapshot 2 -->
        <div id="snapshot2" class="bg-white rounded-xl shadow p-6">
          <h3 class="text-lg font-medium mb-4 text-blue-900">After Series A (2025)</h3>
          <div class="grid grid-cols-1 sm:grid-cols-4 gap-6 mb-6">
            <div>
              <p class="text-sm text-gray-500">Capital raised</p>
              <p id="capitalRaised2" class="text-2xl font-bold">$12,000,000</p>
            </div>
            <div>
              <p class="text-sm text-gray-500">Shares issued</p>
              <p id="sharesIssued2" class="text-2xl font-bold">8,000,000</p>
            </div>
            <div>
              <p class="text-sm text-gray-500">Post‑money valuation</p>
              <p id="postMoney2" class="text-2xl font-bold">$30,000,000</p>
            </div>
            <div>
              <p class="text-sm text-gray-500">New‑investor ownership</p>
              <p id="investorOwnership2" class="text-2xl font-bold">40%</p>
            </div>
          </div>
          <div class="grid grid-cols-1 sm:grid-cols-2 gap-6 mb-6">
            <div class="bg-green-50 p-4 rounded-lg">
              <h4 class="font-medium text-green-800 mb-2">Financial Projections (2025)</h4>
              <ul class="text-sm text-green-700 space-y-1">
                <li>• Revenue: $1,511,769</li>
                <li>• Net Profit: $808,161</li>
                <li>• Revenue Growth: 205%</li>
                <li>• Target: 750 Kaumatua customers</li>
              </ul>
            </div>
            <div class="bg-blue-50 p-4 rounded-lg">
              <h4 class="font-medium text-blue-800 mb-2">Growth Initiatives</h4>
              <ul class="text-sm text-blue-700 space-y-1">
                <li>• Expand to new regions</li>
                <li>• Enhanced community programs</li>
                <li>• Technology platform scaling</li>
                <li>• Team expansion</li>
              </ul>
            </div>
          </div>
          <div class="border-t pt-4">
            <h4 class="text-md font-medium mb-3">Founder ownership & values</h4>
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-4">
              <div class="bg-blue-50 p-3 rounded-lg">
                <p class="text-sm text-gray-600">Founder 1</p>
                <p id="founder1Ownership2" class="text-lg font-semibold">18.0%</p>
                <p id="founder1Value2" class="text-sm text-green-600 font-medium">$5,400,000</p>
              </div>
              <div class="bg-blue-50 p-3 rounded-lg">
                <p class="text-sm text-gray-600">Founder 2</p>
                <p id="founder2Ownership2" class="text-lg font-semibold">13.5%</p>
                <p id="founder2Value2" class="text-sm text-green-600 font-medium">$4,050,000</p>
              </div>
              <div class="bg-blue-50 p-3 rounded-lg">
                <p class="text-sm text-gray-600">Founder 3</p>
                <p id="founder3Ownership2" class="text-lg font-semibold">9.0%</p>
                <p id="founder3Value2" class="text-sm text-green-600 font-medium">$2,700,000</p>
              </div>
              <div class="bg-blue-50 p-3 rounded-lg">
                <p class="text-sm text-gray-600">Founder 4</p>
                <p id="founder4Ownership2" class="text-lg font-semibold">4.5%</p>
                <p id="founder4Value2" class="text-sm text-green-600 font-medium">$1,350,000</p>
              </div>
            </div>
          </div>
        </div>
        
        <!-- Snapshot 3 -->
        <div id="snapshot3" class="bg-white rounded-xl shadow p-6">
          <h3 class="text-lg font-medium mb-4 text-blue-900">After Series B (2026)</h3>
          <div class="grid grid-cols-1 sm:grid-cols-4 gap-6 mb-6">
            <div>
              <p class="text-sm text-gray-500">Capital raised</p>
              <p id="capitalRaised3" class="text-2xl font-bold">$25,000,000</p>
            </div>
            <div>
              <p class="text-sm text-gray-500">Shares issued</p>
              <p id="sharesIssued3" class="text-2xl font-bold">8,333,333</p>
            </div>
            <div>
              <p class="text-sm text-gray-500">Post‑money valuation</p>
              <p id="postMoney3" class="text-2xl font-bold">$75,000,000</p>
            </div>
            <div>
              <p class="text-sm text-gray-500">New‑investor ownership</p>
              <p id="investorOwnership3" class="text-2xl font-bold">33%</p>
            </div>
          </div>
          <div class="grid grid-cols-1 sm:grid-cols-2 gap-6 mb-6">
            <div class="bg-green-50 p-4 rounded-lg">
              <h4 class="font-medium text-green-800 mb-2">Financial Projections (2026)</h4>
              <ul class="text-sm text-green-700 space-y-1">
                <li>• Revenue: $2,727,568</li>
                <li>• Net Profit: $1,696,036</li>
                <li>• Revenue Growth: 80%</li>
                <li>• Target: 1,000+ Kaumatua customers</li>
              </ul>
            </div>
            <div class="bg-blue-50 p-4 rounded-lg">
              <h4 class="font-medium text-blue-800 mb-2">Expansion Plans</h4>
              <ul class="text-sm text-blue-700 space-y-1">
                <li>• National market expansion</li>
                <li>• Advanced energy services</li>
                <li>• Community fund scaling</li>
                <li>• Technology innovation</li>
              </ul>
            </div>
          </div>
          <div class="border-t pt-4">
            <h4 class="text-md font-medium mb-3">Founder ownership & values</h4>
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-4">
              <div class="bg-blue-50 p-3 rounded-lg">
                <p class="text-sm text-gray-600">Founder 1</p>
                <p id="founder1Ownership3" class="text-lg font-semibold">12.0%</p>
                <p id="founder1Value3" class="text-sm text-green-600 font-medium">$9,000,000</p>
              </div>
              <div class="bg-blue-50 p-3 rounded-lg">
                <p class="text-sm text-gray-600">Founder 2</p>
                <p id="founder2Ownership3" class="text-lg font-semibold">9.0%</p>
                <p id="founder2Value3" class="text-sm text-green-600 font-medium">$6,750,000</p>
              </div>
              <div class="bg-blue-50 p-3 rounded-lg">
                <p class="text-sm text-gray-600">Founder 3</p>
                <p id="founder3Ownership3" class="text-lg font-semibold">6.0%</p>
                <p id="founder3Value3" class="text-sm text-green-600 font-medium">$4,500,000</p>
              </div>
              <div class="bg-blue-50 p-3 rounded-lg">
                <p class="text-sm text-gray-600">Founder 4</p>
                <p id="founder4Ownership3" class="text-lg font-semibold">3.0%</p>
                <p id="founder4Value3" class="text-sm text-green-600 font-medium">$2,250,000</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- ===== Business Performance Timeline =============================================== -->
    <section aria-labelledby="timeline" class="mb-10">
      <h2 id="timeline" class="text-xl font-semibold mb-4">Business & Capital Timeline</h2>
      <ol class="relative border-l-4 border-blue-900 pl-6">
        <li class="mb-10">
          <span class="absolute -left-2 flex items-center justify-center w-4 h-4 bg-blue-900 rounded-full"></span>
          <time class="block text-sm font-medium text-gray-600 mb-1">2024 Q1 - Seed Round</time>
          <p class="text-lg font-semibold">$2.5M raised</p>
          <p class="text-sm text-gray-600">Initial funding for solar installation and setup</p>
        </li>
        <li class="mb-10">
          <span class="absolute -left-2 flex items-center justify-center w-4 h-4 bg-blue-900 rounded-full"></span>
          <time class="block text-sm font-medium text-gray-600 mb-1">2025 Q2 - Series A</time>
          <p class="text-lg font-semibold">$12M raised</p>
          <p class="text-sm text-gray-600">Scaling operations, 750 customers, $1.5M revenue</p>
        </li>
        <li class="mb-10">
          <span class="absolute -left-2 flex items-center justify-center w-4 h-4 bg-blue-900 rounded-full"></span>
          <time class="block text-sm font-medium text-gray-600 mb-1">2026 Q3 - Series B</time>
          <p class="text-lg font-semibold">$25M raised</p>
          <p class="text-sm text-gray-600">National expansion, 1,000+ customers, $2.7M revenue</p>
        </li>
        <li>
          <span class="absolute -left-2 flex items-center justify-center w-4 h-4 bg-green-600 rounded-full"></span>
          <time class="block text-sm font-medium text-gray-600 mb-1">2028 - Mature Business</time>
          <p class="text-lg font-semibold">$5.8M revenue, $3.6M profit</p>
          <p class="text-sm text-gray-600">Established market leader, potential exit opportunities</p>
        </li>
      </ol>
    </section>

    <!-- ===== Financial Summary =============================================== -->
    <section class="mb-10">
      <h2 class="text-xl font-semibold mb-4">Financial Summary</h2>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
        <div class="bg-white rounded-xl shadow p-6">
          <h3 class="text-lg font-medium mb-4 text-blue-900">Key Financial Metrics</h3>
          <div class="space-y-3">
            <div class="flex justify-between">
              <span class="text-gray-600">5-Year Revenue CAGR</span>
              <span class="font-semibold text-green-600">85%</span>
            </div>
            <div class="flex justify-between">
              <span class="text-gray-600">Net Margin (2028)</span>
              <span class="font-semibold text-green-600">62%</span>
            </div>
            <div class="flex justify-between">
              <span class="text-gray-600">Payback Period</span>
              <span class="font-semibold">2.5 years</span>
            </div>
            <div class="flex justify-between">
              <span class="text-gray-600">Estimated IRR</span>
              <span class="font-semibold text-green-600">45-50%</span>
            </div>
          </div>
        </div>
        <div class="bg-white rounded-xl shadow p-6">
          <h3 class="text-lg font-medium mb-4 text-blue-900">Social Impact</h3>
          <div class="space-y-3">
            <div class="flex justify-between">
              <span class="text-gray-600">Power Bill Subsidy</span>
              <span class="font-semibold text-blue-600">30%</span>
            </div>
            <div class="flex justify-between">
              <span class="text-gray-600">Target Beneficiaries</span>
              <span class="font-semibold">1,000+ Kaumatua</span>
            </div>
            <div class="flex justify-between">
              <span class="text-gray-600">Community Focus</span>
              <span class="font-semibold text-blue-600">Pensioner Support</span>
            </div>
            <div class="flex justify-between">
              <span class="text-gray-600">Renewable Energy</span>
              <span class="font-semibold text-green-600">Solar Power</span>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>

  <!-- ============================= Script ==================================== -->
  <script>
    (() => {
      /* ---------------- Constants & DOM refs ---------------- */
      const RAISES = [
        {   // Raise 1 (Seed)
          amountInput: document.getElementById('amount1'),
          shareInput: document.getElementById('sharePrice1'),
          valInput: document.getElementById('valuation1'),
          capitalEl: document.getElementById('capitalRaised1'),
          sharesEl: document.getElementById('sharesIssued1'),
          postEl: document.getElementById('postMoney1'),
          ownEl: document.getElementById('investorOwnership1'),
        },
        {   // Raise 2 (Series A)
          amountInput: document.getElementById('amount2'),
          shareInput: document.getElementById('sharePrice2'),
          valInput: document.getElementById('valuation2'),
          capitalEl: document.getElementById('capitalRaised2'),
          sharesEl: document.getElementById('sharesIssued2'),
          postEl: document.getElementById('postMoney2'),
          ownEl: document.getElementById('investorOwnership2'),
        },
        {   // Raise 3 (Series B)
          amountInput: document.getElementById('amount3'),
          shareInput: document.getElementById('sharePrice3'),
          valInput: document.getElementById('valuation3'),
          capitalEl: document.getElementById('capitalRaised3'),
          sharesEl: document.getElementById('sharesIssued3'),
          postEl: document.getElementById('postMoney3'),
          ownEl: document.getElementById('investorOwnership3'),
        },
      ];

      // Founder inputs and display elements
      const FOUNDERS = [
        {
          percentInput: document.getElementById('founder1Percent'),
          ownership: [
            document.getElementById('founder1Ownership1'),
            document.getElementById('founder1Ownership2'),
            document.getElementById('founder1Ownership3')
          ],
          value: [
            document.getElementById('founder1Value1'),
            document.getElementById('founder1Value2'),
            document.getElementById('founder1Value3')
          ]
        },
        {
          percentInput: document.getElementById('founder2Percent'),
          ownership: [
            document.getElementById('founder2Ownership1'),
            document.getElementById('founder2Ownership2'),
            document.getElementById('founder2Ownership3')
          ],
          value: [
            document.getElementById('founder2Value1'),
            document.getElementById('founder2Value2'),
            document.getElementById('founder2Value3')
          ]
        },
        {
          percentInput: document.getElementById('founder3Percent'),
          ownership: [
            document.getElementById('founder3Ownership1'),
            document.getElementById('founder3Ownership2'),
            document.getElementById('founder3Ownership3')
          ],
          value: [
            document.getElementById('founder3Value1'),
            document.getElementById('founder3Value2'),
            document.getElementById('founder3Value3')
          ]
        },
        {
          percentInput: document.getElementById('founder4Percent'),
          ownership: [
            document.getElementById('founder4Ownership1'),
            document.getElementById('founder4Ownership2'),
            document.getElementById('founder4Ownership3')
          ],
          value: [
            document.getElementById('founder4Value1'),
            document.getElementById('founder4Value2'),
            document.getElementById('founder4Value3')
          ]
        }
      ];

      const totalFounderPercentEl = document.getElementById('totalFounderPercent');
      const percentageWarningEl = document.getElementById('percentageWarning');
      const saveStatusEl = document.getElementById('saveStatus');

      // Utility – format a number as NZ currency without decimals
      const formatMoney = (n) => n.toLocaleString('en-NZ', {
        style: 'currency',
        currency: 'NZD',
        minimumFractionDigits: 0,
      });

      /* ---------------- Persistence Functions ---------------- */
      const saveToStorage = () => {
        try {
          const data = {
            founders: FOUNDERS.map(f => parseFloat(f.percentInput.value) || 0),
            raises: RAISES.map(r => ({
              amount: parseFloat(r.amountInput.value) || 0,
              sharePrice: parseFloat(r.shareInput.value) || 0,
              valuation: parseFloat(r.valInput.value) || 0
            }))
          };
          localStorage.setItem('kaumataEnergyCapitalDashboard', JSON.stringify(data));
          saveStatusEl.textContent = 'Data saved ✓';
          saveStatusEl.className = 'text-green-600';
        } catch (e) {
          saveStatusEl.textContent = 'Storage not available in this environment';
          saveStatusEl.className = 'text-amber-600';
        }
      };

      const loadFromStorage = () => {
        try {
          const saved = localStorage.getItem('kaumataEnergyCapitalDashboard');
          if (saved) {
            const data = JSON.parse(saved);
            
            // Restore founder percentages
            FOUNDERS.forEach((founder, index) => {
              if (data.founders[index] !== undefined) {
                founder.percentInput.value = data.founders[index];
              }
            });
            
            // Restore raise data
            RAISES.forEach((raise, index) => {
              if (data.raises[index]) {
                raise.amountInput.value = data.raises[index].amount;
                raise.shareInput.value = data.raises[index].sharePrice;
                raise.valInput.value = data.raises[index].valuation;
              }
            });
            
            saveStatusEl.textContent = 'Data loaded from previous session ✓';
            saveStatusEl.className = 'text-blue-600';
          }
        } catch (e) {
          saveStatusEl.textContent = 'Storage not available in this environment';
          saveStatusEl.className = 'text-amber-600';
        }
      };

      /* ---------------- Update routine ---------------- */
      const update = () => {
        // Calculate founder percentages and validate
        const founderPercents = FOUNDERS.map(f => parseFloat(f.percentInput.value) || 0);
        const totalPercent = founderPercents.reduce((sum, p) => sum + p, 0);
        
        totalFounderPercentEl.textContent = totalPercent.toFixed(1) + '%';
        
        if (Math.abs(totalPercent - 100) > 0.1) {
          percentageWarningEl.classList.remove('hidden');
        } else {
          percentageWarningEl.classList.add('hidden');
        }

        // Calculate initial founder shares (assuming pre-money valuation of first raise represents initial value)
        const initialValuation = parseFloat(RAISES[0].valInput.value) * 1_000_000 || 7_500_000;
        const initialSharePrice = parseFloat(RAISES[0].shareInput.value) || 0.50;
        const initialTotalShares = initialValuation / initialSharePrice;
        
        // Track cumulative values for dilution calculation
        let cumulativeShares = initialTotalShares;
        let founderShares = founderPercents.map(percent => (percent / 100) * initialTotalShares);

        // Calculate for each raise
        RAISES.forEach(({ amountInput, shareInput, valInput, capitalEl, sharesEl, postEl, ownEl }, raiseIndex) => {
          const amount = (parseFloat(amountInput.value) || 0) * 1_000_000;
          const sharePrice = parseFloat(shareInput.value) || 0;
          const preMoneyM = parseFloat(valInput.value) || 0; // millions

          // Capital raised
          capitalEl.textContent = formatMoney(amount);

          // Shares issued at this raise
          const sharesIssued = sharePrice > 0 ? Math.round(amount / sharePrice) : 0;
          sharesEl.textContent = sharesIssued.toLocaleString();

          // Post‑money valuation (NZD)
          const postMoney = preMoneyM * 1_000_000 + amount;
          postEl.textContent = formatMoney(postMoney);

          // New‑investor ownership percentage
          const investorOwnership = postMoney > 0 ? (amount / postMoney) * 100 : 0;
          ownEl.textContent = investorOwnership.toFixed(1) + '%';

          // Update cumulative shares
          cumulativeShares += sharesIssued;

          // Calculate founder ownership and values after this raise
          FOUNDERS.forEach((founder, founderIndex) => {
            const ownershipPercent = (founderShares[founderIndex] / cumulativeShares) * 100;
            const value = (ownershipPercent / 100) * postMoney;
            
            founder.ownership[raiseIndex].textContent = ownershipPercent.toFixed(1) + '%';
            founder.value[raiseIndex].textContent = formatMoney(value);
          });
        });
        
        // Save to storage after calculations
        saveToStorage();
      };

      /* ---------------- Event listeners ---------------- */
      RAISES.forEach(({ amountInput, shareInput, valInput }) => {
        amountInput.addEventListener('input', update);
        shareInput.addEventListener('input', update);
        valInput.addEventListener('input', update);
      });

      FOUNDERS.forEach(({ percentInput }) => {
        percentInput.addEventListener('input', update);
      });

      // Load saved data and perform initial calculation
      loadFromStorage();
      update();
    })();
  </script>
</body>
</html>
