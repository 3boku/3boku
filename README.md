<div style="text-align: center">
    <img
        align="center"
        src="https://capsule-render.vercel.app/api?type=waving&text=Hello%20World!&&color=timeGradient&&animation=twinkling&height=200&fontSize=60"
    />
    <h1 id="dynamic" class="lg-text"></ㅗ>
    <h1 class="sm-text"></h1>

    <img
        src="https://media.tenor.com/TCMWkxIkF9IAAAAC/dancing-gopher.gif"
        alt="고퍼 댄싱"
    />

<pre><code>
    type sambok struct {
        GitHub        GitHub
        Email         Email
        Twitter       Twitter
        Discord       Discord
        Instargram    Instargram
        TechStack     []Technology
        Career        []Career
       }
       
       func (s *sambok) NewSambok() *sambok {
        return *sambok{
         GitHub:    GitHub{"3boku"},
         Email:     Email{"a24746440@gmail.com"},
         Twitter:   Twitter{"3boku__"},
         Discord:   Discord{"3boku__"},
         Instargram : Instargram{"phenomenon._.7"},
         
         TechStack: []Technology{
                 "Go", "Swift", "Python", "Node.js", "Flutter",
                 "HTML", "CSS", "JavaScript", "Unity", "Firebase",
                 "AWS", "Azure", "GCP", "Git", "GitHub",
             },
         Career: []Career{
                 "Seoul Robotics HighSchool Admission",
                 "Digital Sassac Doit Web Project DevOps Work",
                 "HJ Studio's Game 'Rache' UI Work and PD",
                 "SPAM's Speedat Web Site Backend work and PM",
                 "KSDC Lead Organizer",
                 "Google I/O Extended 2023 Incheon Staff",
                 "Flutter MeetUp - In Songdo Staff",
         }
        },
       }
</code></pre>

<img 
    align="center"
    src="https://github-readme-stats.vercel.app/api?username=3boku&show_icons=true&theme=radical"
/>

<h2>How to reach me📫</h2>

</div>
<ul>
    <li>Instargram: https://instagram.com/phenomenon._.7</li>
    <li>Discord: https://discord.com/users/406398616643698689</li>
    <li>e-mail: a24746440@gmail.com</li>
</ul>

<script>
    let target = document.querySelector("#dynamic");

    function randomString() {
        let stringArr = ["Hi There!👋", "はじめまして！👋", "안녕하세요!👋"];
        let selectString =
            stringArr[Math.floor(Math.random() * stringArr.length)];
        let selectStringArr = selectString.split("");

        return selectStringArr;
    }

    //타이핑 리셋
    function resetTyping() {
        target.textContent = "";
        dynamic(randomString());
    }

    //텍스트 한글자 씩 출력 함수
    function dynamic(randomArr) {
        if (randomArr.length > 0) {
            target.textContent += randomArr.shift();
            setTimeout(function () {
                dynamic(randomArr);
            }, 80);
        } else {
            setTimeout(resetTyping, 3000);
        }
    }

    //randomString 옆에 소괄호 까먹지 말기(없으면 작동 안됨)
    dynamic(randomString());
    //커서 깜빡임 효과
    function blink() {
        target.classList.toggle("active");
    }
    setInterval(blink, 500);

    const getToken = () => {
        let cookieName = document.cookie
            .split("; ")
            .find((row) => row.startsWith("token="))
            ?.split("=")[1];
        return cookieName;
    };

    const updateLoginButton = (isLoggedIn) => {
        const navBtn = document.querySelector("#login-btn");
        const link = navBtn.querySelector("a");

        if (isLoggedIn) {
            link.href = "/auth/api/logout";
            link.textContent = "logout";
        } else {
            link.href = "/auth/login";
            link.textContent = "login";
        }
    };

    const getName = (token) => {
        const target = document.querySelector(".sm-text");

        if (!token) {
            target.textContent = "Do IT! WEB Project | anonymous";
            return;
        }
        const base64 = token
            .split(".")[1]
            .replace(/-/g, "+")
            .replace(/_/g, "/");
        const name = JSON.parse(
            decodeURIComponent(escape(window.atob(base64)))
        ).name;
        target.textContent = `Do IT! WEB Project | ${
            name ? name : "anonymous"
        }`;
    };

    window.onload = function () {
        const token = getToken();
        updateLoginButton(!!token);
        getName(token);
    };

    const link = document.querySelector("a");

    // link.addEventListener("click", (event) => {
    //     event.preventDefault(); // 기본 동작 중지

    //     // 링크 가져오기
    //     const href = link.getAttribute("href");

    //     // 페이지 이동
    //     window.location.href = href;
    // });
</script>
