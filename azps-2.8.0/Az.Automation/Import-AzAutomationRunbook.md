---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/import-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationRunbook.md
ms.openlocfilehash: 9ec19ee8e1e6a74de83f77b8dca4e2536af8e425
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667808"
---
# <span data-ttu-id="bfcb6-101">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bfcb6-101">Import-AzAutomationRunbook</span></span>

## <span data-ttu-id="bfcb6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bfcb6-102">SYNOPSIS</span></span>
<span data-ttu-id="bfcb6-103">Automatizálási runbook importál.</span><span class="sxs-lookup"><span data-stu-id="bfcb6-103">Imports an Automation runbook.</span></span>

## <span data-ttu-id="bfcb6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bfcb6-104">SYNTAX</span></span>

```
Import-AzAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfcb6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bfcb6-105">DESCRIPTION</span></span>
<span data-ttu-id="bfcb6-106">Az **import-AzAutomationRunbook** parancsmag az Azure automatizálási runbook importálja.</span><span class="sxs-lookup"><span data-stu-id="bfcb6-106">The **Import-AzAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="bfcb6-107">Adja meg az wps_2 parancsfájl (. ps1) elérési útját, amely az importálandó wps_2-és wps_2 munkafolyamat-runbooks (. graphrunbook) a Python 2 runbooks grafikus runbooks vagy (. vagy) fájljának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bfcb6-107">Specify the path to a wps_2 script (.ps1) file to import for wps_2 and wps_2 Workflow runbooks, (.graphrunbook) file for graphical runbooks, or (.py) file for python 2 runbooks.</span></span> <span data-ttu-id="bfcb6-108">Wps_2 munkafolyamat-runbooks a parancsfájlnak olyan egyetlen wps_2 munkafolyamat-definíciót kell tartalmaznia, amely megfelel a fájl nevének.</span><span class="sxs-lookup"><span data-stu-id="bfcb6-108">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="bfcb6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="bfcb6-109">EXAMPLES</span></span>

### <span data-ttu-id="bfcb6-110">1. példa: runbook importálása fájlból</span><span class="sxs-lookup"><span data-stu-id="bfcb6-110">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="bfcb6-111">Az első parancs két kulcs/érték párokat rendel a $Tags változóhoz.</span><span class="sxs-lookup"><span data-stu-id="bfcb6-111">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="bfcb6-112">A második parancs importál egy GraphicalRunbook06 nevű grafikus runbook a AutomationAccount01 nevű automatizálási fiókba.</span><span class="sxs-lookup"><span data-stu-id="bfcb6-112">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="bfcb6-113">A parancs a $Tagsban tárolt címkéket is kiosztja.</span><span class="sxs-lookup"><span data-stu-id="bfcb6-113">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="bfcb6-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bfcb6-114">PARAMETERS</span></span>

### <span data-ttu-id="bfcb6-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bfcb6-115">-AutomationAccountName</span></span>
<span data-ttu-id="bfcb6-116">Annak az automatizálási fióknak a neve, amelybe a parancsmag runbook importál.</span><span class="sxs-lookup"><span data-stu-id="bfcb6-116">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfcb6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfcb6-117">-DefaultProfile</span></span>
<span data-ttu-id="bfcb6-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bfcb6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcb6-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="bfcb6-119">-Description</span></span>
<span data-ttu-id="bfcb6-120">Az importált runbook leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="bfcb6-120">Specifies a description for the imported runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfcb6-121">-Force</span><span class="sxs-lookup"><span data-stu-id="bfcb6-121">-Force</span></span>
<span data-ttu-id="bfcb6-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="bfcb6-122">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcb6-123">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="bfcb6-123">-LogProgress</span></span>
<span data-ttu-id="bfcb6-124">Meghatározza, hogy a runbook naplózza-e a folyamat adatait.</span><span class="sxs-lookup"><span data-stu-id="bfcb6-124">Specifies whether the runbook logs progress information.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfcb6-125">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="bfcb6-125">-LogVerbose</span></span>
<span data-ttu-id="bfcb6-126">Megadja, hogy a runbook naplózza-e a részletes információkat.</span><span class="sxs-lookup"><span data-stu-id="bfcb6-126">Specifies whether the runbook logs detailed information.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfcb6-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bfcb6-127">-Name</span></span>
<span data-ttu-id="bfcb6-128">Annak a runbook a nevét adja meg, amelyet a parancsmag importál.</span><span class="sxs-lookup"><span data-stu-id="bfcb6-128">Specifies the name of the runbook that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfcb6-129">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="bfcb6-129">-Path</span></span>
<span data-ttu-id="bfcb6-130">A parancsmag által importált. ps1 vagy. graphrunbook fájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bfcb6-130">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourcePath

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfcb6-131">Által közzétett</span><span class="sxs-lookup"><span data-stu-id="bfcb6-131">-Published</span></span>
<span data-ttu-id="bfcb6-132">Jelzi, hogy ez a parancsmag közzéteszi a runbook, amelyet importál.</span><span class="sxs-lookup"><span data-stu-id="bfcb6-132">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcb6-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfcb6-133">-ResourceGroupName</span></span>
<span data-ttu-id="bfcb6-134">Annak az erőforráscsoport a neve, amelyhez a parancsmag runbook importál.</span><span class="sxs-lookup"><span data-stu-id="bfcb6-134">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfcb6-135">-Címkék</span><span class="sxs-lookup"><span data-stu-id="bfcb6-135">-Tags</span></span>
<span data-ttu-id="bfcb6-136">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="bfcb6-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bfcb6-137">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="bfcb6-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfcb6-138">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="bfcb6-138">-Type</span></span>
<span data-ttu-id="bfcb6-139">A parancsmag által létrehozott runbook adja meg.</span><span class="sxs-lookup"><span data-stu-id="bfcb6-139">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="bfcb6-140">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="bfcb6-140">Valid values are:</span></span>
- <span data-ttu-id="bfcb6-141">PowerShell</span><span class="sxs-lookup"><span data-stu-id="bfcb6-141">PowerShell</span></span>
- <span data-ttu-id="bfcb6-142">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="bfcb6-142">GraphicalPowerShell</span></span>
- <span data-ttu-id="bfcb6-143">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="bfcb6-143">PowerShellWorkflow</span></span>
- <span data-ttu-id="bfcb6-144">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="bfcb6-144">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="bfcb6-145">Graph</span><span class="sxs-lookup"><span data-stu-id="bfcb6-145">Graph</span></span>
- <span data-ttu-id="bfcb6-146">Python2 az érték grafikonja elavult.</span><span class="sxs-lookup"><span data-stu-id="bfcb6-146">Python2 The value Graph is obsolete.</span></span>
<span data-ttu-id="bfcb6-147">Egyenértékű a GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="bfcb6-147">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph, Python2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcb6-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bfcb6-148">-Confirm</span></span>
<span data-ttu-id="bfcb6-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bfcb6-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcb6-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfcb6-150">-WhatIf</span></span>
<span data-ttu-id="bfcb6-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bfcb6-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfcb6-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bfcb6-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcb6-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfcb6-153">CommonParameters</span></span>
<span data-ttu-id="bfcb6-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bfcb6-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfcb6-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfcb6-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfcb6-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bfcb6-156">INPUTS</span></span>

### <span data-ttu-id="bfcb6-157">System. String</span><span class="sxs-lookup"><span data-stu-id="bfcb6-157">System.String</span></span>

### <span data-ttu-id="bfcb6-158">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="bfcb6-158">System.Collections.IDictionary</span></span>

### <span data-ttu-id="bfcb6-159">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bfcb6-159">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="bfcb6-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bfcb6-160">OUTPUTS</span></span>

### <span data-ttu-id="bfcb6-161">Microsoft. Azure. Command. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="bfcb6-161">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="bfcb6-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bfcb6-162">NOTES</span></span>

## <span data-ttu-id="bfcb6-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bfcb6-163">RELATED LINKS</span></span>

[<span data-ttu-id="bfcb6-164">Exportálás – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bfcb6-164">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="bfcb6-165">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bfcb6-165">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="bfcb6-166">Új – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bfcb6-166">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="bfcb6-167">Közzététel – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bfcb6-167">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="bfcb6-168">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bfcb6-168">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="bfcb6-169">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bfcb6-169">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="bfcb6-170">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bfcb6-170">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)
