---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
ms.openlocfilehash: 00d6908e244a54fb2dbd501f0d944fc9cfdbdff4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014277"
---
# <span data-ttu-id="dd553-101">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dd553-101">Get-AzAutomationRunbook</span></span>

## <span data-ttu-id="dd553-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd553-102">SYNOPSIS</span></span>
<span data-ttu-id="dd553-103">Runbookot kap.</span><span class="sxs-lookup"><span data-stu-id="dd553-103">Gets a runbook.</span></span>

## <span data-ttu-id="dd553-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dd553-104">SYNTAX</span></span>

### <span data-ttu-id="dd553-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dd553-105">ByAll (Default)</span></span>
```
Get-AzAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd553-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="dd553-106">ByRunbookName</span></span>
```
Get-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd553-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dd553-107">DESCRIPTION</span></span>
<span data-ttu-id="dd553-108">A **Get-AzAutomationRunbook parancsmag** az Azure Automation-runbookokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="dd553-108">The **Get-AzAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="dd553-109">Ha egy adott runbookot meg kell adnia, adja meg a nevét.</span><span class="sxs-lookup"><span data-stu-id="dd553-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="dd553-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dd553-110">EXAMPLES</span></span>

### <span data-ttu-id="dd553-111">1. példa: Az összes runbook lekérte</span><span class="sxs-lookup"><span data-stu-id="dd553-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="dd553-112">Ez a parancs a Contoso17 nevű Azure Automation-fiók összes runbookját beveszi.</span><span class="sxs-lookup"><span data-stu-id="dd553-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="dd553-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd553-113">PARAMETERS</span></span>

### <span data-ttu-id="dd553-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dd553-114">-AutomationAccountName</span></span>
<span data-ttu-id="dd553-115">Annak az automatizálási fióknak a nevét adja meg, amelyben ez a parancsmag runbookokat kap.</span><span class="sxs-lookup"><span data-stu-id="dd553-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="dd553-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd553-116">-DefaultProfile</span></span>
<span data-ttu-id="dd553-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dd553-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd553-118">-Name</span><span class="sxs-lookup"><span data-stu-id="dd553-118">-Name</span></span>
<span data-ttu-id="dd553-119">Annak a runbooknak a nevét adja meg, amelybe ez a parancsmag kerül.</span><span class="sxs-lookup"><span data-stu-id="dd553-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="dd553-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd553-120">-ResourceGroupName</span></span>
<span data-ttu-id="dd553-121">Annak az erőforráscsoportnak a neve, amelynek a parancsmagja runbookokat kap.</span><span class="sxs-lookup"><span data-stu-id="dd553-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="dd553-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd553-122">CommonParameters</span></span>
<span data-ttu-id="dd553-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd553-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd553-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd553-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd553-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dd553-125">INPUTS</span></span>

### <span data-ttu-id="dd553-126">System.String</span><span class="sxs-lookup"><span data-stu-id="dd553-126">System.String</span></span>

## <span data-ttu-id="dd553-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dd553-127">OUTPUTS</span></span>

### <span data-ttu-id="dd553-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span><span class="sxs-lookup"><span data-stu-id="dd553-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="dd553-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dd553-129">NOTES</span></span>

## <span data-ttu-id="dd553-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dd553-130">RELATED LINKS</span></span>

[<span data-ttu-id="dd553-131">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dd553-131">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="dd553-132">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dd553-132">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="dd553-133">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dd553-133">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="dd553-134">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dd553-134">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="dd553-135">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dd553-135">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="dd553-136">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dd553-136">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="dd553-137">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dd553-137">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="dd553-138">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dd553-138">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


