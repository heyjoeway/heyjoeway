<svg>
<foreignObject width="800" height="600">
<div xmlns="http://www.w3.org/1999/xhtml" id="body">

    <!-- No JS needed ;) -->

    <style>

        @font-face {
        font-family: "Pixelated MS Sans Serif";
        src: url(https://unpkg.com/98.css@0.1.16/dist/ms_sans_serif.woff) format("woff");
        src: url(https://unpkg.com/98.css@0.1.16/dist/ms_sans_serif.woff2) format("woff2");
        font-weight: 400;
        font-style: normal;
        }

        @font-face {
        font-family:"Pixelated MS Sans Serif";src:url(https://unpkg.com/98.css@0.1.16/dist/ms_sans_serif_bold.woff) format("woff");src:url(https://unpkg.com/98.css@0.1.16/dist/ms_sans_serif_bold.woff2) format("woff2");font-weight:700;font-style:normal;
        }


        :root {
            --taskbar-bg: #bdbdbd;
            --taskbar-bg-lightest: #fff;
            --taskbar-bg-light: rgba(255,255,255,0.5);
            --taskbar-bg-dark: rgba(0,0,0,0.5);
            --taskbar-bg-darkest: #000;
        }

        * {
            user-select: none;
        }

        #body {
            background: #027D7B;
            margin: 0;
            padding: 0;
            font-family: 'Pixelated MS Sans Serif', sans-serif;
            image-rendering: pixelated;
            height: 100%;
        }

        img:not([src]) {
            visibility: hidden;
        }


        #taskbar {
            background: var(--taskbar-bg);
            position: fixed;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 26px;
            padding: 1px;
        }

        #taskbar::before {
            content: " ";
            position: absolute;
            height: 1px;
            width: 100%;
            bottom: 100%;
            left: 0;
            background: var(--taskbar-bg-light);
            border-bottom: 1px solid var(--taskbar-bg-lightest);
        }

        .taskbar-section > * {
            margin: 1px;
            display: inline-block;
            position: relative;
        }

        .taskbar-section {
            height: 100%;
            display: flex;
            align-items: center;
        }

        .left { float: left; }
        .right { float: right; }


        #start-button {
            display: flex;
            align-items: center;
            font-size: 10px;
            font-weight: bold;
            padding-left: 3px;

            width: 54px;
            height: 22px;
            border-top: 1px solid var(--taskbar-bg-lightest);
            border-left: 1px solid var(--taskbar-bg-lightest);
            border-bottom: 1px solid var(--taskbar-bg-darkest);
            border-right: 1px solid var(--taskbar-bg-darkest);
            box-sizing: border-box;
        }

        /* Inner border */
        #start-button:before {
            content: " ";
            position: absolute;
            left: 0;

            width: 100%;
            height: 100%;

            border-top: 1px solid var(--taskbar-bg-light);
            border-left: 1px solid var(--taskbar-bg-light);
            border-bottom: 1px solid var(--taskbar-bg-dark);
            border-right: 1px solid var(--taskbar-bg-dark);
            box-sizing: border-box;
        }


        #start-button:hover {
            border-bottom: 1px solid var(--taskbar-bg-lightest);
            border-right: 1px solid var(--taskbar-bg-lightest);
            border-top: 1px solid var(--taskbar-bg-darkest);
            border-left: 1px solid var(--taskbar-bg-darkest);

            padding-top: 1px;
            padding-left: 4px;
        }

        /* Inner border */
        #start-button:hover:before {
            content: " ";
            position: absolute;
            left: 0;
            top: 0;

            width: 100%;
            height: 100%;

            border-bottom: 1px solid var(--taskbar-bg-light);
            border-right: 1px solid var(--taskbar-bg-light);
            border-top: 1px solid var(--taskbar-bg-dark);
            border-left: 1px solid var(--taskbar-bg-dark);
            box-sizing: border-box;
        }

        #start-button > div {
            padding-left: 3px;
        }

        .divider {
            width: 2px;
            height: calc(100% - 2px);
            border-right: 1px solid var(--taskbar-bg-light);
            border-left: 1px solid var(--taskbar-bg-dark);
            box-sizing: border-box;
        }

        .grabbable {
            width: 3px;
            height: calc(100% - 4px);

            border-top: 1px solid var(--taskbar-bg-light);
            border-left: 1px solid var(--taskbar-bg-light);
            border-bottom: 1px solid var(--taskbar-bg-dark);
            border-right: 1px solid var(--taskbar-bg-dark);
            box-sizing: border-box;
        }

        #tray {
            /* height: 100%; */
            /* width: 200px; */
            border-top: 1px solid var(--taskbar-bg-dark);
            border-left: 1px solid var(--taskbar-bg-dark);
            border-bottom: 1px solid var(--taskbar-bg-light);
            border-right: 1px solid var(--taskbar-bg-light);
            box-sizing: border-box;
            height: calc(100% - 2px);
            margin-right: 3px;
        }

        #tray-clock {
            margin-left: 6px;
            margin-right: 6px;
            font-size: 10px;
        }

        .icon {
            width: 72px;
            color: #fff;
            font-size: 10px;
            font-weight: 100;
            display: flex;
            flex-direction: column;
            align-items: center;
            height: 72px;
        }

        #desktop {
            padding-top: 2px;
        }

        .icon-text {
            margin-top: 3px;
            padding: 2px;
            box-sizing: border-box;
            border: 1px solid transparent;
            text-align: center;
        }

        .icon:hover > .icon-text {
            background: #00007b;
            border: 1px dotted #ffff84;
        }
        
        .icon:hover > img {
            filter: sepia() brightness(50%) hue-rotate(190deg);
        }

        #quick-launch {
            display: flex;
        }
        #quick-launch > img {
            padding: 2px;
            box-sizing: border-box;
            border: 1px solid transparent;
        }
        #quick-launch > img:hover {
            border-top: 1px solid var(--taskbar-bg-light);
            border-left: 1px solid var(--taskbar-bg-light);
            border-bottom: 1px solid var(--taskbar-bg-dark);
            border-right: 1px solid var(--taskbar-bg-dark);
        }
        #quick-launch > img:active {
            border-top: 1px solid var(--taskbar-bg-dark);
            border-left: 1px solid var(--taskbar-bg-dark);
            border-bottom: 1px solid var(--taskbar-bg-light);
            border-right: 1px solid var(--taskbar-bg-light);
            margin-top: 1px;
            margin-left: 1px;
            margin-bottom: -1px;
            margin-right: -1px;
        }

        #start-menu {
            display: flex;
            flex-direction: column;
            position: absolute;
            left: 0;
            bottom: calc(100% + 1px);
            background: var(--taskbar-bg);
            width: 171px;

            border-top: 1px solid var(--taskbar-bg-light);
            border-left: 1px solid var(--taskbar-bg-lightest);
            border-bottom: 1px solid var(--taskbar-bg-darkest);
            border-right: 1px solid var(--taskbar-bg-darkest);
            box-sizing: border-box;

            font-weight: normal;
            overflow: hidden;
            visibility: hidden;
        }

        /* Inner border */
        #start-menu:after {
            content: " ";
            position: absolute;
            left: 0;

            width: 100%;
            height: 100%;

            border-top: 1px solid var(--taskbar-bg-lightest);
            border-left: 1px solid var(--taskbar-bg-light);
            border-bottom: 1px solid var(--taskbar-bg-dark);
            border-right: 1px solid var(--taskbar-bg-dark);
            box-sizing: border-box;
            pointer-events: none;
        }

        /* Emblem */
        #start-menu::before {
            background: rgb(0,0,123);
            background: linear-gradient(180deg, rgba(0,0,123,1) 0%, rgba(0,0,255,1) 15%, rgba(0,0,123,1) 30%);
            color: #fff;

            content: "Windows 98";
            writing-mode: vertical-lr;
            position: absolute;
            left: 0;
            transform: rotate(180deg);

            width: 21px;
            height: 100%;

            box-sizing: border-box;

            padding-top: 5px;
            font-family: "Arial";
            font-size: 15px;
            font-weight: 800;
        }

        .start-menu-item {
            margin: 1px;
            height: 32px;
            display:flex;
            align-items: center;
        }

        .start-menu-item > img {
            width: 24px;
            height: 24px;
            margin-right: 12px;
            margin-left: 22px;
        }

        .start-menu-item:hover {
            background: #00007b;
            color: #fff;
        }

        #start-button:hover > #start-menu {
            visibility: visible;
            animation-name: start-slide;
            animation-duration: 0.1s;
            animation-timing-function: linear;
            animation-fill-mode: forwards;
        }

        @keyframes start-slide {
            0% { height: 0; }
            100% { height: 342px; }
        }

    </style>

    <div id="desktop">
        <div class="icon">
            <img src="data:image/png;base64,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" />
            <div class="icon-text">My Computer</div>
        </div>
        <div class="icon">
            <img src="data:image/png;base64,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" />
            <div class="icon-text">My Documents</div>
        </div>
        <div class="icon">
            <img src="data:image/png;base64,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" />
            <div class="icon-text"> <!-- BOOOOO THAT'S CHEATING -->
                Internet<br />
                Explorer
            </div>
        </div>
        <div class="icon">
            <img src="data:image/png;base64,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" />
            <div class="icon-text">Recycle Bin</div>
        </div>
    </div>
    <div id="taskbar">
        <div class="taskbar-section left">
            <div id="start-button">
                <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAOCAYAAAAmL5yKAAAAAXNSR0IArs4c6QAAAGhlWElmTU0AKgAAAAgABAEGAAMAAAABAAIAAAESAAMAAAABAAEAAAEoAAMAAAABAAIAAIdpAAQAAAABAAAAPgAAAAAAA6ABAAMAAAABAAEAAKACAAQAAAABAAAAEKADAAQAAAABAAAADgAAAABpet0qAAACC2lUWHRYTUw6Y29tLmFkb2JlLnhtcAAAAAAAPHg6eG1wbWV0YSB4bWxuczp4PSJhZG9iZTpuczptZXRhLyIgeDp4bXB0az0iWE1QIENvcmUgNi4wLjAiPgogICA8cmRmOlJERiB4bWxuczpyZGY9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkvMDIvMjItcmRmLXN5bnRheC1ucyMiPgogICAgICA8cmRmOkRlc2NyaXB0aW9uIHJkZjphYm91dD0iIgogICAgICAgICAgICB4bWxuczp0aWZmPSJodHRwOi8vbnMuYWRvYmUuY29tL3RpZmYvMS4wLyI+CiAgICAgICAgIDx0aWZmOlJlc29sdXRpb25Vbml0PjI8L3RpZmY6UmVzb2x1dGlvblVuaXQ+CiAgICAgICAgIDx0aWZmOk9yaWVudGF0aW9uPjE8L3RpZmY6T3JpZW50YXRpb24+CiAgICAgICAgIDx0aWZmOkNvbXByZXNzaW9uPjE8L3RpZmY6Q29tcHJlc3Npb24+CiAgICAgICAgIDx0aWZmOlBob3RvbWV0cmljSW50ZXJwcmV0YXRpb24+MjwvdGlmZjpQaG90b21ldHJpY0ludGVycHJldGF0aW9uPgogICAgICA8L3JkZjpEZXNjcmlwdGlvbj4KICAgPC9yZGY6UkRGPgo8L3g6eG1wbWV0YT4KlqhK0AAAAKhJREFUKBWNTwkOwCAIQ7P/f9nRudZKXDKShUoPRot/NYqs8S3AQenVWOhoPSdfIs0FYN8eMRDAIoVOvABV6GIjEOBnGOWOb9zTQROC/JPLN2zrUqETGIROjITNzEgb9sR6upHa2ZN5C+leacaoKcTIV0rHlDCADp0wg2B/LqDL8s4wA5hF80m4ftDVUILBtqXAdNavv7iozs6gk7EukMYJDS3UeRsLjhv4sS8GlDXAMgAAAABJRU5ErkJggg==" />
                <div>Start</div>

                <div id="start-menu">
                    <div class="start-menu-item">
                        <img src="data:image/png;base64,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"/>
                        <div>Windows Update</div>
                    </div>
                    <div class="start-menu-div"></div>
                    <div class="start-menu-item">
                        <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAXCAYAAAARIY8tAAAAAXNSR0IArs4c6QAAAGhlWElmTU0AKgAAAAgABAEGAAMAAAABAAIAAAESAAMAAAABAAEAAAEoAAMAAAABAAIAAIdpAAQAAAABAAAAPgAAAAAAA6ABAAMAAAABAAEAAKACAAQAAAABAAAAGKADAAQAAAABAAAAFwAAAADimmdHAAACC2lUWHRYTUw6Y29tLmFkb2JlLnhtcAAAAAAAPHg6eG1wbWV0YSB4bWxuczp4PSJhZG9iZTpuczptZXRhLyIgeDp4bXB0az0iWE1QIENvcmUgNi4wLjAiPgogICA8cmRmOlJERiB4bWxuczpyZGY9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkvMDIvMjItcmRmLXN5bnRheC1ucyMiPgogICAgICA8cmRmOkRlc2NyaXB0aW9uIHJkZjphYm91dD0iIgogICAgICAgICAgICB4bWxuczp0aWZmPSJodHRwOi8vbnMuYWRvYmUuY29tL3RpZmYvMS4wLyI+CiAgICAgICAgIDx0aWZmOlJlc29sdXRpb25Vbml0PjI8L3RpZmY6UmVzb2x1dGlvblVuaXQ+CiAgICAgICAgIDx0aWZmOk9yaWVudGF0aW9uPjE8L3RpZmY6T3JpZW50YXRpb24+CiAgICAgICAgIDx0aWZmOkNvbXByZXNzaW9uPjE8L3RpZmY6Q29tcHJlc3Npb24+CiAgICAgICAgIDx0aWZmOlBob3RvbWV0cmljSW50ZXJwcmV0YXRpb24+MjwvdGlmZjpQaG90b21ldHJpY0ludGVycHJldGF0aW9uPgogICAgICA8L3JkZjpEZXNjcmlwdGlvbj4KICAgPC9yZGY6UkRGPgo8L3g6eG1wbWV0YT4KlqhK0AAAAeZJREFUSA2tVD1PAkEQnTNejx2WllhhYSKWkvBHrAzEioZwuYJAaKgMFytKf4MJCZRSWEClP0E67Clw3t7N7S4sH4fM5XZm3sy+d3e7ex4l1n+hlcQuX3tWqOeq7cLOUQR59WnB0duO3hqxCB4ik4gH8vvS4w5iXfqYDHSyJeKHsB5AvcFNsbel3Yb39U1ndZ4wsN5SCcQ0a59nxmiR7yw+JrJGQyDBmXDKlzKQww71cbc1WgKd7m9SvLKasiTtVhvtakcGYUCWACpBmKPVZ0TebZWzH0Bsl3wjdvvVsk6e36N1j5laQD4Dg9MJSjAQwoQ8zuJRi4EcvZ6PddQefVqgyNk70WhYoAX12aMsVpCAvSs2Md1arpgCxhtcF+TJdXPW6Os7/rwbbyBE+fzxIvN5TA6uMyFMt2IKnCbQAlgDl/kXFPAt5vk5CS3vhbrHLGgBE5UYxEtJEs85RFxCLhEtYCyyUAYIfMkSn+Sj4TgtKOIWp93NP74SiF4vKJrU0gkSPAxHBJH2Er9yPoS830HcZHRc0QKqGPLYsH6kChZESeOYl+5KhG36312EbVqulNODZgkpaR463UhCajbw6zgck4n6HAhieCE1oFRoHyb1rQLmYZHmY7xTQI75MYTrczYEsDCntD9p1ImuGLXbpQAAAABJRU5ErkJggg=="/>
                        <div><u>P</u>rograms...</div>
                    </div>
                    <div class="start-menu-item">
                        <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAUCAYAAACXtf2DAAAAAXNSR0IArs4c6QAAAGhlWElmTU0AKgAAAAgABAEGAAMAAAABAAIAAAESAAMAAAABAAEAAAEoAAMAAAABAAIAAIdpAAQAAAABAAAAPgAAAAAAA6ABAAMAAAABAAEAAKACAAQAAAABAAAAGKADAAQAAAABAAAAFAAAAAClOh2XAAACC2lUWHRYTUw6Y29tLmFkb2JlLnhtcAAAAAAAPHg6eG1wbWV0YSB4bWxuczp4PSJhZG9iZTpuczptZXRhLyIgeDp4bXB0az0iWE1QIENvcmUgNi4wLjAiPgogICA8cmRmOlJERiB4bWxuczpyZGY9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkvMDIvMjItcmRmLXN5bnRheC1ucyMiPgogICAgICA8cmRmOkRlc2NyaXB0aW9uIHJkZjphYm91dD0iIgogICAgICAgICAgICB4bWxuczp0aWZmPSJodHRwOi8vbnMuYWRvYmUuY29tL3RpZmYvMS4wLyI+CiAgICAgICAgIDx0aWZmOlJlc29sdXRpb25Vbml0PjI8L3RpZmY6UmVzb2x1dGlvblVuaXQ+CiAgICAgICAgIDx0aWZmOk9yaWVudGF0aW9uPjE8L3RpZmY6T3JpZW50YXRpb24+CiAgICAgICAgIDx0aWZmOkNvbXByZXNzaW9uPjE8L3RpZmY6Q29tcHJlc3Npb24+CiAgICAgICAgIDx0aWZmOlBob3RvbWV0cmljSW50ZXJwcmV0YXRpb24+MjwvdGlmZjpQaG90b21ldHJpY0ludGVycHJldGF0aW9uPgogICAgICA8L3JkZjpEZXNjcmlwdGlvbj4KICAgPC9yZGY6UkRGPgo8L3g6eG1wbWV0YT4KlqhK0AAAAY9JREFUOBGtlUFOwzAQRR0E90krdQHXgQ0q4jCI7uh16KISzX26CPMm/s6kSdoiOlI7nu/v/+1xlFQpxOdHakM5Gr69p2oEXgDuNY/4+hX9jaBBPjQHq7cQ/mTi5EvicsJkudpSXm1SIf70+CyNq/L3zk3Ocks7MWiP7c1/5u73We5grveT22wMrU9mhOVsG092ivbuhNaVkGKc1nWY1BwYY+VMmTaAFCPX1cM6+dOEkEJcMI2VDZo20GLLiI7CBBxHlCAjGmtwi4sGP/uXkQni4EVU4jF3+jMG2omRFvXCxXSS5erLa/AS4pNlkifDU2SICJAsJNpV9twdN45hogAr6wClsesYQ4MsrMXehlwgKsOIp8ZOwjqEiTi2cmjgDPuDbES1QT1Xe8iDnWd+MZGO5f6SISlM3MMwiS9S3/Ny8fC0jhzrTiEYTEyygJ26OPM5OFm7z70H01wjRp/7E8wRWYSAZUS9bcKkQz0TvYFIcXEcI1DbT5iycDIBJ4S/rkN906G97MqH4+yn8h+u1S8d2dxO0N35uAAAAABJRU5ErkJggg=="/>
                        <div>F<u>a</u>vorites...</div>
                    </div>
                    <div class="start-menu-item">
                        <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAWCAYAAADafVyIAAAAAXNSR0IArs4c6QAAAGhlWElmTU0AKgAAAAgABAEGAAMAAAABAAIAAAESAAMAAAABAAEAAAEoAAMAAAABAAIAAIdpAAQAAAABAAAAPgAAAAAAA6ABAAMAAAABAAEAAKACAAQAAAABAAAAGKADAAQAAAABAAAAFgAAAADf+k73AAACC2lUWHRYTUw6Y29tLmFkb2JlLnhtcAAAAAAAPHg6eG1wbWV0YSB4bWxuczp4PSJhZG9iZTpuczptZXRhLyIgeDp4bXB0az0iWE1QIENvcmUgNi4wLjAiPgogICA8cmRmOlJERiB4bWxuczpyZGY9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkvMDIvMjItcmRmLXN5bnRheC1ucyMiPgogICAgICA8cmRmOkRlc2NyaXB0aW9uIHJkZjphYm91dD0iIgogICAgICAgICAgICB4bWxuczp0aWZmPSJodHRwOi8vbnMuYWRvYmUuY29tL3RpZmYvMS4wLyI+CiAgICAgICAgIDx0aWZmOlJlc29sdXRpb25Vbml0PjI8L3RpZmY6UmVzb2x1dGlvblVuaXQ+CiAgICAgICAgIDx0aWZmOk9yaWVudGF0aW9uPjE8L3RpZmY6T3JpZW50YXRpb24+CiAgICAgICAgIDx0aWZmOkNvbXByZXNzaW9uPjE8L3RpZmY6Q29tcHJlc3Npb24+CiAgICAgICAgIDx0aWZmOlBob3RvbWV0cmljSW50ZXJwcmV0YXRpb24+MjwvdGlmZjpQaG90b21ldHJpY0ludGVycHJldGF0aW9uPgogICAgICA8L3JkZjpEZXNjcmlwdGlvbj4KICAgPC9yZGY6UkRGPgo8L3g6eG1wbWV0YT4KlqhK0AAAAgFJREFUSA2tVLFOAkEQnTM2fAKddGIFhYnYCYmdjZ10hspALIwNoSMYE2MsDMSK0OEHmGhigqUWJEIF9hbwBxYU675x59hbDnJHnOSY2dm37+3s7EIU0xr1hoqzZCMOGOS5vRwVT4qxRCJpgFzNFH+9156KKrIZxl6rUmCHiUSDatWaD80f5CVW3ceuJ4NIHuRq1vQ/e+eogDKYi15JoAKQN+pNGgwHvJnnl1Rg595ui1S/TOLtSlJbXb+Aq2vyqwoI+AgdgLx0ekzT6ZjTyaM3mjzlmdz2O+mkxpWo3SG6vEgYirYSkdBbBHLcltF4wh/IezdpCvPAwCBye/djBNhxH7mU5n2wqTYqapze7jG03WkTjktXAPMI5NK0df1nv6TAM/keKesKcwVWD1osufJnqGcz+nN8lrL0rtM4LukJePQVpmAPsNA2GYvPmEl45GSsw/1cicZfBQaICB6j34PyGSqKUQWoIAIzgq2PCkkvCocs5gUrAFgW2bHk4A2ZWwHgUoUhR8o5ImRAABMyxJITchkLxnj0wjWuoHJOXusBp1WezwsZMiCAOYR/SfMrmEAyrAIbmAkhdUVkDGKNxzHZttgDIQVKFq/yDs49Jl9gfkx6hYgs8zYpYsEh1qYfnW/WQzM57FZMYtcvm5e85RcEcJf/0/ihOYT8H+Lk1hky9y+/gjOMDBKC9wAAAABJRU5ErkJggg=="/>
                        <div><u>D</u>ocuments...</div>
                    </div>
                    <div class="start-menu-item">
                        <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAYCAYAAADgdz34AAAAAXNSR0IArs4c6QAAAGhlWElmTU0AKgAAAAgABAEGAAMAAAABAAIAAAESAAMAAAABAAEAAAEoAAMAAAABAAIAAIdpAAQAAAABAAAAPgAAAAAAA6ABAAMAAAABAAEAAKACAAQAAAABAAAAGKADAAQAAAABAAAAGAAAAABgyvCWAAACC2lUWHRYTUw6Y29tLmFkb2JlLnhtcAAAAAAAPHg6eG1wbWV0YSB4bWxuczp4PSJhZG9iZTpuczptZXRhLyIgeDp4bXB0az0iWE1QIENvcmUgNi4wLjAiPgogICA8cmRmOlJERiB4bWxuczpyZGY9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkvMDIvMjItcmRmLXN5bnRheC1ucyMiPgogICAgICA8cmRmOkRlc2NyaXB0aW9uIHJkZjphYm91dD0iIgogICAgICAgICAgICB4bWxuczp0aWZmPSJodHRwOi8vbnMuYWRvYmUuY29tL3RpZmYvMS4wLyI+CiAgICAgICAgIDx0aWZmOlJlc29sdXRpb25Vbml0PjI8L3RpZmY6UmVzb2x1dGlvblVuaXQ+CiAgICAgICAgIDx0aWZmOk9yaWVudGF0aW9uPjE8L3RpZmY6T3JpZW50YXRpb24+CiAgICAgICAgIDx0aWZmOkNvbXByZXNzaW9uPjE8L3RpZmY6Q29tcHJlc3Npb24+CiAgICAgICAgIDx0aWZmOlBob3RvbWV0cmljSW50ZXJwcmV0YXRpb24+MjwvdGlmZjpQaG90b21ldHJpY0ludGVycHJldGF0aW9uPgogICAgICA8L3JkZjpEZXNjcmlwdGlvbj4KICAgPC9yZGY6UkRGPgo8L3g6eG1wbWV0YT4KlqhK0AAAAqdJREFUSA2lVb1r20AUfy4OpGOHgjUUmrGeakOGZGyge+nUdDIKgcYhQwmdTIbiNS0EO4UQ4an9E1IoxNmcwRB1StdCBwk62FsEGdT7vdM7dPLJGvpAeve+fu9LZ9cGJ4OU/oP6n/oU/45rZRB1GLrv3pbZl+p3dg+X2mHkBDjEcUS3vyK6+H4BkebzOfO75I65vMZXYwqnY2o0PFEt5SZB3uv483FetM5rT9csuUpwJkBQ9OdWx64+IkpmRBnvHvSqMC37A0tyCQoco/Me65EkSeLyKtWVdoCKAXr545K2Xm5xR72jJnkNot6R3hORXwoshvIEqnKMyXvSpOhvRL0PHp2fzfhjQHAUJzQ8batPVKDc3Jlg+822qrLJEbwL7EDR8MtX5q6X3yG+T8GIrDvhTPBw9Rt193T76ACkAOj1qxd8RvWT6wmfs1fa3SOlU9KIE5kklUu+mfqEB+T69m+mpOwafHOD3ayXlaD5zKPD9z6pNtV8A3ZsPW9ZAS4BlQO8vb5otRLkzUgC8PBnaJLl7XIenmpwHo8oc9wkwFLlwbzT+4EB73/MLl0uUI6wSZLBiWh5D7x0a8myWKkcHDosGknj+eIlg012tLkR8Hlyrce7f0CpSYCREGmD1AFwJBEAuc1ih/78TO8Io8QO/I6NYUYkQcJ1QuIxIQkIYwOocOkU4OIj8cJNB6IAB7hUja5qK/oeSEcCWFvZ5zDZF2La6wGP0+DhHy29n6XqNwdL4UctK8WjAlhW80/xKCDWgcNX9ODwRYxgZJxKR6QcFqqRysGLJIvN6fk218MwpJ1dHeB35NfRXpTso/gRiF51UCQGh7IejAIjiNegxa2ymIGID0aQJ9Yrn1TFOEkCi8Y8kPHBrMWxkBhqsRl/KC0BigoSEHGrjP8Hen4qZvFHu1YAAAAASUVORK5CYII=" />
                        <div><u>S</u>ettings...</div>
                    </div>
                    <div class="start-menu-item">
                        <img src="data:image/png;base64,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"/>
                        <div><u>F</u>ind...</div>
                    </div>
                    <div class="start-menu-item">
                        <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABcAAAAWCAYAAAArdgcFAAAAAXNSR0IArs4c6QAAAGhlWElmTU0AKgAAAAgABAEGAAMAAAABAAIAAAESAAMAAAABAAEAAAEoAAMAAAABAAIAAIdpAAQAAAABAAAAPgAAAAAAA6ABAAMAAAABAAEAAKACAAQAAAABAAAAF6ADAAQAAAABAAAAFgAAAAAZeH0iAAACC2lUWHRYTUw6Y29tLmFkb2JlLnhtcAAAAAAAPHg6eG1wbWV0YSB4bWxuczp4PSJhZG9iZTpuczptZXRhLyIgeDp4bXB0az0iWE1QIENvcmUgNi4wLjAiPgogICA8cmRmOlJERiB4bWxuczpyZGY9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkvMDIvMjItcmRmLXN5bnRheC1ucyMiPgogICAgICA8cmRmOkRlc2NyaXB0aW9uIHJkZjphYm91dD0iIgogICAgICAgICAgICB4bWxuczp0aWZmPSJodHRwOi8vbnMuYWRvYmUuY29tL3RpZmYvMS4wLyI+CiAgICAgICAgIDx0aWZmOlJlc29sdXRpb25Vbml0PjI8L3RpZmY6UmVzb2x1dGlvblVuaXQ+CiAgICAgICAgIDx0aWZmOk9yaWVudGF0aW9uPjE8L3RpZmY6T3JpZW50YXRpb24+CiAgICAgICAgIDx0aWZmOkNvbXByZXNzaW9uPjE8L3RpZmY6Q29tcHJlc3Npb24+CiAgICAgICAgIDx0aWZmOlBob3RvbWV0cmljSW50ZXJwcmV0YXRpb24+MjwvdGlmZjpQaG90b21ldHJpY0ludGVycHJldGF0aW9uPgogICAgICA8L3JkZjpEZXNjcmlwdGlvbj4KICAgPC9yZGY6UkRGPgo8L3g6eG1wbWV0YT4KlqhK0AAAAlNJREFUOBGdlbFO3EAQhn9QCspLh8vrcCocKY1LirzAVYCEhKyk4KKTIkoQFXkBC4cm6KRIUarkAa6gdAok+yqcjtJ0pAOJwsw/9i4+zj5MZiSvvZ79/tnZXRt4gR3goHDhFi8Y0i2U4CIsigRJESDoJLLUBU3wcXiMdJRqeIxY2xSp3MXIkDVyGjvrgk1gH75CGZeLX4s3iSyE18HxegTfE5onmNSHJA1M2fEowPszcTHltsLrYOxG8PZk0DrHVTYFoj+ulMrHqrgxzoJGkUb4DNiMEoFobB6AbxelWPRRBMbzAoQvP4aXd41gvhp7qHv0IXg6VJ+ZuSnNq3pEG1h3h2Q+3MtmSpOezmZtwMLBF3ELbwNTfHjxSaGExV/LdFgKWr3ezHhrcwv4WcYovAnMbLnlaOm7BFLxckR1JdQR51akMVMFV++lKZYJ5vPh6NB2W3C4De/+LcBWnEDTPgUHuwGcVccyeLNE+DV+wwuHyEdlFgMM7CHhKTRGMDNtAvf7fQ27PbrVWZBd7ZZy+huTDTihg1/iZrom0+fAvV4PdTCV7IKqrFzcNRfO9zvk/1bsTEympmUsa8xSMGOCOWv2idmzU8H5IfLwxq1qVrWXazmyv5n9YHEkjZD9z/sKdnp3SHbmwYxTFbOo23iNfFITYYRYnMp3b5rh6uhKD8hJeAJCacnOzVzG+kIudgrseE7kMitn0gVM3gycHbRFIhSgnb8/b81YA+TSCDcvjchANt/NxNU1IbwLmIyFcCPC3xoPENfkB9prbOL/q6WIDOz8g34A2uUn1chDuZ8AAAAASUVORK5CYII="/>
                        <div><u>H</u>elp...</div><!-- me... -->
                    </div>
                    <div class="start-menu-item">
                        <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAXCAYAAAARIY8tAAAAAXNSR0IArs4c6QAAAGhlWElmTU0AKgAAAAgABAEGAAMAAAABAAIAAAESAAMAAAABAAEAAAEoAAMAAAABAAIAAIdpAAQAAAABAAAAPgAAAAAAA6ABAAMAAAABAAEAAKACAAQAAAABAAAAGKADAAQAAAABAAAAFwAAAADimmdHAAACC2lUWHRYTUw6Y29tLmFkb2JlLnhtcAAAAAAAPHg6eG1wbWV0YSB4bWxuczp4PSJhZG9iZTpuczptZXRhLyIgeDp4bXB0az0iWE1QIENvcmUgNi4wLjAiPgogICA8cmRmOlJERiB4bWxuczpyZGY9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkvMDIvMjItcmRmLXN5bnRheC1ucyMiPgogICAgICA8cmRmOkRlc2NyaXB0aW9uIHJkZjphYm91dD0iIgogICAgICAgICAgICB4bWxuczp0aWZmPSJodHRwOi8vbnMuYWRvYmUuY29tL3RpZmYvMS4wLyI+CiAgICAgICAgIDx0aWZmOlJlc29sdXRpb25Vbml0PjI8L3RpZmY6UmVzb2x1dGlvblVuaXQ+CiAgICAgICAgIDx0aWZmOk9yaWVudGF0aW9uPjE8L3RpZmY6T3JpZW50YXRpb24+CiAgICAgICAgIDx0aWZmOkNvbXByZXNzaW9uPjE8L3RpZmY6Q29tcHJlc3Npb24+CiAgICAgICAgIDx0aWZmOlBob3RvbWV0cmljSW50ZXJwcmV0YXRpb24+MjwvdGlmZjpQaG90b21ldHJpY0ludGVycHJldGF0aW9uPgogICAgICA8L3JkZjpEZXNjcmlwdGlvbj4KICAgPC9yZGY6UkRGPgo8L3g6eG1wbWV0YT4KlqhK0AAAAmVJREFUSA2lVT1o21AQ/lxc6OgOBWno0K3OZBUKTTc70KGrpqZT6hAINV7apcR0CDKBjsYmEOJ4SyelW4eA2y0pFKJMdjYNHmToYI+BDurd6ceyLcm1c/D07t27++697917yiBGjH3DjTEvbap9riGbFLX+Yj1pail7YgJG2Xj1YyGYM3gL9fEanD8O1EcqnEFPxt3zrsTeW4iwwIHBWRhcen8sA/qk7qB7Xgr8Uvp0n9QEa3lvVSnoiVPtzpnMZfeAuYqx6fTtmFCD+FWU5ZLKDvQCoP1uAoeEelIRaMtPYF57ytAft57bcK5N6A0d2u4T3wrU7j+EsZUHji5CGyvZOpAZamUXOz6kVp5ygAa0O22pDp54+Y6/OsyqSQk+8gBg8AZgnfTZfUrCMzC+GFByCoZjb609q4fx0IIzfgB0vBimR6nm0CoE+/PsNeqMKmBSn5jAcwUYOE4Y3Dq0cUF0MkVqQQ/dSlzzNxswLKJoRsIdBPbTr6eBitfF6QDmXNvlaZ8a37NUfAYUR2FcVJEExHGGjC7TdHx0jO2dbWy+2UT/po9KtQL37yS4ftAK4/c+vRc9zhY6RZXyVtmlK+9yT1edy9cl8JWa/2C680/F7UhWH018F33uDBiMqck/9fiPbv8uiSD0DHpEhyv0MEXNRlNoIuCVe6GIwY39D+EzcPnrUhar5m5BSYKFcyEs3WbOIIf6Ad1tkmi5imHFz1QCBrdtG/yrY/n+s78i7CSMtyz8j8aTWp9Me9rZN3l6xXd2buGYn+urAtU7Hag01qldsd1v9PwFh7wQb9aBV8XB/ytL7+Ifpy4a5wuLfiYAAAAASUVORK5CYII="/>
                        <div><u>R</u>un...</div>
                    </div>
                    <div class="start-menu-div"></div>
                    <div class="start-menu-item">
                        <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABcAAAAYCAYAAAARfGZ1AAAAAXNSR0IArs4c6QAAAGhlWElmTU0AKgAAAAgABAEGAAMAAAABAAIAAAESAAMAAAABAAEAAAEoAAMAAAABAAIAAIdpAAQAAAABAAAAPgAAAAAAA6ABAAMAAAABAAEAAKACAAQAAAABAAAAF6ADAAQAAAABAAAAGAAAAACmSMNDAAACC2lUWHRYTUw6Y29tLmFkb2JlLnhtcAAAAAAAPHg6eG1wbWV0YSB4bWxuczp4PSJhZG9iZTpuczptZXRhLyIgeDp4bXB0az0iWE1QIENvcmUgNi4wLjAiPgogICA8cmRmOlJERiB4bWxuczpyZGY9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkvMDIvMjItcmRmLXN5bnRheC1ucyMiPgogICAgICA8cmRmOkRlc2NyaXB0aW9uIHJkZjphYm91dD0iIgogICAgICAgICAgICB4bWxuczp0aWZmPSJodHRwOi8vbnMuYWRvYmUuY29tL3RpZmYvMS4wLyI+CiAgICAgICAgIDx0aWZmOlJlc29sdXRpb25Vbml0PjI8L3RpZmY6UmVzb2x1dGlvblVuaXQ+CiAgICAgICAgIDx0aWZmOk9yaWVudGF0aW9uPjE8L3RpZmY6T3JpZW50YXRpb24+CiAgICAgICAgIDx0aWZmOkNvbXByZXNzaW9uPjE8L3RpZmY6Q29tcHJlc3Npb24+CiAgICAgICAgIDx0aWZmOlBob3RvbWV0cmljSW50ZXJwcmV0YXRpb24+MjwvdGlmZjpQaG90b21ldHJpY0ludGVycHJldGF0aW9uPgogICAgICA8L3JkZjpEZXNjcmlwdGlvbj4KICAgPC9yZGY6UkRGPgo8L3g6eG1wbWV0YT4KlqhK0AAAAfZJREFUSA2tVLFOAkEQfWcooCCh9BfolMRCWhI/QEsre2NiqAyEgpyxJ/6CJRYUmJgQOy1MgI5fMLGgoMDEYp03xxx3eBycMsnezs7uvnnzdveADOa3fSfL2XZrBJ5+Tl23191tAgOez+aObfA82E2C+nU9BDRZmODfFRAsxrRTdmAT3WPxrCfwC5gHSeDvRf/XBAZMdvSHKGujj4uA+fBdb41WkEmiKDgleMC+Ey00AccEdlKBJeABJx3y3ia5ZBPO8YERyqhgQmz0n3yMxkDlCOB89bi6CWY5H2VOxktWWgBD0hoaz3ywBCcgUbiZYEtdGQ4SbgJOleWx10WhmMd89oXJeKISAF4oRf+lj9pJjSV7y7rTPWUmS0KGVgmZsoJNjA0+lrFxA3d7BwiYzaPZaqovoCjlS2E8E2MCy07H5052vGpsFufcSgsTpToEIBA3UwIDtn6RIBUjaTLHjX47PtVsAWenwOEB9D4v5pl8KxNpA7mNdZIE0ZdoVWzTCwMlkjMqfHE0uQnaF4oF7S1uvQYTPq9vkJcKsL/vAJdXcApuGymFgQrrmHFT1AyIMfq0aAKOQ+Yc0FZBg6gyMVf7Bbs037N7zj+c2mp2BqVEmq3VgXyoq8USfXv+Hv9wUWArdQ0wExjwWj+6gIuSrtvqGq7byn4A6VDNoc+VaIsAAAAASUVORK5CYII="/>
                        <div><u>L</u>og Off heyjoeway...</div>
                    </div>
                    <div class="start-menu-item">
                        <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAYCAYAAADgdz34AAAAAXNSR0IArs4c6QAAAGhlWElmTU0AKgAAAAgABAEGAAMAAAABAAIAAAESAAMAAAABAAEAAAEoAAMAAAABAAIAAIdpAAQAAAABAAAAPgAAAAAAA6ABAAMAAAABAAEAAKACAAQAAAABAAAAGKADAAQAAAABAAAAGAAAAABgyvCWAAACC2lUWHRYTUw6Y29tLmFkb2JlLnhtcAAAAAAAPHg6eG1wbWV0YSB4bWxuczp4PSJhZG9iZTpuczptZXRhLyIgeDp4bXB0az0iWE1QIENvcmUgNi4wLjAiPgogICA8cmRmOlJERiB4bWxuczpyZGY9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkvMDIvMjItcmRmLXN5bnRheC1ucyMiPgogICAgICA8cmRmOkRlc2NyaXB0aW9uIHJkZjphYm91dD0iIgogICAgICAgICAgICB4bWxuczp0aWZmPSJodHRwOi8vbnMuYWRvYmUuY29tL3RpZmYvMS4wLyI+CiAgICAgICAgIDx0aWZmOlJlc29sdXRpb25Vbml0PjI8L3RpZmY6UmVzb2x1dGlvblVuaXQ+CiAgICAgICAgIDx0aWZmOk9yaWVudGF0aW9uPjE8L3RpZmY6T3JpZW50YXRpb24+CiAgICAgICAgIDx0aWZmOkNvbXByZXNzaW9uPjE8L3RpZmY6Q29tcHJlc3Npb24+CiAgICAgICAgIDx0aWZmOlBob3RvbWV0cmljSW50ZXJwcmV0YXRpb24+MjwvdGlmZjpQaG90b21ldHJpY0ludGVycHJldGF0aW9uPgogICAgICA8L3JkZjpEZXNjcmlwdGlvbj4KICAgPC9yZGY6UkRGPgo8L3g6eG1wbWV0YT4KlqhK0AAAArNJREFUSA2dVTFr20AUfioJKJu0xZu1VZ3arfaWGAxNpsRT6zHQKRSCOxoPwavJLzD5BXW3BAq1N7lQSDNV3WTI4NHaIsjg3vekJ51sS057IN27e+993333dCeDNrT+ZX+pT3d7XUMf/4udSxTg2ttaDuPm9obHg6tBLj4XVDDgBAF2X7vkVBwOXSwWZNs2oUcLo5C8icf2plcRuQHwzkUnzQlmAUVRlI5h6CTz2ZyCIGB//aBOlmmxXaRyh73qhRVSpFbN8SZZlsNzABQlDFYlqlQrhHn/3ud0bOnRuyOB4vqJopQA4GcfP1O9VickvHLjeIAB2P8Tg5HaMSwG8zSLY6Y/pmwIEW/nvbecTqbGizgkfge3Fer2HqnRHNPwekS//TmrCsOA3JcuP1Aj28IkKtWy4m1qNBsMBHXHB8ewl5kC02anSy3uu70vqh9T/3KPFdl2RKZpUmXfVER18qZeqgRbJXVKlTIKUaZAbZHeQIRHFKGIfqCAVKkAgq3ESvGUtUyBFuXTm3j0ROTuxmas6I46Fx61P7RZgZZSaGYK9BAFLA1kTPjUZ0WDK1Ncz+ozgqQGnIVVK5JHOQ+s5FcKKPudTpQYGYFeAyhQJKa5x0Sw020rAdvkygg0r7sbr9YgdWaSGriUKdBCt5o5Ap/21Urxeari6oBK0f8q4K9oeD2k1vsWzR/afLgazYQkWb2o2LpcLUDqxATjyZgvMMdxqHVyuE6UHD4tv9TEZajuIsQYO/IzOT05XeImhRNEOEh3P1t8QkVRKWri1MGZYTUJRJhzqk5KhDEk445C+/7tkHu5FsIwZH+yavjSH9PaSR59HbFzVREuOwFm9OJXCo6QNQLJKyOSmOf0hQSSXEQkfvTyxehzYufkyGRZv1ojxJ5/OpeUNby1CYnc1guRUojQQpy/wOk3XGsAFI4AAAAASUVORK5CYII=" />
                        <div>Sh<u>u</u>t Down...</div>
                    </div>
                </div>
            </div>
            <div class="divider"></div>
            <div class="grabbable"></div>
            <div class="float-right"></div>
            <div id="quick-launch">
                <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAAAAXNSR0IArs4c6QAAAGhlWElmTU0AKgAAAAgABAEGAAMAAAABAAIAAAESAAMAAAABAAEAAAEoAAMAAAABAAIAAIdpAAQAAAABAAAAPgAAAAAAA6ABAAMAAAABAAEAAKACAAQAAAABAAAAEKADAAQAAAABAAAAEAAAAAC2qvTJAAACC2lUWHRYTUw6Y29tLmFkb2JlLnhtcAAAAAAAPHg6eG1wbWV0YSB4bWxuczp4PSJhZG9iZTpuczptZXRhLyIgeDp4bXB0az0iWE1QIENvcmUgNi4wLjAiPgogICA8cmRmOlJERiB4bWxuczpyZGY9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkvMDIvMjItcmRmLXN5bnRheC1ucyMiPgogICAgICA8cmRmOkRlc2NyaXB0aW9uIHJkZjphYm91dD0iIgogICAgICAgICAgICB4bWxuczp0aWZmPSJodHRwOi8vbnMuYWRvYmUuY29tL3RpZmYvMS4wLyI+CiAgICAgICAgIDx0aWZmOlJlc29sdXRpb25Vbml0PjI8L3RpZmY6UmVzb2x1dGlvblVuaXQ+CiAgICAgICAgIDx0aWZmOk9yaWVudGF0aW9uPjE8L3RpZmY6T3JpZW50YXRpb24+CiAgICAgICAgIDx0aWZmOkNvbXByZXNzaW9uPjE8L3RpZmY6Q29tcHJlc3Npb24+CiAgICAgICAgIDx0aWZmOlBob3RvbWV0cmljSW50ZXJwcmV0YXRpb24+MjwvdGlmZjpQaG90b21ldHJpY0ludGVycHJldGF0aW9uPgogICAgICA8L3JkZjpEZXNjcmlwdGlvbj4KICAgPC9yZGY6UkRGPgo8L3g6eG1wbWV0YT4KlqhK0AAAAWxJREFUOBGVkrFKA0EQhv8LCr5GynQ5u1xnCkFLU4kghFSalMHKJ5BUx0ZLQbDMC9jYXRPYs0vpK6QUUozz797eXiREsrDZ2dn9/vl3LsCBQy4uxXYhB2L+us0hklsxiAJH0MSWWllgcfazleKmvZ4i7QHz51NMdL94m8ngdqqRCoyWIk5oaMQujchGqmnd6ipvjJihq1zfVVqL0wHnTtiKg5eo4Y7ecwV1jQI7YJOrG765UZm2ZWOFIizoBfbBjcoB5hM5nQif4A/im1mZPTD5qLbdhOmAe95zDqKAfp4KpgAPQzMZ++Z6mHEQaOmhjhLTh3eM78Z+q78Kuzg5TugSaTdD+VWg3TnB9yp+5koAmD3dIDvPagEGAb667juYOcIUCaM1WPdDjOJjXovsgykyLz3mHCQvtYYT+Q9+/Gw4IDrqpWiKaJOwyzYrE87uY6+S6g/hLaQZDIpo508UbIf06nWCRDe+3SF74PoLXDxyVG+ayhYAAAAASUVORK5CYII=" />
                <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAAAAXNSR0IArs4c6QAAAGhlWElmTU0AKgAAAAgABAEGAAMAAAABAAIAAAESAAMAAAABAAEAAAEoAAMAAAABAAIAAIdpAAQAAAABAAAAPgAAAAAAA6ABAAMAAAABAAEAAKACAAQAAAABAAAAEKADAAQAAAABAAAAEAAAAAC2qvTJAAACC2lUWHRYTUw6Y29tLmFkb2JlLnhtcAAAAAAAPHg6eG1wbWV0YSB4bWxuczp4PSJhZG9iZTpuczptZXRhLyIgeDp4bXB0az0iWE1QIENvcmUgNi4wLjAiPgogICA8cmRmOlJERiB4bWxuczpyZGY9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkvMDIvMjItcmRmLXN5bnRheC1ucyMiPgogICAgICA8cmRmOkRlc2NyaXB0aW9uIHJkZjphYm91dD0iIgogICAgICAgICAgICB4bWxuczp0aWZmPSJodHRwOi8vbnMuYWRvYmUuY29tL3RpZmYvMS4wLyI+CiAgICAgICAgIDx0aWZmOlJlc29sdXRpb25Vbml0PjI8L3RpZmY6UmVzb2x1dGlvblVuaXQ+CiAgICAgICAgIDx0aWZmOk9yaWVudGF0aW9uPjE8L3RpZmY6T3JpZW50YXRpb24+CiAgICAgICAgIDx0aWZmOkNvbXByZXNzaW9uPjE8L3RpZmY6Q29tcHJlc3Npb24+CiAgICAgICAgIDx0aWZmOlBob3RvbWV0cmljSW50ZXJwcmV0YXRpb24+MjwvdGlmZjpQaG90b21ldHJpY0ludGVycHJldGF0aW9uPgogICAgICA8L3JkZjpEZXNjcmlwdGlvbj4KICAgPC9yZGY6UkRGPgo8L3g6eG1wbWV0YT4KlqhK0AAAAa9JREFUOBGVUz1PAkEQfWeusdNOSjrXirOTUn4CiYlQAYmJQmNIrCytqAEbkJJfgeXZsXTb2kEH/+B8sx/nHYmFk9zd7My8N197Ef4jnXVWCl9cR1HJUDwcBwcfQUEFY+L8EBQPVEiCxX0TDWNtrMKTSMwvG8NUbZ0Z4np8khtgMHVYxbOAFTyJ1ggkOYGAgRT1LtC6VGgszy1aMVZEiPGUoFcD5u/UPcmJOJ048OyRmZe3wYjxaG8fIVJf2jbRY0wQSyDZ+12NGcu+eugHH1b3+1wXInwwMS3zDV8JS+K8bAvD52HWblUxmdbZhIjUWxAOUMQNsWBnG3EAg+WxCXqFImGwA9nwXM2VnMWtkeC2nrnBFJMXd55Dykq83W2RVk9pFXbXgGSXHZtyrF2z7d3bDSawQ5zoPoxOYTZb8tQJdkQypMBh1yyDOxK3RiZfjRQz7OgmmCQgu72NJFGdLCtmFg7JjsUgiisXFWhf63jUQvOuKX5U8MlZCokE8w74zVigBBAsH/tyVzjl3iUcaLwYnH2/4nB4Y1WsJmF71sOXB4bj0VV2ZrMp/HEh8o/vD0C/nbmThhdLAAAAAElFTkSuQmCC" />
                <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAOCAYAAAAmL5yKAAAAAXNSR0IArs4c6QAAAGhlWElmTU0AKgAAAAgABAEGAAMAAAABAAIAAAESAAMAAAABAAEAAAEoAAMAAAABAAIAAIdpAAQAAAABAAAAPgAAAAAAA6ABAAMAAAABAAEAAKACAAQAAAABAAAAEKADAAQAAAABAAAADgAAAABpet0qAAACC2lUWHRYTUw6Y29tLmFkb2JlLnhtcAAAAAAAPHg6eG1wbWV0YSB4bWxuczp4PSJhZG9iZTpuczptZXRhLyIgeDp4bXB0az0iWE1QIENvcmUgNi4wLjAiPgogICA8cmRmOlJERiB4bWxuczpyZGY9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkvMDIvMjItcmRmLXN5bnRheC1ucyMiPgogICAgICA8cmRmOkRlc2NyaXB0aW9uIHJkZjphYm91dD0iIgogICAgICAgICAgICB4bWxuczp0aWZmPSJodHRwOi8vbnMuYWRvYmUuY29tL3RpZmYvMS4wLyI+CiAgICAgICAgIDx0aWZmOlJlc29sdXRpb25Vbml0PjI8L3RpZmY6UmVzb2x1dGlvblVuaXQ+CiAgICAgICAgIDx0aWZmOk9yaWVudGF0aW9uPjE8L3RpZmY6T3JpZW50YXRpb24+CiAgICAgICAgIDx0aWZmOkNvbXByZXNzaW9uPjE8L3RpZmY6Q29tcHJlc3Npb24+CiAgICAgICAgIDx0aWZmOlBob3RvbWV0cmljSW50ZXJwcmV0YXRpb24+MjwvdGlmZjpQaG90b21ldHJpY0ludGVycHJldGF0aW9uPgogICAgICA8L3JkZjpEZXNjcmlwdGlvbj4KICAgPC9yZGY6UkRGPgo8L3g6eG1wbWV0YT4KlqhK0AAAAHdJREFUKBVjrK6s/s9AAWAB6XVydCLZiH379zG0trcygA0A6XZ2I82M6kqIergBuLT//+3EwMjKyPD/938UmoGhGqyFERQGIC+AnEQqQPFCS1MLSfpr6mrA6plI0oVF8agBDAwUhwE4IYHSADnpABQpjEBMUWYCAGXDINJcMqgDAAAAAElFTkSuQmCC" />
            </div>
            <div class="divider"></div>
            <div class="grabbable"></div>
            <div class="float-clear"></div>
        </div>
        <div class="taskbar-section right">
            <div class="divider"></div>
            <div class="taskbar-section" id="tray">
                <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAAAAXNSR0IArs4c6QAAAGhlWElmTU0AKgAAAAgABAEGAAMAAAABAAIAAAESAAMAAAABAAEAAAEoAAMAAAABAAIAAIdpAAQAAAABAAAAPgAAAAAAA6ABAAMAAAABAAEAAKACAAQAAAABAAAAEKADAAQAAAABAAAAEAAAAAC2qvTJAAACC2lUWHRYTUw6Y29tLmFkb2JlLnhtcAAAAAAAPHg6eG1wbWV0YSB4bWxuczp4PSJhZG9iZTpuczptZXRhLyIgeDp4bXB0az0iWE1QIENvcmUgNi4wLjAiPgogICA8cmRmOlJERiB4bWxuczpyZGY9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkvMDIvMjItcmRmLXN5bnRheC1ucyMiPgogICAgICA8cmRmOkRlc2NyaXB0aW9uIHJkZjphYm91dD0iIgogICAgICAgICAgICB4bWxuczp0aWZmPSJodHRwOi8vbnMuYWRvYmUuY29tL3RpZmYvMS4wLyI+CiAgICAgICAgIDx0aWZmOlJlc29sdXRpb25Vbml0PjI8L3RpZmY6UmVzb2x1dGlvblVuaXQ+CiAgICAgICAgIDx0aWZmOk9yaWVudGF0aW9uPjE8L3RpZmY6T3JpZW50YXRpb24+CiAgICAgICAgIDx0aWZmOkNvbXByZXNzaW9uPjE8L3RpZmY6Q29tcHJlc3Npb24+CiAgICAgICAgIDx0aWZmOlBob3RvbWV0cmljSW50ZXJwcmV0YXRpb24+MjwvdGlmZjpQaG90b21ldHJpY0ludGVycHJldGF0aW9uPgogICAgICA8L3JkZjpEZXNjcmlwdGlvbj4KICAgPC9yZGY6UkRGPgo8L3g6eG1wbWV0YT4KlqhK0AAAARBJREFUOBF9UlEWwiAMKz4v5jzWph9uHGt4tNlkZHTKk/egbWigKaTxMW5WR55zijFgYNrvWRKW18K9lJJt235eeRe7D3fzA3s8Yjj8Cs95Tmx5iNeyx3lu+NnLDC9YI7kXA1vL4Gs+LDAMHoAb44jx+DCXYQZJkCOrfEroVVDee4r6IwLs9JxiaFDP6Q08/IgBj6O+FHINFfAlhhs0oh/E6WuZoiaB1VLCF3YKRV4CGgWwiWHv5Ips+AuoTNPj+jv2cqFpLWuUSf+g1R1/j5ZT+/a3ApUTu55SFOANRFLtqvKbnbNRe6ex+L7x+0DLz4QETpeIgYtkgVdOu7Dn6RDPVgt5qMixih5fGG77HuR+AKjHxVyo5XeTAAAAAElFTkSuQmCC" />
                <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAAAAXNSR0IArs4c6QAAAGhlWElmTU0AKgAAAAgABAEGAAMAAAABAAIAAAESAAMAAAABAAEAAAEoAAMAAAABAAIAAIdpAAQAAAABAAAAPgAAAAAAA6ABAAMAAAABAAEAAKACAAQAAAABAAAAEKADAAQAAAABAAAAEAAAAAC2qvTJAAACC2lUWHRYTUw6Y29tLmFkb2JlLnhtcAAAAAAAPHg6eG1wbWV0YSB4bWxuczp4PSJhZG9iZTpuczptZXRhLyIgeDp4bXB0az0iWE1QIENvcmUgNi4wLjAiPgogICA8cmRmOlJERiB4bWxuczpyZGY9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkvMDIvMjItcmRmLXN5bnRheC1ucyMiPgogICAgICA8cmRmOkRlc2NyaXB0aW9uIHJkZjphYm91dD0iIgogICAgICAgICAgICB4bWxuczp0aWZmPSJodHRwOi8vbnMuYWRvYmUuY29tL3RpZmYvMS4wLyI+CiAgICAgICAgIDx0aWZmOlJlc29sdXRpb25Vbml0PjI8L3RpZmY6UmVzb2x1dGlvblVuaXQ+CiAgICAgICAgIDx0aWZmOk9yaWVudGF0aW9uPjE8L3RpZmY6T3JpZW50YXRpb24+CiAgICAgICAgIDx0aWZmOkNvbXByZXNzaW9uPjE8L3RpZmY6Q29tcHJlc3Npb24+CiAgICAgICAgIDx0aWZmOlBob3RvbWV0cmljSW50ZXJwcmV0YXRpb24+MjwvdGlmZjpQaG90b21ldHJpY0ludGVycHJldGF0aW9uPgogICAgICA8L3JkZjpEZXNjcmlwdGlvbj4KICAgPC9yZGY6UkRGPgo8L3g6eG1wbWV0YT4KlqhK0AAAAN9JREFUOBGVklESgzAIRJNOb23th5pjaY+W8jAYJjW2ZSaySHaBISFcW5Y0p2u3XmYYQx7GQdPiL0U+NCDnrJX/I6JkZKpaZVE7sFWznMXqjQxBfuR1W4FqnuDxHSZE/DLxBUbAqUFOc6oX9qrZVWP+vQNRUMzHV/XKZQsmiK8dyAghRst5WsU6Qg2NvPvttdVUQWedSHu6cxovLR8rLHF/BDqIaYaQtMYy1TEY4ZvZS4SFUHg8ofTnPhuhLXKMxGUzT/S4JVusIhLoenlQLamNjej9IfLLZU/0mH1yuvYGBKHAc7PE6CUAAAAASUVORK5CYII=" />
                <div id="tray-clock">10:36 PM</div>
            </div>
        </div>
    </div>
</div>
</foreignObject>
</svg>
