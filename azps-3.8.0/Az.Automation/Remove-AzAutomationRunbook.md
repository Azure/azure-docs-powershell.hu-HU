---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
ms.openlocfilehash: d6ce3a737063763d77ed408072d275c52ee5884c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014925"
---
# <span data-ttu-id="49062-101">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="49062-101">Remove-AzAutomationRunbook</span></span>

## <span data-ttu-id="49062-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="49062-102">SYNOPSIS</span></span>
<span data-ttu-id="49062-103">Eltávolít egy runbook.</span><span class="sxs-lookup"><span data-stu-id="49062-103">Removes a runbook.</span></span>

## <span data-ttu-id="49062-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="49062-104">SYNTAX</span></span>

```
Remove-AzAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="49062-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="49062-105">DESCRIPTION</span></span>
<span data-ttu-id="49062-106">A **Remove-AzAutomationRunbook** parancsmag eltávolítja a Runbook az Azure automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="49062-106">The **Remove-AzAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="49062-107">Példák</span><span class="sxs-lookup"><span data-stu-id="49062-107">EXAMPLES</span></span>

### <span data-ttu-id="49062-108">1. példa: runbook eltávolítása</span><span class="sxs-lookup"><span data-stu-id="49062-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="49062-109">Ez a parancs eltávolítja a Contoso17 nevű Azure automatizálási fiók Runbook03 nevű runbook.</span><span class="sxs-lookup"><span data-stu-id="49062-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="49062-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="49062-110">PARAMETERS</span></span>

### <span data-ttu-id="49062-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="49062-111">-AutomationAccountName</span></span>
<span data-ttu-id="49062-112">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag eltávolítja a runbook.</span><span class="sxs-lookup"><span data-stu-id="49062-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="49062-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49062-113">-DefaultProfile</span></span>
<span data-ttu-id="49062-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="49062-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49062-115">-Force</span><span class="sxs-lookup"><span data-stu-id="49062-115">-Force</span></span>
<span data-ttu-id="49062-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="49062-116">ps_force</span></span>

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

### <span data-ttu-id="49062-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="49062-117">-Name</span></span>
<span data-ttu-id="49062-118">Annak a runbook a nevét adja meg, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="49062-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="49062-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49062-119">-ResourceGroupName</span></span>
<span data-ttu-id="49062-120">Annak az erőforráscsoportnak a neve, amelyhez a parancsmag runbook tesz közzé.</span><span class="sxs-lookup"><span data-stu-id="49062-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="49062-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="49062-121">-Confirm</span></span>
<span data-ttu-id="49062-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="49062-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49062-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49062-123">-WhatIf</span></span>
<span data-ttu-id="49062-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="49062-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49062-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="49062-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49062-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49062-126">CommonParameters</span></span>
<span data-ttu-id="49062-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="49062-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49062-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49062-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49062-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="49062-129">INPUTS</span></span>

### <span data-ttu-id="49062-130">System. String</span><span class="sxs-lookup"><span data-stu-id="49062-130">System.String</span></span>

## <span data-ttu-id="49062-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49062-131">OUTPUTS</span></span>

### <span data-ttu-id="49062-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="49062-132">System.Void</span></span>

## <span data-ttu-id="49062-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="49062-133">NOTES</span></span>

## <span data-ttu-id="49062-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49062-134">RELATED LINKS</span></span>

[<span data-ttu-id="49062-135">Exportálás – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="49062-135">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="49062-136">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="49062-136">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="49062-137">Importálás – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="49062-137">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="49062-138">Új – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="49062-138">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="49062-139">Új – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="49062-139">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="49062-140">Közzététel – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="49062-140">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="49062-141">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="49062-141">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="49062-142">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="49062-142">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


