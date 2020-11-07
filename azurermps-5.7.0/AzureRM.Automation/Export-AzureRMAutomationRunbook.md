---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/export-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRMAutomationRunbook.md
ms.openlocfilehash: 7bc8305c8b0d861398807f7eefae4a741f60cc52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680442"
---
# <span data-ttu-id="f000a-101">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f000a-101">Export-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="f000a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f000a-102">SYNOPSIS</span></span>
<span data-ttu-id="f000a-103">Automatizálási runbook exportálása</span><span class="sxs-lookup"><span data-stu-id="f000a-103">Exports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f000a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f000a-104">SYNTAX</span></span>

```
Export-AzureRmAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f000a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f000a-105">DESCRIPTION</span></span>
<span data-ttu-id="f000a-106">Az **export-AzureRmAutomationRunbook** parancsmag az Azure automatizálási runbook wps_2 parancsfájlba (. ps1) exportálja, wps_2 vagy wps_2 munkafolyamat-runbooks, illetve grafikus runbook (. graphrunbook) grafikus runbooks esetén.</span><span class="sxs-lookup"><span data-stu-id="f000a-106">The **Export-AzureRmAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="f000a-107">A runbook neve lesz az exportált fájl neve.</span><span class="sxs-lookup"><span data-stu-id="f000a-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="f000a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f000a-108">EXAMPLES</span></span>

### <span data-ttu-id="f000a-109">1. példa: runbook exportálása</span><span class="sxs-lookup"><span data-stu-id="f000a-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzureRmAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="f000a-110">Ez a parancs exportálja az automatizálási runbook közzétett verzióját egy asztali számítógépre.</span><span class="sxs-lookup"><span data-stu-id="f000a-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="f000a-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f000a-111">PARAMETERS</span></span>

### <span data-ttu-id="f000a-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f000a-112">-AutomationAccountName</span></span>
<span data-ttu-id="f000a-113">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag exportál egy runbook.</span><span class="sxs-lookup"><span data-stu-id="f000a-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="f000a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f000a-114">-DefaultProfile</span></span>
<span data-ttu-id="f000a-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f000a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f000a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f000a-116">-Force</span></span>
<span data-ttu-id="f000a-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="f000a-117">ps_force</span></span>

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

### <span data-ttu-id="f000a-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f000a-118">-Name</span></span>
<span data-ttu-id="f000a-119">A parancsmag által exportált runbook nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f000a-119">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="f000a-120">A runbook neve az exportfájl neve lesz.</span><span class="sxs-lookup"><span data-stu-id="f000a-120">The name of the runbook becomes the name of the export file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f000a-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="f000a-121">-OutputFolder</span></span>
<span data-ttu-id="f000a-122">Annak a mappának az elérési útját adja meg, amelyben ez a parancsmag létrehozta az exportálási fájlt.</span><span class="sxs-lookup"><span data-stu-id="f000a-122">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

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

### <span data-ttu-id="f000a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f000a-123">-ResourceGroupName</span></span>
<span data-ttu-id="f000a-124">Annak az erőforráscsoport a neve, amelyhez a parancsmag runbook exportál.</span><span class="sxs-lookup"><span data-stu-id="f000a-124">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="f000a-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="f000a-125">-Slot</span></span>
<span data-ttu-id="f000a-126">Megadja, hogy ez a parancsmag exportálja-e a runbook piszkozatát vagy közzétett tartalmát.</span><span class="sxs-lookup"><span data-stu-id="f000a-126">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="f000a-127">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="f000a-127">Valid values are:</span></span> 

- <span data-ttu-id="f000a-128">Közzétett</span><span class="sxs-lookup"><span data-stu-id="f000a-128">Published</span></span> 
- <span data-ttu-id="f000a-129">Piszkozat</span><span class="sxs-lookup"><span data-stu-id="f000a-129">Draft</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f000a-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f000a-130">-Confirm</span></span>
<span data-ttu-id="f000a-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f000a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f000a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f000a-132">-WhatIf</span></span>
<span data-ttu-id="f000a-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f000a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f000a-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f000a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f000a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f000a-135">CommonParameters</span></span>
<span data-ttu-id="f000a-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f000a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f000a-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f000a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f000a-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f000a-138">INPUTS</span></span>

### <span data-ttu-id="f000a-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="f000a-139">None</span></span>
<span data-ttu-id="f000a-140">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="f000a-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f000a-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f000a-141">OUTPUTS</span></span>

### <span data-ttu-id="f000a-142">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="f000a-142">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="f000a-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f000a-143">NOTES</span></span>

## <span data-ttu-id="f000a-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f000a-144">RELATED LINKS</span></span>

[<span data-ttu-id="f000a-145">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f000a-145">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f000a-146">Importálás – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f000a-146">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f000a-147">Új – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f000a-147">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f000a-148">Új – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f000a-148">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f000a-149">Közzététel – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f000a-149">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f000a-150">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f000a-150">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f000a-151">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f000a-151">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f000a-152">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f000a-152">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


