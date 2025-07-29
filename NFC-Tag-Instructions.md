# NFC Tag Project Instructions

This guide will show you how to program NFC tags to link to a **Slate Portal** or **vCard contact card**, making it easy for others to tap and instantly view contact information.

**Suitcase ID:** `c1e93c5d-b4e9-4781-9a70-6fb100639120:bmt`

---

## Supplies

Choose one or more NFC tag types based on your needs:

1. **Blank Black Business Card Type**  
   [Amazon Link](https://www.amazon.com/dp/B0DJX5MQM4?ref=nb_sb_ss_w_as-reorder_k0_1_8&crid=34W0EL27YC9GH&sprefix=nfc%2Btags&th=1)

2. **Sticker Coin Type (round stickers)**  
   [Amazon Link](https://www.amazon.com/NFC-Tag-Stickers-Rewritable-Compatible/dp/B0CNVZ6LPR)

3. **Key Tag Type**  
   [Amazon Link](https://www.amazon.com/Rewritable-Business-Programmable-Memory%EF%BC%8CCompatible-NFC21WHITE-10PCS/dp/B0F4JY21MR)

---

## App Required

Download the **NFC Tools app** (free) to your phone:

- **Android:** [Google Play Store](https://play.google.com/store/apps/details?id=com.wakdev.wdnfc&pcampaignid=web_share)
- **iPhone:** [Apple App Store](https://apps.apple.com/us/app/nfc-tools/id1252962749)

---

## Steps: Program NFC Tags (URL/Portal Link)

1. **Open the NFC Tools app** on your phone.
2. Tap **"Write"** from the main menu.
3. Tap **"Add a record"**.
4. Choose **"URL/Link"**.
5. Paste the **link to the Slate Portal or hosted vCard file**.  
   - Example:  
     `https://university.edu/contact-card?id=12345`
6. Tap **"OK"**.
7. Tap **"Write"**.
8. Hold the NFC tag near the back of your phone until you see the confirmation message.

### Tap Location Diagram
Most phones read/write NFC tags from the top-back area near the camera.  

![NFC Tap Diagram](https://upload.wikimedia.org/wikipedia/commons/thumb/d/de/NFC-Symbol.svg/200px-NFC-Symbol.svg.png)

---

## Alternative: Program NFC Tags with Direct vCard (No Portal)

If you want the tag itself to hold the contact card (instead of a URL):

1. In **NFC Tools**, choose **"Write"** > **"Add a record"** > **"Contact"** or **"Text Record"**.
2. Paste the vCard text:
   ```
   BEGIN:VCARD
   VERSION:3.0
   FN:Jane Doe
   ORG:Belmont University
   TITLE:Admissions Counselor
   TEL;WORK:(615) 460-8201
   EMAIL:jane.doe@belmont.edu
   END:VCARD
   ```
3. Tap **"OK"** > **"Write"** > hold the tag to your phone.

**Note:** NFC tags have small memory (144 bytes). If the contact info is long, use the **Portal URL method** above instead.

---

## Testing

1. Tap the programmed NFC tag with your phone.  
2. It should open the linked portal or prompt you to save the contact (if using a vCard).  

---

## Next Steps

- For counselors or staff, consider building a **Slate Portal that outputs a vCard** for each user.  
- Distribute NFC cards, stickers, or key tags to staff for use at events, school visits, and recruiting trips.
