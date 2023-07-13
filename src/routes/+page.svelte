<script>
    import "../app.css";
    import Menu from "./components/menu.svelte"
    import StarBackground from "./components/startbackground.svelte"
    import { onMount } from "svelte";
    import { loadFull } from "tsparticles";

    let ParticlesComponent;

    onMount(async () => {
        const module = await import("svelte-particles");

        ParticlesComponent = module.default;
    });

    let particlesUrl = "http://foo.bar/particles.json"; // placeholder, replace it with a real url

    let particlesConfig = {
  "autoPlay": true,
  "background": {
    "color": {
      "value": "#000"
    },
    "image": "",
    "position": "",
    "repeat": "",
    "size": "",
    "opacity": 1
  },
  "backgroundMask": {
    "composite": "destination-out",
    "cover": {
      "color": {
        "value": "#fff"
      },
      "opacity": 1
    },
    "enable": false
  },
  "defaultThemes": {},
  "delay": 0,
  "fullScreen": {
    "enable": true,
    "zIndex": 1
  },
  "detectRetina": true,
  "duration": 0,
  "fpsLimit": 120,
  "interactivity": {
    "detectsOn": "window",
    "events": {
      "onClick": {
        "enable": true,
        "mode": "push"
      },
      "onDiv": {
        "selectors": [],
        "enable": false,
        "mode": [],
        "type": "circle"
      },
      "onHover": {
        "enable": true,
        "mode": "repulse",
        "parallax": {
          "enable": false,
          "force": 2,
          "smooth": 10
        }
      },
      "resize": {
        "delay": 0.5,
        "enable": true
      }
    },
    "modes": {
      "attract": {
        "distance": 200,
        "duration": 0.4,
        "easing": "ease-out-quad",
        "factor": 1,
        "maxSpeed": 50,
        "speed": 1
      },
      "bounce": {
        "distance": 200
      },
      "bubble": {
        "distance": 200,
        "duration": 0.4,
        "mix": false,
        "divs": {
          "distance": 200,
          "duration": 0.4,
          "mix": false,
          "selectors": []
        }
      },
      "connect": {
        "distance": 80,
        "links": {
          "opacity": 0.5
        },
        "radius": 60
      },
      "grab": {
        "distance": 100,
        "links": {
          "blink": false,
          "consent": false,
          "opacity": 1
        }
      },
      "push": {
        "default": true,
        "groups": [],
        "quantity": 4
      },
      "remove": {
        "quantity": 2
      },
      "repulse": {
        "distance": 200,
        "duration": 0.4,
        "factor": 100,
        "speed": 1,
        "maxSpeed": 50,
        "easing": "ease-out-quad",
        "divs": {
          "distance": 200,
          "duration": 0.4,
          "factor": 100,
          "speed": 1,
          "maxSpeed": 50,
          "easing": "ease-out-quad",
          "selectors": []
        }
      },
      "slow": {
        "factor": 3,
        "radius": 200
      },
      "trail": {
        "delay": 1,
        "pauseOnStop": false,
        "quantity": 1
      },
      "light": {
        "area": {
          "gradient": {
            "start": {
              "value": "#ffffff"
            },
            "stop": {
              "value": "#000000"
            }
          },
          "radius": 1000
        },
        "shadow": {
          "color": {
            "value": "#000000"
          },
          "length": 2000
        }
      }
    }
  },
  "manualParticles": [],
  "particles": {
    "bounce": {
      "horizontal": {
        "random": {
          "enable": false,
          "minimumValue": 0.1
        },
        "value": 1
      },
      "vertical": {
        "random": {
          "enable": false,
          "minimumValue": 0.1
        },
        "value": 1
      }
    },
    "collisions": {
      "absorb": {
        "speed": 2
      },
      "bounce": {
        "horizontal": {
          "random": {
            "enable": false,
            "minimumValue": 0.1
          },
          "value": 1
        },
        "vertical": {
          "random": {
            "enable": false,
            "minimumValue": 0.1
          },
          "value": 1
        }
      },
      "enable": false,
      "maxSpeed": 50,
      "mode": "bounce",
      "overlap": {
        "enable": true,
        "retries": 0
      }
    },
    "color": {
      "value": "#ff0000",
      "animation": {
        "h": {
          "count": 0,
          "enable": false,
          "offset": 0,
          "speed": 1,
          "delay": 0,
          "decay": 0,
          "sync": true
        },
        "s": {
          "count": 0,
          "enable": false,
          "offset": 0,
          "speed": 1,
          "delay": 0,
          "decay": 0,
          "sync": true
        },
        "l": {
          "count": 0,
          "enable": false,
          "offset": 0,
          "speed": 1,
          "delay": 0,
          "decay": 0,
          "sync": true
        }
      }
    },
    "groups": {},
    "move": {
      "angle": {
        "offset": 0,
        "value": 90
      },
      "attract": {
        "distance": 200,
        "enable": false,
        "rotate": {
          "x": 3000,
          "y": 3000
        }
      },
      "center": {
        "x": 50,
        "y": 50,
        "mode": "percent",
        "radius": 0
      },
      "decay": 0,
      "distance": {},
      "direction": "none",
      "drift": 0,
      "enable": true,
      "gravity": {
        "acceleration": 9.81,
        "enable": false,
        "inverse": false,
        "maxSpeed": 50
      },
      "path": {
        "clamp": true,
        "delay": {
          "random": {
            "enable": false,
            "minimumValue": 0
          },
          "value": 0
        },
        "enable": false,
        "options": {}
      },
      "outModes": {
        "default": "out",
        "bottom": "out",
        "left": "out",
        "right": "out",
        "top": "out"
      },
      "random": false,
      "size": false,
      "speed": 2,
      "spin": {
        "acceleration": 0,
        "enable": false
      },
      "straight": false,
      "trail": {
        "enable": false,
        "length": 10,
        "fill": {}
      },
      "vibrate": false,
      "warp": false
    },
    "number": {
      "density": {
        "enable": true,
        "width": 1920,
        "height": 1080
      },
      "limit": 0,
      "value": 80
    },
    "opacity": {
      "random": {
        "enable": false,
        "minimumValue": 0.1
      },
      "value": {
        "min": 0.1,
        "max": 0.5
      },
      "animation": {
        "count": 0,
        "enable": true,
        "speed": 3,
        "decay": 0,
        "delay": 0,
        "sync": false,
        "mode": "auto",
        "startValue": "random",
        "destroy": "none"
      }
    },
    "reduceDuplicates": false,
    "shadow": {
      "blur": 0,
      "color": {
        "value": "#000"
      },
      "enable": false,
      "offset": {
        "x": 0,
        "y": 0
      }
    },
    "shape": {
      "close": true,
      "fill": true,
      "options": {},
      "type": "circle"
    },
    "size": {
      "random": {
        "enable": false,
        "minimumValue": 1
      },
      "value": {
        "min": 0.1,
        "max": 5
      },
      "animation": {
        "count": 0,
        "enable": true,
        "speed": 20,
        "decay": 0,
        "delay": 0,
        "sync": false,
        "mode": "auto",
        "startValue": "random",
        "destroy": "none"
      }
    },
    "stroke": {
      "width": 0
    },
    "zIndex": {
      "random": {
        "enable": false,
        "minimumValue": 0
      },
      "value": 0,
      "opacityRate": 1,
      "sizeRate": 1,
      "velocityRate": 1
    },
    "life": {
      "count": 0,
      "delay": {
        "random": {
          "enable": false,
          "minimumValue": 0
        },
        "value": 0,
        "sync": false
      },
      "duration": {
        "random": {
          "enable": false,
          "minimumValue": 0.0001
        },
        "value": 0,
        "sync": false
      }
    },
    "rotate": {
      "random": {
        "enable": false,
        "minimumValue": 0
      },
      "value": 0,
      "animation": {
        "enable": false,
        "speed": 0,
        "decay": 0,
        "sync": false
      },
      "direction": "clockwise",
      "path": false
    },
    "destroy": {
      "bounds": {},
      "mode": "none",
      "split": {
        "count": 1,
        "factor": {
          "random": {
            "enable": false,
            "minimumValue": 0
          },
          "value": 3
        },
        "rate": {
          "random": {
            "enable": false,
            "minimumValue": 0
          },
          "value": {
            "min": 4,
            "max": 9
          }
        },
        "sizeOffset": true,
        "particles": {}
      }
    },
    "roll": {
      "darken": {
        "enable": false,
        "value": 0
      },
      "enable": false,
      "enlighten": {
        "enable": false,
        "value": 0
      },
      "mode": "vertical",
      "speed": 25
    },
    "tilt": {
      "random": {
        "enable": false,
        "minimumValue": 0
      },
      "value": 0,
      "animation": {
        "enable": false,
        "speed": 0,
        "decay": 0,
        "sync": false
      },
      "direction": "clockwise",
      "enable": false
    },
    "twinkle": {
      "lines": {
        "enable": true,
        "frequency": 0.005,
        "opacity": 1,
        "color": {
          "value": "#ff0000"
        }
      },
      "particles": {
        "enable": true,
        "frequency": 0.05,
        "opacity": 1,
        "color": {
          "value": "#ffff00"
        }
      }
    },
    "wobble": {
      "distance": 5,
      "enable": false,
      "speed": {
        "angle": 50,
        "move": 10
      }
    },
    "orbit": {
      "animation": {
        "count": 0,
        "enable": false,
        "speed": 1,
        "decay": 0,
        "delay": 0,
        "sync": false
      },
      "enable": false,
      "opacity": 1,
      "rotation": {
        "random": {
          "enable": false,
          "minimumValue": 0
        },
        "value": 45
      },
      "width": 1
    },
    "links": {
      "blink": false,
      "color": {
        "value": "#ffffff"
      },
      "consent": false,
      "distance": 150,
      "enable": true,
      "frequency": 1,
      "opacity": 0.4,
      "shadow": {
        "blur": 5,
        "color": {
          "value": "#000"
        },
        "enable": false
      },
      "triangles": {
        "enable": false,
        "frequency": 1
      },
      "width": 1,
      "warp": false
    },
    "repulse": {
      "random": {
        "enable": false,
        "minimumValue": 0
      },
      "value": 0,
      "enabled": false,
      "distance": 1,
      "duration": 1,
      "factor": 1,
      "speed": 1
    }
  },
  "pauseOnBlur": true,
  "pauseOnOutsideViewport": true,
  "responsive": [],
  "smooth": false,
  "style": {},
  "themes": [],
  "zLayers": 100,
  "motion": {
    "disable": false,
    "reduce": {
      "factor": 4,
      "value": true
    }
  }
}

    let onParticlesLoaded = event => {
        const particlesContainer = event.detail.particles;

        // you can use particlesContainer to call all the Container class
        // (from the core library) methods like play, pause, refresh, start, stop
    };

    let particlesInit = async main => {
        // you can use main to customize the tsParticles instance adding presets or custom shapes
        // this loads the tsparticles package bundle, it's the easiest method for getting everything ready
        // starting from v2 you can add only the features you need reducing the bundle size
        await loadFull(main);
    };
