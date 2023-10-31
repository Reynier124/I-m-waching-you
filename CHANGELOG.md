# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.4.1] - 2023-10-18

### Added

- Added new method in the class "Scrabble" named "get_current_player_id" and is self explanatory

### Changed

- Changed README to more complete instructions

### Fixed

- Fixed problem with the test "test_play_game"
- Fixed problem with a print on the tests

## [0.4.0] - 2023-10-16

### Added

- Added 6 new methods to the class "Main" named "player_action", "quite_game", "get_word_location_orientation", "validate_and_put_word", "convert_tiles_in_another_tile" and "convert_wildcard_into_tile". These methods are for refactoring or are self explanatory

- Added 3 new methods to the class "Scrabble" named "clean_word_to_use", "comprobate_is_an_int" and "comprobate_is_an_orientation". Again these methods are for refactoring or are self explanatory

- Added new method to the class "Dictionary" named "remove_accents".

- Added new method to the class "Board" named "get_validation_of_another_board". This method will simulate the same "structure" of the method "validate_words_around" in another board but with the difference that now will put the word and corroborate if another word is created

- Added new attribute and method to the class "Cell" named "reset_cell". These attribute will save the state of the cell so the method "reset_cell" will be able to reset the cell to the original state

- Added new class named "Converter" and your function is convert anything is needed for any class

- Added 2 new methods to the class "Converter" named "word_to_false_cells" and "result_to_list_of_words". These 2 are to specific methods and are to facilitate and refactorized your respective methods

- Added a new class called "Tools" and its function is to have all the specific actions that do not need to import anything from another class (actually it is to avoid circular import)

- Added new method for the class "Tools" named "move_pointer". This is self explanatory

- Added 5 new methods for the class "Miscellaneos" named "check_cells_before_horizontal", "check_cells_before_vertical", "check_cells_after_horizontal", "check_cells_after_vertical" and "find_words_in_directions". All of these methods are to refactorized "validate_words_around" (Are more of them in other classes)

### Changed
Practilly change everything except for the class "Tile" and "Cell" (This is in a nutshell)

- In player only change a .append to .insert because is more understandable

- Uppdate the method "put" and "initial_tiles" of the class "Bagtiles". "put" now will accept tile and not only a list of tile and now "initial_tiles" work correctly

- The majority of the methods to the class "Miscellaneos" were move for another classes. The next method move to the class "Converter": "string_to_tiles", "especial_to_tiles", "converter_word_to_tiles", "converter_locations_to_positions" and "converter_word_to_cells". The next method move to the class "Tools": "is_active_and_letter_multiplier", "is_active_and_word_multiplier", "format_placed_word_cell", "format_active_cell", "format_cell_contents", "format_multiplier", "filter_reapeted_column" and "filter_reapeted_row"

- All methods that started with "check..." in the class "Board" are moved to the class "Miscellaneos" and now are refactorized.

- Change the "all_words.txt" to "all_words_cleaned.txt" because the new one i remove accents, dieresis and all the letter of the file "all_words.txt" so is more easy to use

- Change the README. Now is more beautiful

- In the class "Scrabble": was add validate_words_around in the method "validate_word" and change the method "calculate_score" and now it calculates the words that the player forms residually

### Fixed

- Fixed one problem with the method "put_tiles_in_rack" that never allowed the number of tiles in the bag to reach 0

- Fixed one problem with "initial_tiles" where the distribution are totally wrong

## [0.3.9] - 2023-10-11

### Added

- Added configuration to the docker file
- Added explanation to play the scrabble game
- Added test to the method "validate_words_around"
- Added new method to the class "Dictionary" named "verify_word_list" and is self explanatory
- Added new 2 methods to the class "Miscellaneos" named "filter_reapeted_column" and "filter_reapeted_row". These method is for the method "validate_words_around" and is essencial for this method
- Added news tests for the class "Main" (Just a little)

### Changed

- Complete the method "validate_words_around" of the class "Board"
## [0.3.8] - 2023-10-10

### Added

