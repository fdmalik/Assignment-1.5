# Assignment-1.5

        Dim mName As String = ""
        Dim mId As Integer = 0
        Dim found As Boolean = False
        Dim TelNum As String = ""
        Dim MSD As Date

        FileOpen(1, "c:\Assignment 1\mRec.txt", OpenMode.Input)
        FileOpen(2, "c:\Assignment 1\Detailed mRec.txt", OpenMode.Output)

        While Not EOF(1)

            Input(1, mName)
            Input(1, mId)


            Console.WriteLine(" Please Enter the Membership Start Date For " & mName & " : ")
            MSD = Console.ReadLine()
            Console.WriteLine(" Please Enter the Telephone Number For " & mName & " : ")
            TelNum = Console.ReadLine()



            WriteLine(2, mName)
            WriteLine(2, mId)
            WriteLine(2, MSD)
            WriteLine(2, TelNum)


        End While

        FileClose(1)
        FileClose(2)

        My.Computer.FileSystem.DeleteFile("c:\Assignment 1\mRec.txt")
        My.Computer.FileSystem.RenameFile("c:\Assignment 1\Detailed mRec.txt", "c:\Assignment 1\mRec.txt")

        Console.ReadKey()
