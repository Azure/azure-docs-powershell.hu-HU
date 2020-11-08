---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
ms.openlocfilehash: 0c37c33b60d430bc1782254401033934552f5663
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024914"
---
# <span data-ttu-id="fbec2-101">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="fbec2-101">Remove-AzAutomationSchedule</span></span>

## <span data-ttu-id="fbec2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fbec2-102">SYNOPSIS</span></span>
<span data-ttu-id="fbec2-103">Automatizálási ütemterv törlése</span><span class="sxs-lookup"><span data-stu-id="fbec2-103">Deletes an Automation schedule.</span></span>

## <span data-ttu-id="fbec2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fbec2-104">SYNTAX</span></span>

```
Remove-AzAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fbec2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fbec2-105">DESCRIPTION</span></span>
<span data-ttu-id="fbec2-106">A **Remove-AzAutomationSchedule** parancsmag az Azure Automation szolgáltatásból törli az ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="fbec2-106">The **Remove-AzAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="fbec2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fbec2-107">EXAMPLES</span></span>

### <span data-ttu-id="fbec2-108">1. példa: ütemterv eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fbec2-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="fbec2-109">Ez a parancs törli a Schedule01 az automatizálási fiók Contoso17 az erőforrás csoport ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="fbec2-109">This command deletes the schedule named Schedule01 in automation account Contoso17 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="fbec2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fbec2-110">PARAMETERS</span></span>

### <span data-ttu-id="fbec2-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fbec2-111">-AutomationAccountName</span></span>
<span data-ttu-id="fbec2-112">Annak az automatizálási fióknak a nevét adja meg, amelyhez ez a parancsmag eltávolítja az ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="fbec2-112">Specifies the name of an Automation account for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="fbec2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbec2-113">-DefaultProfile</span></span>
<span data-ttu-id="fbec2-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fbec2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbec2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fbec2-115">-Force</span></span>
<span data-ttu-id="fbec2-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="fbec2-116">ps_force</span></span>

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

### <span data-ttu-id="fbec2-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fbec2-117">-Name</span></span>
<span data-ttu-id="fbec2-118">A parancsmag által eltávolított ütemterv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fbec2-118">Specifies the name for the schedule that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbec2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbec2-119">-ResourceGroupName</span></span>
<span data-ttu-id="fbec2-120">Annak a csoportnak a nevét adja meg, amelyhez ez a parancsmag eltávolítja az ütemtervet.</span><span class="sxs-lookup"><span data-stu-id="fbec2-120">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="fbec2-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fbec2-121">-Confirm</span></span>
<span data-ttu-id="fbec2-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fbec2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbec2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbec2-123">-WhatIf</span></span>
<span data-ttu-id="fbec2-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fbec2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbec2-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fbec2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbec2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbec2-126">CommonParameters</span></span>
<span data-ttu-id="fbec2-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fbec2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbec2-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbec2-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbec2-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbec2-129">INPUTS</span></span>

### <span data-ttu-id="fbec2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fbec2-130">System.String</span></span>

## <span data-ttu-id="fbec2-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbec2-131">OUTPUTS</span></span>

### <span data-ttu-id="fbec2-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="fbec2-132">System.Void</span></span>

## <span data-ttu-id="fbec2-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fbec2-133">NOTES</span></span>

## <span data-ttu-id="fbec2-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fbec2-134">RELATED LINKS</span></span>

[<span data-ttu-id="fbec2-135">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="fbec2-135">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="fbec2-136">Új – AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="fbec2-136">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="fbec2-137">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="fbec2-137">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


