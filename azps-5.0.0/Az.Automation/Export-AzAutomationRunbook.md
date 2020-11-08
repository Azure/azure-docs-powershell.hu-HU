---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
ms.openlocfilehash: 03a57c35063a401aa5f730e11538532bdbbbc58c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187088"
---
# <span data-ttu-id="dda31-101">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dda31-101">Export-AzAutomationRunbook</span></span>

## <span data-ttu-id="dda31-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dda31-102">SYNOPSIS</span></span>
<span data-ttu-id="dda31-103">Automatizálási runbook exportálása</span><span class="sxs-lookup"><span data-stu-id="dda31-103">Exports an Automation runbook.</span></span>

## <span data-ttu-id="dda31-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dda31-104">SYNTAX</span></span>

```
Export-AzAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dda31-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dda31-105">DESCRIPTION</span></span>
<span data-ttu-id="dda31-106">Az **export-AzAutomationRunbook** parancsmag az Azure automatizálási runbook wps_2 parancsfájlba (. ps1) exportálja, wps_2 vagy wps_2 munkafolyamat-runbooks, illetve grafikus runbook (. graphrunbook) grafikus runbooks esetén.</span><span class="sxs-lookup"><span data-stu-id="dda31-106">The **Export-AzAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="dda31-107">A runbook neve lesz az exportált fájl neve.</span><span class="sxs-lookup"><span data-stu-id="dda31-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="dda31-108">Példák</span><span class="sxs-lookup"><span data-stu-id="dda31-108">EXAMPLES</span></span>

### <span data-ttu-id="dda31-109">1. példa: runbook exportálása</span><span class="sxs-lookup"><span data-stu-id="dda31-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="dda31-110">Ez a parancs exportálja az automatizálási runbook közzétett verzióját egy asztali számítógépre.</span><span class="sxs-lookup"><span data-stu-id="dda31-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="dda31-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dda31-111">PARAMETERS</span></span>

### <span data-ttu-id="dda31-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dda31-112">-AutomationAccountName</span></span>
<span data-ttu-id="dda31-113">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag exportál egy runbook.</span><span class="sxs-lookup"><span data-stu-id="dda31-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="dda31-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dda31-114">-DefaultProfile</span></span>
<span data-ttu-id="dda31-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dda31-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dda31-116">-Force</span><span class="sxs-lookup"><span data-stu-id="dda31-116">-Force</span></span>
<span data-ttu-id="dda31-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="dda31-117">ps_force</span></span>

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

### <span data-ttu-id="dda31-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dda31-118">-Name</span></span>
<span data-ttu-id="dda31-119">A parancsmag által exportált runbook nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dda31-119">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="dda31-120">A runbook neve az exportfájl neve lesz.</span><span class="sxs-lookup"><span data-stu-id="dda31-120">The name of the runbook becomes the name of the export file.</span></span>

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

### <span data-ttu-id="dda31-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="dda31-121">-OutputFolder</span></span>
<span data-ttu-id="dda31-122">Annak a mappának az elérési útját adja meg, amelyben ez a parancsmag létrehozta az exportálási fájlt.</span><span class="sxs-lookup"><span data-stu-id="dda31-122">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

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

### <span data-ttu-id="dda31-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dda31-123">-ResourceGroupName</span></span>
<span data-ttu-id="dda31-124">Annak az erőforráscsoport a neve, amelyhez a parancsmag runbook exportál.</span><span class="sxs-lookup"><span data-stu-id="dda31-124">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="dda31-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="dda31-125">-Slot</span></span>
<span data-ttu-id="dda31-126">Megadja, hogy ez a parancsmag exportálja-e a runbook piszkozatát vagy közzétett tartalmát.</span><span class="sxs-lookup"><span data-stu-id="dda31-126">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="dda31-127">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="dda31-127">Valid values are:</span></span> 
- <span data-ttu-id="dda31-128">Közzétett</span><span class="sxs-lookup"><span data-stu-id="dda31-128">Published</span></span> 
- <span data-ttu-id="dda31-129">Piszkozat</span><span class="sxs-lookup"><span data-stu-id="dda31-129">Draft</span></span>

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

### <span data-ttu-id="dda31-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dda31-130">-Confirm</span></span>
<span data-ttu-id="dda31-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dda31-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dda31-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dda31-132">-WhatIf</span></span>
<span data-ttu-id="dda31-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dda31-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dda31-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dda31-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dda31-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dda31-135">CommonParameters</span></span>
<span data-ttu-id="dda31-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dda31-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dda31-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dda31-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dda31-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dda31-138">INPUTS</span></span>

### <span data-ttu-id="dda31-139">System. String</span><span class="sxs-lookup"><span data-stu-id="dda31-139">System.String</span></span>

## <span data-ttu-id="dda31-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dda31-140">OUTPUTS</span></span>

### <span data-ttu-id="dda31-141">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="dda31-141">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="dda31-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dda31-142">NOTES</span></span>

## <span data-ttu-id="dda31-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dda31-143">RELATED LINKS</span></span>

[<span data-ttu-id="dda31-144">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dda31-144">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="dda31-145">Importálás – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dda31-145">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="dda31-146">Új – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dda31-146">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="dda31-147">Új – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dda31-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="dda31-148">Közzététel – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dda31-148">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="dda31-149">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dda31-149">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="dda31-150">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dda31-150">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="dda31-151">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dda31-151">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


