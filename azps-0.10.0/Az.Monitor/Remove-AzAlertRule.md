---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzAlertRule.md
ms.openlocfilehash: 693a945466e294ed17e856671d3bd6fc93ad2f3d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841930"
---
# <span data-ttu-id="d68d3-101">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="d68d3-101">Remove-AzAlertRule</span></span>

## <span data-ttu-id="d68d3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d68d3-102">SYNOPSIS</span></span>
<span data-ttu-id="d68d3-103">Figyelmeztetési szabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d68d3-103">Removes an alert rule.</span></span>

## <span data-ttu-id="d68d3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d68d3-104">SYNTAX</span></span>

```
Remove-AzAlertRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d68d3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d68d3-105">DESCRIPTION</span></span>
<span data-ttu-id="d68d3-106">A **Remove-AzAlertRule** parancsmag eltávolít egy figyelmeztetési szabályt.</span><span class="sxs-lookup"><span data-stu-id="d68d3-106">The **Remove-AzAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="d68d3-107">Meg kell adnia a riasztási szabály és az erőforrás-csoport nevét, amelyhez hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="d68d3-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>
<span data-ttu-id="d68d3-108">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="d68d3-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="d68d3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d68d3-109">EXAMPLES</span></span>

### <span data-ttu-id="d68d3-110">1. példa: figyelmeztetési szabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d68d3-110">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="d68d3-111">Ez a parancs eltávolítja a myalert-7da64548-214d-42CA-b12b-b245bb8f0ac8 nevű riasztási szabályt az erőforráscsoport Default-Web-CentralUS.</span><span class="sxs-lookup"><span data-stu-id="d68d3-111">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="d68d3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d68d3-112">PARAMETERS</span></span>

### <span data-ttu-id="d68d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d68d3-113">-DefaultProfile</span></span>
<span data-ttu-id="d68d3-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d68d3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d68d3-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d68d3-115">-Name</span></span>
<span data-ttu-id="d68d3-116">Az eltávolítandó figyelmeztetési szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d68d3-116">Specifies the name of the alert rule to remove.</span></span>

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

### <span data-ttu-id="d68d3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d68d3-117">-ResourceGroupName</span></span>
<span data-ttu-id="d68d3-118">Az értesítési szabály erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d68d3-118">Specifies the name of the resource group for the alert rule.</span></span>

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

### <span data-ttu-id="d68d3-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d68d3-119">-Confirm</span></span>
<span data-ttu-id="d68d3-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d68d3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d68d3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d68d3-121">-WhatIf</span></span>
<span data-ttu-id="d68d3-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d68d3-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d68d3-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d68d3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d68d3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d68d3-124">CommonParameters</span></span>
<span data-ttu-id="d68d3-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d68d3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d68d3-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d68d3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d68d3-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d68d3-127">INPUTS</span></span>

### <span data-ttu-id="d68d3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d68d3-128">System.String</span></span>

## <span data-ttu-id="d68d3-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d68d3-129">OUTPUTS</span></span>

### <span data-ttu-id="d68d3-130">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d68d3-130">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="d68d3-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d68d3-131">NOTES</span></span>

## <span data-ttu-id="d68d3-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d68d3-132">RELATED LINKS</span></span>

[<span data-ttu-id="d68d3-133">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="d68d3-133">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="d68d3-134">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="d68d3-134">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="d68d3-135">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="d68d3-135">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="d68d3-136">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="d68d3-136">Get-AzAlertRule</span></span>](./Get-AzAlertRule.md)


