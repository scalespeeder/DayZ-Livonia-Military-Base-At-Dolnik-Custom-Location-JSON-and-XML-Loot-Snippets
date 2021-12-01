DayZ Livonia Dolnik Military Base For Console and PC xml json Mod Instructions & Terms Of Use

Limited Testing on PC Livonia Local Server DAYZ Version 1.15 Dec 2021.

Created by @scalespeeder. Please report bugs & errors to scalespeeder@gmail.com with screenshots.

Many Thanks To Inclement Dab for his amazing DayZ Editor that makes this all possible: https://steamcommunity.com/sharedfiles/filedetails/?id=2250764298

TERMS OF USE
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS
OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN
AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH
THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Using these modded xml / json files and instructions could break the functioning of your DAYZ server, requiring a reinstall that would wipe
all player progress.

Using these modded files neccessitates increased regular restarts to prevent server crashing.

It is suggested you thoroughly test your server after applying these files to ensure proper
functioning of your server.

I always recomend you validate your files at: https://www.xmlvalidation.com/ and https://jsonformatter.curiousconcept.com/

Instructions:

Click the "Code" button and "Download Zip" on the Github Repository and extract the files on your local PC for access.

Ensure your DayZ Server has activated the cfggameplay.json. For console users on Nitrado Servers, go to "General Settings" on your server and tick "Enable cfggameplay.json".

On PC Servers add the following line to your serverDZ.cfg:

enableCfgGameplayFile = 1;

(On some PC servers, including Nitrado, the serverDZ.cfg is "hidden", so you need to enable "expert mode" in settings,
then go to "expert settings", which is the serverDZ.cfg. Stop the server before making changes this way.)

