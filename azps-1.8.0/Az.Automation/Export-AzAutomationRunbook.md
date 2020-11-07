---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
ms.openlocfilehash: 6d0af3f0d991d8d6b1f73c3277f9f86ac8dd0dae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671645"
---
# <span data-ttu-id="f022f-101">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f022f-101">Export-AzAutomationRunbook</span></span>

## <span data-ttu-id="f022f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f022f-102">SYNOPSIS</span></span>
<span data-ttu-id="f022f-103">Automatizálási runbook exportálása</span><span class="sxs-lookup"><span data-stu-id="f022f-103">Exports an Automation runbook.</span></span>

## <span data-ttu-id="f022f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f022f-104">SYNTAX</span></span>

```
Export-AzAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f022f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f022f-105">DESCRIPTION</span></span>
<span data-ttu-id="f022f-106">Az **export-AzAutomationRunbook** parancsmag az Azure automatizálási runbook wps_2 parancsfájlba (. ps1) exportálja, wps_2 vagy wps_2 munkafolyamat-runbooks, illetve grafikus runbook (. graphrunbook) grafikus runbooks esetén.</span><span class="sxs-lookup"><span data-stu-id="f022f-106">The **Export-AzAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="f022f-107">A runbook neve lesz az exportált fájl neve.</span><span class="sxs-lookup"><span data-stu-id="f022f-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="f022f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f022f-108">EXAMPLES</span></span>

### <span data-ttu-id="f022f-109">1. példa: runbook exportálása</span><span class="sxs-lookup"><span data-stu-id="f022f-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="f022f-110">Ez a parancs exportálja az automatizálási runbook közzétett verzióját egy asztali számítógépre.</span><span class="sxs-lookup"><span data-stu-id="f022f-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="f022f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f022f-111">PARAMETERS</span></span>

### <span data-ttu-id="f022f-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f022f-112">-AutomationAccountName</span></span>
<span data-ttu-id="f022f-113">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag exportál egy runbook.</span><span class="sxs-lookup"><span data-stu-id="f022f-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="f022f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f022f-114">-DefaultProfile</span></span>
<span data-ttu-id="f022f-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f022f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f022f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f022f-116">-Force</span></span>
<span data-ttu-id="f022f-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="f022f-117">ps_force</span></span>

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

### <span data-ttu-id="f022f-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f022f-118">-Name</span></span>
<span data-ttu-id="f022f-119">A parancsmag által exportált runbook nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f022f-119">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="f022f-120">A runbook neve az exportfájl neve lesz.</span><span class="sxs-lookup"><span data-stu-id="f022f-120">The name of the runbook becomes the name of the export file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f022f-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="f022f-121">-OutputFolder</span></span>
<span data-ttu-id="f022f-122">Annak a mappának az elérési útját adja meg, amelyben ez a parancsmag létrehozta az exportálási fájlt.</span><span class="sxs-lookup"><span data-stu-id="f022f-122">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

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

### <span data-ttu-id="f022f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f022f-123">-ResourceGroupName</span></span>
<span data-ttu-id="f022f-124">Annak az erőforráscsoport a neve, amelyhez a parancsmag runbook exportál.</span><span class="sxs-lookup"><span data-stu-id="f022f-124">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="f022f-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="f022f-125">-Slot</span></span>
<span data-ttu-id="f022f-126">Megadja, hogy ez a parancsmag exportálja-e a runbook piszkozatát vagy közzétett tartalmát.</span><span class="sxs-lookup"><span data-stu-id="f022f-126">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="f022f-127">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="f022f-127">Valid values are:</span></span> 
- <span data-ttu-id="f022f-128">Közzétett</span><span class="sxs-lookup"><span data-stu-id="f022f-128">Published</span></span> 
- <span data-ttu-id="f022f-129">Piszkozat</span><span class="sxs-lookup"><span data-stu-id="f022f-129">Draft</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f022f-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f022f-130">-Confirm</span></span>
<span data-ttu-id="f022f-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f022f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f022f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f022f-132">-WhatIf</span></span>
<span data-ttu-id="f022f-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f022f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f022f-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f022f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f022f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f022f-135">CommonParameters</span></span>
<span data-ttu-id="f022f-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f022f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f022f-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f022f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f022f-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f022f-138">INPUTS</span></span>

### <span data-ttu-id="f022f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f022f-139">System.String</span></span>

## <span data-ttu-id="f022f-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f022f-140">OUTPUTS</span></span>

### <span data-ttu-id="f022f-141">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="f022f-141">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="f022f-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f022f-142">NOTES</span></span>

## <span data-ttu-id="f022f-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f022f-143">RELATED LINKS</span></span>

[<span data-ttu-id="f022f-144">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f022f-144">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="f022f-145">Importálás – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f022f-145">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="f022f-146">Új – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f022f-146">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="f022f-147">Új – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f022f-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="f022f-148">Közzététel – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f022f-148">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="f022f-149">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f022f-149">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="f022f-150">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f022f-150">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="f022f-151">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f022f-151">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


