---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: b9f23105b6fa84781ef1b0f0ba4be0e52e06ee08
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671530"
---
# <span data-ttu-id="85a93-101">Remove-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="85a93-101">Remove-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="85a93-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="85a93-102">SYNOPSIS</span></span>
<span data-ttu-id="85a93-103">Eltávolítja a hibrid munkás csoportot az automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="85a93-103">Removes hybrid worker group from Automation.</span></span>

## <span data-ttu-id="85a93-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="85a93-104">SYNTAX</span></span>

```
Remove-AzAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="85a93-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="85a93-105">DESCRIPTION</span></span>
<span data-ttu-id="85a93-106">Az Remove-AzAutomationHybridWorkerGroup parancsmag eltávolítja a hibrid munkacsoportot az automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="85a93-106">The Remove-AzAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="85a93-107">Példák</span><span class="sxs-lookup"><span data-stu-id="85a93-107">EXAMPLES</span></span>

### <span data-ttu-id="85a93-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="85a93-108">Example 1</span></span>
<span data-ttu-id="85a93-109">Ez a parancs eltávolítja a hibrid munkatársat név szerint.</span><span class="sxs-lookup"><span data-stu-id="85a93-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="85a93-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="85a93-110">PARAMETERS</span></span>

### <span data-ttu-id="85a93-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="85a93-111">-AutomationAccountName</span></span>
<span data-ttu-id="85a93-112">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="85a93-112">The automation account name.</span></span>

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

### <span data-ttu-id="85a93-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85a93-113">-DefaultProfile</span></span>
<span data-ttu-id="85a93-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="85a93-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85a93-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="85a93-115">-Name</span></span>
<span data-ttu-id="85a93-116">A hibrid munkatárs csoport neve.</span><span class="sxs-lookup"><span data-stu-id="85a93-116">The hybrid worker group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85a93-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85a93-117">-ResourceGroupName</span></span>
<span data-ttu-id="85a93-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="85a93-118">The resource group name.</span></span>

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

### <span data-ttu-id="85a93-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="85a93-119">-Confirm</span></span>
<span data-ttu-id="85a93-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="85a93-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85a93-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85a93-121">-WhatIf</span></span>
<span data-ttu-id="85a93-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="85a93-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85a93-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="85a93-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85a93-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85a93-124">CommonParameters</span></span>
<span data-ttu-id="85a93-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="85a93-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85a93-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85a93-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85a93-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="85a93-127">INPUTS</span></span>

### <span data-ttu-id="85a93-128">System. String</span><span class="sxs-lookup"><span data-stu-id="85a93-128">System.String</span></span>

## <span data-ttu-id="85a93-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="85a93-129">OUTPUTS</span></span>

### <span data-ttu-id="85a93-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="85a93-130">System.Void</span></span>

## <span data-ttu-id="85a93-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="85a93-131">NOTES</span></span>

## <span data-ttu-id="85a93-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="85a93-132">RELATED LINKS</span></span>
