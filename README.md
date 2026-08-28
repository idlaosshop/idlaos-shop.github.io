<!DOCTYPE html>
<html lang="lo">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ID Laos Shop - ເວັບຂາຍໄອດີ ແລະ ເຕີມເກມອອນໄລນ໌</title>
    <style>
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Phetsarath OT', 'Noto Sans Lao', sans-serif; }
        body { background-color: #0f172a; color: #f8fafc; }
        
        header { background-color: #1e293b; padding: 1rem 5%; display: flex; justify-content: space-between; align-items: center; border-bottom: 2px solid #334155; position: sticky; top: 0; z-index: 100; }
        .logo { font-size: 1.8rem; font-weight: bold; color: #38bdf8; text-transform: uppercase; }
        .logo span { color: #f43f5e; }
        nav a { color: #cbd5e1; text-decoration: none; margin-left: 1.5rem; font-weight: 500; transition: 0.3s; }
        nav a:hover { color: #38bdf8; }

        .hero { background: linear-gradient(rgba(15, 23, 42, 0.85), rgba(15, 23, 42, 0.85)), url('https://images.unsplash.com/photo-1542751371-adc38448a05e?q=80&w=1000') center/cover; padding: 4rem 1rem; text-align: center; }
        .hero h1 { font-size: 2.2rem; margin-bottom: 0.5rem; color: #ffffff; }
        .hero p { font-size: 1.1rem; color: #38bdf8; margin-bottom: 1.5rem; }

        .container { max-width: 1200px; margin: 2rem auto; padding: 0 1rem; }
        .section-title { font-size: 1.5rem; border-left: 4px solid #38bdf8; padding-left: 10px; margin: 2.5rem 0 1.5rem 0; color: #ffffff; }
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap: 1.5rem; }
        
        .card { background: #1e293b; border-radius: 12px; overflow: hidden; border: 1px solid #334155; transition: 0.3s; display: flex; flex-direction: column; justify-content: space-between; }
        .card:hover { transform: translateY(-5px); border-color: #38bdf8; box-shadow: 0 10px 20px rgba(56, 189, 248, 0.1); }
        .card img { width: 100%; height: 170px; object-fit: cover; }
        .card-body { padding: 1.2rem; text-align: center; flex-grow: 1; }
        .card-body h3 { margin-bottom: 0.5rem; color: #f8fafc; }
        .card-body p { color: #94a3b8; font-size: 0.9rem; margin-bottom: 1rem; }

        .btn { background: #38bdf8; color: #0f172a; font-weight: bold; border: none; padding: 0.7rem 1.2rem; border-radius: 6px; cursor: pointer; width: 100%; transition: 0.3s; font-size: 1rem; }
        .btn:hover { background: #0284c7; color: white; }
        .btn-danger { background: #f43f5e; color: white; }
        .btn-danger:hover { background: #e11d48; }

        .form-group { margin-bottom: 1.2rem; text-align: left; }
        .form-group label { display: block; margin-bottom: 0.5rem; color: #cbd5e1; }
        .form-group input, .form-group select { width: 100%; padding: 0.8rem; border-radius: 6px; border: 1px solid #334155; background: #0f172a; color: white; font-size: 1rem; }

        .modal { display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.85); justify-content: center; align-items: center; z-index: 1000; }
        .modal-content { background: #1e293b; padding: 2rem; border-radius: 12px; max-width: 480px; width: 90%; position: relative; border: 1px solid #38bdf8; }
        .close-btn { position: absolute; top: 12px; right: 18px; color: #cbd5e1; font-size: 1.8rem; cursor: pointer; }

        footer { background: #0b1120; text-align: center; padding: 2rem; margin-top: 4rem; color: #64748b; border-top: 1px solid #1e293b; }
    </style>
</head>
<body>

    <header>
        <div class="logo">ID LAOS <span>SHOP</span></div>
        <nav>
            <a href="#topup">ເຕີມເກມ</a>
            <a href="#market">ຊື້ໄອດີ</a>
            <a href="#payment">ແຈ້ງໂອນ</a>
        </nav>
    </header>

    <section class="hero">
        <h1>ID LAOS SHOP</h1>
        <p>ສູນລວມໄອດີເກມ ແລະ ບໍລິການເຕີມເກມອອນໄລນ໌ ປອດໄພ 100%</p>
    </section>

    <div class="container">
        
        <div id="topup">
            <h2 class="section-title">ບໍລິການເຕີມເກມ (Top-Up)</h2>
            <div class="grid">
                <div class="card">
                    <img src="https://images.unsplash.com/photo-1538481199705-c710c4e965fc?q=80&w=500" alt="Free Fire">
                    <div class="card-body">
                        <h3>Free Fire</h3>
                        <p>ເຕີມເພັດຜ່ານ UID ເກມ ເຂົ້າໄວ</p>
                        <button class="btn" onclick="openModal('Free Fire')">ເຕີມເລີຍ</button>
                    </div>
                </div>
                <div class="card">
                    <img src="https://images.unsplash.com/photo-1511512578047-dfb367046420?q=80&w=500" alt="ROV">
                    <div class="card-body">
                        <h3>ROV</h3>
                        <p>ເຕີມຄູປອງ ລາຄາຖືກກວ່າເຕີມເອງ</p>
                        <button class="btn" onclick="openModal('ROV')">ເຕີມເລີຍ</button>
                    </div>
                </div>
                <div class="card">
                    <img src="https://images.unsplash.com/photo-1560253023-3ec5d502959f?q=80&w=500" alt="PUBG Mobile">
                    <div class="card-body">
                        <h3>PUBG Mobile</h3>
                        <p>ເຕີມ UC ເກມ PUBG ອັດໂຕໂນມັດ</p>
                        <button class="btn" onclick="openModal('PUBG Mobile')">ເຕີມເລີຍ</button>
                    </div>
                </div>
            </div>
        </div>

        <div id="market">
            <h2 class="section-title">ໄອດີເກມພ້ອມຂາຍ (Account Shop)</h2>
            <div class="grid">
                <div class="card">
                    <img src="https://images.unsplash.com/photo-1542751371-adc38448a05e?q=80&w=500" alt="ID ROV">
                    <div class="card-body">
                        <h3>ID ROV #001</h3>
                        <p>ຮີໂຣ່ 85, ສະກິນ 120 (ມີຮີໂຣ່ Legend)</p>
                        <p style="color: #f43f5e; font-weight: bold; font-size: 1.1rem; margin-bottom: 1rem;">350,000 ກີບ</p>
                        <button class="btn btn-danger" onclick="alert('ກະລຸນາຕິດຕໍ່ແອດມິນຜ່ານ WhatsApp ເພື່ອສັ່ງຊື້ໄອດີນີ້!')">ຊື້ໄອດີນີ້</button>
                    </div>
                </div>
                <div class="card">
                    <img src="https://images.unsplash.com/photo-1580234811497-9df7fd2f357e?q=80&w=500" alt="ID Free Fire">
                    <div class="card-body">
                        <h3>ID Free Fire #002</h3>
                        <p>ຊຸດເກົ່າ ປີ 2020, ອາວຸດອັບເກຣດ Level Max</p>
                        <p style="color: #f43f5e; font-weight: bold; font-size: 1.1rem; margin-bottom: 1rem;">500,000 ກີບ</p>
                        <button class="btn btn-danger" onclick="alert('ກະລຸນາຕິດຕໍ່ແອດມິນຜ່ານ WhatsApp ເພື່ອສັ່ງຊື້ໄອດີນີ້!')">ຊື້ໄອດີນີ້</button>
                    </div>
                </div>
            </div>
        </div>

        <div id="payment" style="margin-top: 3rem; background: #1e293b; padding: 2rem; border-radius: 12px; border: 1px solid #334155;">
            <h2 style="margin-bottom: 1rem; color: #38bdf8;">ແຈ້ງໂອນເງິນ (Confirm Payment)</h2>
            <form onsubmit="handlePayment(event)">
                <div class="form-group">
                    <label>ເລືອກທະນາຄານ:</label>
                    <select required>
                        <option value="bcel">BCEL One (ວັນແບ້ງ)</option>
                    </select>
                </div>
                <div class="form-group">
                    <label>ຈຳນວນເງິນ (ກີບ):</label>
                    <input type="number" placeholder="ເຊັ່ນ: 50000" required>
                </div>
                <div class="form-group">
                    <label>ແນບຮູບໃບໂອນເງິນ (Slip):</label>
                    <input type="file" accept="image/*" required>
                </div>
                <button type="submit" class="btn">ສົ່ງຫຼັກຖານການໂອນ</button>
            </form>
        </div>

    </div>

    <div class="modal" id="topupModal">
        <div class="modal-content">
            <span class="close-btn" onclick="closeModal()">&times;</span>
            <h2 id="modalGameTitle" style="margin-bottom: 1rem; color: #38bdf8;">ເຕີມເກມ</h2>
            <form onsubmit="handleTopup(event)">
                <div class="form-group">
                    <label>ID ເກມ (UID):</label>
                    <input type="text" placeholder="ປ້ອນ UID ຂອງທ່ານ" required>
                </div>
                <div class="form-group">
                    <label>ເລືອກແພັກເກັດ:</label>
                    <select required>
                        <option value="">-- ເລືອກແພັກເກັດ --</option>
                        <option value="1">100 ເພັດ / ຄູປອງ - 20,000 ກີບ</option>
                        <option value="2">300 ເພັດ / ຄູປອງ - 55,000 ກີບ</option>
                        <option value="3">1,000 ເພັດ / ຄູປອງ - 180,000 ກີບ</option>
                    </select>
                </div>
                <button type="submit" class="btn">ຢືນຢັນການເຕີມເກມ</button>
            </form>
        </div>
    </div>

    <footer>
        <p>&copy; 2026 ID Laos Shop - All Rights Reserved.</p>
    </footer>

    <script>
        function openModal(gameName) {
            document.getElementById('modalGameTitle').innerText = 'ເຕີມເກມ: ' + gameName;
            document.getElementById('topupModal').style.display = 'flex';
        }

        function closeModal() {
            document.getElementById('topupModal').style.display = 'none';
        }

        function handleTopup(e) {
            e.preventDefault();
            alert('ບັນທຶກຂໍ້ມູນແນວ! ກະລຸນາແຈ້ງໂອນເງິນຢູ່ຟອມແຈ້ງໂອນເງິນ.');
            closeModal();
        }

        function handlePayment(e) {
            e.preventDefault();
            alert('ສົ່ງຫຼັກຖານສຳເລັດ! ທີມງານຈະກວດສອບ ແລະ ເຕີມໃຫ້ພາຍໃນ 5-10 ນາທີ.');
        }
    </script>
</body>
</html>
