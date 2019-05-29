weird xs x = if even x then xs else reverse xs

boustrophedon xss = [ css  | xs <- xss, if length xs `mod` 2 == 0 then xs else reverse xs ]

stringSplitter "" = []
stringSplitter xs = (take 20 xs):(stringSplitter (drop 20 xs))  