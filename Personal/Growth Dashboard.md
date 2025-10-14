**Live overview of your 6-month roadmap progress**

---

## 🔹 Weekly Completion Summary
```dataview
TABLE week AS "Week", phase AS "Phase", focus AS "Focus", average AS "Avg %"
FROM #weekly-review
SORT week ASC
```

---

## 🔹 Average Progress by Pillar

```dataviewjs
// --- Helper: Parse any kind of input into a number (handles 5/7, "60", null, etc.)
const parseVal = v => {
	if (v == null) return 0;
	if (typeof v === "number") return v;
	if (typeof v === "string") {
		if (v.includes("/")) {
			const [n, d] = v.split("/").map(Number);
			return d ? (n / d) * 100 : 0;
		}
		const num = Number(v.replace(/[^0-9.]/g, ""));
		return isNaN(num) ? 0 : num;
	}
	return 0;
};

// --- Grab all weekly-review notes ---
const pages = dv.pages("#weekly-review").array(); // force to array

// --- Defensive average calculation ---
const getAvg = key => {
	const vals = pages
		.map(p => parseVal(p[key]))
		.filter(v => typeof v === "number" && !isNaN(v));
	return vals.length ? vals.reduce((a,b)=>a+b,0)/vals.length : 0;
};

const avgBody = getAvg("body");
const avgMind = getAvg("mind");
const avgSpirit = getAvg("spirit");
const avgWealth = getAvg("wealth");
const overall = (avgBody + avgMind + avgSpirit + avgWealth)/4;

// --- Color logic + bar generator ---
const getColor = val =>
	val >= 80 ? "#4CAF50" : val >= 50 ? "#FFC107" : "#F44336";

const makeBar = val => {
	const color = getColor(val);
	const filled = Math.round(val / 5);
	return `<div style="font-family:monospace;">
	<span style="color:${color}">${"█".repeat(filled)}</span>${"░".repeat(20 - filled)}
	</div>`;
};

// --- Render table ---
dv.table(
	["Pillar", "Avg %", "Progress"],
	[
		["🏋️‍♂️ Body", `${Math.round(avgBody)}%`, makeBar(avgBody)],
		["🧠 Mind", `${Math.round(avgMind)}%`, makeBar(avgMind)],
		["🙏 Spirit", `${Math.round(avgSpirit)}%`, makeBar(avgSpirit)],
		["💰 Wealth", `${Math.round(avgWealth)}%`, makeBar(avgWealth)],
		["🌱 Overall Avg", `${Math.round(overall)}%`, makeBar(overall)]
	]
);
```

---

## 🔹 Reflection Log

```dataview
LIST
FROM #weekly-review
WHERE contains(file.tags, "weekly-review")
SORT week DESC
```

---

## 🔹 Notes

Use this section to summarize insights every few weeks.

Patterns noticed:

Areas of growth:

Course corrections:


---