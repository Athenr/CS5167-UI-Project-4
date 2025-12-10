<script>
    import information from '$lib/assets/diseases.json';

    let selectedDisease = "";

    let definition = "";
    let medical_attention = "";
    let severity = "";
    let causes = "";
    let symptoms = "";
    let diagnosis = "";
    let treatment = "";
    let recovery = "";

    function selectDisease(name) {
        for (const disease of information) {
            if(disease.name == name) {
                selectedDisease = name;

                definition = disease.definition;
                medical_attention = disease.medical_attention;
                severity = disease.severity;
                causes = disease.causes;
                symptoms = disease.symptoms;
                diagnosis = disease.diagnosis;
                treatment = disease.treatment;
                recovery = disease.recovery;
                break;
            }
        }
    }

    const diseases = [
        { type: 'Musculoskeletal', name: 'Arthritis' },
        { type: 'Musculoskeletal', name: 'Laminitis' },
        { type: 'Gastrointestinal', name: 'Colic' },
        { type: 'Gastrointestinal', name: 'Gastric Ulcers' },
    ];
</script>

<div id="equipediaPage">
    <div id="selectionFrame">
        {#each diseases as disease, i}
            {#if i === 0 || disease.type !== diseases[i - 1].type}
                <div class="diseaseTypeHeader">
                    <span class="diseaseTypeName">{disease.type}</span>
                </div>
            {/if}

            <div 
                class="disease" 
                class:selected={disease.name === selectedDisease}
                on:click={() => selectDisease(disease.name)}
            >
                <span class="diseaseName">{disease.name}</span>
            </div>
        {/each}
    </div>
    <div id="informationFrame">
        <div class="subinfoFrame">
            <div class="subinfoFrameHeader">
                <span class="subinfoFrameHeaderText">Definition and Causes</span>
            </div>

            <div class="subinfoFrameBody">
                <span class="bold">Definition:</span> {definition}
            </div>

            <div class="subinfoFrameBody">
                <span class="bold">Medical Attention Required:</span> {medical_attention}
            </div>

            <div class="subinfoFrameBody">
                <span class="bold">Severity:</span> {severity}
            </div>

            <div class="subinfoFrameBody">
                <span class="bold">Causes:</span> {causes}
            </div>

        </div>
        <div class="subinfoFrame">
            <div class="subinfoFrameHeader">
                <span class="subinfoFrameHeaderText">Symptom and Diagnosis</span>
            </div>

            <div class="subinfoFrameBody">
                <span class="bold">Symptoms:</span> {symptoms}
            </div>

            <div class="subinfoFrameBody">
                <span class="bold">Diagnosis:</span> {diagnosis}
            </div>
        </div>
        <div class="subinfoFrame">
            <div class="subinfoFrameHeader">
                <span class="subinfoFrameHeaderText">Treatment</span>
            </div>

            <div class="subinfoFrameBody">
                <span class="bold">Treatment:</span> {treatment}
            </div>

            <div class="subinfoFrameBody">
                <span class="bold">Recovery:</span> {recovery}
            </div>
        </div>
    </div>
</div>

<style>

.disease.selected {
    border: 3px solid #FFF;
}

#equipediaPage {
    display: flex;
    height: auto;
    min-height: 90vh;
    padding: 40px;
    align-items: flex-start;
    width: 100%;
    gap: 40px;
}

.bold {
    font-weight: 800;
}

.subinfoFrameBody {
    align-self: stretch;
    color: #FFF;
    font-family: Inter;
    font-size: 20px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;
}

.subinfoFrameHeader {
    display: flex;
    height: 45px;
    justify-content: center;
    align-items: center;
    gap: 10px;
    align-self: stretch;
    border-bottom: 3px solid #FFF;
}

.subinfoFrameHeaderText {
    color: #FFF;
    text-align: center;
    font-family: Inter;
    font-size: 30px;
    font-style: normal;
    font-weight: 800;
    line-height: normal;
}

.subinfoFrame {
    display: flex;
    padding: 15px;
    flex-direction: column;
    align-items: flex-start;
    gap: 15px;
    flex: 1 0 0;
    align-self: stretch;
    border-radius: 20px;
    background: linear-gradient(112deg, #27334C 0%, #556588 100%);
}

.disease {
    display: flex;
    height: 65px;
    padding: 10px 18px;
    align-items: center;
    gap: 10px;
    flex-shrink: 0;
    align-self: stretch;
    border-radius: 25px;
    background: linear-gradient(91deg, #1D4778 0%, #4674A9 100%);
}

.diseaseName {
    display: flex;
    height: 45px;
    flex-direction: column;
    justify-content: center;
    flex: 1 0 0;
    color: #FFF;
    font-family: Inter;
    font-size: 24px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
}

.diseaseTypeName {
    color: #FFF;
    text-align: center;
    font-family: Inter;
    font-size: 30px;
    font-style: normal;
    font-weight: 800;
    line-height: normal;
}

.diseaseTypeHeader {
    display: flex;
    padding: 3px 12px 11px 12px;
    justify-content: center;
    align-items: center;
    align-self: stretch;
    border-bottom: 3px solid #FFF;
}

#selectionFrame {
    display: flex;
    width: 320px;
    height: 100%;
    padding: 25px;
    flex-direction: column;
    align-items: flex-start;
    gap: 15px;
    border-radius: 20px;
    background: rgba(90, 90, 90, .7);
}

#informationFrame {
    display: flex;
    height: 100%;
    width: 100%;
    padding: 30px;
    align-items: flex-start;
    gap: 30px;
    flex: 1 0 0;
    border-radius: 20px;
    background: rgba(90, 90, 90, .7);
}
</style>