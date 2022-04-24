# WorkOrder
bixfile=FileOpenDialog("BIX File","\\SERVER\blm\ProTube\ProductionLists","bix (*.bix*)") Local $oXML = ObjCreate("Microsoft.XMLDOM") $oXML.load($bixfile)  $oWorkOrders = $oXML.SelectNodes("//Data/Orders/Order") For $oWorkOrder In $oWorkOrders     ConsoleWrite("$oWorkOrder.text=[" &amp; $oWorkOrder.text    &amp; "]" &amp; @CRLF) Next