</script>

<!-- <Menu/> -->


<section class="text-white text-center h-4/5 py-40 px-10 bg-transparant-1" style="background-color: rgba(0,0,0,0.2)">
    <svelte:component
        this="{ParticlesComponent}"
        id="tsparticles"
        class="foo bar"
        style="position: absolute; z-index: -1;"
        options="{particlesConfig}"
        on:particlesLoaded="{onParticlesLoaded}"
        particlesInit="{particlesInit}"
    />
    <img class="mx-auto my-10 " src="images/toekomst_logo(1).png">
    <h1 class="text-3xl font-bold">Kom en maak deel uit van de digitale revolutie</h1>
    <h2 class="text-2xl font-bold p-4 text-blue-500">Join onze programeer community!</h2>
    <div class="mt-4">
        <a href="#meldjeaan"><button class=" bg-white text-black border-2 hover:bg-transparant hover:bg-blue-500 hover:text-white py-2 px-4 rounded">Meld je aan</button></a>
        <!-- <button class="bg-transparant text-white hover:text-blue-500 hover:border-blue-500 border-2 py-2 px-4 rounded mr-4">Skill test</button> -->

    </div>
</section>

<section class="py-10 bg-black text-white">
    <div class="container mx-auto">
        <h2 class="text-2xl font-bold text-center p-3">Voor wie?</h2>

        <div class="flex flex-wrap justify-center w-2/3 m-auto">
            <div class="w-full md:w-1/4 p-4 text-center">
                <img src="images/who/dino.png" class="w-11 m-auto invert" alt="dino">
                <h3 class="text-xl font-semibold">All creatures welcome</h3>
            </div>
            <div class="w-full md:w-1/4 p-4 text-center">
                <img src="images/who/skill.png" class="w-11 m-auto invert" alt="skill">
                <h3 class="text-xl font-semibold">beginnend en gevorderd</h3>
            </div>
            <div class="w-full md:w-1/4 p-4 text-center">
                <img src="images/who/age.png" class="w-11 m-auto invert" alt="age">
                <h3 class="text-xl font-semibold">12 - 20 jaar</h3>
            </div>
            <div class="w-full md:w-1/4 p-4 text-center">
                <img src="images/who/microscope.png" class="w-11 m-auto invert" alt="microscope">
                <h3 class="text-xl font-semibold">Een goeie dosis nieuwsgierigheid</h3>
            </div>
        </div>
    </div>
