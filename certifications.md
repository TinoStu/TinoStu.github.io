---
layout: single
title: "Certifications"
permalink: /certifications/
---



<style>
  .certifications-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
    padding: 20px 0;
    align-items: stretch;
  }

  .cert-card {
    display: flex;
    align-items: center;
    background-color: #2d2d2d;
    color: #f0f0f0;
    border-radius: 10px;
    padding: 20px;
    box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.2);
    max-width: 480px;
    width: 100%;
  }

  /* THIS IS THE CORRECTED BLOCK FOR THE BADGE IMAGE */
  img.cert-badge {
    width: 120px;            /* Restored original width */
    height: auto !important; /* Crucial for maintaining aspect ratio, !important to override conflicts */
    margin-right: 20px;      /* Increased margin for better separation */
    display: block;          /* Good practice for image layout consistency */
    border-radius: 8px;      /* Optional: keeps the rounded corners if you liked them */
  }

  .cert-info {
    flex: 1;
    display: flex;
    flex-direction: column;
    height: 100%;
  }

  .cert-info h3 {
    margin: 0 0 8px;
    font-size: 1.3em;
    color: #ffffff;
  }

  .cert-info p {
    /* margin: 0 0 12px; */ /* Replaced by specific rule below */
    font-size: 0.9em;
    line-height: 1.5;
  }

  .cert-info p:not(.cert-link-wrapper) {
    margin-bottom: 12px;
  }
  
  .cert-info .cert-link-wrapper {
    margin-top: auto;
    margin-bottom: 0;
    padding-top: 10px;
  }

  .cert-link {
    color: #5dade2;
    text-decoration: none;
    font-weight: bold;
    font-size: 0.95em;
  }
  .cert-link:hover {
    text-decoration: underline;
    color: #85c1e9;
  }
</style>

<!--<style>
    .certifications-container {
        display: flex;
        gap: 20px;
        justify-content: center;
        flex-wrap: wrap;
        padding: 20px;
    }

    .cert-card {
        display: flex;
        align-items: center;
        background: #1e1e1e;
        color: white;
        padding: 15px;
        border-radius: 10px;
        box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.2);
        max-width: 480px;
    }

    .cert-badge {
        width: 120px;
        height: auto;
        margin-right: 15px;
    }

    .cert-info {
        flex: 1;
    }

    .cert-info h3 {
        margin: 0;
        font-size: 1.2em;
    }

    .cert-info p {
        margin: 5px 0;
        font-size: 0.9em;
        line-height: 1.4;
    }

    .cert-link {
        color: #5FB6D9;
        text-decoration: none;
        font-weight: bold;
    }
</style>-->



<div class="certifications-container">
    <div class="cert-card">
        <img src="/assets/images/az104-badge.png" alt="AZ-104 Badge" class="cert-badge">
        <div class="cert-info">
            <h3>Azure Administrator Associate</h3>
            <p><strong>Earned:</strong> November 2024 | <strong>Issued by:</strong> Microsoft</p>
            <p><strong>Skills:</strong> Manage identities & governance • Implement & manage storage • Deploy compute resources • Virtual networking • Monitor & maintain resources</p>
            <p class="cert-link-wrapper"><a href="https://learn.microsoft.com/api/credentials/share/en-us/StuartGleasure-0154/E26B4D82697BF84D?sharingId=84BF06797E61A7DD1" target="_blank" class="cert-link">View Credential</a></p>
            <!--<a href="https://learn.microsoft.com/api/credentials/share/en-us/StuartGleasure-0154/E26B4D82697BF84D?sharingId=84BF06797E61A7DD1" target="_blank" class="cert-link">View Credential</a>-->
         </div>
</div>
            <p></p>
<div class="cert-card">
        <img src="/assets/images/az305-badge.png" alt="AZ-305 Badge" class="cert-badge">
        <div class="cert-info">
            <h3>Azure Solutions Architect Expert</h3>
            <p><strong>Earned:</strong> February 2025 | <strong>Issued by:</strong> Microsoft</p>
            <p><strong>Skills:</strong> Design identity & governance • Data storage solutions • Business continuity solutions • Infrastructure solutions</p>
            <p class="cert-link-wrapper"><a href="https://learn.microsoft.com/api/credentials/share/en-us/StuartGleasure-0154/5B006BDA4A927A05?sharingId=84BF06797E61A7DD1" target="_blank" class="cert-link">View Credential</a></p>
           <!--<a href="https://learn.microsoft.com/api/credentials/share/en-us/StuartGleasure-0154/5B006BDA4A927A05?sharingId=84BF06797E61A7DD1" target="_blank" class="cert-link">View Credential</a>-->
        </div>
    </div>
</div>



<!--<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 60px; margin: 40px 0;">

<div style="display: flex; flex-direction: column; align-items: center; text-align: left;">
    <img src="/assets/images/az104-badge.png" alt="AZ-104 Badge" style="width: 200px; margin-bottom: 30px;">
    
    <div style="width: 100%; padding: 0 20px;">
        <h2 style="text-align: center; margin-bottom: 20px;">Microsoft Certified: Azure Administrator Associate</h2>
        
        <p style="text-align: center; margin-bottom: 30px;">Earned: November 2024 | Issued by: Microsoft</p>
        
        <h3 style="margin-bottom: 15px; font-size: 1.1em;">Skills measured:</h3>
        <ul style="list-style-type: none; padding-left: 0; margin-bottom: 30px; font-size: 0.95em; line-height: 1.6;">
            <li>• Manage Azure identities and governance</li>
            <li>• Implement and manage storage</li>
            <li>• Deploy and manage Azure compute resources</li>
            <li>• Implement and manage virtual networking</li>
            <li>• Monitor and maintain Azure resources</li>
        </ul>
        
        <p style="text-align: left;">
            <a href="https://learn.microsoft.com/api/credentials/share/en-us/StuartGleasure-0154/E26B4D82697BF84D?sharingId=84BF06797E61A7DD1" 
               target="_blank" 
               style="color: #5FB6D9; text-decoration: none;">View Credential</a>
        </p>
    </div>
</div>

<div style="display: flex; flex-direction: column; align-items: center; text-align: left;">
    <img src="/assets/images/az305-badge.png" alt="AZ-305 Badge" style="width: 200px; margin-bottom: 30px;">
    
    <div style="width: 100%; padding: 0 20px;">
        <h2 style="text-align: center; margin-bottom: 20px;">Microsoft Certified: Azure Solutions Architect Expert</h2>
        
        <p style="text-align: center; margin-bottom: 30px;">Earned: February 2025 | Issued by: Microsoft</p>
        
        <h3 style="margin-bottom: 15px; font-size: 1.1em;">Skills measured:</h3>
        <ul style="list-style-type: none; padding-left: 0; margin-bottom: 30px; font-size: 0.95em; line-height: 1.6;">
            <li>• Design identity, governance, and monitoring solutions</li>
            <li>• Design data storage solutions</li>
            <li>• Design business continuity solutions</li>
            <li>• Design infrastructure solutions</li>
        </ul>
        
        <p style="text-align: left;">
            <a href="https://learn.microsoft.com/api/credentials/share/en-us/StuartGleasure-0154/5B006BDA4A927A05?sharingId=84BF06797E61A7DD1" 
               target="_blank" 
               style="color: #5FB6D9; text-decoration: none;">View Credential</a>
        </p>
    </div>
</div>

</div>-->

