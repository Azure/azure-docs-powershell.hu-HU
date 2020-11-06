---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
ms.openlocfilehash: f6399c35316deb5590eada9eccd474ba7e47b116
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498508"
---
# <span data-ttu-id="130ff-101">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="130ff-101">Import-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="130ff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="130ff-102">SYNOPSIS</span></span>
<span data-ttu-id="130ff-103">Automatizálási runbook importál.</span><span class="sxs-lookup"><span data-stu-id="130ff-103">Imports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="130ff-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="130ff-104">SYNTAX</span></span>

```
Import-AzureRmAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="130ff-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="130ff-105">DESCRIPTION</span></span>
<span data-ttu-id="130ff-106">Az **import-AzureRmAutomationRunbook** parancsmag az Azure automatizálási runbook importálja.</span><span class="sxs-lookup"><span data-stu-id="130ff-106">The **Import-AzureRmAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="130ff-107">Adja meg az wps_2 parancsfájl (. ps1) elérési útját, amely az importálandó wps_2-és wps_2 munkafolyamat-runbooks (. graphrunbook) a Python 2 runbooks grafikus runbooks vagy (. vagy) fájljának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="130ff-107">Specify the path to a wps_2 script (.ps1) file to import for wps_2 and wps_2 Workflow runbooks, (.graphrunbook) file for graphical runbooks, or (.py) file for python 2 runbooks.</span></span> <span data-ttu-id="130ff-108">Wps_2 munkafolyamat-runbooks a parancsfájlnak olyan egyetlen wps_2 munkafolyamat-definíciót kell tartalmaznia, amely megfelel a fájl nevének.</span><span class="sxs-lookup"><span data-stu-id="130ff-108">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="130ff-109">Példák</span><span class="sxs-lookup"><span data-stu-id="130ff-109">EXAMPLES</span></span>

### <span data-ttu-id="130ff-110">1. példa: runbook importálása fájlból</span><span class="sxs-lookup"><span data-stu-id="130ff-110">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzureRmAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="130ff-111">Az első parancs két kulcs/érték párokat rendel a $Tags változóhoz.</span><span class="sxs-lookup"><span data-stu-id="130ff-111">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="130ff-112">A második parancs importál egy GraphicalRunbook06 nevű grafikus runbook a AutomationAccount01 nevű automatizálási fiókba.</span><span class="sxs-lookup"><span data-stu-id="130ff-112">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="130ff-113">A parancs a $Tagsban tárolt címkéket is kiosztja.</span><span class="sxs-lookup"><span data-stu-id="130ff-113">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="130ff-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="130ff-114">PARAMETERS</span></span>

### <span data-ttu-id="130ff-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="130ff-115">-AutomationAccountName</span></span>
<span data-ttu-id="130ff-116">Annak az automatizálási fióknak a neve, amelybe a parancsmag runbook importál.</span><span class="sxs-lookup"><span data-stu-id="130ff-116">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="130ff-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="130ff-117">-DefaultProfile</span></span>
<span data-ttu-id="130ff-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="130ff-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="130ff-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="130ff-119">-Description</span></span>
<span data-ttu-id="130ff-120">Az importált runbook leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="130ff-120">Specifies a description for the imported runbook.</span></span>

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

### <span data-ttu-id="130ff-121">-Force</span><span class="sxs-lookup"><span data-stu-id="130ff-121">-Force</span></span>
<span data-ttu-id="130ff-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="130ff-122">ps_force</span></span>

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

### <span data-ttu-id="130ff-123">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="130ff-123">-LogProgress</span></span>
<span data-ttu-id="130ff-124">Meghatározza, hogy a runbook naplózza-e a folyamat adatait.</span><span class="sxs-lookup"><span data-stu-id="130ff-124">Specifies whether the runbook logs progress information.</span></span>

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

### <span data-ttu-id="130ff-125">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="130ff-125">-LogVerbose</span></span>
<span data-ttu-id="130ff-126">Megadja, hogy a runbook naplózza-e a részletes információkat.</span><span class="sxs-lookup"><span data-stu-id="130ff-126">Specifies whether the runbook logs detailed information.</span></span>

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

### <span data-ttu-id="130ff-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="130ff-127">-Name</span></span>
<span data-ttu-id="130ff-128">Annak a runbook a nevét adja meg, amelyet a parancsmag importál.</span><span class="sxs-lookup"><span data-stu-id="130ff-128">Specifies the name of the runbook that this cmdlet imports.</span></span>

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

### <span data-ttu-id="130ff-129">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="130ff-129">-Path</span></span>
<span data-ttu-id="130ff-130">A parancsmag által importált. ps1 vagy. graphrunbook fájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="130ff-130">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

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

### <span data-ttu-id="130ff-131">Által közzétett</span><span class="sxs-lookup"><span data-stu-id="130ff-131">-Published</span></span>
<span data-ttu-id="130ff-132">Jelzi, hogy ez a parancsmag közzéteszi a runbook, amelyet importál.</span><span class="sxs-lookup"><span data-stu-id="130ff-132">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

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

### <span data-ttu-id="130ff-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="130ff-133">-ResourceGroupName</span></span>
<span data-ttu-id="130ff-134">Annak az erőforráscsoport a neve, amelyhez a parancsmag runbook importál.</span><span class="sxs-lookup"><span data-stu-id="130ff-134">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="130ff-135">-Címkék</span><span class="sxs-lookup"><span data-stu-id="130ff-135">-Tags</span></span>
<span data-ttu-id="130ff-136">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="130ff-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="130ff-137">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="130ff-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="130ff-138">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="130ff-138">-Type</span></span>
<span data-ttu-id="130ff-139">A parancsmag által létrehozott runbook adja meg.</span><span class="sxs-lookup"><span data-stu-id="130ff-139">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="130ff-140">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="130ff-140">Valid values are:</span></span>
- <span data-ttu-id="130ff-141">PowerShell</span><span class="sxs-lookup"><span data-stu-id="130ff-141">PowerShell</span></span>
- <span data-ttu-id="130ff-142">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="130ff-142">GraphicalPowerShell</span></span>
- <span data-ttu-id="130ff-143">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="130ff-143">PowerShellWorkflow</span></span>
- <span data-ttu-id="130ff-144">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="130ff-144">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="130ff-145">Graph</span><span class="sxs-lookup"><span data-stu-id="130ff-145">Graph</span></span>
- <span data-ttu-id="130ff-146">Python2 az érték grafikonja elavult.</span><span class="sxs-lookup"><span data-stu-id="130ff-146">Python2 The value Graph is obsolete.</span></span>
<span data-ttu-id="130ff-147">Egyenértékű a GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="130ff-147">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

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

### <span data-ttu-id="130ff-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="130ff-148">-Confirm</span></span>
<span data-ttu-id="130ff-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="130ff-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="130ff-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="130ff-150">-WhatIf</span></span>
<span data-ttu-id="130ff-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="130ff-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="130ff-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="130ff-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="130ff-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="130ff-153">CommonParameters</span></span>
<span data-ttu-id="130ff-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="130ff-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="130ff-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="130ff-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="130ff-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="130ff-156">INPUTS</span></span>

### <span data-ttu-id="130ff-157">System. String</span><span class="sxs-lookup"><span data-stu-id="130ff-157">System.String</span></span>

### <span data-ttu-id="130ff-158">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="130ff-158">System.Collections.IDictionary</span></span>

### <span data-ttu-id="130ff-159">System. null ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="130ff-159">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="130ff-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="130ff-160">OUTPUTS</span></span>

### <span data-ttu-id="130ff-161">Microsoft. Azure. Command. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="130ff-161">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="130ff-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="130ff-162">NOTES</span></span>

## <span data-ttu-id="130ff-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="130ff-163">RELATED LINKS</span></span>

[<span data-ttu-id="130ff-164">Exportálás – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="130ff-164">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="130ff-165">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="130ff-165">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="130ff-166">Új – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="130ff-166">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="130ff-167">Új – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="130ff-167">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="130ff-168">Közzététel – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="130ff-168">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="130ff-169">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="130ff-169">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="130ff-170">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="130ff-170">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="130ff-171">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="130ff-171">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