</section>

<section class="py-10 bg-white">
    <div class="container mx-auto">
        <h2 class="text-2xl font-bold text-center p-3">Wat ga je bij ons leren bouwen?</h2>

        <div class="flex flex-wrap justify-center w-2/3 m-auto">
            <div class="w-full md:w-1/4 p-4 text-center">
                <img src="images/bouwen/websites.png" class="w-11 m-auto" alt="websites">
                <h3 class="text-xl font-semibold">Websites</h3>
            </div>
            <div class="w-full md:w-1/4 p-4 text-center">
                <img src="images/bouwen/games.png" class="w-11 m-auto" alt="games">
                <h3 class="text-xl font-semibold">Games</h3>
            </div>
            <div class="w-full md:w-1/4 p-4 text-center">
                <img src="images/bouwen/apps.png" class="w-11 m-auto" alt="apps">
                <h3 class="text-xl font-semibold">Apps</h3>
            </div>
            <div class="w-full md:w-1/4 p-4 text-center">
                <img src="images/bouwen/iot.png" class="w-11 m-auto" alt="iot">
                <h3 class="text-xl font-semibold">IOT</h3>
            </div>
        </div>
    </div>
</section>

<section class="bg-black text-white py-8">
    <div class="container mx-auto text-center">
        <img class="my-5 w-2/3 mx-auto" src="images/replit.gif" alt="replit">
        
        <h2 class="text-3xl font-bold text-center m-10">Online community & multiplayer coding</h2>
        <div class="flex flex-wrap justify-center">
            <div class="w-full sm:w-1/2 lg:w-1/3 p-4">
                <img src="images/community/live.png" class="w-11 invert mx-auto" alt="live">
                <h3 class="text-xl font-semibold mb-2">videocurssussen<br> en<br> live lessen</h3>
            </div>
            <div class="w-full sm:w-1/2 lg:w-1/3 p-4">
                <img src="images/community/challange.png" class="w-11 invert mx-auto" alt="challange">
                <h3 class="text-xl font-semibold mb-2">Wekelijkse<br> coding<br> challenges</h3>
                
            </div>
            <div class="w-full sm:w-1/2 lg:w-1/3 p-4">
                <img src="images/community/friends.png" class="w-11 invert mx-auto" alt="fiends">
                <h3 class="text-xl font-semibold mb-2">Ontmoet<br> nieuwe<br> vrienden</h3>
            </div>
        </div>
    </div>
