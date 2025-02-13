# До минификации

```js
(function polyfill() {
  const relList = document.createElement("link").relList;
  if (relList && relList.supports && relList.supports("modulepreload")) {
    return;
  }
  for (const link2 of document.querySelectorAll('link[rel="modulepreload"]')) {
    processPreload(link2);
  }
  new MutationObserver((mutations) => {
    for (const mutation of mutations) {
      if (mutation.type !== "childList") {
        continue;
      }
      for (const node of mutation.addedNodes) {
        if (node.tagName === "LINK" && node.rel === "modulepreload")
          processPreload(node);
      }
    }
  }).observe(document, { childList: true, subtree: true });
})();
```


---
transition: fade
---

# После минификации


```js
* @vue/shared v3.5.13
* (c) 2018-present Yuxi (Evan) You and Vue contributors
* @license MIT
//*! #__NO_SIDE_EFFECTS__ */
function yl(e){const t=Object.create(null);for(const n of e.split(","))t[n]=1;return n=>n in t}const oe={},un=[],yt=()=>{},
$a=()=>!1,zn=e=>e.charCodeAt(0)===111&&e.charCodeAt(1)===110&&(e.charCodeAt(2)>122||e.charCodeAt(2)<97),vl=e=>e.startsWith("onUpdate:"),
Me=Object.assign,wl=(e,t)=>{const n=e.indexOf(t);n>-1&&e.splice(n,1)},Sa=Object.prototype.hasOwnProperty,de=(e,t)=>Sa.call(e,t),
Y=Array.isArray,cn=e=>vs(e)==="[object Map]",ui=e=>vs(e)==="[object Set]",ne=e=>typeof e=="function",Ee=e=>typeof e=="string",
Et=e=>typeof e=="symbol",Pe=e=>e!==null&&typeof e=="object",ci=e=>(Pe(e)||ne(e))&&ne(e.then)&&ne(e.catch),fi=Object.prototype.toString,
vs=e=>fi.call(e),Ra=e=>vs(e).slice(8,-1),di=e=>vs(e)==="[object Object]",xl=e=>Ee(e)&&e!=="NaN"&&e[0]!=="-"&&""+parseInt(e,10)===
e,fn=yl(",key,ref,ref_for,ref_key,onVnodeBeforeMount,onVnodeMounted,onVnodeBeforeUpdate,onVnodeUpdated,onVnodeBeforeUnmount,onVnodeUnmounted")
,ws=e=>{const t=Object.create(null);return n=>t[n]||(t[n]=e(n))},Ca=/-(\w)/g,nt=ws(e=>e.replace(Ca,(t,n)=>n?n.toUpperCase():"")),
Ta=/\B([A-Z])/g,It=ws(e=>e.replace(Ta,"-$1").toLowerCase()),xs=ws(e=>e.charAt(0).toUpperCase()+e.slice(1)),Ls=ws(e=>e?`on${xs(e)}`:""),
We=(e,t)=>!Object.is(e,t),Fs=(e,...t)=>{for(let n=0;n<e.length;n++)e[n](...t)},pi=(e,t,n,s=!1)=>{Object.defineProperty(e,t,{configurable:!0,
enumerable:!1,writable:s,value:n})},Pa=e=>{const t=parseFloat(e);return isNaN(t)?e:t};let rr;const ks=()=>rr||(rr=typeof globalThis<"u"?
globalThis:typeof self<"u"?self:typeof window<"u"?window:typeof global<"u"?global:{});function _n(e){if(Y(e)){const t={};for(let n=0;n<e.length;n++){
const s=e[n],l=Ee(s)?Aa(s):_n(s);if(l)for(const r in l)t[r]=l[r]}return t}else if(Ee(e)||Pe(e))return e}const Ea=/;(?![^(]*\))/g,Ia=/:([^]+)/,Ma=/\/\*[^]*?\*\//g;
function Aa(e){const t={};return e.replace(Ma,"").split(Ea).forEach(n=>{if(n){const s=n.split(Ia);s.length>1&&(t[s[0].trim()]=s[1].trim())}}),t}function A(e){let t="";if(Ee(e))t=e;else if(Y(e))for(let n=0;n<e.length;n++){const s=A(e[n]);s&&(t+=s+" ")}else if(Pe(e))for(const n in e)e[n]&&(t+=n+" ");return t.trim()}const Oa="itemscope,allowfullscreen,formnovalidate,ismap,nomodule,novalidate,readonly",Ba=yl(Oa);function hi(e){return!!e||e===""}const mi=e=>!!(e&&e.__v_isRef===!0),Ce=e=>Ee(e)?e:e==null?"":Y(e)||Pe(e)&&(e.toString===fi||!ne(e.toString))?mi(e)?Ce(e.value):JSON.stringify(e,gi,2):String(e),gi=(e,t)=>mi(t)?gi(e,t.value):cn(t)?{[`Map(${t.size})`]:[...t.entries()].reduce((n,[s,l],r)=>(n[Vs(s,r)+" =>"]=l,n),{})}:ui(t)?{[`Set(${t.size})`]:[...t.values()].map(n=>Vs(n))}:Et(t)?Vs(t):Pe(t)&&!Y(t)&&!di(t)?String(t):t,Vs=(e,t="")=>{var n;return Et(e)?`Symbol(${(n=e.description)!=null?n:t})`:e};/**
```

---
layout: center
layoutClass: gap-16
---

# 470.32 kB -> 186.86 kB

<v-click>

## -

## <span class="green">~60%</span>

</v-click>

<style>
	.red {
		color: var(--twoslash-error-color);
	}

	.green {
		color: var(--twoslash-tag-annotate-color);
	}
</style>

