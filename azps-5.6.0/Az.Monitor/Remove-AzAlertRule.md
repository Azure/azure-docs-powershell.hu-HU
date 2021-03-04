---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAlertRule.md
ms.openlocfilehash: 61a24b5ec7e63ce9a3059257cf1772c4e15d100b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924810"
---
# <span data-ttu-id="3acfe-101">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="3acfe-101">Remove-AzAlertRule</span></span>

## <span data-ttu-id="3acfe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3acfe-102">SYNOPSIS</span></span>
<span data-ttu-id="3acfe-103">Eltávolít egy riasztási szabályt.</span><span class="sxs-lookup"><span data-stu-id="3acfe-103">Removes an alert rule.</span></span>

## <span data-ttu-id="3acfe-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3acfe-104">SYNTAX</span></span>

```
Remove-AzAlertRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3acfe-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3acfe-105">DESCRIPTION</span></span>
<span data-ttu-id="3acfe-106">Az **Remove-AzAlertRule** parancsmag eltávolít egy riasztási szabályt.</span><span class="sxs-lookup"><span data-stu-id="3acfe-106">The **Remove-AzAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="3acfe-107">Meg kell adnia a riasztási szabály nevét és azt az erőforráscsoportot, amelyhez hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="3acfe-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>
<span data-ttu-id="3acfe-108">Ez a parancsmag implementálja a ShouldProcess mintát, azaz megerősítést kérhet a felhasználótól, mielőtt ténylegesen létrehozza, módosítja vagy eltávolítja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="3acfe-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="3acfe-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3acfe-109">EXAMPLES</span></span>

### <span data-ttu-id="3acfe-110">1. példa: Értesítési szabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3acfe-110">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="3acfe-111">Ez a parancs eltávolítja a Myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 nevű riasztási szabályt a Default-Web-CentralUS erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="3acfe-111">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="3acfe-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3acfe-112">PARAMETERS</span></span>

### <span data-ttu-id="3acfe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3acfe-113">-DefaultProfile</span></span>
<span data-ttu-id="3acfe-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3acfe-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3acfe-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3acfe-115">-Name</span></span>
<span data-ttu-id="3acfe-116">Az eltávolítható riasztási szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3acfe-116">Specifies the name of the alert rule to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3acfe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3acfe-117">-ResourceGroupName</span></span>
<span data-ttu-id="3acfe-118">A riasztási szabály erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3acfe-118">Specifies the name of the resource group for the alert rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3acfe-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3acfe-119">-Confirm</span></span>
<span data-ttu-id="3acfe-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3acfe-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3acfe-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3acfe-121">-WhatIf</span></span>
<span data-ttu-id="3acfe-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3acfe-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3acfe-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3acfe-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3acfe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3acfe-124">CommonParameters</span></span>
<span data-ttu-id="3acfe-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3acfe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3acfe-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3acfe-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3acfe-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3acfe-127">INPUTS</span></span>

### <span data-ttu-id="3acfe-128">System.String</span><span class="sxs-lookup"><span data-stu-id="3acfe-128">System.String</span></span>

## <span data-ttu-id="3acfe-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3acfe-129">OUTPUTS</span></span>

### <span data-ttu-id="3acfe-130">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3acfe-130">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="3acfe-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3acfe-131">NOTES</span></span>

## <span data-ttu-id="3acfe-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3acfe-132">RELATED LINKS</span></span>

[<span data-ttu-id="3acfe-133">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="3acfe-133">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="3acfe-134">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="3acfe-134">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="3acfe-135">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="3acfe-135">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="3acfe-136">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="3acfe-136">Get-AzAlertRule</span></span>](./Get-AzAlertRule.md)