- Added 5 new methods for the class "Board" named "check_cells_before", "check_cells_after", "check_tiles_around_word_horizontal", "check_tiles_around_word_vertical" and "validate_words_around". All of these don't have tests for now
- Added 3 new methods for the class "Miscellaneos" named "get_cell_around_word_horizontal", "get_cell_around_word_vertical" and "verify_cell_around_word". All of these have test
- These methods are were created with the objective of create a method to validate the intersecion between multiple words

## [0.3.7] - 2023-10-09

### Added

- Added 3 new methods for the class "Main" named "player_play", "change_wildcard_to_tile" and "get_tiles_to_full_rack". "player_play" is a menu to put_words, reorganize your tiles, exchange your tiles, etc. "change_wildcard_to_tile" will convert the wildcard to another tile you want and "get_tiles_to_full_rack" will send tiles to the player who needs it

### Changed

- Update the next 4 methods "check_right_letters", "validate_word_horizontal", "validate_word_vertical" and "validate_word_place_word" for the class "Board". Now are more efective and more efficient
- Also update the method "compare_tiles_and_letters" with the same purpose
- Update "place_word", "show_board" and "play_game"

## [0.3.6] - 2023-10-08

### Added

- Added 2 new methods for the class "Tile" named "is_wildcard" and "convert_tile". The first one is self explanatory and the second one will convert a tile in another one
- Added 2 new methods for the class "Player" named "has_wildcard" and "find_wildcard". These methods are self explanatory
- Added new method for the class "Scrabble" named "convert_wildcard" and this will convert a wildcard in another tile

### Changed

- Now the method "show_rack" is in the class "Main"

### Removed

- Removed the method "display_rack" for the class "Player" and the method "show_rack" for the class "Scrabble" because are problematic and unnecesary

## [0.3.5] - 2023-10-08

### Added

- Added test to the method "descount_tiles_to_player" of the class "Scrabble" and a new test for the method "validate_place_word" of the class "Board"

### Fixed

- In too many methods of the class Board named the column in row and row in column so i fixed that

### Changed

- I changed a little the class "descount_tiles_to_player"

## [0.3.4] - 2023-10-07

### Added

- Added 2 methods for the class "Miscellaneos" named "get_tiles_for_word_placement" and "tiles_needed_to_form_word" and your function is get a list of tiles that will need the player to form the word
- Added new method for the class "Scrabble" named "descount_tiles_to_player". This will discount the tiles to the player for form the word and for now don't work your tests

### Change

- Move the method "deactive_cell" of the class "Miscellaneos" to the class "Cell" for obvious reasons

### Remove

- Finally remove the next 2 methods: "display_board" and generate_row_string"

## [0.3.3] - 2023-10-07

### Added

- Added tests for the majority of the methods of the class "Main". The only ones who don't have test is because i don't have much idea of how will be these methods

### Changed

- Changed a little the method take_turn for the class "Main" for less cognitive complexity but i regretted so in the future will be factorized

###  Remove

- Removed the method "show_scores" of the class "Scrabble". This is because only in the class "Main" should have print

### Deprecated

- "display_board" and generate_row_string" in the next commit will be eliminate and will be useful for another method that will change the status of the cell when you put a word

## [0.3.2] - 2023-10-06

###  Added

- Added "test.sh" this is for have codeclimate local
- Added 2 new methods and new attribute for the class "Main". These methods are named "initial_tiles" and "show_board", the first one  will put tiles in the rack of all players and put 100 tiles in the bag and the second one will show the board to the player. The attribute is the board of the game
- Added new method to the class "Cell" named "__repr__" and is how will show the cell in the print and use colorama
- Added new method fot the class "Scrabble" named "get_board" and is self explanatory

### Changed

- Changed "all words.txt" because it had no conjunctions

### Remove

- Remove the method "show_board" to the class "Scrabble"

### Deprecated

- The next 2 methods for now are useless: "display_board" and "generate_row_string". Will stay in code for a time in case if something of your code is useful if not will be remove

## [0.3.1] - 2023-10-03

###  Added

- Added 4 new methods for the class "Main" named "exchange_tiles", "reorganize", "add_score", "placed_word".

### Changed

- Now these methods: "take_turn", "next_turn", "display_final_scores" and "play_game" they already work

