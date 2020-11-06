---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
ms.openlocfilehash: d28166ec0a9a339017aa11bc30c0c5f0394afe94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497975"
---
# <span data-ttu-id="0c3d3-101">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0c3d3-101">Import-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="0c3d3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0c3d3-102">SYNOPSIS</span></span>
<span data-ttu-id="0c3d3-103">Automatizálási runbook importál.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-103">Imports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c3d3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0c3d3-104">SYNTAX</span></span>

```
Import-AzureRmAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c3d3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0c3d3-105">DESCRIPTION</span></span>
<span data-ttu-id="0c3d3-106">Az **import-AzureRmAutomationRunbook** parancsmag az Azure automatizálási runbook importálja.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-106">The **Import-AzureRmAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="0c3d3-107">Adja meg a wps_2-és wps_2 munkafolyamat-runbooks, illetve a grafikus runbooks grafikus runbook (. graphrunbook) elérési wps_2 útját.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-107">Specify the path to a wps_2 script (.ps1 ) file to import for wps_2 and wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file for graphical runbooks.</span></span> <span data-ttu-id="0c3d3-108">A fájl neve a runbook neve lesz.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-108">The name of the file becomes the name of the runbook.</span></span> <span data-ttu-id="0c3d3-109">Wps_2 munkafolyamat-runbooks a parancsfájlnak olyan egyetlen wps_2 munkafolyamat-definíciót kell tartalmaznia, amely megfelel a fájl nevének.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-109">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="0c3d3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0c3d3-110">EXAMPLES</span></span>

### <span data-ttu-id="0c3d3-111">1. példa: runbook importálása fájlból</span><span class="sxs-lookup"><span data-stu-id="0c3d3-111">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzureRmAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="0c3d3-112">Az első parancs két kulcs/érték párokat rendel a $Tags változóhoz.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-112">The first command assigns two key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="0c3d3-113">A második parancs importál egy GraphicalRunbook06 nevű grafikus runbook a AutomationAccount01 nevű automatizálási fiókba.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-113">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="0c3d3-114">A parancs a $Tagsban tárolt címkéket is kiosztja.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-114">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="0c3d3-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0c3d3-115">PARAMETERS</span></span>

### <span data-ttu-id="0c3d3-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0c3d3-116">-AutomationAccountName</span></span>
<span data-ttu-id="0c3d3-117">Annak az automatizálási fióknak a neve, amelybe a parancsmag runbook importál.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-117">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="0c3d3-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="0c3d3-118">-Description</span></span>
<span data-ttu-id="0c3d3-119">Az importált runbook leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-119">Specifies a description for the imported runbook.</span></span>

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

### <span data-ttu-id="0c3d3-120">-Force</span><span class="sxs-lookup"><span data-stu-id="0c3d3-120">-Force</span></span>
<span data-ttu-id="0c3d3-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="0c3d3-121">ps_force</span></span>

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

### <span data-ttu-id="0c3d3-122">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="0c3d3-122">-LogProgress</span></span>
<span data-ttu-id="0c3d3-123">Meghatározza, hogy a runbook naplózza-e a folyamat adatait.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-123">Specifies whether the runbook logs progress information.</span></span>

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

### <span data-ttu-id="0c3d3-124">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="0c3d3-124">-LogVerbose</span></span>
<span data-ttu-id="0c3d3-125">Megadja, hogy a runbook naplózza-e a részletes információkat.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-125">Specifies whether the runbook logs detailed information.</span></span>

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

### <span data-ttu-id="0c3d3-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0c3d3-126">-Name</span></span>
<span data-ttu-id="0c3d3-127">Annak a runbook a nevét adja meg, amelyet a parancsmag importál.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-127">Specifies the name of the runbook that this cmdlet imports.</span></span>

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

### <span data-ttu-id="0c3d3-128">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="0c3d3-128">-Path</span></span>
<span data-ttu-id="0c3d3-129">A parancsmag által importált. ps1 vagy. graphrunbook fájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-129">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

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

### <span data-ttu-id="0c3d3-130">Által közzétett</span><span class="sxs-lookup"><span data-stu-id="0c3d3-130">-Published</span></span>
<span data-ttu-id="0c3d3-131">Jelzi, hogy ez a parancsmag közzéteszi a runbook, amelyet importál.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-131">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

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

### <span data-ttu-id="0c3d3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c3d3-132">-ResourceGroupName</span></span>
<span data-ttu-id="0c3d3-133">Annak az erőforráscsoport a neve, amelyhez a parancsmag runbook importál.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-133">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="0c3d3-134">-Címkék</span><span class="sxs-lookup"><span data-stu-id="0c3d3-134">-Tags</span></span>
<span data-ttu-id="0c3d3-135">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0c3d3-136">Példa:</span><span class="sxs-lookup"><span data-stu-id="0c3d3-136">For example:</span></span>

<span data-ttu-id="0c3d3-137">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="0c3d3-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0c3d3-138">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="0c3d3-138">-Type</span></span>
<span data-ttu-id="0c3d3-139">A parancsmag által létrehozott runbook adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-139">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="0c3d3-140">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="0c3d3-140">Valid values are:</span></span>

- <span data-ttu-id="0c3d3-141">PowerShell</span><span class="sxs-lookup"><span data-stu-id="0c3d3-141">PowerShell</span></span>
- <span data-ttu-id="0c3d3-142">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="0c3d3-142">GraphicalPowerShell</span></span>
- <span data-ttu-id="0c3d3-143">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="0c3d3-143">PowerShellWorkflow</span></span>
- <span data-ttu-id="0c3d3-144">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="0c3d3-144">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="0c3d3-145">Graph</span><span class="sxs-lookup"><span data-stu-id="0c3d3-145">Graph</span></span>

<span data-ttu-id="0c3d3-146">Az érték gráf elavult.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-146">The value Graph is obsolete.</span></span>
<span data-ttu-id="0c3d3-147">Egyenértékű a GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-147">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c3d3-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0c3d3-148">-Confirm</span></span>
<span data-ttu-id="0c3d3-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c3d3-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c3d3-150">-WhatIf</span></span>
<span data-ttu-id="0c3d3-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c3d3-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c3d3-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c3d3-153">-DefaultProfile</span></span>
<span data-ttu-id="0c3d3-154">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0c3d3-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c3d3-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c3d3-155">CommonParameters</span></span>
<span data-ttu-id="0c3d3-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0c3d3-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c3d3-157">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c3d3-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c3d3-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c3d3-158">INPUTS</span></span>

## <span data-ttu-id="0c3d3-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c3d3-159">OUTPUTS</span></span>

### <span data-ttu-id="0c3d3-160">Microsoft. Azure. Command. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="0c3d3-160">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="0c3d3-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0c3d3-161">NOTES</span></span>

## <span data-ttu-id="0c3d3-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c3d3-162">RELATED LINKS</span></span>

[<span data-ttu-id="0c3d3-163">Exportálás – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0c3d3-163">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="0c3d3-164">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0c3d3-164">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="0c3d3-165">Új – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0c3d3-165">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="0c3d3-166">Új – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0c3d3-166">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="0c3d3-167">Közzététel – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0c3d3-167">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="0c3d3-168">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0c3d3-168">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="0c3d3-169">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0c3d3-169">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="0c3d3-170">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0c3d3-170">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
