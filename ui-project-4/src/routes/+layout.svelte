<script>
	import "../global.css";
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<header>
	<div id="headerBackground">
		<div id="title">
			<img id="logo" alt="StablEye">
			StablEye
		</div>

		<div id="navBar">
			<div class="navItem">Horses</div>
			<div class="navItem">Map</div>
			<div class="navItem">EquiPedia</div>
			<div class="navItem">VetScanner</div>
		</div>

		<div id="profile">
			<div id="profileImageDiv">
				<img id="profileImage" alt="Profile Avatar">
			</div>
			AdminUser12
		</div>

		<div id="logout">
			<div id="themeChange">
				<div id="themeChangeIconBox">
					<svg width="35" height="36" viewBox="0 0 35 36" fill="none" xmlns="http://www.w3.org/2000/svg" id="themeChangeIconBox">
  						<path d="M17.5 22.5C18.7153 22.5 19.7483 22.0625 20.599 21.1875C21.4497 20.3125 21.875 19.25 21.875 18C21.875 16.75 21.4497 15.6875 20.599 14.8125C19.7483 13.9375 18.7153 13.5 17.5 13.5C16.2848 13.5 15.2518 13.9375 14.4011 14.8125C13.5504 15.6875 13.125 16.75 13.125 18C13.125 19.25 13.5504 20.3125 14.4011 21.1875C15.2518 22.0625 16.2848 22.5 17.5 22.5ZM17.5 25.5C15.4827 25.5 13.7631 24.7688 12.3412 23.3063C10.9193 21.8438 10.2084 20.075 10.2084 18C10.2084 15.925 10.9193 14.1562 12.3412 12.6938C13.7631 11.2312 15.4827 10.5 17.5 10.5C19.5174 10.5 21.237 11.2312 22.6589 12.6938C24.0808 14.1562 24.7917 15.925 24.7917 18C24.7917 20.075 24.0808 21.8438 22.6589 23.3063C21.237 24.7688 19.5174 25.5 17.5 25.5ZM7.29171 19.5H1.45837V16.5H7.29171V19.5ZM33.5417 19.5H27.7084V16.5H33.5417V19.5ZM16.0417 7.5V1.5H18.9584V7.5H16.0417ZM16.0417 34.5V28.5H18.9584V34.5H16.0417ZM9.33337 11.625L5.65108 7.9875L7.72921 5.775L11.2292 9.525L9.33337 11.625ZM27.2709 30.225L23.7344 26.4375L25.6667 24.375L29.349 28.0125L27.2709 30.225ZM23.698 9.6L27.2344 5.8125L29.3855 7.95L25.7396 11.55L23.698 9.6ZM5.61462 28.05L9.29692 24.4125L11.3021 26.4L7.76567 30.1875L5.61462 28.05Z" fill="#FEF7FF"/>
						
						<svg width="33" height="33" viewBox="0 0 33 33" fill="none" xmlns="http://www.w3.org/2000/svg" id="themeChangeIcon">
  							<path d="M16.0417 21C17.2569 21 18.2899 20.5625 19.1406 19.6875C19.9913 18.8125 20.4167 17.75 20.4167 16.5C20.4167 15.25 19.9913 14.1875 19.1406 13.3125C18.2899 12.4375 17.2569 12 16.0417 12C14.8264 12 13.7934 12.4375 12.9427 13.3125C12.092 14.1875 11.6667 15.25 11.6667 16.5C11.6667 17.75 12.092 18.8125 12.9427 19.6875C13.7934 20.5625 14.8264 21 16.0417 21ZM16.0417 24C14.0243 24 12.3047 23.2688 10.8828 21.8063C9.46094 20.3438 8.75 18.575 8.75 16.5C8.75 14.425 9.46094 12.6562 10.8828 11.1938C12.3047 9.73125 14.0243 9 16.0417 9C18.059 9 19.7786 9.73125 21.2005 11.1938C22.6224 12.6562 23.3333 14.425 23.3333 16.5C23.3333 18.575 22.6224 20.3438 21.2005 21.8063C19.7786 23.2688 18.059 24 16.0417 24ZM5.83333 18H0V15H5.83333V18ZM32.0833 18H26.25V15H32.0833V18ZM14.5833 6V0H17.5V6H14.5833ZM14.5833 33V27H17.5V33H14.5833ZM7.875 10.125L4.19271 6.4875L6.27083 4.275L9.77083 8.025L7.875 10.125ZM25.8125 28.725L22.276 24.9375L24.2083 22.875L27.8906 26.5125L25.8125 28.725ZM22.2396 8.1L25.776 4.3125L27.9271 6.45L24.2812 10.05L22.2396 8.1ZM4.15625 26.55L7.83854 22.9125L9.84375 24.9L6.30729 28.6875L4.15625 26.55Z" fill="#FEF7FF"/>
						</svg>
					</svg>
				</div>
			</div>
			<button id="logoutButton">
				Logout
			</button>
		</div>

	</div>
</header>

<main>
	<div id="mainPage">
		{@render children()}
	</div>
</main>

<style>
* {
	color: #FFF;
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
	font-size: 30px;
	font-style: normal;
	font-weight: 800;
	line-height: normal;
}

#mainPage {
	display: flex;
	width: 1920px;
	height: 1100px;
	padding: 40px;
	flex-direction: column;
	align-items: flex-start;
	flex-shrink: 0;
}

#headerBackground {
	display: flex;
	width: 1920px;
	padding: 10px;
	align-items: center;
	gap: 20px;
	background: #0077B6;
}

#title {
	display: flex;
	width: 350px;
	align-items: center;
	gap: 10px;
	flex-shrink: 0;
	
}

#navBar {
	display: flex;
	width: 900px;
	padding: 10px 0;
	justify-content: center;
	align-items: center;
	gap: 90px;
	flex-shrink: 0;
}

#profile {
	display: flex;
	width: 350px;
	align-items: center;
	gap: 10px;
	flex-shrink: 0;
}

#profileImage {
	width: 70px;
	height: 70px;
	flex-shrink: 0;
	aspect-ratio: 1/1;
	border-radius: 50px;
	background: url(../lib/assets/SiteLogo.png) lightgray 50% / cover no-repeat;
}

#profileImageDiv {
	display: flex;
	width: 70px;
	height: 70px;
	justify-content: center;
	align-items: center;
	flex-shrink: 0;
}

#logout {
	display: flex;
	width: 240px;
	height: 60px;
	padding: 5px 0;
	justify-content: center;
	align-items: center;
	gap: 30px;
	flex-shrink: 0;
}

#logoutButton {
	display: flex;
	width: 120px;
	height: 55px;
	padding: 5px 0;
	justify-content: center;
	align-items: center;
	flex-shrink: 0;
	border-radius: 30px;
	border: 4px solid #FFF;
	background: #FF6B6B;
}

#themeChange {
	display: flex;
	width: 55px;
	height: 55px;
	padding: 16px 48px;
	justify-content: center;
	align-items: center;
	gap: 10px;
	flex-shrink: 0;
	border-radius: 30px;
	border: 4px solid #FFF;
	background: #0077B6;
}

#themeChangeIconBox {
	width: 35px;
	height: 36px;
	flex-shrink: 0;
}

#themeChangeIcon {
	width: 32.083px;
	height: 33px;
	fill: var(--Schemes-Background, #FEF7FF);
}

#logo {
	display: flex;
	width: 80px;
	height: 80px;
	justify-content: center;
	align-items: center;
	flex-shrink: 0;
	border-radius: 15px;
	background: url(../lib/assets/SiteLogo.png) lightgray 50% / cover no-repeat;
}

</style>