## [0.3.0] - 2023-10-02

###  Added

- Added a new method for the class "Player" named "display_rack". This will show the rack
- Added 9 new method for the class "Scrabble" named "show_board", "show_rack", "put_word", "show_scores", "show_amount_tiles_bag", "shuffle_rack", "game_over", "put_tiles_in_rack" and "put_initial_bag". All of this method are self explanatory and very easy to create because the only function of these methods are to comunicate all the code with an future main

### Changed

- Changed named of the method "put_words" to the class "Board" to "put_words_board" because it is a name more discritible
- Changed the method "validate_word" to the class "Scrabble". Now this method will be more aware of more factors like the dictionary, if the board is empty, if already is a another word, etc

### Fixed

- Fixed one problem with the method "display_board". This problem don't allow show the board modify and now is possible

## [0.2.9] - 2023-10-02

###  Added

- Added new method to the class "Miscellaneos" named "converter_word_to_cells" This method will be useful to facility the use of the method "calculate_word_value"
- Added new attribute "id" to the player for the future "Main"
- Added 4 new method to the class "Main" named "show_current_player", "take_turn", "next_turn" and "display_final_scores". For now this method does absolutly nothing but if for orientation and guide in the constructuion of the main

### Changed

- Changed some things about the class "Player" and "Scrabble" in order to add the attribute id
- "Optimized" the method "valid_player_count". Now ocupied less lines
- Now don't work the tests of the class "Main" because of the multiple changes and, for now, won't have tests

## [0.2.8] - 2023-10-02

###  Added

- Added new method for the class "Board" named "generate_row_string". This method is for factorized the another method named "display_board"
- Added new 6 methods for the class "Miscellaneos" named "format_placed_word_cell", "format_active_cell", "format_cell_contents", "format_multiplier", "deactivate_cell" and "converter_locations_to_positions". These methods are to factorized "display_board" and "converter_locations_to_positions" to facility the use of the method in the future

### Changed

- Factorized the method "display_board" to the class "Board"

## [0.2.7] - 2023-10-01

###  Added

- Added new method in the class "Board" named "display_board". As your name indicate will show the board to the player and for now don't have tests. Will be modify in the future because have too much cognitive complexity
- Added colorama into requirements.txt

## [0.2.6] - 2023-10-01

### Added

- Added new class named "Miscellaneos". This class will save methods that don't fit too much with your respective class

###  Changed

- Moved 5 methods of the class "board" at the class "Miscellaneos". These methods are: "string_to_tiles", "special_to_tiles", "converter_word_to_tiles", "calculate_word_value" and "compare_tiles_and_letters" and your test to "test_miscellaneos"
- Modifed the tests to work with the new structure

## [0.2.5] - 2023-09-30

###  Changed

- Refactored 3 methods, 2 of the class "Board" and 1 of the class "Player". These methods are: "string_to_tiles", "converter_word_to_tiles" and "has_letters"
- Modified the class "Dictionary" because had code out of the class

### Remove

- Removed the method "remove_accents" of the class "Dictionary" because was unnecesary

## [0.2.4] - 2023-09-30

###  Added

- Added new method for the class "Board" named "put_words". This method will put letter for letter in your respective cell

### Changed 

- Moved many methods of the class "Scrabble" to the class "Board". This method are: "string_to_tiles", "especial_to_tiles" and "converter_word_to_tiles"

## [0.2.3] - 2023-09-30

###  Added

- Added new attribute for the class "Player" named score. This is self explanatory
- Added new method for the class "Scrabble" named "calculate_score". This will add the score you get

## [0.2.2] - 2023-09-29

###  Added

- Added 2 method for the class "Scrabble" named "special_to_tiles" and "converter_word_to_tiles". "converter_word_to_tiles" will converter any word into a list of tiles and now "string_to_tiles" and "especial_to_tiles" is used to factorized
- Added new tests for the new methods

### Changed

- Now the method "string_to_tiles" is used to factorized the method "converter_word_to_tiles"
- Changed the tests of the method to "string_to_tiles" for test "converter_word_to_tiles"

### Removed

