self.addEventListener('install', e=>{
  e.waitUntil(caches.open('office-verde-v1').then(c=>c.addAll(['./','./index.html','./icon.png','./manifest.json'])))
});
self.addEventListener('fetch', e=>{
  e.respondWith(caches.match(e.request).then(r=>r||fetch(e.request)))
});
