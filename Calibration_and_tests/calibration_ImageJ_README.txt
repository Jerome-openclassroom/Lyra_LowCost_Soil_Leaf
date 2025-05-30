📝 Instructions for the `calibration_ImageJ.txt` file:

This file contains a **custom calibration scale** for ImageJ, based on my own scanner. The values might differ from yours depending on your device and scanning conditions.

**Example:**
249.844	69.03
This means that a **ROI** (Region Of Interest — the selected area you define in ImageJ) with a **grey value of 69.03** corresponds to a **green density of 249.844** (on my scanner).

There are **10 such value pairs** included in the file, which allows you to perform a **polynomial fit** over the standard range of measurement. (See the `polynomial_fit.png` image for an example.)

🔧 If you don’t have a calibrated green scale:

- You can **print a reference color chart** (many are freely available online) and **measure it with a handheld densitometer** — try asking someone in the printing or graphic arts industry.

- Alternatively, if you don’t have access to such tools, you can give this file to **GPT-4 or any recent multimodal LLM** and ask it to estimate a green density scale **based on the values in the file**.  
  *I’ve tested this — with some trial and error, it worked surprisingly well!*