- Removed some test of the "string_to_tiles" because now are obsolete

## [0.2.1] - 2023-09-28

###  Added

- Added new method for the class "Scrabble" named "string_to_tiles". This will pass one word into a list of tiles and this will use in the future for another method
- Added tests for the new method

## [0.2.0] - 2023-09-27

###  Added

- Added new method for the class "Player" named "has_letters". This will validate if the player has the tile in your rack to form the word

## [0.1.9] - 2023-09-23

###  Added

- Added in the contructor the multiplier of the board and your tests
- Added a new method for the class "Board" named "put_multipliers". This will receive a list of list to put the multipliers in the cell

## [0.1.8] - 2023-09-22

###  Added

- Added new method in the class "Board" named check_conditions and is used for solved problem with code duplicity

### Changed

- Refactored the method "word_in_the_center"(again)

### Fixed

- Solved another 2 new problems with code duplicity, one in the method "validate_word_horizontal" and "validate_word_vertical" and the another one in "word_in_the_center"

### Removed

- Removed the method "word_in_the_center_vertical" and "word_in_the_center_horizontal" for unnecesary and problematic

## [0.1.7] - 2023-09-21

###  Added

- Added 5 new methods for the class "Board" named "word_in_the_center_horizontal", "word_in_the_center_vertical", "compare_tiles_and_letters" and "check_right_letters". All of them are used for factorized and one of them will use in the future for another thing
- Added new tests for the class "Board"

### Changed

- Refactored the method "word_in_the_center"
- Refactored the method "validate_word_horizontal"
- Refactored the method "validate_word_vertical"

### Fixed

- Solved problem with code duplicity in the method "validate_word_horizontal" and "validate_word_vertical"

## [0.1.6] - 2023-09-20

###  Added

- Added 3 new methods for the class "Board" named "word_in_the_center", "validate_word_horizontal" and "validate_word_vertical".
- "word_in_the_center" will check if the word of the player will be in the center
- "validate_word_horizontal" will check if the word of the player will use the tile of the another player in the form horizontal
- "validate_word_vertical" will check if the word of the player will use the of the another player in the form vertical
-  Added new tests for the class "Board"
- Now the method "validate_word_place_board" is complete

### Changed

- Refactored the method "validate_word_place_board" for less cognitive complexity

### Fixed

- Fixed one problem with the method "validate_word_inside_board" and some of your test. This method recieve one location like that: (7,4) and 7 is the column and 4 is the row but in the method is the other way so i fixed that

## [0.1.5] - 2023-09-19

###  Added

- Added new method for the class "Board" named "validate_word_place_board". the idea is the method "validate_word_place_board" check if is possible put the tile. For now only work one part and the other part will be finish soon and will add new tests for this method

## [0.1.4] - 2023-09-14

###  Added

- Added new method for the class "Board" named "is_empty" your tests. "is_empty" comprobate if the board is empty

### Changed

- Changed some name of variables in the method "validate_word_inside_board" to more legible

## [0.1.3] - 2023-09-11

###  Added

- Added new method for the class "Main" named "valid_player_count" and your only propurse is down the cognitive complexity of the method "get_player_count"

### Changed

- Refactored the method "get_player_count" of the class "Main" for less cognitive complexity (again)
- Refactored the method "initial_tiles" of the class "BagTiles" for less cognitive complexity 

## [0.1.2] - 2023-09-10

###  Added

- Added new class named "Dictionary" and this will be verify if exist the word in the dictionary.
- Added methods for the class "Dictionary" named "verify_word" and "remove_accents". "verify_word" will be compare the word with the file "all_words" and if exist then return True and "remove_accents" don't do nothing for now

### Changed

- Refactored the method "get_player_count" of the class "Main" for less cognitive complexity

## [0.1.1] - 2023-09-09

###  Added

- Added new method for the class "Scrabble" named "validate_word". This is only for connect scrabble with another method of the class "Board"
- Added new method for the class "Board" named "validate_word_inside_board". This will check is if possible to put the word in the board.
- Added new 2 attributes for the new class "Main" named "player_count" and "game". "player_count" will recive of the user the number of player will play the game through the method "get_player_count" and game is an instace for the class "Scrabble"
- Added new 2 method for the new class "Main" named "get_player_count" and "play". "get_player_count" will ask how many players are and only accept a value between 2-4 and "play" will control the turns

