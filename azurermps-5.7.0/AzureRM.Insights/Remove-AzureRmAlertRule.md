---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
ms.openlocfilehash: eaa7cfa9f58bb9bb5affa7a035d194910bcf0006
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494501"
---
# <span data-ttu-id="0f2cb-101">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="0f2cb-101">Remove-AzureRmAlertRule</span></span>

## <span data-ttu-id="0f2cb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0f2cb-102">SYNOPSIS</span></span>
<span data-ttu-id="0f2cb-103">Figyelmeztetési szabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0f2cb-103">Removes an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f2cb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0f2cb-104">SYNTAX</span></span>

```
Remove-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f2cb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0f2cb-105">DESCRIPTION</span></span>
<span data-ttu-id="0f2cb-106">A **Remove-AzureRmAlertRule** parancsmag eltávolít egy figyelmeztetési szabályt.</span><span class="sxs-lookup"><span data-stu-id="0f2cb-106">The **Remove-AzureRmAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="0f2cb-107">Meg kell adnia a riasztási szabály és az erőforrás-csoport nevét, amelyhez hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="0f2cb-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>

<span data-ttu-id="0f2cb-108">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="0f2cb-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="0f2cb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0f2cb-109">EXAMPLES</span></span>

### <span data-ttu-id="0f2cb-110">1. példa: figyelmeztetési szabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0f2cb-110">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="0f2cb-111">Ez a parancs eltávolítja a myalert-7da64548-214d-42CA-b12b-b245bb8f0ac8 nevű riasztási szabályt az erőforráscsoport Default-Web-CentralUS.</span><span class="sxs-lookup"><span data-stu-id="0f2cb-111">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="0f2cb-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0f2cb-112">PARAMETERS</span></span>

### <span data-ttu-id="0f2cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f2cb-113">-DefaultProfile</span></span>
<span data-ttu-id="0f2cb-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0f2cb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f2cb-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0f2cb-115">-Name</span></span>
<span data-ttu-id="0f2cb-116">Az eltávolítandó figyelmeztetési szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f2cb-116">Specifies the name of the alert rule to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f2cb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f2cb-117">-ResourceGroupName</span></span>
<span data-ttu-id="0f2cb-118">Az értesítési szabály erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f2cb-118">Specifies the name of the resource group for the alert rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f2cb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f2cb-119">CommonParameters</span></span>
<span data-ttu-id="0f2cb-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0f2cb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f2cb-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f2cb-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f2cb-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f2cb-122">INPUTS</span></span>

### <span data-ttu-id="0f2cb-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="0f2cb-123">None</span></span>
<span data-ttu-id="0f2cb-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="0f2cb-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0f2cb-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f2cb-125">OUTPUTS</span></span>

### <span data-ttu-id="0f2cb-126">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0f2cb-126">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="0f2cb-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0f2cb-127">NOTES</span></span>

## <span data-ttu-id="0f2cb-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f2cb-128">RELATED LINKS</span></span>

[<span data-ttu-id="0f2cb-129">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="0f2cb-129">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="0f2cb-130">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="0f2cb-130">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="0f2cb-131">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="0f2cb-131">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="0f2cb-132">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="0f2cb-132">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)


