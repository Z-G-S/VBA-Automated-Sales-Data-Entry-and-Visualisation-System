# VBA
Contains VBA based projects.
Option Explicit

' This module is designed to initialise the workbook when it is first opened.
' It hides all sheets and displays the LoginForm for user authentication.

Public Sub Workbook_Open()
    ' This subroutine is triggered automatically when the workbook is opened.

    ' Set sheets with sensitive data to be very hidden (not visible in the Excel UI) upon opening the workbook.
    ActiveWorkbook.Sheets("Data_Entry").Visible = xlVeryHidden
    ActiveWorkbook.Sheets("Completed").Visible = xlVeryHidden
    ActiveWorkbook.Sheets("Cancelled").Visible = xlVeryHidden
    ActiveWorkbook.Sheets("Calculations").Visible = xlVeryHidden
    ActiveWorkbook.Sheets("Support_Data").Visible = xlVeryHidden
    ActiveWorkbook.Sheets("Prices_Costs_Data").Visible = xlVeryHidden

    ' Activate the Login sheet (Sheet1) when the workbook opens.
    Sheet1.Activate

    ' Display the LoginForm to the user.
    LoginForm.Show

End Sub
