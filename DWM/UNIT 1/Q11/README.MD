Drill-Down Operation
• Purpose: Moves from summary to detail — it increases the level of granularity.
• How it works: You start from a higher-level summary (e.g., department-level sales) and move down to more detailed data (e.g., product-level sales).
• Example: In the cube hierarchy of a product dimension —
Department → Product Line → Category → Sub-category → Product
Drilling down would mean navigating from:
• Department → Product Line
• Product Line → Category
• Category → Sub-category
• Sub-category → Product
• Result: Each step down gives more specific and detailed sales figures. For example, drilling from Department-level sales (300,000) to Product-level sales (1,200).

⸻

Roll-Up Operation
• Purpose: Moves from detail to summary — it decreases the level of granularity.
• How it works: You begin with detailed data (e.g., individual product sales) and aggregate it to get summaries (e.g., total sales per department).
• Example: Moving up the same hierarchy:
• Product → Sub-category
• Sub-category → Category
• Category → Product Line
• Product Line → Department
• Result: Aggregated sales numbers increase as you move up, such as:
• Product (1,200) → Sub-category (5,000) → Category (15,000) → Product Line (60,000) → Department (300,000)
