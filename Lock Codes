List Box Historique Code :

 ListBox1.Items.Add(My.Settings.list)
-------------------------------------------
Lock File Code  :

  Dim text1 As String = ".{2559a1f2-21d7-11d4-bdaf-00c04f60b9f0}"
        Shell("cmd /c" & "ren " & TextBox1.Text & " " & TextBox2.Text & text1)
        Shell("cmd /c" & "attrib +s +h " & TextBox1.Text & ".{2559a1f2-21d7-11d4-bdaf-00c04f60b9f0}\*.*" & " /S /D")
        Shell("cmd /c" & "attrib +s +h " & TextBox1.Text & ".{2559a1f2-21d7-11d4-bdaf-00c04f60b9f0}" & " /S /D")

        ListBox1.Items.Add(TextBox1.Text)
        My.Settings.list = TextBox1.Text
        My.Settings.Save()
-------------------------------------------------------
Unlock File Code :

 Dim text1 As String = ".{2559a1f2-21d7-11d4-bdaf-00c04f60b9f0}"
        Shell("cmd /c" & "attrib -s -h " & TextBox1.Text & ".{2559a1f2-21d7-11d4-bdaf-00c04f60b9f0}" & " /S /D")
        Shell("cmd /c" & "attrib -s -h " & TextBox1.Text & ".{2559a1f2-21d7-11d4-bdaf-00c04f60b9f0}\*.*" & " /S /D")
        System.Threading.Thread.Sleep(1000)
        Shell("cmd /c" & "ren " & TextBox1.Text & text1 & " " & TextBox2.Text)
-------------------------------------------------------
Browse Code      :

   Dim last As String

        FolderBrowserDialog1.ShowDialog()
        TextBox1.Text = FolderBrowserDialog1.SelectedPath
        last = Path.GetFileName(FolderBrowserDialog1.SelectedPath)
        TextBox2.Text = last
        TextBox1.Text = TextBox1.Text.Replace(".{2559a1f2-21d7-11d4-bdaf-00c04f60b9f0}", "")
        TextBox2.Text = TextBox2.Text.Replace(".{2559a1f2-21d7-11d4-bdaf-00c04f60b9f0}", "")
----------------------------------------------------------------------- 
Liste box last activitie Code :

 On Error Resume Next
        TextBox1.Text = ListBox1.SelectedItem
        TextBox2.Text = TextBox1.Text.Split("\")(1)
