# Waypoints README

There is a proposal to adopt a replacement new format of South Island waypoints by GNZ / SRC.  This repo contains working files and SeeYou CUP waypoint files to support that activity.  The prior Lxxx and 3 digit turnpoint numbers will be removed and waypoints relabelled with a nationally unique four letter CODE and Name.

## Example

**Old Format** L748 Acheron House<br>
"L748 Acheron House","L748",NZ,4224.038S,17257.599E,719m,3,060,500m,,,1km SW of river junction on S side of river near bridge & buildings.,

**New Format** ACHE Acheron House<br>
"ACHE Acheron House","ACHE",NZ,4224.038S,17257.599E,719m,3,060,500m,,,1km SW of river junction on S side of river near bridge & buildings.,

## CUP File Standard Description
name,code,country,lat,lon,elev,style,rwdir,rwlen,rwwidth,freq,desc,userdata,pics
1. **name**: New format of four letter code followed a space and the common name
2. **code**: Four character code that meaningfully relates to the waypoint name and is unique within NZ
3. **country**: NZ
4. **lat**:	ddmm.dddS  For landout places this should be in the middle of the runway.
5. **;on**:  dddmm.dddE 	For landout places this should be in the middle of the runway.
6. **elev**: metres  The software converts to ft if that is the user’s chosen option
    -  EVERY waypoint including VRPs should have an elevation
    -	 Elevation for a landable waypoint (Style, 2,3,4, 5) is at the highest elevation of the landout so as to err on the safe side with any glide calculations to that waypoint.
7. **style**:  EVERY waypoint should have a Style
    - 0  Unknown (In NZ Let’s not use this)
    - 1  Waypoint
    - 2  Airport with Grass Runway.<br>
Glider can land here AND aerotow out (Suggested GNZ Convention)
Perhaps this also means that a glider can land in either direction ?
    - 3  Outlanding Place
Glider can land here BUT NOT aerotow out (Suggested GNZ Convention)
    - 4  Glider Site
NZKO, NZWP, NZDY, NZMA, NZCG, NZSD, NZHS, NZYP, NZPW, NZLE, NZTU, NZSF, NZOA
    - 5  Airport with Solid Runway
    - 6  Mountain Pass
    - 7  Mountain Top (NZ standard use for EVERY high point EVEN North Island hills).
    - 8  Sender
    - 9  VOR
    - 10  NDB
    - 11  Cooltower
    - 12  Dam
    - 13  Tunnel
    - 14  Bridge
    - 15  Powerplant
    - 16  Castle
    - 17  Road Intersection (In NZ use for Visual Reporting Points, VRP)
8. **rwdir** (for landouts  i.e. Style 2,3,4 or 5 ONLY)
    - ICAO Aerodromes use the **Magnetic Compass** directions as in AIP
        - Style 2, 3, 4 or 5 
        - NZOA Omarama should have runway dir 090 (currently 011)
        - Description should reference runway 09 / 27
    - NON ICAO landouts (e.g. airstrips etc) use **True Compass** direction (e.g.) 
	      - Style 2, 3, 4 or 5
        - e.g. OHAC Ohau Canal has rwdir 170 which is a True Compass direction.
9. **rwlen**: metres
    - required for Style 2,3,4 or 5
10. **rwwidth**: metres.  Helps large span gliders decide if it’s useable by them.
11. **freq**: radio frequency where required for landing
12. **description**: provides useful information about the waypoint in a consistent format and wording.
    - The description for landouts should be in 4 parts in the following order:
        1. Brief location / description aid
           - e.g. 1.5km N of Road Int
        2. %slope up to Cardinal True direction.
           - e.g.  Land 5% uphill to NW
        3. Special notes
           - e.g. Hazard (trees - power lines etc)
           - Approach between trees towards shed.
        4. Access / Retrieve information.
           - Poor phone reception. Aerotow ok.
           - Phone at Farm Office 1 NM South.
           - Padlock Code 4527 etc
    - ICAO Aerodromes
      - Runway vectors and circuit directions
      - Additional frequency information
      - AIP info regarding hazards / limitations etc. 
12. **userdata**:
13. **pics**:	hopefully to be used at a later date to provide say a landout picture.

