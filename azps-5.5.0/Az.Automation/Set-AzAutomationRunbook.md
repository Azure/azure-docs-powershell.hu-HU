---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
ms.openlocfilehash: 0f65d59a29b06959a9763d3900a8ef07dfa517b7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149354"
---
# <span data-ttu-id="511ef-101">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="511ef-101">Set-AzAutomationRunbook</span></span>

## <span data-ttu-id="511ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="511ef-102">SYNOPSIS</span></span>
<span data-ttu-id="511ef-103">Módosít egy runbookot.</span><span class="sxs-lookup"><span data-stu-id="511ef-103">Modifies a runbook.</span></span>

## <span data-ttu-id="511ef-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="511ef-104">SYNTAX</span></span>

```
Set-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="511ef-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="511ef-105">DESCRIPTION</span></span>
<span data-ttu-id="511ef-106">A **Set-AzAutomationRunbook** parancsmag módosítja egy Azure Automation-runbook konfigurációját az APS-ben.</span><span class="sxs-lookup"><span data-stu-id="511ef-106">The **Set-AzAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="511ef-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="511ef-107">EXAMPLES</span></span>

### <span data-ttu-id="511ef-108">1. példa: Részletes naplózás engedélyezése a runbookhoz</span><span class="sxs-lookup"><span data-stu-id="511ef-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="511ef-109">Ez a parancs részletes naplózást tesz lehetővé a Contoso17 nevű Azure Automation-fiók megadott runbookján.</span><span class="sxs-lookup"><span data-stu-id="511ef-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="511ef-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="511ef-110">PARAMETERS</span></span>

### <span data-ttu-id="511ef-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="511ef-111">-AutomationAccountName</span></span>
<span data-ttu-id="511ef-112">Annak az automatizálási fióknak a nevét adja meg, amelyben ez a parancsmag módosít egy runbookot.</span><span class="sxs-lookup"><span data-stu-id="511ef-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="511ef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="511ef-113">-DefaultProfile</span></span>
<span data-ttu-id="511ef-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="511ef-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="511ef-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="511ef-115">-Description</span></span>
<span data-ttu-id="511ef-116">Megadja a runbook leírását.</span><span class="sxs-lookup"><span data-stu-id="511ef-116">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="511ef-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="511ef-117">-LogProgress</span></span>
<span data-ttu-id="511ef-118">Azt adja meg, hogy a runbook naplói haladnak-e.</span><span class="sxs-lookup"><span data-stu-id="511ef-118">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="511ef-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="511ef-119">-LogVerbose</span></span>
<span data-ttu-id="511ef-120">Megadja, hogy a naplózás tartalmaz-e részletes információkat.</span><span class="sxs-lookup"><span data-stu-id="511ef-120">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="511ef-121">-Name</span><span class="sxs-lookup"><span data-stu-id="511ef-121">-Name</span></span>
<span data-ttu-id="511ef-122">Annak a parancsmagnak a nevét adja meg, amely módosítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="511ef-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="511ef-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="511ef-123">-ResourceGroupName</span></span>
<span data-ttu-id="511ef-124">Annak az erőforráscsoportnak a nevét adja meg, amelynek a parancsmagja módosítja a runbookot.</span><span class="sxs-lookup"><span data-stu-id="511ef-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="511ef-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="511ef-125">-Tag</span></span>
<span data-ttu-id="511ef-126">A runbook címkéi.</span><span class="sxs-lookup"><span data-stu-id="511ef-126">The runbook tags.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="511ef-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="511ef-127">CommonParameters</span></span>
<span data-ttu-id="511ef-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="511ef-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="511ef-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="511ef-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="511ef-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="511ef-130">INPUTS</span></span>

### <span data-ttu-id="511ef-131">System.String</span><span class="sxs-lookup"><span data-stu-id="511ef-131">System.String</span></span>

### <span data-ttu-id="511ef-132">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="511ef-132">System.Collections.IDictionary</span></span>

### <span data-ttu-id="511ef-133">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="511ef-133">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="511ef-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="511ef-134">OUTPUTS</span></span>

### <span data-ttu-id="511ef-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span><span class="sxs-lookup"><span data-stu-id="511ef-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="511ef-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="511ef-136">NOTES</span></span>

## <span data-ttu-id="511ef-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="511ef-137">RELATED LINKS</span></span>

[<span data-ttu-id="511ef-138">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="511ef-138">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="511ef-139">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="511ef-139">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="511ef-140">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="511ef-140">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="511ef-141">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="511ef-141">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="511ef-142">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="511ef-142">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="511ef-143">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="511ef-143">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="511ef-144">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="511ef-144">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="511ef-145">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="511ef-145">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


