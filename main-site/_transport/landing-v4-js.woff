(()=>{
  const CHECKOUT='https://pay.hotmart.com/A98424225S?bid=1773208589822&checkoutMode=10&off=njqo49xj';
  const KEEP=['utm_source','utm_medium','utm_campaign','utm_content','utm_term','fbclid'];
  const TESTIMONIALS=[
    'https://static.wixstatic.com/media/279a76_a2da35cf7c034534bd3dd8a35b6bb533~mv2.jpeg',
    'https://static.wixstatic.com/media/279a76_31b7a1cc048e484aaa617ef5f0f46342~mv2.jpeg',
    'https://static.wixstatic.com/media/279a76_65cb56988a414e4ab046c28d73df92f1~mv2.jpeg',
    'https://static.wixstatic.com/media/279a76_3751faff93864c399da5f65ec64f6c72~mv2.jpeg',
    'https://static.wixstatic.com/media/279a76_0c587d22bcac4156bf9b886f3b7d45e0~mv2.jpeg',
    'https://static.wixstatic.com/media/279a76_01d550d213794f1da5a6d6b66b5da8bf~mv2.jpeg',
    'https://static.wixstatic.com/media/279a76_650db30af46a413486334b760df661ca~mv2.jpg',
    'https://static.wixstatic.com/media/279a76_a6d49d97e35a4685a3ce1ed947890ef9~mv2.jpg',
    'https://static.wixstatic.com/media/279a76_7c2c9be619cf43b4a2d647bea01edcb8~mv2.jpeg',
    'https://static.wixstatic.com/media/279a76_b80d5ec3e3b7477e92e8c38cd0b7a8dd~mv2.jpg',
    'https://static.wixstatic.com/media/279a76_0ea8daf5aba04fada5a3dae29ee52deb~mv2.jpeg',
    'https://static.wixstatic.com/media/279a76_3ad7853dcad2404a8637abbf340f9ec0~mv2.jpeg'
  ];

  function checkoutUrl(){
    const cur=new URLSearchParams(location.search),url=new URL(CHECKOUT);
    KEEP.forEach(k=>{const v=cur.get(k);if(v)url.searchParams.set(k,v)});
    return url.toString();
  }

  function setupCheckout(){
    document.querySelectorAll('[data-checkout]').forEach(a=>{
      a.href=checkoutUrl();
      a.addEventListener('click',()=>{
        if(window.fbq){
          fbq('trackCustom','CTA_Click',{location:a.dataset.location||'unknown',product:'Sistema Bypass Neural'});
          fbq('track','InitiateCheckout',{value:37,currency:'BRL',content_name:'Sistema Bypass Neural'});
        }
      });
    });
  }

  let pixel=false;
  function loadPixel(){
    if(pixel)return; pixel=true;
    !function(f,b,e,v,n,t,s){if(f.fbq)return;n=f.fbq=function(){n.callMethod?n.callMethod.apply(n,arguments):n.queue.push(arguments)};if(!f._fbq)f._fbq=n;n.push=n;n.loaded=!0;n.version='2.0';n.queue=[];t=b.createElement(e);t.async=!0;t.src=v;s=b.getElementsByTagName(e)[0];s.parentNode.insertBefore(t,s)}(window,document,'script','https://connect.facebook.net/en_US/fbevents.js');
    fbq('init','341131507668987');
    fbq('track','PageView');
    fbq('track','ViewContent',{content_name:'Sistema Bypass Neural',content_type:'product'});
  }

  function setupConsent(){
    const b=document.getElementById('cookieBanner'); if(!b)return;
    const v=localStorage.getItem('sbn_cookie_consent');
    if(v==='accepted')loadPixel(); else if(!v)b.style.display='grid';
    document.getElementById('cookieAccept')?.addEventListener('click',()=>{localStorage.setItem('sbn_cookie_consent','accepted');b.style.display='none';loadPixel()});
    document.getElementById('cookieReject')?.addEventListener('click',()=>{localStorage.setItem('sbn_cookie_consent','rejected');b.style.display='none'});
  }

  function setupTestimonials(){
    const g=document.getElementById('testimonialsGrid'); if(!g)return;
    TESTIMONIALS.forEach((src,i)=>{
      const b=document.createElement('button'); b.type='button'; b.className='testimonial lightbox-trigger'; b.dataset.lightboxSrc=src; b.setAttribute('aria-label',`Ampliar depoimento original ${i+1}`);
      const img=document.createElement('img'); img.src=src; img.loading='lazy'; img.decoding='async'; img.alt=`Depoimento original ${i+1}`;
      b.appendChild(img); g.appendChild(b);
    });
  }

  function setupLightbox(){
    const box=document.getElementById('lightbox'),img=document.getElementById('lightboxImg'); if(!box||!img)return;
    const close=()=>{box.classList.remove('open');img.src='';document.body.style.overflow=''};
    document.addEventListener('click',e=>{const t=e.target.closest?.('.lightbox-trigger');if(!t)return;const src=t.dataset.lightboxSrc;if(!src)return;img.src=src;box.classList.add('open');document.body.style.overflow='hidden'});
    document.getElementById('lightboxClose')?.addEventListener('click',close);
    box.addEventListener('click',e=>{if(e.target===box)close()});
    document.addEventListener('keydown',e=>{if(e.key==='Escape')close()});
  }

  function setupAuthor(){
    const img=document.getElementById('authorPhoto'); if(!img)return;
    img.addEventListener('error',()=>{const f=img.dataset.fallback;if(f&&img.src!==f)img.src=f},{once:true});
  }

  function setupInventory(){
    const anchor=document.querySelector('.vault-note');
    if(!anchor||document.querySelector('.inventory-audit'))return;
    const modules=[
      ['01','Boas-vindas','2 conteúdos','core'],
      ['02','Manual do Bypass Neural','1 conteúdo','core'],
      ['03','Hipnose e comunicação — conteúdo histórico','3 conteúdos','complement'],
      ['04','Despertando a Mente Milionária','11 conteúdos — legado, não vendido como bônus','legacy'],
      ['05','Curso de AutoHypnosis','18 conteúdos','complement'],
      ['06','Conclusão','1 conteúdo','core'],
      ['07','E-books Bônus','4 conteúdos','complement'],
      ['08','Sessões de Hypnosis','10 conteúdos','complement'],
      ['09','Treinamento Acorda pra Vida','5 conteúdos','complement'],
      ['10','Vencendo a Ansiedade','3 conteúdos','complement'],
      ['11','00 — Comece Aqui: Operação Bypass 21','trilha moderna','core'],
      ['12','01 — Fundamentos e Diagnóstico','trilha moderna','core'],
      ['13','02 — Perguntas e Contexto','trilha moderna','core'],
      ['14','03 — Valor, Proposta e Condições','trilha moderna','core'],
      ['15','04 — Hesitação e Objeções','trilha moderna','core'],
      ['16','05 — Canais e Próximos Passos','trilha moderna','core'],
      ['17','06 — Sprint de Ativação de 7 Dias','trilha moderna','core'],
      ['18','07 — Biblioteca e Recursos','trilha moderna','core']
    ];
    const section=document.createElement('div'); section.className='inventory-audit';
    section.innerHTML=`<div class="inventory-head"><div><span class="tag">INVENTÁRIO AUDITADO</span><h3>18 módulos identificados na área de membros</h3><p><strong>58 conteúdos</strong> foram explicitamente contabilizados nos módulos históricos/complementares, além da trilha moderna 00–07. O inventário abaixo separa o que é núcleo, complementar e legado para não transformar conteúdo antigo em promessa nova.</p></div><b>18</b></div><div class="inventory-grid">${modules.map(([n,name,meta,type])=>`<div class="inventory-item ${type}"><span>${n}</span><div><b>${name}</b><small>${meta}</small></div></div>`).join('')}</div><div class="inventory-legend"><span><i class="core-dot"></i>Núcleo / trilha atual</span><span><i class="complement-dot"></i>Complementar</span><span><i class="legacy-dot"></i>Legado / não usado como bônus comercial</span></div>`;
    anchor.insertAdjacentElement('afterend',section);
    const style=document.createElement('style');
    style.textContent=`.inventory-audit{margin-top:16px;padding:20px;border:1px solid rgba(210,163,74,.28);border-radius:17px;background:linear-gradient(135deg,#0f0d09,#080706)}.inventory-head{display:flex;justify-content:space-between;align-items:center;gap:20px;margin-bottom:14px}.inventory-head h3{font-size:30px;margin:8px 0 4px}.inventory-head p{margin:0;color:var(--muted);font-size:9px;max-width:850px}.inventory-head p strong{color:var(--gold2)}.inventory-head>b{font-family:'Barlow Condensed';font-size:72px;line-height:.8;color:var(--gold2);opacity:.82}.inventory-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:7px}.inventory-item{display:grid;grid-template-columns:36px 1fr;gap:8px;align-items:center;padding:9px 10px;border:1px solid rgba(255,255,255,.055);border-radius:9px;background:#080706}.inventory-item>span{display:grid;place-items:center;width:34px;height:34px;border:1px solid var(--line);border-radius:8px;color:var(--gold2);font-family:'Barlow Condensed';font-size:15px}.inventory-item b{display:block;color:#d7cdbf;font-size:8px}.inventory-item small{display:block;color:var(--muted2);font-size:7px;margin-top:2px}.inventory-item.legacy{opacity:.62;border-style:dashed}.inventory-legend{display:flex;flex-wrap:wrap;gap:15px;margin-top:12px;padding-top:10px;border-top:1px solid rgba(255,255,255,.05);color:var(--muted2);font-size:7px}.inventory-legend span{display:flex;align-items:center;gap:5px}.inventory-legend i{width:7px;height:7px;border-radius:50%}.core-dot{background:#f0d18a}.complement-dot{background:#a77c30}.legacy-dot{background:#5f584e}@media(max-width:850px){.inventory-grid{grid-template-columns:1fr 1fr}}@media(max-width:560px){.inventory-head{align-items:flex-start}.inventory-head>b{font-size:52px}.inventory-grid{grid-template-columns:1fr}}`;
    document.head.appendChild(style);
  }

  let player=null,requestedSound=false,playingWithSound=false;
  function hideOverlay(){document.getElementById('soundOverlay')?.classList.add('hidden')}
  window.onYouTubeIframeAPIReady=()=>{
    if(!document.getElementById('youtubePlayer'))return;
    player=new YT.Player('youtubePlayer',{videoId:'R5-Q0ccApXM',playerVars:{autoplay:1,mute:0,playsinline:1,rel:0,controls:1,modestbranding:1,enablejsapi:1},events:{
      onReady:e=>{const l=document.getElementById('vslLoading');if(l)l.style.display='none';try{e.target.unMute();e.target.setVolume(100);if(requestedSound)e.target.seekTo(0,true);e.target.playVideo()}catch(_){}setTimeout(()=>{try{if(e.target.getPlayerState()===YT.PlayerState.PLAYING&&!e.target.isMuted()){playingWithSound=true;hideOverlay()}}catch(_){}},1200)},
      onStateChange:e=>{try{if(e.data===YT.PlayerState.PLAYING&&!e.target.isMuted()){playingWithSound=true;hideOverlay()}}catch(_){}}
    }});
  };

  function setupSound(){
    const o=document.getElementById('soundOverlay'); if(!o)return;
    o.addEventListener('click',()=>{requestedSound=true;const label=o.querySelector('[data-sound-label]');if(label)label.textContent='INICIANDO COM SOM…';if(player){try{player.unMute();player.setVolume(100);player.seekTo(0,true);player.playVideo()}catch(_){}}});
    setTimeout(()=>{if(playingWithSound)hideOverlay()},1800);
  }

  document.addEventListener('DOMContentLoaded',()=>{
    setupCheckout();
    setupConsent();
    setupTestimonials();
    setupLightbox();
    setupAuthor();
    setupInventory();
    setupSound();
  });
})();