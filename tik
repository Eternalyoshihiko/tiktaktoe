
game = [[0, 0, 0],
        [0, 0, 0],
        [0, 0, 0], ]


def win(current_game, won = False):

    for row in game:
        if row.count(row[0]) == len(row) and row[0] != 0:
            print(f"Player {row[0]} is the winner Horizontally -")
            won = True
            return won

    for col in range(len(game)):
        check = []
        for row in game:
            check.append(row[col])
        if check.count(check[0]) == len(check) and check[0] != 0:
           print(f"Player {row[0]} is the winner Verticlly |")
           won = True
           return won

    diags = []
    for ix in range(len(game)):
        diags.append(game[ix][ix])
    if diags.count(diags[0]) == len(diags) and diags[0] != 0:
        print(f"Player {diags[0]} is the winner Side \\")

    diags = []
    for col, row in enumerate(reversed(range(len(game)))):
        diags.append(game[row][col])
    if diags.count(diags[0]) == len(diags) and diags[0] != 0:
        print(f"Player {diags[0]} is the winner Side /")


def game_board(game_map, player=0, row=0, column=0, just_display=False):
    try:

        if not just_display:
            if game_map[row][column] == 0:
                game_map[row][column] = player
                print("   A  B  C")
                for count, row in enumerate(game_map):
                    print()
                    return game_map
            else:
                print("   A  B  C")
                print("try another spot")
                for count, row in enumerate(game_map):
                    print()
        else:
            for count, row in enumerate(game_map):
                print(count, row)
    except IndexError as e:
            print('something went wrong', e)


i = 2
still_in_play = True
while still_in_play:
    active_player = (i % 2) + 1
    i += 1

    active_move = input(f"Player {active_player} Please enter your move (input example: a2): ")
    if active_move[0] == "a" or active_move[0] == "A":
        Col = 0
    elif active_move[0] == "b" or active_move[0] == "B":
        Col = 1
    elif active_move[0] == "c" or active_move[0] == "C":
        Col = 2
    else:
        print("Please enter a valid move")
        i -= 1
        continue
    game_board(game, active_player, row=int(active_move[1]), column=Col, just_display=False)
    game_board(game_map=game, just_display=True)
    if win(game):
        still_in_play = False


"""
mypath= 'H:\\Temp'
onlyfiles = [f for f in listdir(mypath) if isfile(join(mypath, f))]
print(onlyfiles)



#get a list of numbers aeperated by space join them and sort
a = [int(x) for x in input().split()]
b = [int(x) for x in input().split()]
a += b
print(a)
a.sort()
print(a)


#convert csv file to Jason
import csv
import json

csvfile = open('H:\\123.csv', 'r')
jsonfile = open('H:\\file1.json', 'w')

fieldnames = ("FirstName","LastName", "IDNumber", "Message")
reader = csv.DictReader( csvfile, fieldnames)
for row in reader:
    json.dump(row, jsonfile)"""
