---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: 78674e3245da1b8a58e099948bff23df9159efec
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014926"
---
# <span data-ttu-id="56517-101">Remove-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="56517-101">Remove-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="56517-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="56517-102">SYNOPSIS</span></span>
<span data-ttu-id="56517-103">Eltávolítja a hibrid munkás csoportot az automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="56517-103">Removes hybrid worker group from Automation.</span></span>

## <span data-ttu-id="56517-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="56517-104">SYNTAX</span></span>

```
Remove-AzAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="56517-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="56517-105">DESCRIPTION</span></span>
<span data-ttu-id="56517-106">Az Remove-AzAutomationHybridWorkerGroup parancsmag eltávolítja a hibrid munkacsoportot az automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="56517-106">The Remove-AzAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="56517-107">Példák</span><span class="sxs-lookup"><span data-stu-id="56517-107">EXAMPLES</span></span>

### <span data-ttu-id="56517-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="56517-108">Example 1</span></span>
<span data-ttu-id="56517-109">Ez a parancs eltávolítja a hibrid munkatársat név szerint.</span><span class="sxs-lookup"><span data-stu-id="56517-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="56517-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="56517-110">PARAMETERS</span></span>

### <span data-ttu-id="56517-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="56517-111">-AutomationAccountName</span></span>
<span data-ttu-id="56517-112">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="56517-112">The automation account name.</span></span>

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

### <span data-ttu-id="56517-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56517-113">-DefaultProfile</span></span>
<span data-ttu-id="56517-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="56517-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56517-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="56517-115">-Name</span></span>
<span data-ttu-id="56517-116">A hibrid munkatárs csoport neve.</span><span class="sxs-lookup"><span data-stu-id="56517-116">The hybrid worker group name.</span></span>

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

### <span data-ttu-id="56517-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56517-117">-ResourceGroupName</span></span>
<span data-ttu-id="56517-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="56517-118">The resource group name.</span></span>

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

### <span data-ttu-id="56517-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="56517-119">-Confirm</span></span>
<span data-ttu-id="56517-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="56517-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56517-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56517-121">-WhatIf</span></span>
<span data-ttu-id="56517-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="56517-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56517-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="56517-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56517-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56517-124">CommonParameters</span></span>
<span data-ttu-id="56517-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="56517-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56517-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56517-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56517-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="56517-127">INPUTS</span></span>

### <span data-ttu-id="56517-128">System. String</span><span class="sxs-lookup"><span data-stu-id="56517-128">System.String</span></span>

## <span data-ttu-id="56517-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="56517-129">OUTPUTS</span></span>

### <span data-ttu-id="56517-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="56517-130">System.Void</span></span>

## <span data-ttu-id="56517-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="56517-131">NOTES</span></span>

## <span data-ttu-id="56517-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="56517-132">RELATED LINKS</span></span>
