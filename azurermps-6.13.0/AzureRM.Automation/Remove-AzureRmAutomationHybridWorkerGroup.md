---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationHybridWorkerGroup.md
ms.openlocfilehash: b6f15bc55c2e9f9a05e60e7e6f2c139ddbb70454
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672324"
---
# <span data-ttu-id="2b09c-101">Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="2b09c-101">Remove-AzureRmAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="2b09c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2b09c-102">SYNOPSIS</span></span>
<span data-ttu-id="2b09c-103">Eltávolítja a hibrid munkás csoportot az automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="2b09c-103">Removes hybrid worker group from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b09c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2b09c-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b09c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2b09c-105">DESCRIPTION</span></span>
<span data-ttu-id="2b09c-106">Az Remove-AzureRmAutomationHybridWorkerGroup parancsmag eltávolítja a hibrid munkacsoportot az automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="2b09c-106">The Remove-AzureRmAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="2b09c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2b09c-107">EXAMPLES</span></span>

### <span data-ttu-id="2b09c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2b09c-108">Example 1</span></span>
<span data-ttu-id="2b09c-109">Ez a parancs eltávolítja a hibrid munkatársat név szerint.</span><span class="sxs-lookup"><span data-stu-id="2b09c-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzureRmAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="2b09c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2b09c-110">PARAMETERS</span></span>

### <span data-ttu-id="2b09c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2b09c-111">-AutomationAccountName</span></span>
<span data-ttu-id="2b09c-112">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="2b09c-112">The automation account name.</span></span>

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

### <span data-ttu-id="2b09c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b09c-113">-DefaultProfile</span></span>
<span data-ttu-id="2b09c-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2b09c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b09c-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2b09c-115">-Name</span></span>
<span data-ttu-id="2b09c-116">A hibrid munkatárs csoport neve.</span><span class="sxs-lookup"><span data-stu-id="2b09c-116">The hybrid worker group name.</span></span>

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

### <span data-ttu-id="2b09c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b09c-117">-ResourceGroupName</span></span>
<span data-ttu-id="2b09c-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="2b09c-118">The resource group name.</span></span>

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

### <span data-ttu-id="2b09c-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2b09c-119">-Confirm</span></span>
<span data-ttu-id="2b09c-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2b09c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b09c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b09c-121">-WhatIf</span></span>
<span data-ttu-id="2b09c-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2b09c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b09c-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2b09c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b09c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b09c-124">CommonParameters</span></span>
<span data-ttu-id="2b09c-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2b09c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b09c-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b09c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b09c-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b09c-127">INPUTS</span></span>

### <span data-ttu-id="2b09c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2b09c-128">System.String</span></span>

## <span data-ttu-id="2b09c-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b09c-129">OUTPUTS</span></span>

### <span data-ttu-id="2b09c-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="2b09c-130">System.Void</span></span>

## <span data-ttu-id="2b09c-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2b09c-131">NOTES</span></span>

## <span data-ttu-id="2b09c-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b09c-132">RELATED LINKS</span></span>
