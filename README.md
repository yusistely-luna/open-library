# 📚 Open Library — Search & API Testing

**Manual Testing · Web · API** — Personal QA Project (2026)
> 🚧 In Progress

---

## 🎯 Problem

QA of the search feature on [openlibrary.org](https://openlibrary.org/search): manual testing of the web search experience across browsers, and separate API-level testing of the underlying search endpoint. This is a self-directed project — designed and scoped independently, outside the bootcamp curriculum, to practice test design on a real public API.

---

## 📍 Status

| Area                      | Status          |
| --------------------------- | ----------------- |
| Web test case design         | ✅ Done (16 cases) |
| Web test execution           | 🚧 In progress (1 of 16 executed) |
| API test case design         | ✅ Done (20 cases) |
| API test execution           | ⬜ Not started    |
| Bug reporting                 | ⬜ Not started    |


---

## 🎯 Scope (Web — Search Feature)

**URL under test:** `openlibrary.org/search`
**Environments:** Chrome (desktop) and Safari (desktop)

16 test cases designed across four categories:

| Category                | Cases | Focus |
| -------------------------- | ----- | ------- |
| Basic Search                | 3     | Title, author, and exact ISBN search |
| Equivalence / Boundary      | 6     | Empty query, whitespace, special characters, 500-char string, numeric-only input, accented characters |
| Security-Aware              | 2     | Script/HTML injection, SQL-injection-style input |
| UI / Functional              | 5     | Search bar visibility, autocomplete, pagination, sort/filter, result navigation |

---

## 🎯 Scope (API — Search Endpoint)

**Endpoint under test:** `GET openlibrary.org/search.json`
**Tool:** Postman

20 test cases designed across six categories:

| Category                | Cases | Focus |
| -------------------------- | ----- | ------- |
| Basic Search                | 3     | Title, author, and ISBN search via `q`, `author` parameters |
| Equivalence / Boundary      | 7     | Empty query, no parameter, whitespace, special characters, 500-char string, numeric-only input, accented characters |
| Boundary — Pagination        | 3     | `page=0`, negative page, page number far past the last result |
| Boundary — Limit              | 2     | `limit=0`, very high limit value |
| Security-Aware               | 2     | Script injection, SQL-injection-style input |
| Response Structure           | 2     | Presence of `numFound`/`docs`, correct fields per book |
| Performance                  | 1     | Response time for a normal search |

---

## ⚙️ What's Done So Far

- Designed 16 web test cases spanning functional, boundary, and security-aware scenarios for the search UI
- Designed 20 API test cases for the search endpoint, covering the same kind of boundary and security input as the web cases, plus pagination, response limits, and response-structure checks that only make sense at the API level
- Structured the web checklist to track results per browser (Chrome / Safari) side by side
- Structured the API checklist to track actual response, status code, status, severity, and bug link per case

---

## 🔜 Next Steps

- Execute the remaining 15 web test cases across both browsers and log actual results
- Execute the 20 API test cases in Postman and log actual results
- File and track any defects found
- Add a results summary once execution is complete
- Optional: add a small set of cross-check cases that compare a specific API response against what the browser actually renders for the same query — that would be the point where this becomes a genuine end-to-end test rather than two parallel test efforts

---

## 🛠️ Skills

Manual Testing · Web Testing · API Testing · Postman · Cross-Browser Testing · Equivalence Partitioning · Boundary Value Analysis · Security-Aware Testing · Test Case Design

---

## 📁 Project Structure

- `Open_Library_Test_Cases.xlsx` — test case checklist for the search feature (web), in progress
- `Open_Library_API_Test_Cases.xlsx` — test case checklist for the search endpoint (API), not yet executed
