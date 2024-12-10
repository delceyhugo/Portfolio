<script setup>
const fromLeft = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    entry.target.classList.toggle('from-left', entry.isIntersecting);
    setTimeout(() => entry.target.classList.toggle('from-left', false), 500);
    entry.target.classList.toggle('to-left', !entry.isIntersecting);
  })
}, {threshold: .3})
const fromRight = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    entry.target.classList.toggle('from-right', entry.isIntersecting);
    setTimeout(() => entry.target.classList.toggle('from-right', false), 500);
    entry.target.classList.toggle('to-right', !entry.isIntersecting);
  })
}, {threshold: .3})
const fromTop = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    entry.target.classList.toggle('from-top', entry.isIntersecting);
    setTimeout(() => entry.target.classList.toggle('from-top', false), 500);
    entry.target.classList.toggle('to-top', !entry.isIntersecting);
  })
}, {threshold: .3})
const fromBottom = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    entry.target.classList.toggle('from-bottom', entry.isIntersecting);
    setTimeout(() => entry.target.classList.toggle('from-bottom', false), 500);
    entry.target.classList.toggle('to-bottom', !entry.isIntersecting);
  })
}, {threshold: .3})
const fromCenter = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    entry.target.classList.toggle('from-center', entry.isIntersecting);
    setTimeout(() => entry.target.classList.toggle('from-center', false), 500);
    entry.target.classList.toggle('to-center', !entry.isIntersecting);
  })
}, {threshold: .3})

window.onload = () => {
  document.querySelectorAll('.anim-from-left').forEach(el => fromLeft.observe(el))
  document.querySelectorAll('.anim-from-right').forEach(el => fromRight.observe(el))
  document.querySelectorAll('.anim-from-top').forEach(el => fromTop.observe(el))
  document.querySelectorAll('.anim-from-bottom').forEach(el => fromBottom.observe(el))
  document.querySelectorAll('.anim-from-center').forEach(el => fromCenter.observe(el))
}
</script>


<template>

</template>


<style lang='scss'>

@keyframes from-top {
    from {opacity: 0;transform: translateY(-50px);}
    to {opacity: 1;transform: translateY(0);}
}
.from-top{
    animation: from-top 0.5s ease-in-out forwards;
}

@keyframes from-bottom {
    from {opacity: 0;transform: translateY(50px);}
    to {opacity: 1;transform: translateY(0);}
}
.from-bottom{
    animation: from-bottom 0.5s ease-in-out forwards;
}

@keyframes from-left {
    from {opacity: 0;transform: translateX(-200px);}
    to {opacity: 1;transform: translateX(0);}
}
.from-left{
    animation: from-left 0.5s ease-in-out forwards;
}

@keyframes from-right {
    from {opacity: 0;transform: translateX(200px);}
    to {opacity: 1;transform: translateX(0);}
}
.from-right{
    animation: from-right 0.5s ease-in-out forwards;
}

@keyframes from-center {
    from {opacity: 0;transform: scale(0.5);}
    to {opacity: 1;transform: scale(1);}
}
.from-center{
    animation: from-center 0.5s ease-in-out forwards;
}

.anim-from-left, .anim-from-right, .anim-from-top, .anim-from-bottom, .anim-from-center{
  transition: all 0.5s ease-in-out;
}
.to-bottom{
  animation: to-bottom 0.5s ease-in-out forwards;
}

.to-left{
  animation: to-left 0.5s ease-in-out forwards;
}
.to-right{
  animation: to-right 0.5s ease-in-out forwards;
}
.to-top{
  animation: to-top 0.5s ease-in-out forwards;
}
.to-center{
  animation: to-center 0.5s ease-in-out forwards;
}


@keyframes to-left {
  from {opacity: 1;transform: translateX(0px);}
  to {opacity: 0;transform: translateX(-200px);}
}
@keyframes to-right {
  from {opacity: 1;transform: translateX(0px);}
  to {opacity: 0;transform: translateX(200px);}  
}
@keyframes to-top {
  from {opacity: 1;transform: translateY(0px);}
  to {opacity: 0;transform: translateY(-50px);}
}
@keyframes to-bottom {
  from {opacity: 1;transform: translateY(0px);}
  to {opacity: 0;transform: translateY(50px);}
}
@keyframes to-center {
  from {opacity: 1;transform: scale(1);}
  to {opacity: 0;transform: scale(0.5);}
}

</style>