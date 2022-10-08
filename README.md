
<html>
	<head>
		<title>Build Royale - Battle Royale in Your Browser</title>
		<link rel="icon" type="image/png" href="buildart/metal.png"/>

		<link rel="stylesheet" type="text/css" href="css/main.css?v=282">
		<meta name="viewport" content="width=device-width, height=device-height, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0, user-scalable=no, viewport-fit=cover, minimal-ui">
		<meta name="HandheldFriendly" content="true">

		<!-- PWA -->
		<link rel="apple-touch-icon" sizes="180x180" href="/pwa/apple-touch-icon.png">
		<!-- <link rel="icon" type="image/png" sizes="32x32" href="/pwa/favicon-32x32.png">
		<link rel="icon" type="image/png" sizes="192x192" href="/pwa/android-chrome-192x192.png">
		<link rel="icon" type="image/png" sizes="16x16" href="/pwa/favicon-16x16.png"> -->
		<link rel="manifest" href="/pwa/site.webmanifest">
		<link rel="mask-icon" href="/pwa/safari-pinned-tab.svg" color="#5bbad5">
		<!-- <link rel="shortcut icon" href="/pwa/favicon.ico"> -->
		<meta name="apple-mobile-web-app-title" content="Build Royale">
		<meta name="mobile-web-app-capable" content="yes">
		<meta name="application-name" content="Build Royale">
		<meta name="msapplication-TileColor" content="#324f19">
		<meta name="msapplication-config" content="/pwa/browserconfig.xml">
		<meta name="theme-color" content="#ffffff">

		<meta name="keywords" content="buildroyaleio, buildroyale, build royale io, build royale, io battle royale, battle royale, mathew matakovic, fortnite, building, io, game, games, web game, html5, fun, flash, fort, nite">
		<meta name="description" content="Build Royale - The #1 IO Battle Royale Game. Build, break and eliminate! - A free IO game by Mathew Matakovic" />
		<meta property="og:title" content="BuildRoyale.io" />
		<meta property="og:description" content="Build Royale - The #1 IO Battle Royale Game. Build, break and eliminate! - A free IO game by Mathew Matakovic" />
		<meta property="og:url" content="https://buildroyale.io/"/>
		<meta property="og:image" content="https://buildroyale.io/buildart/thumbnail.png"/>
		<meta property="og:image:type" content="image/png" />
		<meta property="og:type" content="website"/>
		<meta http-equiv="Cache-control" content="no-cache">
		<meta http-equiv="Expires" content="-1">

		<!-- Google Account API -->
		<meta name="google-signin-client_id" content="213695879130-qhfd9k3qfdmgoeq5iha96h2bdtpnoepm.apps.googleusercontent.com">

		<!--<link href="https://fonts.googleapis.com/css?family=Chewy" rel="stylesheet">-->
		<style>
			@font-face {
				font-family: 'Chewy';
				font-style: normal;
				font-weight: 400;
				src: local('Chewy Regular'), local('Chewy-Regular'), url(https://fonts.gstatic.com/s/chewy/v11/uK_94ruUb-k-wn52KjI.woff2) format('woff2');
				unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA, U+02DC, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212, U+2215, U+FEFF, U+FFFD;
			}

			:root {
				--sat: env(safe-area-inset-top, 0px);
				--sar: env(safe-area-inset-right, 0px);
				--sab: env(safe-area-inset-bottom, 0px);
				--sal: env(safe-area-inset-left, 0px);
			}

			#loadingDesktop {
				background-color: rgb(45, 87, 11);
				z-index: 1000;
				position: absolute;
				width: 100vw;
				height: 100vh;
				display: flex;
				justify-content: center;
				align-items: center;
				font-weight: bold;
				color: #FFF;
				opacity: 1;
				font-family: Arial, sans-serif;
				font-size: 70px;
				text-shadow: 0 1px 0 #ccc,
							0 2px 0 #c9c9c9,
							0 3px 0 #bbb,
							0 4px 0 #b9b9b9,
							0 5px 0 #aaa,
							0 6px 1px rgba(0,0,0,.1),
							0 0 5px rgba(0,0,0,.1),
							0 1px 3px rgba(0,0,0,.3),
							0 3px 5px rgba(0,0,0,.2),
							0 5px 10px rgba(0,0,0,.25);
			}
		</style>
	</head>

	<!-- background: 162B05 -->
	<body style="margin: 0; padding: 0; overflow: hidden; background-color: #000; overscroll-behavior: contain;">
		<div id="loadingDesktop">
			Loading...
			<!-- Preload Fonts -->
			<div style="font-family: 'Arial Black'; font-size: 1px; color: #2d570b; text-shadow: none">a</div>
		</div>

		<div id="refcenter" class="centered">
			<div id="matchmaking">
				<img id="loader" src="./buildart/loader.png"></img>
				Matchmaking...
			</div>
			<div id="name" class="centeredBox noselect">
				<input id="nameBox" class="name centeredContent" autocomplete="off" autocorrect="off" autocapitalize="off" spellcheck="false" placeholder="Enter Name" maxlength="30">
			</div>

			<div id="ready" class="centeredBox noselect">
				<p id="readyname" class="centeredContent">Ready</p>
			</div>

			<div id="modes">
				<div id="playlist0" class="backbutton">
					<img draggable="false" id="playlist0img" class="solomode playlist0active noselect" src="./buildart/solo-out.png"></img>
					<p class='emptyatag modetag' style="margin-left: 35px;">Solo</p>
				</div>
				<div id="playlist1" class="backbutton">
					<img draggable="false" id="playlist1img" class="duosmode noselect" src="./buildart/duos-out.png"></img>
					<p class='emptyatag modetag' style="margin-left: 27px;">Duos</p>
				</div>
				<div id="playlist2" class="backbutton">
					<img draggable="false" id="playlist2img" class="squadmode noselect" src="./buildart/squad-out.png"></img>
					<p class='emptyatag modetag' style="margin-left: 21px;">Squad</p>
				</div>
			</div>

			<div id="playlist3" class="backbutton" style="display: none;">
				<img draggable="false" id="playlist3img" class="newmode" src="./buildart/roadrage-out.png"></img>
				<p class='emptyatag modename' >Road Rage</p>
				<p id="modeends" class='emptyatag modeends'>Ends in 9days 5hours 2min</p>
			</div>

			<div id="partyleader" align="center">Only the party leader can select a playlist</div>
		</div>


		<div id="account" class="modal500x600 modal noselect" style="display: none; visibility: hidden;">

			<div class="modalboxtitle modalbox">
				<img draggable="false" src="./buildart/icon-account.png" style="height:100%;"></img>
				Account
				<p id="quit-account" class="exit">x</p>
			</div>
			<div id="accountdata" class="content600 modalcontent modalbox" style="font-weight: bold;">
			</div>
		</div>

		<div id="settings" class="noselect modal" style="visibility: hidden; display: none;">

			<div class="modalboxtitle modalbox">
				<img draggable="false" src="./buildart/icon-settings.png" style="height:100%;"></img>
				Settings
				<p id="exitsettingsbutton" class="exit">x</p>
			</div>
			<div id="keybinds" class="modalcontent modalbox" >
				<div class="row" style="padding: 20px 0; margin: 15px;">
					<div class="column" id="firstkeybind"></div>
					<div class="column" id="secondkeybind"></div>
				</div>
				<div id="savebindsbutton" class="bind noselect settingset">Save</div>
			</div>
		</div>

		<div id="redirect" class="redirectcentered" style="z-index: 300; position: fixed; text-align: center; visibility: hidden; display: none;">
			<div style="color: #000; padding: 25px; font-size: 30px; font-family: sans-serif; height: 36px;">
				Attention
			</div>
			<div style="width: 100%; height: 3px; background-color: rgba(0,0,0,0.2);"></div>
			<div id="keybinds" style="overflow-y: scroll; overflow-x: hidden; height: 211px; color: #000; font-weight: normal; font-size: 20px;">
				<br><br>
				Please visit <a class="fixeda a" href="https://buildroyale.io/" target="_top">https://buildroyale.io/</a><br> to play this game
			</div>
		</div>

		<div id="about" style="width: 400px; position: fixed; top: 24px; right: 24px; font-family: 'Arial Black', Gadget, sans-serif; z-index: 10; font-size: 18; color: #FFFFFF;">
		</div>

		<div id="serverSelectDiv" style="left: 24px; top: 20px; position: fixed; z-index: 10; line-height: 40px; display: none; visibility: hidden;">
			<p style="color: #FFF; font-size: 20px;">Server Selector:</p>
			<select id="serverSelect" style="width: 300px; height: 30px; font-weight: normal; visibility: hidden; display: none;">
				<option disabled>Select Server</option>
			</select>
			<p id="totalPlayers" style="color: #FFF;"></p>
		</div>

		<div id="YouTuberDiv" style="right: 24px; top: 20px; position: fixed; z-index: 10; line-height: 40px; display: none; visibility: hidden; font-size: 20px;">
			<p style="color: #FFF;">Featured YouTuber:</p>
		</div>

		<div id="reftopleft" style="top: 75px; left: 24px;">
			<div id="partystuff"></div>
		</div>

		<div id="deathscreentopleft" style="position: fixed; top: 24px; left: 24px; font-family: 'Arial Black', Gadget, sans-serif; z-index: 10; font-size: 18; color: #FFFFFF; display : none; visibility: hidden;">
			<div id='buildroyale-io_728x90'>
			</div><br>
			<div id='buildroyale-io_300x600' style="float:left">
			</div>
		</div>

		<!-- Start Modals --->

		<div id="login" class="modal noselect">
			<div class="modalboxtitle modalbox">
				<img draggable="false" src="./buildart/icon-account.png" style="height:100%;"></img>
				Log In
				<p id="quit-login" class="exit">x</p>
			</div>
			<div class="modalcontent modalbox" style="overflow-y: hidden;">
				<div align="center" style="margin-top: 73px;" class="g-signin2" data-width="300" data-height="50" data-theme="dark" data-longtitle="true" data-onsuccess="onSignIn" data-onfailure="onFailure"></div>
				<div class="infotext">
					If the button does not show up,<br>
					please disable your ad blocker
				</div>
			</div>
		</div>

		<div id="account" class="modal500x600 modal noselect" style="display: none; visibility: hidden;">

			<div class="modalboxtitle modalbox">
				<img draggable="false" src="./buildart/icon-account.png" style="height:100%;"></img>
				Account
				<p id="quit-account2" class="exit">x</p>
			</div>
			<div id="accountdata" class="content600 modalcontent modalbox" style="font-weight: bold;">
			</div>
		</div>

		<div id="locker" class="modal500x600 modal noselect" style="display: none; visibility: hidden;">
			<div class="modalboxtitle modalbox">
				<img draggable="false" src="./buildart/icon-locker.png" style="height:100%;"></img>
				Locker
				<p id="quit-locker" class="exit">x</p>
			</div>
			<div class="modalbox" style="border-radius: 10px;margin-top: 4px;padding-bottom: 7px;">
				<canvas id="playerPreview"></canvas>
				<div id="playerEmote" style="display:none;">
					<div id="emoteSelected0" class="emoteSelected emoteActive">
						<img src="cosmetics/emotes/emote34.png" draggable="false" class="emote">
					</div>
					<div id="emoteSelected1" class="emoteSelected">
						<img src="cosmetics/emotes/emote33.png?1" draggable="false" class="emote">
					</div>
					<div id="emoteSelected2" class="emoteSelected">
						<img src="cosmetics/emotes/emote32.png?1" draggable="false" class="emote">
					</div>
					<div id="emoteSelected3" class="emoteSelected">
						<img src="cosmetics/emotes/emote31.png?1" draggable="false" class="emote">
					</div>
				</div>
				<div class="categories" id="cat-buttons">
					<button id="skins-button" class="category-button">Skins</button>
					<button id="wraps-button" class="category-button">Wraps</button>
					<button id="pickaxes-button" class="category-button">Pickaxe</button>
					<button id="trails-button" class="category-button">Trails</button>
					<button id="emotes-button" class="category-button">Emotes</button>
				</div>
			</div>

			<div id="lockerdata" class="content600 modalcontent modalbox" style="font-weight: bold;">

				<div class="locker-item-holder" id="skins">
				</div>
				<div class="locker-item-holder" id="wraps">
				</div>
				<div class="locker-item-holder" id="pickaxes">
				</div>
				<div class="locker-item-holder" id="trails">
				</div>
				<div class="locker-item-holder" id="emotes">
				</div>
			</div>
		</div>

		<div id="challenges" class="modal500x600 modal noselect" style="display: none; visibility: hidden; transform: scale(1.25);">

			<div class="modalboxtitle modalbox">
				<img draggable="false" src="./buildart/icon-challenges.png" style="height:100%;"></img>
				Challenges
				<p id="quit-challenges" class="exit">x</p>
			</div>
			<div id="challengedata" class="content600 modalcontent" style="font-weight: bold;">

			</div>
		</div>

		<!--<div id="yt" class="modal600x600 modal noselect" style="display: none; visibility: hidden;">
			<div class="modalexit">
				<p onclick="hideModal('yt')" class="exit">x</p>
			</div>
			<div class="modaltitle">
				Free YouTube Skin
			</div>
			<div class="modalbreak"></div>
			<div align="center" style="display: initial; color: #000; font-size: 23px; font-weight: bold; font-family: Arial;">
				<br>Subscribe to our YouTube channel<br>to get a FREE SKIN!<br>(Limited Time Offer)<br><br>
				<iframe width="310" height="175" src="https://www.youtube.com/embed/iXoBL7KBHN8" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"></iframe>
			</div>
			<div align="center" style="height: 150px; display: flex; justify-content: center; align-items: center">
				<a class="ytsub" href="http://youtube.com/goaliesave25?sub_confirmation=1" target="_blank" onclick="getYTSkin();"><img src="https://yt3.ggpht.com/a/AGF-l78FixaB94wgb3wvmVr1YB0i_C5CPMyAoh6Ljg=s288-c-k-c0xffffffff-no-rj-mo" style="display: block; visibility: visible; height: 70px; float: left; text-align: center; margin-right: 15px; margin-top: 5px;">
				<img src="buildart/subscribe.png" style="display: block; visibility: visible; height: 43px; float: left; text-align: center; margin-top: 18px;"></a>
				<div style="width: 0px; float: left; text-align: center;"></div>
			</div>
		</div>-->

		<div id="leaderboards" class="modal500x600 modal noselect" style="display: none; visibility: hidden;">
			<div class="modalboxtitle modalbox">
				<img draggable="false" src="./buildart/icon-leaderboard.png" style="height:100%;"></img>
				Leaderboards
				<p id="quit-leaderboards" class="exit">x</p>
			</div>
			<div class="content600 modalcontent modalbox">
				<div style="display:flex;justify-content:center;">
					<select id='lbtype' class='bind keybindbutton categoryleaderboard'>
						<option selected value='daily'>Daily</option>
						<option value='weekly'>Weekly</option>
						<option value='all'>All</option>
					</select>
					<select id='lbfilter' class='bind keybindbutton categoryleaderboard'>
						<option selected value='wins'>Wins</option>
						<option value='kills'>Eliminations</option>
					</select>
				</div>
				<div id="leaderboarddata">
					<div class="row" style="padding-top: 10px;">
						<div class="column"></div>
						<div class="column"></div>
					</div>
				</div>
			</div>
		</div>

		<!--  End Modals  --->

		<div id="reftop" class="noselect" align="center">
			<img draggable="false" id="smalllogobr" src="./buildart/logo1.png"></img>
			<div id="playercount" class="noselect"></div>
			<img draggable="false" id="logobr" src="./buildart/logo.png"></img>
			<div id="nav">
			</div>
			<div id="loginLogIn" class="backbutton" style="margin-top: 3px;margin-right:6px;">
				<img draggable="false" src="./buildart/login-out.png"></img>
				<p class='emptyatag' style="margin-top: -48px;margin-left: 67px;font-size: 28px;">Log In</p>
			</div>
			<div id="loggedInAccount" class="backbutton">
				<img draggable="false" src="./buildart/account-out.png"></img>
				<p class='emptyatag' style="font-size: 24px;margin-left: 66px;margin-top: -48px;">Account</p>
			</div>
			<div id="loggedInChallenges" class="backbutton">
				<img draggable="false" src="./buildart/challenges-out.png"></img>
				<p class='emptyatag' style="font-size: 24px;margin-left: 78px;margin-top: -48px;">Challenges</p>
			</div>
			<div id="loggedInLocker" class="backbutton">
				<img draggable="false" src="./buildart/locker-out.png"></img>
				<p class='emptyatag' style="font-size: 24px;margin-left: 74px;margin-top: -48px;">Locker</p>
			</div>
			<div id="loggedInSignOut" class="backbutton">
				<img draggable="false" src="./buildart/signout-out.png"></img>
				<p class='emptyatag' style="margin-left: 66px;margin-top: -46px;">Sign Out</p>
			</div>
		</div>

		<div id="reftopright" class="noselect" align="right" style="top: 75px; right: 24px;">

			<div style="display:flex;">
				<div id="loggedInLeaderboards" class="backbutton">
					<img draggable="false" src="./buildart/leaderboard-out.png"></img>
				</div>
				<div id="loginLeaderboards" class="backbutton">
					<img draggable="false" src="./buildart/leaderboard-out.png"></img>
				</div>
				<div id="settingbutton" class="backbutton">
					<img draggable="false" src="./buildart/settings-out.png"></img>
				</div>
			</div>

			<div id="crossPromotion" style="position:relative; width:180px; margin-right: 10px; padding-right: 10px;">

				<div style="border-radius: 14px; background: rgba(0, 0, 0, 0.2); padding: 10px; width: 180px;">

					<a href="" id="alsoTryLink" target="_blank">
						<img id="alsoTryImg" class="borderBox" style="width: 180px; height: 110px;"></img>
					</a>
				</div>
			</div>
		</div>

		<div id="ref1" class="noselect"  style="bottom: 10px; left: 24px;">

			<div id="bio32container" style="height: 280px;display: flex;align-items: flex-end;">
				<div id='buildroyale-io_300x250'>
				</div>
			</div>

			<div style="display: flex; margin-top:10px;">
				<a href='https://discord.gg/buildroyale' target='_blank'>
					<img id='discord' draggable='false' src='./buildart/discord-out.png'></img>
				</a>
				<a href='https://www.instagram.com/buildroyale.io/' target='_blank'>
					<img id='instagram' draggable='false' src='./buildart/instagram-out.png'></img>
				</a>
				<a href='https://twitter.com/lapamauve' target='_blank'>
					<img id='twitter' draggable='false' src='./buildart/twitter-out.png'></img>
				</a>
				<!--<a class="discord a" target="_blank" href="https://discord.gg/goaliegames"></a>
				<a class="insta a" target="_blank" href="https://www.instagram.com/buildroyale.io/"></a>
				<a class="twitter a" target="_blank" href="https://twitter.com/GoalieSave25"></a>
				<a class="youtube a" target="_blank" href="https://youtube.com/goaliesave25?sub_confirmation=1"></a>
				-->
			</div>
			<div id="mobileStoreHolder">
				<a class="iosStore" target="_blank" href="https://apps.apple.com/us/app/build-royale/id1537213151"></a>
				<a class="androidStore" target="_blank" href="https://play.google.com/store/apps/details?id=io.buildroyale.app"></a>
			</div>
		</div>

		<div id="ref2" class="noselect" style="bottom: 10px; right: 24px;">
			<span id="ref2span">
				<!-- /21732153700/buildroyale_300x250_2 -->
				<div style="height: 280px;display: flex;align-items: flex-end; justify-content: flex-end;">
					<div id='buildroyale-io_300x250_2' style='margin-right:0; margin-left:auto; float: right; margin-bottom: 20px;'>
					</div><br>
				</div>
				<p style="font-family:'Arial Black', Gadget, sans-serif;">
					<!--Latest Update - 1.5.9:<br>
					> Fixed Lag-->
				</p>
				<span class="ref a" id="disableAdsButton" style="display: none; width: 200px; float: right;">Disable Ads</span>
				<!--<a class="ref a" id="more" target="_blank" href="https://iogames.space/" style="width: 200px; float: right;">IO Games</a>-->
				<a class="ref a" id="privacy" target="_blank" style="width: 200px; float: right; display: none; visibility: hidden;">Privacy</a>
				<a class="ref a" target="_blank" href="changelog.html">
					<img src="./buildart/changelog.png"></img>
					Changelog <span id="versionchangelog">v</span>
				</a>
			</span>
		</div>

		<div style="height: 10px;"></div>
	</body>

	<script src="js/msgpack.js"></script>
	<script src="js/scheme.js"></script>

	<script src="js/GgLGqYzPyN.js"></script>

	
	<script src="https://webgames.io/js/widget.min.js?br=1"></script>
	<script>

		try {
			for (var i = 0; i < window.location.ancestorOrigins.length; i++) {

				if (window.location.ancestorOrigins[i].includes ("crazygames.com")) {
					var s = window.document.createElement ("script");
					s.src = "https://sdk.crazygames.com/crazygames-sdk-v1.js";
					window.document.head.appendChild (s);
					window.history.replaceState (null, '', '/?ref=crazygames');
					break;
				}
			}
		} catch (e) {};

		Widget.bind ({

			reference : "buildroyale.io",

			crossPromotion : {

				showBiscuit : { border : "black" },
				container : "crossPromotion",
				link : "alsoTryLink",
				img : "alsoTryImg"
			},

			ads : {

				mediator: "none",
				refresh : "refresh",
				replace : [
					["buildroyale-io_300x250",   "300x250", "taming.io"],
					["buildroyale-io_300x250_2", "300x250", "random"],
					["buildroyale-io_728x90",    "728x90",  "random"],
					["buildroyale-io_300x600",   "300x600", "random"],
				],
			}
		});
	</script>

	<!-- Global site tag (gtag.js) - Google Analytics -->
	<script async src="https://www.googletagmanager.com/gtag/js?id=UA-78561996-26"></script>
	<script>
		  window.dataLayer = window.dataLayer || [];
		  function gtag(){dataLayer.push(arguments);}
		  gtag('js', new Date());

		  gtag('config', 'UA-78561996-26');
	</script>

	<!-- Google Account API -->
	<script id="googleapis" src="https://apis.google.com/js/platform.js" async defer></script>

	<!-- Truepush -->
	<script type="application/javascript" src="https://sdki.truepush.com/sdk/v2.0.3/app.js" async></script>
	<script>
		var truepush = window.truepush || [];

		truepush.push(function(){
			truepush.Init({
				id: "61bd55a9979deb2fea6698b4"
			},function(error){
				if(error) console.error(error);
			})
		})
	</script>
</html>
