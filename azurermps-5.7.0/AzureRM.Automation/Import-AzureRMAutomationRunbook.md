---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
ms.openlocfilehash: 1f7c50f0f5b11c80fce203b0c44128e380834bdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492403"
---
# <span data-ttu-id="70aec-101">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="70aec-101">Import-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="70aec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="70aec-102">SYNOPSIS</span></span>
<span data-ttu-id="70aec-103">Automatizálási runbook importál.</span><span class="sxs-lookup"><span data-stu-id="70aec-103">Imports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70aec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="70aec-104">SYNTAX</span></span>

```
Import-AzureRmAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70aec-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="70aec-105">DESCRIPTION</span></span>
<span data-ttu-id="70aec-106">Az **import-AzureRmAutomationRunbook** parancsmag az Azure automatizálási runbook importálja.</span><span class="sxs-lookup"><span data-stu-id="70aec-106">The **Import-AzureRmAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="70aec-107">Adja meg az wps_2 parancsfájl (. ps1) elérési útját, amely az importálandó wps_2-és wps_2 munkafolyamat-runbooks (. graphrunbook) a Python 2 runbooks grafikus runbooks vagy (. vagy) fájljának elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="70aec-107">Specify the path to a wps_2 script (.ps1) file to import for wps_2 and wps_2 Workflow runbooks, (.graphrunbook) file for graphical runbooks, or (.py) file for python 2 runbooks.</span></span> <span data-ttu-id="70aec-108">Wps_2 munkafolyamat-runbooks a parancsfájlnak olyan egyetlen wps_2 munkafolyamat-definíciót kell tartalmaznia, amely megfelel a fájl nevének.</span><span class="sxs-lookup"><span data-stu-id="70aec-108">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="70aec-109">Példák</span><span class="sxs-lookup"><span data-stu-id="70aec-109">EXAMPLES</span></span>

### <span data-ttu-id="70aec-110">1. példa: runbook importálása fájlból</span><span class="sxs-lookup"><span data-stu-id="70aec-110">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzureRmAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="70aec-111">Az első parancs két kulcs/érték párokat rendel a $Tags változóhoz.</span><span class="sxs-lookup"><span data-stu-id="70aec-111">The first command assigns two key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="70aec-112">A második parancs importál egy GraphicalRunbook06 nevű grafikus runbook a AutomationAccount01 nevű automatizálási fiókba.</span><span class="sxs-lookup"><span data-stu-id="70aec-112">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="70aec-113">A parancs a $Tagsban tárolt címkéket is kiosztja.</span><span class="sxs-lookup"><span data-stu-id="70aec-113">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="70aec-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="70aec-114">PARAMETERS</span></span>

### <span data-ttu-id="70aec-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="70aec-115">-AutomationAccountName</span></span>
<span data-ttu-id="70aec-116">Annak az automatizálási fióknak a neve, amelybe a parancsmag runbook importál.</span><span class="sxs-lookup"><span data-stu-id="70aec-116">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70aec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70aec-117">-DefaultProfile</span></span>
<span data-ttu-id="70aec-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="70aec-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70aec-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="70aec-119">-Description</span></span>
<span data-ttu-id="70aec-120">Az importált runbook leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="70aec-120">Specifies a description for the imported runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70aec-121">-Force</span><span class="sxs-lookup"><span data-stu-id="70aec-121">-Force</span></span>
<span data-ttu-id="70aec-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="70aec-122">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70aec-123">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="70aec-123">-LogProgress</span></span>
<span data-ttu-id="70aec-124">Meghatározza, hogy a runbook naplózza-e a folyamat adatait.</span><span class="sxs-lookup"><span data-stu-id="70aec-124">Specifies whether the runbook logs progress information.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70aec-125">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="70aec-125">-LogVerbose</span></span>
<span data-ttu-id="70aec-126">Megadja, hogy a runbook naplózza-e a részletes információkat.</span><span class="sxs-lookup"><span data-stu-id="70aec-126">Specifies whether the runbook logs detailed information.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70aec-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="70aec-127">-Name</span></span>
<span data-ttu-id="70aec-128">Annak a runbook a nevét adja meg, amelyet a parancsmag importál.</span><span class="sxs-lookup"><span data-stu-id="70aec-128">Specifies the name of the runbook that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70aec-129">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="70aec-129">-Path</span></span>
<span data-ttu-id="70aec-130">A parancsmag által importált. ps1 vagy. graphrunbook fájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="70aec-130">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourcePath

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70aec-131">Által közzétett</span><span class="sxs-lookup"><span data-stu-id="70aec-131">-Published</span></span>
<span data-ttu-id="70aec-132">Jelzi, hogy ez a parancsmag közzéteszi a runbook, amelyet importál.</span><span class="sxs-lookup"><span data-stu-id="70aec-132">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70aec-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70aec-133">-ResourceGroupName</span></span>
<span data-ttu-id="70aec-134">Annak az erőforráscsoport a neve, amelyhez a parancsmag runbook importál.</span><span class="sxs-lookup"><span data-stu-id="70aec-134">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70aec-135">-Címkék</span><span class="sxs-lookup"><span data-stu-id="70aec-135">-Tags</span></span>
<span data-ttu-id="70aec-136">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="70aec-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="70aec-137">Példa:</span><span class="sxs-lookup"><span data-stu-id="70aec-137">For example:</span></span>

<span data-ttu-id="70aec-138">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="70aec-138">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70aec-139">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="70aec-139">-Type</span></span>
<span data-ttu-id="70aec-140">A parancsmag által létrehozott runbook adja meg.</span><span class="sxs-lookup"><span data-stu-id="70aec-140">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="70aec-141">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="70aec-141">Valid values are:</span></span>

- <span data-ttu-id="70aec-142">PowerShell</span><span class="sxs-lookup"><span data-stu-id="70aec-142">PowerShell</span></span>
- <span data-ttu-id="70aec-143">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="70aec-143">GraphicalPowerShell</span></span>
- <span data-ttu-id="70aec-144">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="70aec-144">PowerShellWorkflow</span></span>
- <span data-ttu-id="70aec-145">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="70aec-145">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="70aec-146">Graph</span><span class="sxs-lookup"><span data-stu-id="70aec-146">Graph</span></span>
- <span data-ttu-id="70aec-147">Python2</span><span class="sxs-lookup"><span data-stu-id="70aec-147">Python2</span></span>

<span data-ttu-id="70aec-148">Az érték gráf elavult.</span><span class="sxs-lookup"><span data-stu-id="70aec-148">The value Graph is obsolete.</span></span>
<span data-ttu-id="70aec-149">Egyenértékű a GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="70aec-149">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph, Python

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70aec-150">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="70aec-150">-Confirm</span></span>
<span data-ttu-id="70aec-151">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="70aec-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70aec-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70aec-152">-WhatIf</span></span>
<span data-ttu-id="70aec-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="70aec-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70aec-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="70aec-154">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70aec-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70aec-155">CommonParameters</span></span>
<span data-ttu-id="70aec-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="70aec-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70aec-157">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70aec-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70aec-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="70aec-158">INPUTS</span></span>

### <span data-ttu-id="70aec-159">Nincs</span><span class="sxs-lookup"><span data-stu-id="70aec-159">None</span></span>
<span data-ttu-id="70aec-160">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="70aec-160">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="70aec-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70aec-161">OUTPUTS</span></span>

### <span data-ttu-id="70aec-162">Microsoft. Azure. Command. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="70aec-162">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="70aec-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="70aec-163">NOTES</span></span>

## <span data-ttu-id="70aec-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70aec-164">RELATED LINKS</span></span>

[<span data-ttu-id="70aec-165">Exportálás – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="70aec-165">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="70aec-166">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="70aec-166">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="70aec-167">Új – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="70aec-167">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="70aec-168">Új – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="70aec-168">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="70aec-169">Közzététel – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="70aec-169">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="70aec-170">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="70aec-170">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="70aec-171">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="70aec-171">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="70aec-172">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="70aec-172">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
