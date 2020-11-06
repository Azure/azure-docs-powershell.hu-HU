---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
ms.openlocfilehash: de0c1f8fa66b195452d7f2c9447189b4e925136b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501843"
---
# <span data-ttu-id="3de7a-101">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="3de7a-101">Remove-AzureRmAlertRule</span></span>

## <span data-ttu-id="3de7a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3de7a-102">SYNOPSIS</span></span>
<span data-ttu-id="3de7a-103">Figyelmeztetési szabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3de7a-103">Removes an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3de7a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3de7a-104">SYNTAX</span></span>

```
Remove-AzureRmAlertRule -ResourceGroup <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3de7a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3de7a-105">DESCRIPTION</span></span>
<span data-ttu-id="3de7a-106">A **Remove-AzureRmAlertRule** parancsmag eltávolít egy figyelmeztetési szabályt.</span><span class="sxs-lookup"><span data-stu-id="3de7a-106">The **Remove-AzureRmAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="3de7a-107">Meg kell adnia a riasztási szabály és az erőforrás-csoport nevét, amelyhez hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="3de7a-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>

## <span data-ttu-id="3de7a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="3de7a-108">EXAMPLES</span></span>

### <span data-ttu-id="3de7a-109">1. példa: figyelmeztetési szabály eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3de7a-109">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="3de7a-110">Ez a parancs eltávolítja a myalert-7da64548-214d-42CA-b12b-b245bb8f0ac8 nevű riasztási szabályt az erőforráscsoport Default-Web-CentralUS.</span><span class="sxs-lookup"><span data-stu-id="3de7a-110">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="3de7a-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3de7a-111">PARAMETERS</span></span>

### <span data-ttu-id="3de7a-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3de7a-112">-Name</span></span>
<span data-ttu-id="3de7a-113">Az eltávolítandó figyelmeztetési szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3de7a-113">Specifies the name of the alert rule to remove.</span></span>

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

### <span data-ttu-id="3de7a-114">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3de7a-114">-ResourceGroup</span></span>
<span data-ttu-id="3de7a-115">Az értesítési szabály erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3de7a-115">Specifies the name of the resource group for the alert rule.</span></span>

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

### <span data-ttu-id="3de7a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3de7a-116">-DefaultProfile</span></span>
<span data-ttu-id="3de7a-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3de7a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3de7a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3de7a-118">CommonParameters</span></span>
<span data-ttu-id="3de7a-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3de7a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3de7a-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3de7a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3de7a-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3de7a-121">INPUTS</span></span>

## <span data-ttu-id="3de7a-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3de7a-122">OUTPUTS</span></span>

### <span data-ttu-id="3de7a-123">System. Collections. Generic. list ' 1 [Microsoft. Azure. AzureOperationResponse]</span><span class="sxs-lookup"><span data-stu-id="3de7a-123">System.Collections.Generic.List\`1[Microsoft.Azure.AzureOperationResponse]</span></span>

## <span data-ttu-id="3de7a-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3de7a-124">NOTES</span></span>

## <span data-ttu-id="3de7a-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3de7a-125">RELATED LINKS</span></span>

[<span data-ttu-id="3de7a-126">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="3de7a-126">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="3de7a-127">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="3de7a-127">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="3de7a-128">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="3de7a-128">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="3de7a-129">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="3de7a-129">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="3de7a-130">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="3de7a-130">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)