### Changed

- Now main is a class and with this now have attributes and methods.

## [0.1.0] - 2023-09-08

###  Added

- Added the mechanics of the turns in the main
- Finally added tests for the main

### Changed

- Now the function "calculate_word_value" is a method for the class "Board" and your tests now is in "test_board.py".

### Removed

- Because of the change of "calculate_word_value" is eliminated 2 files: "calculate_word_value.py" and "test_calculate_word_value.py"

## [0.0.9] - 2023-09-07

###  Added

- Added Dockerfile and your configure
- Added new function and tests for the method "next_turn" for the class "Scrabble"
- Added new attribute for the class "Scrabble" named "current_player". This attribute will show who is the player of this turn

## [0.0.8] - 2023-09-02

###  Added

- Added new attribute for the class "Scrabble" named "turn". "turn" will count the total of turns of the game
- Added 2 new method for the class "Scrabble" named "playing" and "next_turn". "playing" the only thing will do is return true with the objetive to finish the game and "next turn" increment for 1 the attribute of turn
- Added the function "main". This will be the interface of the game and for now doesn't have tests and doesn't do too much
- Added integration with CodeClimate

## [0.0.7] - 2023-08-30

###  Added

- Added new attribute a the class "Cell" named "status". "status" is 'activate' o 'deactivate' and depend of the status if the multiplier aplicated
- Added new function named "calculate_word_value". This calculate the value depend of the multiplier and the status of the cell

### Fixed

- In some many times the attribute of the class "Cell" is named with multiplayer and this is wrong, is multiplier.

## [0.0.6] - 2023-08-29

###  Changed

- Added new attribute to the class "Scrabble" named "gameid". The "gameid" is a id with the objetive to, in the future, view past game for very motives you want
- Finally added the joker tile, but still is not work how is intendeed because still don't program the interface

## [0.0.5] - 2023-08-28

###  Changed

- The method "get_tiles" now work differently because is only one bag for game and not for player
- The method "exchange_tiles" now work differently because is only one bag for game and not for player. Besides now the player select the tile they wanted and receive one tile random

## [0.0.4] - 2023-08-28

###  Changed

- The method "initial_tiles" of the class "Player" now is in the class "BagTiles" this is because in the game only is one bag and not every player have one bag

### Removed

- The attribute "name" of the class "Player" is remove because is unnecessary
 
## [0.0.3] - 2023-08-27

### Added

- Added new 2 methods for "player" and yours tests
- The new 2 methods are: "get_tiles" and "exchange_tiles". In the class "get_tiles" the player recive random tiles for you bag and "exchange_tiles" eliminate the oldest tile of the bag of the player a recive a new random tile

## [0.0.2] - 2023-08-27

### Added

- Added new methods, attribute and tests a the class "player".
- The new optional attribute is "name" and is self explanatory
- The 2 methods are: "change_name" and "initial_tiles". The method "change_name" is self explanatory and "initial_tiles" this is going to send to the player all 98 tiles (for now not exist the joker tile) to be able to begin of the game

## [0.0.1] - 2023-08-27

### Added

- For now is grouped in two module: "Game" and "Tests"
- Definition of the class "Tile" and your tests
- Definition of the class "BagTiles" and your tests
- BagTiles have 2 metods: "take" and "put". Take will retire tiles in the bag and put will input tiles in the bag
- Definition of the class "Player" and your tests
- Player have 2 attributes for now: name and tiles. "Name" is the identificator of the player and "tiles" is the amount of tiles for the player
- Player have 1 method: "initial_tiles". This is going to send all of the 98 initial tiles for the beginnig of the game
- Definition of the class "board" and yours tests
- Definition of the class "cell" and yours tests
- Definition of the class "scrabble" and yours tests
- "cell" have 2 methods: "add_letter" and "calculate_value". "add_letter" is self explaining and "calculate_value" is the calculation of the value and the multiplication of the cell.
