### B. Deploy Frontend to Vercel
1. In Vercel, import your GitHub repository.
2. Set the **Root Directory** to `frontend`.
3. Add `VITE_API_BASE_URL` pointing to your Render backend URL (e.g., `https://your-service.onrender.com`).
4. Click **Deploy**. SPA rewrites are automatically handled by `frontend/vercel.json`.

---

## 🧪 Borrow System Verification

Use the built-in flow checker script to validate the transactional flow before releasing:

```bash
python backend/scripts/verify_borrow_flow.py --base-url http://localhost:8000
```

**What it validates:**
- Borrow record creation.
- Dynamic decrement of `available_copies` on borrow.
- Returns and idempotent state verification.
- Dynamic increment of `available_copies` on return.
- Record lookup in the general history log.

---

## 📜 License
This project is open-source under the MIT License. Developed with ❤️ by [shreyashmane-dev](https://github.com/shreyashmane-dev).
- Minor documentation improvements. (2026-07-10 16:13:46.908635)
- Added maintenance update. (2026-07-11 14:43:56.922454)
- Updated implementation notes. (2026-07-17 22:38:18.141880)
