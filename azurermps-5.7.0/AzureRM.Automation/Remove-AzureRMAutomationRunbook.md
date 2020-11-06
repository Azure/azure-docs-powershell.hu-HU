---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationRunbook.md
ms.openlocfilehash: a4f65e20253ef979cba5d3907faeba3fb58e7fe6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504592"
---
# <span data-ttu-id="dce9c-101">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dce9c-101">Remove-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="dce9c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dce9c-102">SYNOPSIS</span></span>
<span data-ttu-id="dce9c-103">Eltávolít egy runbook.</span><span class="sxs-lookup"><span data-stu-id="dce9c-103">Removes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dce9c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dce9c-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dce9c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dce9c-105">DESCRIPTION</span></span>
<span data-ttu-id="dce9c-106">A **Remove-AzureRmAutomationRunbook** parancsmag eltávolítja a Runbook az Azure automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="dce9c-106">The **Remove-AzureRmAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="dce9c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dce9c-107">EXAMPLES</span></span>

### <span data-ttu-id="dce9c-108">1. példa: runbook eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dce9c-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="dce9c-109">Ez a parancs eltávolítja a Contoso17 nevű Azure automatizálási fiók Runbook03 nevű runbook.</span><span class="sxs-lookup"><span data-stu-id="dce9c-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="dce9c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dce9c-110">PARAMETERS</span></span>

### <span data-ttu-id="dce9c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dce9c-111">-AutomationAccountName</span></span>
<span data-ttu-id="dce9c-112">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag eltávolítja a runbook.</span><span class="sxs-lookup"><span data-stu-id="dce9c-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="dce9c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dce9c-113">-DefaultProfile</span></span>
<span data-ttu-id="dce9c-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dce9c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dce9c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="dce9c-115">-Force</span></span>
<span data-ttu-id="dce9c-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="dce9c-116">ps_force</span></span>

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

### <span data-ttu-id="dce9c-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dce9c-117">-Name</span></span>
<span data-ttu-id="dce9c-118">Annak a runbook a nevét adja meg, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="dce9c-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dce9c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dce9c-119">-ResourceGroupName</span></span>
<span data-ttu-id="dce9c-120">Annak az erőforráscsoportnak a neve, amelyhez a parancsmag runbook tesz közzé.</span><span class="sxs-lookup"><span data-stu-id="dce9c-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="dce9c-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dce9c-121">-Confirm</span></span>
<span data-ttu-id="dce9c-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dce9c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dce9c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dce9c-123">-WhatIf</span></span>
<span data-ttu-id="dce9c-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dce9c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dce9c-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dce9c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dce9c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dce9c-126">CommonParameters</span></span>
<span data-ttu-id="dce9c-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dce9c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dce9c-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dce9c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dce9c-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dce9c-129">INPUTS</span></span>

### <span data-ttu-id="dce9c-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="dce9c-130">None</span></span>
<span data-ttu-id="dce9c-131">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="dce9c-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dce9c-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dce9c-132">OUTPUTS</span></span>

## <span data-ttu-id="dce9c-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dce9c-133">NOTES</span></span>

## <span data-ttu-id="dce9c-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dce9c-134">RELATED LINKS</span></span>

[<span data-ttu-id="dce9c-135">Exportálás – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dce9c-135">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="dce9c-136">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dce9c-136">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="dce9c-137">Importálás – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dce9c-137">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="dce9c-138">Új – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dce9c-138">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="dce9c-139">Új – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dce9c-139">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="dce9c-140">Közzététel – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dce9c-140">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="dce9c-141">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dce9c-141">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="dce9c-142">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dce9c-142">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


