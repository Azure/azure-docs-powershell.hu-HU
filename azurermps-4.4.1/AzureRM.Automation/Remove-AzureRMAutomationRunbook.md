---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationRunbook.md
ms.openlocfilehash: 96a82f4cc39952517bf5cfaeca24191cc4dd2d9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499235"
---
# <span data-ttu-id="59cfb-101">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="59cfb-101">Remove-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="59cfb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="59cfb-102">SYNOPSIS</span></span>
<span data-ttu-id="59cfb-103">Eltávolít egy runbook.</span><span class="sxs-lookup"><span data-stu-id="59cfb-103">Removes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59cfb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="59cfb-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59cfb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="59cfb-105">DESCRIPTION</span></span>
<span data-ttu-id="59cfb-106">A **Remove-AzureRmAutomationRunbook** parancsmag eltávolítja a Runbook az Azure automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="59cfb-106">The **Remove-AzureRmAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="59cfb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="59cfb-107">EXAMPLES</span></span>

### <span data-ttu-id="59cfb-108">1. példa: runbook eltávolítása</span><span class="sxs-lookup"><span data-stu-id="59cfb-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="59cfb-109">Ez a parancs eltávolítja a Contoso17 nevű Azure automatizálási fiók Runbook03 nevű runbook.</span><span class="sxs-lookup"><span data-stu-id="59cfb-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="59cfb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="59cfb-110">PARAMETERS</span></span>

### <span data-ttu-id="59cfb-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="59cfb-111">-AutomationAccountName</span></span>
<span data-ttu-id="59cfb-112">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag eltávolítja a runbook.</span><span class="sxs-lookup"><span data-stu-id="59cfb-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="59cfb-113">-Force</span><span class="sxs-lookup"><span data-stu-id="59cfb-113">-Force</span></span>
<span data-ttu-id="59cfb-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="59cfb-114">ps_force</span></span>

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

### <span data-ttu-id="59cfb-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="59cfb-115">-Name</span></span>
<span data-ttu-id="59cfb-116">Annak a runbook a nevét adja meg, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="59cfb-116">Specifies the name of the runbook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="59cfb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59cfb-117">-ResourceGroupName</span></span>
<span data-ttu-id="59cfb-118">Annak az erőforráscsoportnak a neve, amelyhez a parancsmag runbook tesz közzé.</span><span class="sxs-lookup"><span data-stu-id="59cfb-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="59cfb-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="59cfb-119">-Confirm</span></span>
<span data-ttu-id="59cfb-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="59cfb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59cfb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59cfb-121">-WhatIf</span></span>
<span data-ttu-id="59cfb-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="59cfb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59cfb-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="59cfb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59cfb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59cfb-124">-DefaultProfile</span></span>
<span data-ttu-id="59cfb-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59cfb-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59cfb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59cfb-126">CommonParameters</span></span>
<span data-ttu-id="59cfb-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="59cfb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59cfb-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59cfb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59cfb-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="59cfb-129">INPUTS</span></span>

## <span data-ttu-id="59cfb-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59cfb-130">OUTPUTS</span></span>

## <span data-ttu-id="59cfb-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="59cfb-131">NOTES</span></span>

## <span data-ttu-id="59cfb-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59cfb-132">RELATED LINKS</span></span>

[<span data-ttu-id="59cfb-133">Exportálás – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="59cfb-133">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="59cfb-134">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="59cfb-134">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="59cfb-135">Importálás – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="59cfb-135">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="59cfb-136">Új – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="59cfb-136">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="59cfb-137">Új – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="59cfb-137">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="59cfb-138">Közzététel – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="59cfb-138">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="59cfb-139">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="59cfb-139">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="59cfb-140">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="59cfb-140">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


