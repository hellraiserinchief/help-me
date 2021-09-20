* G28
* G29 P1          ; Automatically probe accessible area
* G29 P3          ; Fill un-probed areas with reasonable values - may need to be repeated
* G26             ; Start test print / validation process
* M421 ... Qx.xx  ; Direct edit mesh point, using offset
* G29 S1          ; Save to slot 1, return to G26 for further refinement.

G29 Px T : see mesh as it is created
G29 T : look at mesh