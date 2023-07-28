# Bagelshoes-AnimalControl
Animal Control by Bagelshoes

Animal Control is a mod for 7 Days to die that removes certain amials from the game depending on what version is downloaded and used.

There are 7 versions of this mod. Here is a list of the versions and thier effects.
1. No Vultures
2. No Zombie Dogs
3. No Zombie Bears
4. No Vultures & No Zombie Dogs
5. No Vultures & No Zombie Bears
6. No Zombie Dogs & No Zombie Bears
7. No Vultures, No Zombie Dogs, & No Zombie Bears

Choose the appropriate version and install into your mods folder.

SPECIAL INSTRUCTIONS IF YOU ARE USING IMPROVED HORDES BY FILUNDERSCORE ONLY.

If you are using Improved Hordes by FilUnderscore you need to edit the hordes.xml file to completely remove the desired spawns.
In hordes.xml, which is located at 7DaysToDie/Mods/ImprovedHordes/config/ImprovedHordes/hordes.xml, The node named "wandering_animal_enemy" contains 4 groups.
Delete the group associated with the spawns you want removed. 
Example: In the following excerpt from hordes.xml you will see the "wandering_animal_enemy" node. If I only want to remove vultures I will remove the vultures group.

	<horde type="wandering_animal_enemy">
		<merge />
		<groups>
			<group name="Wolves" chance="0.1">
				<entity biomes="desert,snow" name="animalCoyote" minCount="1" maxCount="2"/>
				<entity biomes="pine_forest,burnt_forest" name="animalWolf" minCount="2" maxCount="4"/>

				<entity time="night" biomes="pine_forest,desert,wasteland,burnt_forest" name="animalDireWolf" minCount="1" maxCount="2"/>
				<entity biomes="snow" name="animalMountainLion" minCount="1" maxCount="2"/>
			</group>
   
			<group name="Bears" chance="0">                                                                             <---------------
				<entity biomes="pine_forest,snow" name="animalBear" minCount="1" maxCount="2"/>                            
					                                                                                                  Remove this section to eliminate bears.
				<entity time="night" biomes="wasteland,burnt_forest" name="animalZombieBear" minCount="1" maxCount="2"/>  
			</group>                                                                                                    <---------------
					
			<group name="ZombieDogs" chance="0">                                                                        <---------------
				<entity biomes="wasteland" name="animalZombieDog" minCount="1" maxCount="10"/>                            Remove this section to eliminate dogs
			</group>                                                                                                    <---------------
			
			<group name="Vultures" chance="0">                                                                          <-------------- 
				<entity biomes="wasteland,desert,burnt_forest" name="animalZombieVulture" minCount="1" maxCount="6"/>      
				                                                                                                          Remove this section to eliminate vultures.
				<entity biomes="wasteland" name="animalZombieVultureRadiated" minCount="1" maxCount="2"/>                  
			</group>                                                                                                    <--------------
   
		</groups>
	</horde>

Once the appropriate groups are removed save hordes.xml and enjoy.
