---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
ms.openlocfilehash: 03a57c35063a401aa5f730e11538532bdbbbc58c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478773"
---
# <span data-ttu-id="7ffeb-101">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7ffeb-101">Export-AzAutomationRunbook</span></span>

## <span data-ttu-id="7ffeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ffeb-102">SYNOPSIS</span></span>
<span data-ttu-id="7ffeb-103">Automatizálási runbook exportálása.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-103">Exports an Automation runbook.</span></span>

## <span data-ttu-id="7ffeb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7ffeb-104">SYNTAX</span></span>

```
Export-AzAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ffeb-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7ffeb-105">DESCRIPTION</span></span>
<span data-ttu-id="7ffeb-106">Az **Export-AzAutomationRunbook** parancsmag egy Azure Automation-runbookot exportál egy wps_2-parancsfájlba (.ps1) egy wps_2- vagy wps_2-munkafolyamat-runbookba, illetve grafikus runbookfájlba (.graphrunbook) grafikus runbookok számára.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-106">The **Export-AzAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="7ffeb-107">A runbook neve lesz az exportált fájl neve.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="7ffeb-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7ffeb-108">EXAMPLES</span></span>

### <span data-ttu-id="7ffeb-109">1. példa: Runbook exportálása</span><span class="sxs-lookup"><span data-stu-id="7ffeb-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="7ffeb-110">Ez a parancs exportálja az Automatizálási runbook közzétett verzióját egy felhasználói asztalra.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="7ffeb-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ffeb-111">PARAMETERS</span></span>

### <span data-ttu-id="7ffeb-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7ffeb-112">-AutomationAccountName</span></span>
<span data-ttu-id="7ffeb-113">Annak az automatizálási fióknak a nevét adja meg, amelybe ez a parancsmag egy runbookot exportál.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="7ffeb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ffeb-114">-DefaultProfile</span></span>
<span data-ttu-id="7ffeb-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7ffeb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ffeb-116">-Force</span><span class="sxs-lookup"><span data-stu-id="7ffeb-116">-Force</span></span>
<span data-ttu-id="7ffeb-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="7ffeb-117">ps_force</span></span>

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

### <span data-ttu-id="7ffeb-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7ffeb-118">-Name</span></span>
<span data-ttu-id="7ffeb-119">Annak a parancsmagnak a nevét adja meg, amely exportálja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-119">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="7ffeb-120">A runbook neve lesz az exportált fájl neve.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-120">The name of the runbook becomes the name of the export file.</span></span>

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

### <span data-ttu-id="7ffeb-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="7ffeb-121">-OutputFolder</span></span>
<span data-ttu-id="7ffeb-122">Annak a mappának az elérési útját adja meg, amelyben ez a parancsmag létrehozza az exportálási fájlt.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-122">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

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

### <span data-ttu-id="7ffeb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ffeb-123">-ResourceGroupName</span></span>
<span data-ttu-id="7ffeb-124">Annak az erőforráscsoportnak a neve, amelynek a parancsmagja runbookot exportál.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-124">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="7ffeb-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="7ffeb-125">-Slot</span></span>
<span data-ttu-id="7ffeb-126">Azt adja meg, hogy a parancsmag exportálja-e a runbook piszkozatát vagy közzétett tartalmát.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-126">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="7ffeb-127">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="7ffeb-127">Valid values are:</span></span> 
- <span data-ttu-id="7ffeb-128">Közzétéve</span><span class="sxs-lookup"><span data-stu-id="7ffeb-128">Published</span></span> 
- <span data-ttu-id="7ffeb-129">Piszkozat</span><span class="sxs-lookup"><span data-stu-id="7ffeb-129">Draft</span></span>

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

### <span data-ttu-id="7ffeb-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ffeb-130">-Confirm</span></span>
<span data-ttu-id="7ffeb-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ffeb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ffeb-132">-WhatIf</span></span>
<span data-ttu-id="7ffeb-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ffeb-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ffeb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ffeb-135">CommonParameters</span></span>
<span data-ttu-id="7ffeb-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ffeb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ffeb-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ffeb-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ffeb-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ffeb-138">INPUTS</span></span>

### <span data-ttu-id="7ffeb-139">System.String</span><span class="sxs-lookup"><span data-stu-id="7ffeb-139">System.String</span></span>

## <span data-ttu-id="7ffeb-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ffeb-140">OUTPUTS</span></span>

### <span data-ttu-id="7ffeb-141">System.IO.DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="7ffeb-141">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="7ffeb-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7ffeb-142">NOTES</span></span>

## <span data-ttu-id="7ffeb-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ffeb-143">RELATED LINKS</span></span>

[<span data-ttu-id="7ffeb-144">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7ffeb-144">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="7ffeb-145">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7ffeb-145">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="7ffeb-146">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7ffeb-146">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="7ffeb-147">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7ffeb-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="7ffeb-148">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7ffeb-148">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="7ffeb-149">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7ffeb-149">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="7ffeb-150">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7ffeb-150">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="7ffeb-151">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7ffeb-151">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