</section>



<section class="text-white text-center h-4/5 py-40 px-10" style="background-color: rgba(0,0,0,0.5)" id="meldjeaan">
    <div class="container mx-auto">
        <h1 class="text-3xl font-bold">Launching this summer!</h1>
        <h2 class="text-2xl">Ontvang direct toegang tot ons beta programma</h2>
        <!-- <form class="mt-4 flex flex-col w-52 mx-auto">
            <input type="text" class="border border-gray-300 rounded py-2 px-4 mb-2" placeholder="Naam">
            <input type="email" class="border border-gray-300 rounded py-2 px-4 mb-2" placeholder="E-mail">
            <input type="tel" class="border border-gray-300 rounded py-2 px-4 mb-2" placeholder="Telefoonnummer">
            <button class="bg-blue-500 text-white hover:bg-white hover:text-blue-500 py-2 px-4 rounded">Verzenden</button>
        </form> -->
        <a href="https://discord.gg/zejaJtzkMQ"><button class="mx-auto my-10 bg-white text-black border-2 hover:bg-transparant hover:bg-blue-500 hover:text-white py-2 px-4 rounded flex" ><img src="images/discord.png" class="w-7 mx-1"> Join onze Discord</button></a>
    </div>
</section>

  

<footer class="bg-gray-800 text-white py-8">
    <div class="container mx-auto">
        <p class="mt-4 text-center">info@toekomst.school</p>
    </div>
</footer>


<style>


  li:before {
    content: "\2713";
    color: #10B981;
    display: inline-block;
    margin-right: 0.5rem;
  }

</style>