Upload "dolnik-military-base.json" from the extracted files to inside the "custom" folder of the mission directory on your server. This file places the structures on your map.
(If you haven't got a "custom" folder, create one.)

Open the cfggameplay.json file in the correct mission file for your server and look for the "objectSpawnersArr" line.

This file tells your server to access your custom file.

Edit it to look like this: 

	"objectSpawnersArr": ["custom/dolnik-military-base.json"]
	
If you already are calling custom jsons to spawn items, seperate the files like this:

	"objectSpawnersArr": ["custom/dolnik-military-base.json","custom/differentfile.json"]
	
Save your changes & upload if you need to.
	
Next we add loot to the structures by adding the following code snippet to the top of your mapgrouppos.xml file, after <map> 

	<!--Dolnik Base-->
	<group name="Land_Mil_Tent_Big1_1" pos="11550.099609 212.468994 509.079987" rpy="0.000000 0.000000 -54.170094" a="144.17"/>
	<group name="Land_Mil_Fortified_Nest_Small" pos="11433.799805 213.959000 567.995972" rpy="0.000000 0.000000 132.546967" a="-42.547"/>
	<group name="Land_Mil_Fortified_Nest_Small" pos="11422.099609 213.468994 560.322021" rpy="3.999999 0.000000 132.072006" a="-42.072"/>
	<group name="Land_Wreck_sed01_aban1_police" pos="11423.599609 213.492004 566.611023" rpy="0.000000 0.000000 0.000000" a="90"/>
	<group name="Land_Wreck_sed01_aban2_police" pos="11427.000000 213.785995 570.166016" rpy="0.000000 0.000000 90.224998" a="-0.224998"/>
	<group name="Land_Mil_Fortified_Nest_Watchtower" pos="11438.799805 214.276001 554.265991" rpy="0.000000 0.000000 132.547989" a="-42.548"/>
	<group name="Land_Medical_Tent_Big" pos="11508.316406 212.438965 441.741547" rpy="0.000000 0.000000 -51.314754" a="141.315"/>
	<group name="Land_Medical_Tent_Big" pos="11516.965820 212.444962 435.242096" rpy="0.000000 0.000000 -50.193741" a="140.194"/>
	<group name="Land_Medical_Tent_Shower" pos="11521.617188 213.961960 428.842407" rpy="0.000000 0.000000 -52.283722" a="142.284"/>
	<group name="Land_Mil_Tent_Big2_4" pos="11476.400391 214.759995 456.846008" rpy="0.000000 0.000000 130.164978" a="-40.165"/>
	<group name="Land_Mil_Tent_Big2_4" pos="11481.708984 214.611847 452.550507" rpy="-0.000000 -0.000000 127.825470" a="-37.8255"/>
	<group name="Land_Misc_Toilet_Mobile" pos="11484.015625 213.732620 443.750977" rpy="0.000000 0.000000 -136.476974" a="-133.523"/>
	<group name="Land_Misc_Toilet_Mobile" pos="11485.416016 213.730194 442.485992" rpy="0.000000 0.000000 -137.406998" a="-132.593"/>
	<group name="Land_Mil_Tent_Big1_1" pos="11582.099609 212.554291 386.902008" rpy="0.000000 0.000000 -174.535263" a="-95.4647"/>
	<group name="Land_Mil_Tent_Big2_1" pos="11565.730469 214.533127 398.834656" rpy="-0.000000 -0.000000 0.000000" a="90"/>
	<group name="Land_Mil_Tent_Big1_1" pos="11591.477539 212.410614 396.399506" rpy="-0.000000 -0.000000 178.163528" a="-88.1635"/>
	<group name="Land_Mil_Tent_Big2_1" pos="11572.213867 214.469528 406.859467" rpy="-0.000000 -0.000000 0.000000" a="90"/>
	<group name="Land_Mil_Fortified_Nest_Watchtower" pos="11714.000000 222.358994 449.145996" rpy="-0.500000 -9.000000 -135.563995" a="-134.436"/>
	<group name="Wreck_UH1Y" pos="11575.400391 218.460999 528.065002" rpy="-6.500000 0.000000 -44.000000" a="134"/>
	<group name="Land_Mil_Tent_Big1_1" pos="11572.605469 213.328415 482.556671" rpy="-0.000000 -0.000000 0.000000" a="90"/>
	<group name="Land_Mil_Tent_Big1_1" pos="11580.700195 213.552994 475.126007" rpy="-2.500000 3.000000 0.000000" a="90"/>
	<group name="Land_Mil_Tent_Big1_1" pos="11589.099609 213.632996 467.200012" rpy="0.000000 4.999999 0.000000" a="90"/>
	<group name="Land_wreck_truck01_aban2_orange" pos="11526.700195 212.216995 483.434998" rpy="0.000000 0.000000 -66.441704" a="156.442"/>
	<group name="Land_wreck_truck01_aban1_blue" pos="11517.200195 212.235992 488.041992" rpy="0.000000 0.000000 0.000000" a="90"/>
	<group name="Land_wreck_truck01_aban2_green" pos="11439.329102 212.512085 562.765991" rpy="-0.000000 -0.000000 127.550514" a="-37.5505"/>
	<group name="Land_wreck_truck01_aban2_green" pos="11447.318359 212.301086 557.137329" rpy="-0.000000 -0.000000 126.655472" a="-36.6555"/>
	<group name="Land_wreck_truck01_aban2_blue" pos="11455.020508 212.085846 551.337341" rpy="-0.000000 -0.000000 125.501854" a="-35.5019"/>
	<group name="Land_wreck_truck01_aban1_green" pos="11463.307617 211.853958 545.461914" rpy="-0.000000 -0.000000 132.377518" a="-42.3775"/>
	<group name="Land_wreck_truck01_aban1_green" pos="11470.050781 212.039810 535.960144" rpy="-0.000000 -0.000000 140.750595" a="-50.7506"/>
	
Save your changes & upload if you need to.

Restart your server and the new structures will appear immediatly, and then they will slowly stock with loot.

Thanks, Rob.
