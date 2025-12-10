<script>

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
                <div id="horseImage">
                </div>
            </div>

            <div class="horseStatusFrame">

            </div>

            <div class="horseStatusFrame">
                
            </div>
        </div>

        <div id="horseCare">
            <div class="horseCareFrame">
                
            </div>
            <div class="horseCareFrame">
                
            </div>
            <div class="horseCareFrame">
                
            </div>
        </div>
    </div>
</div>

<style>

.horseStatusFrame {
    display: flex;
    width: 525px;
    padding: 15px;
    flex-direction: column;
    align-items: flex-start;
    gap: 10px;
    align-self: stretch;
    border-radius: 20px;
    background: linear-gradient(112deg, #27334C 0%, #556588 100%);
}

.horseCareFrame {
    display: flex;
    width: 460px;
    padding: 15px;
    flex-direction: column;
    align-items: flex-start;
    gap: 10px;
    align-self: stretch;
    border-radius: 20px;
    background: linear-gradient(112deg, #27334C 0%, #556588 100%);
}

#horseImage {
    width: 330px;
    height: 330px;
    flex-shrink: 0;
    aspect-ratio: 1/1;
    background: url(../../lib/assets/andalusian.png) lightgray -476.185px 0px / 300.415% 169.091% no-repeat;
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
    height: 625px;
    padding: 10px;
    align-items: center;
    gap: 25px;
    flex-shrink: 0;
    align-self: stretch;
}

#barnBar {
    display: flex;
    width: 320px;
    height: 1020px;
    padding: 15px;
    flex-direction: column;
    align-items: flex-start;
    gap: 15px;
    border-radius: 20px;
    background: rgba(202, 202, 202, 0.30);
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
}

.male {
    background: linear-gradient(91deg, #1D4778 0%, #4674A9 100%);
}

.female {
    background: linear-gradient(91deg, #781D31 0%, #A94681 100%);
}

#horsePage {
    display: flex;
    height: 1100px;
    padding: 40px;
    align-items: flex-start;
    gap: 40px;
}
</style>