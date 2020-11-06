---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
ms.openlocfilehash: bca70877b8821b06e6662f334120f126328f4451
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503676"
---
# <span data-ttu-id="36788-101">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="36788-101">Remove-AzureRmAlertRule</span></span>

## <span data-ttu-id="36788-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="36788-102">SYNOPSIS</span></span>
<span data-ttu-id="36788-103">Figyelmeztetési szabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="36788-103">Removes an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36788-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="36788-104">SYNTAX</span></span>

```
Remove-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36788-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="36788-105">DESCRIPTION</span></span>
<span data-ttu-id="36788-106">A **Remove-AzureRmAlertRule** parancsmag eltávolít egy figyelmeztetési szabályt.</span><span class="sxs-lookup"><span data-stu-id="36788-106">The **Remove-AzureRmAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="36788-107">Meg kell adnia a riasztási szabály és az erőforrás-csoport nevét, amelyhez hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="36788-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>
<span data-ttu-id="36788-108">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="36788-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="36788-109">Példák</span><span class="sxs-lookup"><span data-stu-id="36788-109">EXAMPLES</span></span>

### <span data-ttu-id="36788-110">1. példa: figyelmeztetési szabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="36788-110">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="36788-111">Ez a parancs eltávolítja a myalert-7da64548-214d-42CA-b12b-b245bb8f0ac8 nevű riasztási szabályt az erőforráscsoport Default-Web-CentralUS.</span><span class="sxs-lookup"><span data-stu-id="36788-111">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="36788-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="36788-112">PARAMETERS</span></span>

### <span data-ttu-id="36788-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36788-113">-DefaultProfile</span></span>
<span data-ttu-id="36788-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="36788-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36788-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="36788-115">-Name</span></span>
<span data-ttu-id="36788-116">Az eltávolítandó figyelmeztetési szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="36788-116">Specifies the name of the alert rule to remove.</span></span>

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

### <span data-ttu-id="36788-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36788-117">-ResourceGroupName</span></span>
<span data-ttu-id="36788-118">Az értesítési szabály erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="36788-118">Specifies the name of the resource group for the alert rule.</span></span>

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

### <span data-ttu-id="36788-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="36788-119">-Confirm</span></span>
<span data-ttu-id="36788-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="36788-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36788-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36788-121">-WhatIf</span></span>
<span data-ttu-id="36788-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="36788-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36788-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="36788-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36788-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36788-124">CommonParameters</span></span>
<span data-ttu-id="36788-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="36788-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36788-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36788-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36788-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="36788-127">INPUTS</span></span>

### <span data-ttu-id="36788-128">System. String</span><span class="sxs-lookup"><span data-stu-id="36788-128">System.String</span></span>

## <span data-ttu-id="36788-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36788-129">OUTPUTS</span></span>

### <span data-ttu-id="36788-130">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="36788-130">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="36788-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="36788-131">NOTES</span></span>

## <span data-ttu-id="36788-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36788-132">RELATED LINKS</span></span>

[<span data-ttu-id="36788-133">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="36788-133">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="36788-134">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="36788-134">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="36788-135">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="36788-135">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="36788-136">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="36788-136">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)


