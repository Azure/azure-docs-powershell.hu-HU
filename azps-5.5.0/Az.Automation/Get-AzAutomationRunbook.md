---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
ms.openlocfilehash: edae476893de5a64e950902d2de7b31fe53b51ea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166883"
---
# <span data-ttu-id="fbde6-101">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fbde6-101">Get-AzAutomationRunbook</span></span>

## <span data-ttu-id="fbde6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbde6-102">SYNOPSIS</span></span>
<span data-ttu-id="fbde6-103">Runbookot kap.</span><span class="sxs-lookup"><span data-stu-id="fbde6-103">Gets a runbook.</span></span>

## <span data-ttu-id="fbde6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fbde6-104">SYNTAX</span></span>

### <span data-ttu-id="fbde6-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fbde6-105">ByAll (Default)</span></span>
```
Get-AzAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbde6-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="fbde6-106">ByRunbookName</span></span>
```
Get-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbde6-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fbde6-107">DESCRIPTION</span></span>
<span data-ttu-id="fbde6-108">A **Get-AzAutomationRunbook parancsmag** az Azure Automation-runbookokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fbde6-108">The **Get-AzAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="fbde6-109">Ha egy adott runbookot meg kell adnia, adja meg a nevét.</span><span class="sxs-lookup"><span data-stu-id="fbde6-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="fbde6-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fbde6-110">EXAMPLES</span></span>

### <span data-ttu-id="fbde6-111">1. példa: Az összes runbook lekérte</span><span class="sxs-lookup"><span data-stu-id="fbde6-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="fbde6-112">Ez a parancs a Contoso17 nevű Azure Automation-fiók összes runbookját beveszi.</span><span class="sxs-lookup"><span data-stu-id="fbde6-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="fbde6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbde6-113">PARAMETERS</span></span>

### <span data-ttu-id="fbde6-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fbde6-114">-AutomationAccountName</span></span>
<span data-ttu-id="fbde6-115">Annak az automatizálási fióknak a nevét adja meg, amelyben ez a parancsmag runbookokat kap.</span><span class="sxs-lookup"><span data-stu-id="fbde6-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="fbde6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbde6-116">-DefaultProfile</span></span>
<span data-ttu-id="fbde6-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fbde6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbde6-118">-Name</span><span class="sxs-lookup"><span data-stu-id="fbde6-118">-Name</span></span>
<span data-ttu-id="fbde6-119">A parancsmag által lekért runbook nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fbde6-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbde6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbde6-120">-ResourceGroupName</span></span>
<span data-ttu-id="fbde6-121">Annak az erőforráscsoportnak a neve, amelynek a parancsmagja runbookokat kap.</span><span class="sxs-lookup"><span data-stu-id="fbde6-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="fbde6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbde6-122">CommonParameters</span></span>
<span data-ttu-id="fbde6-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbde6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbde6-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbde6-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbde6-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fbde6-125">INPUTS</span></span>

### <span data-ttu-id="fbde6-126">System.String</span><span class="sxs-lookup"><span data-stu-id="fbde6-126">System.String</span></span>

## <span data-ttu-id="fbde6-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbde6-127">OUTPUTS</span></span>

### <span data-ttu-id="fbde6-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span><span class="sxs-lookup"><span data-stu-id="fbde6-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="fbde6-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fbde6-129">NOTES</span></span>

## <span data-ttu-id="fbde6-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fbde6-130">RELATED LINKS</span></span>

[<span data-ttu-id="fbde6-131">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fbde6-131">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="fbde6-132">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fbde6-132">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="fbde6-133">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fbde6-133">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="fbde6-134">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fbde6-134">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="fbde6-135">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fbde6-135">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="fbde6-136">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fbde6-136">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="fbde6-137">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fbde6-137">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="fbde6-138">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fbde6-138">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


