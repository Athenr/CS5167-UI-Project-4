<script>
    let videoFile;
    let videoURL;

    let lameness = "Negative";
    let medical_attention = "No";
    let severity = "None";
    let additional_notes = "None";
    
    let severity_options = ["None", "Low", "Medium", "High", "Extreme"];

    function handleVideo(event) {
        videoFile = event.target.files[0];

        if (videoURL) {
            URL.revokeObjectURL(videoURL);
        }
        if (videoFile) {
            videoURL = URL.createObjectURL(videoFile);
        } else {
            videoURL = null;
        }
    }

    function scanVideo(event) {
        if (videoURL) {
            giveSeverity();
        }
    }

    function giveSeverity() {
        severity = severity_options[Math.floor(Math.random() * severity_options.length)];

        switch (severity) {
            case "None":
                lameness = "Negative";
                medical_attention = "No";
                additional_notes = "None";
                break;
            case "Low":
                lameness = "Negative";
                medical_attention = "Yes";
                additional_notes = "Horse should be taken to clinic within a week.";
                break;
            case "Medium":
                lameness = "Positive";
                medical_attention = "Yes";
                additional_notes = "Horse should be taken to equine hospital within a few days."
                break;
            case "High":
                lameness = "Positive";
                medical_attention = "Yes";
                additional_notes = "Horse should be taken to equine hospital today!"
                break;
            case "Extreme":
                lameness = "Positive";
                medical_attention = "Yes";
                additional_notes = "Horse should be taken to equine hospital IMMEDIATELY!!";
                break;
        }
    }

</script>

<div id="scannerPage">
    <div id="uploadFrame">
        <div class="header">
            <span class="headerText">VetScanner</span>
        </div>

        <span class="subText">Upload a video of your horse's movement and press the scan button to check for signs of lameness.</span>

        <div id="resultsFrame">
            <div id="resultsTitleBox">
                <span id="resultsTitle">Lameness Results</span>
            </div>

            <div class="line"> 
                <span class="bold">Signs of Lameness:</span> {lameness}
            </div>
            <div class="line">
                <span class="bold">Medical Attention Required:</span> {medical_attention}
            </div>
            <div class="line">
                <span class="bold">Severity:</span> {severity}
            </div>
            <div class="line">
                <span class="bold">Additional Notes:</span> {additional_notes}
            </div>
        </div>

        <input type="file" accept="video/*" on:change={handleVideo} />

        <div id="scanButton" on:click={scanVideo}>
            <span id="scanText">SCAN</span>
        </div>
    </div>
    <div id="videoFrame">
        <div id="video">
            {#if videoURL}
                <video src={videoURL} controls style="max-width: 100%; max-height: 100%;">
                    Your browser does not support the video tag.
                </video>
            {:else}
                <span style="color: #ccc; font-size: 30px;">Upload a video to preview it here.</span>
            {/if}
        </div>
    </div>
</div>

<style>
input {
    color: #FFF;
    font-family: Inter;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: normal; 
}

p {
    color: #FFF;
    font-family: Inter;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;
}

#scanButton {
    display: flex;
    padding: 10px 15px;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 10px;
    border-radius: 50px;
    border: 3px solid #FFF;
    background: #0077B6;
}

#scanText {
    color: #FFF;
    font-family: Inter;
    font-size: 24px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
}

.line {
    display: block;
    font-weight: 400;
}

.bold {
    font-weight: 800;
}

#resultsTitle {
    color: #FFF;
    text-align: center;
    font-family: Inter;
    font-size: 30px;
    font-style: normal;
    font-weight: 800;
    line-height: normal;
}

#video {
    display: flex;
    height: 100%;
    padding: 15px;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 15px;
    flex-shrink: 0;
    align-self: stretch;
    border-radius: 20px;
    background: #303030;
}

video {
    width: 100%;
    height: auto;
    max-height: 100%;
    object-fit: contain;
    border-radius: 10px;
}

#resultsTitleBox {
    display: flex;
    height: 45px;
    justify-content: center;
    align-items: center;
    gap: 10px;
    flex-shrink: 0;
    align-self: stretch;
    border-bottom: 3px solid #FFF;
}

#resultsFrame {
    display: flex;
    height: 55%;
    padding: 15px;
    flex-direction: column;
    align-items: flex-start;
    gap: 15px;
    flex-shrink: 0;
    align-self: stretch;
    border-radius: 20px;
    background: linear-gradient(112deg, #27334C 0%, #556588 100%);
}

.header {
    display: flex;
    padding: 3px 0 11px 0;
    justify-content: center;
    align-items: center;
    align-self: stretch;
    border-bottom: 3px solid #FFF;
}

.subText {
    align-self: stretch;
    color: #FFF;
    text-align: center;
    font-family: Inter;
    font-size: 24px;
    font-style: normal;
    font-weight: 500;
    line-height: normal;
}

.headerText {
    display: flex;
    width: 595px;
    height: 36px;
    flex-direction: column;
    justify-content: center;
    color: #FFF;
    text-align: center;
    font-family: Inter;
    font-size: 30px;
    font-style: normal;
    font-weight: 800;
    line-height: normal;
}

#scannerPage {
    display: flex;
    height: auto;
    min-height: 93vh;
    padding: 40px;
    align-items: flex-start;
    gap: 40px;
}

#uploadFrame {
    display: flex;
    width: 550px;
    height: 100%;
    padding: 25px;
    flex-direction: column;
    align-items: center;
    gap: 25px;
    border-radius: 20px;
    background: rgba(90, 90, 90, .7);
}

#videoFrame {
    display: flex;
    width: 1250px;
    height: 100%;
    padding: 35px;
    flex-direction: column;
    align-items: flex-start;
    gap: 15px;
    border-radius: 20px;
    background: rgba(90, 90, 90, .7);
}

</style>