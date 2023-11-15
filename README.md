.cover::after { /*left triangle*/
  position: absolute;
  content: '';
  border-left: 24.5vmin solid #ffbbc1;
  border-bottom: 15vmin solid transparent;
  border-top: 15vmin solid transparent;
  top: -15vmin;
  left: -24vmin;
}

.cover::before {
  position: absolute;
  content: '';
  border-right: 24.5vmin solid #ffbbc1;
  border-bottom: 15vmin solid transparent;
  border-top: 15vmin solid transparent;
  top: -15vmin;
  left: -0.5vmin;
}

.lid {
  position: absolute;
  height: 0;
  width: 0;
  
  border-top: 15vmin solid #ff8896;
  border-left: 24vmin solid transparent;
  border-right: 24vmin solid transparent;

  top: 0;
  transform-origin: top;
  animation: open-rev 2s;
}

.container:hover .lid {
  animation: open 0.5s;
  animation-fill-mode: forwards;
}

.container:hover .card {
  animation: slide 0.2s;
  animation-delay: 0.5s;
  animation-fill-mode: forwards;
}

.shadow {
  position: relative;
  top: 3vmin;
  border-radius: 50%; 
  opacity: 0.7;
  height: 2vmin;
  width: 48vmin;
  background: #e8c5d0;
}

@keyframes open {
  100% {
    transform: rotatex(180deg);
  }
}

@keyframes slide {
  100% {
    transform: translatey(-15vmin);
    z-index: 2;
  }
}

@keyframes open-rev {
  from {
    transform: rotatex(-180deg);

  }
}

@keyframes slide-rev {
  from {
    transform: translatey(-15vmin);
  }
}
