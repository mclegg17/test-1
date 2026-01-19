<form id="leadForm" autocomplete="on">
  <div class="row">
    <div class="col">
      <label for="first">First name</label>
      <input id="first" name="first" required />
    </div>
    <div class="col">
      <label for="last">Last name</label>
      <input id="last" name="last" required />
    </div>
  </div>

  <label for="email">Email</label>
  <input id="email" name="email" type="email" required />

  <div class="row">
    <div class="col">
      <label for="phone">Phone</label>
      <input id="phone" name="phone" placeholder="e.g. 555-123-4567" required />
    </div>
    <div class="col">
      <label for="zip">ZIP</label>
      <input id="zip" name="zip" required />
    </div>
  </div>

  <label for="product">I'm looking for</label>
  <select id="product" name="product" required>
    <option value="pnc">Property & Casualty (Auto/Home/etc.)</option>
    <option value="life">Life Insurance</option>
  </select>

  <!-- P&C block -->
  <div id="pncBlock">
    <label for="pncLine">P&C type</label>
    <select id="pncLine" name="pncLine">
      <option value="auto">Auto</option>
      <option value="home">Home</option>
      <option value="renters">Renters</option>
      <option value="other">Other</option>
    </select>

    <label for="carrier">Current carrier (if any)</label>
    <input id="carrier" name="carrier" placeholder="e.g. State Farm" />

    <div id="autoFields">
      <label for="vehicle">Vehicle (year, make, model)</label>
      <input id="vehicle" name="vehicle" placeholder="e.g. 2018 Toyota Camry" />
      <div class="row">
        <div class="col">
          <label for="mileage">Annual mileage (approx)</label>
          <input id="mileage" name="mileage" />
        </div>
        <div class="col">
          <label for="drivingHistory">Recent driving incidents?</label>
          <select id="drivingHistory" name="drivingHistory">
            <option value="none">No incidents in last 5 years</option>
            <option value="accident">Accident</option>
            <option value="violation">Violation</option>
            <option value="both">Both</option>
          </select>
        </div>
      </div>
    </div>

    <div id="homeFields" style="display:none">
      <label for="homeYear">Home year built</label>
      <input id="homeYear" name="homeYear" />
      <label for="homeClaims">Any prior home claims in last 5 years?</label>
      <select id="homeClaims" name="homeClaims">
        <option value="no">No</option>
        <option value="yes">Yes</option>
      </select>
    </div>
  </div>

  <!-- Life block -->
  <div id="lifeBlock" style="display:none">
    <label for="dob">Date of birth</label>
    <input id="dob" name="dob" type="date" />
    <label for="smoker">Tobacco use?</label>
    <select id="smoker" name="smoker">
      <option value="no">No</option>
      <option value="yes">Yes</option>
    </select>
    <label for="lifeAmount">Desired coverage amount (optional)</label>
    <input id="lifeAmount" name="lifeAmount" placeholder="e.g. $250,000" />
    <label for="lifePurpose">Purpose</label>
    <select id="lifePurpose" name="lifePurpose">
      <option value="incomeProtection">Income protection</option>
      <option value="mortgage">Mortgage protection</option>
      <option value="finalExpenses">Final expenses</option>
      <option value="other">Other</option>
    </select>
  </div>

  <label for="notes">Anything else we should know? (optional)</label>
  <textarea id="notes" name="notes" rows="3"></textarea>

  <label class="consent">
    <input type="checkbox" id="consent" required />
    By providing my phone number I consent to be contacted by phone and SMS about insurance options. I agree to the <a id="ppLink" href="#" target="_blank">privacy policy</a>.
  </label>

  <button type="submit">Get my personalized quote</button>
  <div id="error" class="error" role="alert"></div>

  <p class="small">We only use this info to provide quotes. No SSN or financial details are collected here. You can request deletion at any time.</p>
</form>
