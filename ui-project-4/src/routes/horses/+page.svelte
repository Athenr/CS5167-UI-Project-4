<script>
    import andalusian from '$lib/assets/andalusian.png';
</script>

<div id="horsePage">
    <div id="barnBar">
        <div class="barnCategory">
            Stallion Barn
        </div>
        <div class="male horse">
            Bucephalus
        </div>
        <div class="male horse">
            Adagio
        </div>
        <div class="barnCategory">
            Yearling Barn
        </div>
        <div class="female horse">
            Epona
        </div>
        <div class="female horse">
            Morrigan
        </div>
        <div class="male horse">
            Chapel
        </div>
        <div class="female horse">
            Odette
        </div>
    </div>
    <div id="horseInfo">
        <div id="horseStatus">
            <div id="horseImageBox">
                <img id="horseImage" alt="Andalusian" src={andalusian}>
            </div>
            <div class="status box">
                <div class="boxHeader">
                    Bucephalus
                </div>       
                <div class="line"> 
                    <span class="bold">Breed:</span> Andalusian 
                    </div>
                
                <div class="line">
                    <span class="bold">Date of Birth:</span> 05/24/2018
                    </div>
                
                <div class="line">
                    <span class="bold">Age:</span> 7
                </div>
                
                <div class="line">
                    <span class="bold">Sex:</span> Gelding
                </div>
                
                <div class="line">
                    <span class="bold">Height:</span> 17.1 HH
                </div>
                
                <div class="line">
                    <span class="bold">Weight:</span> 554 KG
                </div>
            </div>

            <div class="status box">
                <div class="boxHeader">
                    Status
                </div>       
                <div class="line"> 
                    <span class="bold">Location:</span> Turnout 
                    </div>
                
                <div class="line">
                    <span class="bold">Assigned Stall:</span> Stallion Barn - B12
                    </div>
                
                <div class="line">
                    <span class="bold">Assigned Turnout:</span> Stallion Paddock 5
                </div>
            </div>
        </div>
        <div id="horseCare">
            <div class="care box">
                <div class="boxHeader">
                    Feed
                </div>       
                <div class="line"> 
                    <span class="bold">AM Feed:</span> Mixed Timothy/Alfalfa Hay 
                    </div>
                
                <div class="line">
                    <span class="bold">PM Feed:</span> Premium Timothy Hay
                    </div>
                
                <div class="line">
                    <span class="bold">Pasture:</span> Orchard Grass
                </div>

                <div class="line">
                    <span class="bold">Water:</span> Free Choice
                </div>

                <div class="line">
                    <span class="bold">Notes:</span> Alfalfa adds protein for muscle and calcium to buffer stomach acid. Placed in a small-hole hay net to ensure continuous chewing (reducing colic/ulcer risk). Limited access to prevent over-consumption of high-sugar grass.
                </div>
            </div>

            <div class="care box">
                <div class="boxHeader">
                    Supplement
                </div>       
                <div class="line"> 
                    <span class="bold">AM Supplements:</span> Performance Pellet (12% Protein); Linseed (Flax) Oil
                    </div>
                
                <div class="line">
                    <span class="bold">PM Supplements:</span> Performance Pellet (12% Protein); Joint Support Supplement; Digestive Probiotic Paste
                    </div>
                
                <div class="line">
                    <span class="bold">Pasture:</span> Orchard Grass
                </div>

                <div class="line">
                    <span class="bold">Unlimited Hay Net:</span> Yes
                </div>
            </div>

            <div class="care box">
                <div class="boxHeader">
                    Nutrition
                </div>       
                <div class="line"> 
                    <span class="bold">Training Schedule:</span> Dressage schooling lessons T/Th. Trail ride Sat. All feeds must be finished 1 hour prior to work to avoid gut issues.
                </div>
                
                <div class="line">
                    <span class="bold">Medical Note:</span> Horse is a "hard keeper" (burns calories easily). Monitor weight weekly. If BCS drops below 5, increase AM/PM pellets by 0.25lb each.
                </div>
                <div class="line">
                    <span class="bold">Handling Note:</span> Orchard Grass
                </div>
            </div>
        </div>
    </div>
</div>

<style>

.boxHeader {
    width: 490px;
    height: 35px;
    color: #FFF;
    font-family: Inter;
    font-size: 30px;
    font-style: normal;
    font-weight: 800;
    line-height: normal;
}

.line {
    display: block;
}

.bold {
    font-weight: 800;
}

.box {
    display: flex;
    padding: 15px;
    flex-direction: column;
    align-items: flex-start;
    gap: 15px;
    align-self: stretch;
    border-radius: 20px;
    background: linear-gradient(112deg, #27334C 0%, #556588 100%);
    color: #FFF;
    font-family: Inter;
    font-size: 20px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;
    height: 100%;
}

.status {
    width: 525px;
}

.care {
    width: 460px;
}

#horseImageBox {
    display: flex;
    width: 330px;
    height: 330px;
    justify-content: center;
    align-items: center;
    aspect-ratio: 1/1;
    border-radius: 20px;
    border: 5px solid #FFF;
}

#horseImage {
    width: 330px;
    height: 330px;
    flex-shrink: 0;
    aspect-ratio: 1/1;
    border-radius: 20px;
    border: 5px solid #FFF;
}

#horseStatus {
    display: flex;
    height: 350px;
    padding: 10px;
    align-items: center;
    gap: 25px;
    flex-shrink: 0;
    align-self: stretch;
}

#horseCare {
    display: flex;
    height: 52%;
    padding: 10px;
    align-items: center;
    gap: 25px;
    flex-shrink: 0;
    align-self: stretch;
}

#barnBar {
    display: flex;
    width: 320px;
    height: 100%;
    padding: 15px;
    flex-direction: column;
    align-items: flex-start;
    gap: 15px;
    border-radius: 20px;
    background: rgba(90, 90, 90, .7);
}

#horseInfo {
    display: flex;
    height: 100%;
    padding: 15px;
    flex-direction: column;
    align-items: flex-start;
    gap: 15px;
    flex: 1 0 0;
    border-radius: 20px;
    background: rgba(90, 90, 90, .7);
}

.barnCategory {
    display: flex;
    padding: 3px 0 11px 0;
    justify-content: center;
    align-items: center;
    align-self: stretch;
    border-bottom: 3px solid #FFF;
}

.horse {
    display: flex;
    height: 65px;
    padding: 10px 18px;
    align-items: center;
    gap: 10px;
    flex-shrink: 0;
    align-self: stretch;
    border-radius: 25px;
    color: #FFF;
    font-family: Inter;
    font-size: 24px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
}

.male {
    background: linear-gradient(91deg, #1D4778 0%, #4674A9 100%);
}

.female {
    background: linear-gradient(91deg, #781D31 0%, #A94681 100%);
}

#horsePage {
    display: flex;
    height: auto;
    min-height: 93vh;
    padding: 40px;
    align-items: flex-start;
    gap: 40px;
}
</style>