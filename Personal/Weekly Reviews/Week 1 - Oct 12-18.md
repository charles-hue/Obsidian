---
week: "1"
start: 2025-10-12
end: 2025-10-18
phase: Stability
focus: Body
tags:
  - weekly-review
body: 0/7
mind: 2/7
spirit: 1/7
wealth: 1/7
average: 19

---

# 🗓️ Weekly Review – Week {{week}}

## 🔹 Check-In Summary

---

## 🔹 Wins
- 
- 

## 🔹 Lessons / Mistakes
- 
- 

## 🔹 Faith & Mindset Reflection
> What moment felt peaceful this week?  
> Where did I drift from my values?

Notes →  

---

## 🔹 Metrics
| Metric | Start | End | Δ |
|:--|:-:|:-:|:-:|
| Weight |  |  |  |
| Hours Studied |  |  |  |
| Money Saved |  |  |  |

---

## 🔹 Gratitude
1.  
2.  
3.  

---

## 🔹 Next Week Intentions
-  
-  
-  

---

## 🔹 Completion Status

```dataviewjs
const parseVal = v => {
	if (v == null) return 0;
	if (typeof v === "number") return v;
	if (typeof v === "string" && v.includes("/")) {
		const [num, den] = v.split("/").map(Number);
		return den ? Math.round((num / den) * 100) : 0;
	}
	return Number(v) || 0;
};

const f = dv.current();
const vals = ["body","mind","spirit","wealth"].map(k => parseVal(f[k]));
const valid = vals.filter(v => v > 0);
const avg = valid.length ? Math.round(valid.reduce((a,b)=>a+b,0)/valid.length) : 0;

// Update the frontmatter automatically (requires Templater or MetaEdit plugin)
try {
	await app.plugins.plugins["metaedit"].api.update("average", avg, f.file.path);
} catch (e) {
	console.warn("MetaEdit not available — skipping YAML update");
}

// Visual bar
const color = avg >= 80 ? "#4CAF50" : avg >= 50 ? "#FFC107" : "#F44336";
const filled = Math.round(avg/5);
const bar = `<div style="font-family:monospace;"><span style="color:${color}">${"█".repeat(filled)}</span>${"░".repeat(20 - filled)}</div>`;

dv.paragraph(`**Weekly Completion:** ${avg}%`);
dv.el("div", bar);