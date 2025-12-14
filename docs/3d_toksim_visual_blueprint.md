# 3D-TokSIM Visual Blueprint

This document records the finalized visual blueprint prompt for rendering the 3D-TokSIM architecture diagram. The prompt is enclosed between BEGIN/END markers so it can be copied directly into an image-generation workflow without additional formatting.

---BEGIN PROMPT---

[Visual Schema Blueprint]

Art Style: Professional academic architecture diagram. Flat vector graphics with clean thin outlines and soft pastel fills (Azure Blue, Slate Grey, Coral Orange, Mint Green). White background. No shadows, no 3D effects, clean sans-serif font (e.g., Roboto Bold).

Layout: A three-tier vertical hierarchy. The entire diagram depicts a hardware accelerator named "3D-TokSIM".

Zone 1 (Top Tier - Memory Layer):

Container: A wide, thick horizontal rectangle at the top, colored Slate Grey, with a subtle texture of a fine grid.

Visual Structure: The rectangle represents a slab. From its bottom, multiple (e.g., 12) thin, vertical silver cylinders (Through-Silicon Vias) extend downward to connect to the tier below.

Key Text Labels (to render inside image): "3D High-Bandwidth DRAM", "Hybrid Bonding (HB) TSVs"

Zone 2 (Central Tier - Compute Layer):

Container: A large rectangular panel directly below Zone 1, spanning the width of the image. It is internally divided into four adjacent, connected rectangular blocks.

Visual Structure (Left to Right):

Input Buffer: A vertical rectangle (Azure Blue). Contains a small vertical stack of 3-4 small Mint Green squares entering from the left.

Drafting CIM: A square block. Its background is a fine, light grey grid of dots (SRAM array). A large, circular Coral Orange arrow overlays it, indicating stationary data flow. It outputs a horizontal sequence of 6-8 Mint Green squares.

Verification CIM: A wider rectangle. Background is the same SRAM grid. Inside, four parallel, thick Coral Orange arrows strike through the grid horizontally, processing the incoming token stream in parallel.

Output Buffers: A two-part structure.

Top: A wide, horizontal "FIFO Buffer" (Azure Blue) divided into 3 sections, each holding a Mint Green square.

Bottom: A smaller, separate "Rejection Buffer" (light Slate Grey).

Key Text Labels (to render inside image): "Logic Die", "SRAM-based Compute-in-Memory (CIM)", "Drafting CIM", "Verification CIM", "Speculative Tokens", "Parallel Verification", "Accepted Tokens", "Rejected Tokens", "Token-Stationary Dataflow"

Zone 3 (Bottom Tier - Control & Output):

Container: A narrow horizontal strip at the bottom.

Visual Structure: A light-grey rounded rectangle in the center labeled "Control Logic". Thin, grey dashed lines extend from it upward into Zone 2. To its right, a single, final Mint Green square exits the frame via a bold rightward arrow.

Key Text Labels (to render inside image): "Controller", "Verified Output Token"

Connections (to render as arrows/lines):

A thick bundle of parallel, straight, Coral Orange arrows flows down from the bottom of the TSVs in Zone 1 into the Drafting CIM block in Zone 2. Label this arrow bundle: "High-Bandwidth Parallel Access".

A solid Mint Green arrow flows from the Input Buffer to the Drafting CIM.

A thick, dashed Mint Green arrow flows from the Drafting CIM to the Verification CIM, carrying the "Speculative Tokens".

A single, curved Coral Orange arrow loops from the Verification CIM back to the Input Buffer. Label: "Feedback Loop (Re-sampling)".

Straight Mint Green arrows carry "Accepted Tokens" from Verification CIM to the FIFO Buffer.

A thin grey arrow carries "Rejected Tokens" from Verification CIM to the Rejection Buffer.

A final, bold flow arrow carries the "Verified Output Token" from the FIFO Buffer, past the "Controller", and out of the frame.

---END PROMPT---
