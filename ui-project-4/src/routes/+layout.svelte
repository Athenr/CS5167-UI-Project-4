<script>
	import { goto } from '$app/navigation';
	import "../global.css";
	import favicon from "$lib/assets/favicon.svg";
	import SiteLogo from "$lib/assets/SiteLogo.png";

	let isDarkMode = true;

	function gotoHome() {
        goto('/'); 
    }

	function gotoHorses() {
        goto('/horses'); 
    }

	function gotoEquiPedia() {
        goto('/equipedia'); 
    }

	function gotoVetScanner() {
        goto('/vetScanner'); 
    }

	function changeThemeMode() {
        isDarkMode = !isDarkMode;
		document.body.classList.toggle('light-mode', !isDarkMode);
    }

  	let { children } = $props();
</script>

<svelte:head>
  	<link rel="icon" href={favicon} />
</svelte:head>

<div id="headerBackground">
	<div id="title" on:click={gotoHome}>
		<div id="logoDiv">
			<img id="logo" src={SiteLogo} alt="logo"/>
		</div>
		StablEye
	</div>

	<div id="navBar">
		<div class="navItem" on:click={gotoHorses}>Horses</div>
		<div class="navItem" on:click={gotoEquiPedia}>EquiPedia</div>
		<div class="navItem" on:click={gotoVetScanner}>VetScanner</div>
	</div>

	<div id="profile">
		<div id="profileImageDiv">
		<img id="profileImage" src={SiteLogo} alt="profile"/>
		</div>
		AdminUser12
	</div>

	<div id="logout">
		<div id="themeChange" on:click={changeThemeMode}>
			<div id="themeChangeIconBox">
				<svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 28 28" fill="none">
					<path d="M14 17.5C14.9722 17.5 15.7986 17.1597 16.4791 16.4792C17.1597 15.7986 17.5 14.9722 17.5 14C17.5 13.0278 17.1597 12.2014 16.4791 11.5208C15.7986 10.8403 14.9722 10.5 14 10.5C13.0277 10.5 12.2013 10.8403 11.5208 11.5208C10.8402 12.2014 10.5 13.0278 10.5 14C10.5 14.9722 10.8402 15.7986 11.5208 16.4792C12.2013 17.1597 13.0277 17.5 14 17.5ZM14 19.8333C12.3861 19.8333 11.0104 19.2646 9.87288 18.1271C8.73538 16.9896 8.16663 15.6139 8.16663 14C8.16663 12.3861 8.73538 11.0104 9.87288 9.87291C11.0104 8.73541 12.3861 8.16666 14 8.16666C15.6138 8.16666 16.9895 8.73541 18.127 9.87291C19.2645 11.0104 19.8333 12.3861 19.8333 14C19.8333 15.6139 19.2645 16.9896 18.127 18.1271C16.9895 19.2646 15.6138 19.8333 14 19.8333ZM5.83329 15.1667H1.16663V12.8333H5.83329V15.1667ZM26.8333 15.1667H22.1666V12.8333H26.8333V15.1667ZM12.8333 5.83332V1.16666H15.1666V5.83332H12.8333ZM12.8333 26.8333V22.1667H15.1666V26.8333H12.8333ZM7.46663 9.04166L4.52079 6.21249L6.18329 4.49166L8.98329 7.40832L7.46663 9.04166ZM21.8166 23.5083L18.9875 20.5625L20.5333 18.9583L23.4791 21.7875L21.8166 23.5083ZM18.9583 7.46666L21.7875 4.52082L23.5083 6.18332L20.5916 8.98332L18.9583 7.46666ZM4.49163 21.8167L7.43746 18.9875L9.04163 20.5333L6.21246 23.4792L4.49163 21.8167Z" fill="#FEF7FF"/>
				</svg>
			</div>
		</div>
		<button id="logoutButton"> Logout </button>
	</div>
</div>

<main>
  <div id="mainPage">
    {@render children()}
  </div>
</main>

<style>
* {
	color: #fff;
	font-family: Inter;
	font-size: 30px;
	font-style: normal;
	font-weight: 800;
	line-height: normal;
}

.navItem {
	display: flex;
	height: 50px;
	justify-content: center;
	align-items: center;
	color: #FFF;
	font-family: Inter;
	font-size: 25px;
	font-style: normal;
	font-weight: 800;
	line-height: normal;
}

#mainPage {
	display: flex;
	width: 100%;
	flex-direction: column;
	align-items: flex-start;
	flex-shrink: 0;
	height: calc(100vh - 100px);
}

#headerBackground {
	display: flex;
	width: 100%;
	height: 70px;
	padding: 10px;
	align-items: center;
	gap: 20px;
	background: #0077B6;
}

#navBar {
	display: flex;
	width: 45%;
	padding: 10px 0;
	justify-content: center;
	align-items: center;
	gap: 90px;
	flex-shrink: 0;
	align-self: stretch;

}

#title {
	width: 20%;
	display: flex;
	height: 70px;
	align-items: center;
	gap: 10px;
	flex-shrink: 0;
	color: #FFF;
	font-family: "Baloo 2";
	font-size: 48px;
	font-style: normal;
	font-weight: 800;
	line-height: normal;
}

#profile {
	display: flex;
	width: 15%;
	align-items: center;
	gap: 10px;
	flex-shrink: 0;
	align-self: stretch;
	color: #FFF;
	font-family: Inter;
	font-size: 25px;
	font-style: normal;
	font-weight: 500;
	line-height: normal;
}

#logout {
	display: flex;
	width: 15%;
	padding: 5px 0;
	justify-content: center;
	align-items: center;
	gap: 30px;
	flex-shrink: 0;
	align-self: stretch;
}

#profileImage {
	width: 50px;
	height: 50px;
	flex-shrink: 0;
	aspect-ratio: 1/1;
	border-radius: 50px;
}

#profileImageDiv {
	display: flex;
	width: 50px;
	height: 50px;
	justify-content: center;
	align-items: center;
	flex-shrink: 0;
	aspect-ratio: 1/1;
}

#logoutButton {
	display: flex;
	width: 120px;
	padding: 5px 0;
	justify-content: center;
	align-items: center;
	flex-shrink: 0;
	align-self: stretch;
	border-radius: 30px;
	border: 4px solid #FFF;
	background: #FF6B6B;
	color: #FFF;
	text-align: center;
	font-family: Inter;
	font-size: 25px;
	font-style: normal;
	font-weight: 500;
	line-height: normal;
}

#themeChange {
	display: flex;
	width: 40px;
	padding: 16px 16px;
	justify-content: center;
	align-items: center;
	gap: 10px;
	flex-shrink: 0;
	align-self: stretch;
	aspect-ratio: 1/1;
	border-radius: 30px;
	border: 4px solid #FFF;
	background: #0077B6;
}

#themeChangeIconBox {
	width: 28px;
	height: 28px;
	flex-shrink: 0;
	aspect-ratio: 1/1;
}

#themeChangeIcon {
	width: 25.667px;
	height: 25.667px;
	fill: var(--Schemes-Background, #fef7ff);
}

#logoDiv {
	display: flex;
	width: 70px;
	height: 70px;
	justify-content: center;
	align-items: center;
	aspect-ratio: 1/1;
}

#logo {
	width: 70px;
	height: 70px;
	flex-shrink: 0;
	aspect-ratio: 1/1;
}
</style>
