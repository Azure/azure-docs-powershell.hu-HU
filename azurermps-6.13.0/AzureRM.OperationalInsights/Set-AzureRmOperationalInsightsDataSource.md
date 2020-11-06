---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 5bf4f178ee3343b5100dad87836c3215fba4cfb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501988"
---
# <span data-ttu-id="6f50f-101">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="6f50f-101">Set-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="6f50f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6f50f-102">SYNOPSIS</span></span>
<span data-ttu-id="6f50f-103">Frissít egy adatforrást.</span><span class="sxs-lookup"><span data-stu-id="6f50f-103">Updates a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f50f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6f50f-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsDataSource [-DataSource] <PSDataSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f50f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6f50f-105">DESCRIPTION</span></span>
<span data-ttu-id="6f50f-106">A **set-AzureRmOperationalInsightsDataSource** parancsmag frissíti az adatforrást.</span><span class="sxs-lookup"><span data-stu-id="6f50f-106">The **Set-AzureRmOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="6f50f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6f50f-107">EXAMPLES</span></span>

## <span data-ttu-id="6f50f-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6f50f-108">PARAMETERS</span></span>

### <span data-ttu-id="6f50f-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="6f50f-109">-DataSource</span></span>
<span data-ttu-id="6f50f-110">A parancsmag által frissített adatforrást adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f50f-110">Specifies the data source that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f50f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f50f-111">-DefaultProfile</span></span>
<span data-ttu-id="6f50f-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6f50f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f50f-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f50f-113">CommonParameters</span></span>
<span data-ttu-id="6f50f-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6f50f-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f50f-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f50f-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f50f-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f50f-116">INPUTS</span></span>

### <span data-ttu-id="6f50f-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="6f50f-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>
<span data-ttu-id="6f50f-118">Paraméterek: DataSource (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6f50f-118">Parameters: DataSource (ByValue)</span></span>

## <span data-ttu-id="6f50f-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f50f-119">OUTPUTS</span></span>

### <span data-ttu-id="6f50f-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="6f50f-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="6f50f-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6f50f-121">NOTES</span></span>
* <span data-ttu-id="6f50f-122">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, működési, betekintések</span><span class="sxs-lookup"><span data-stu-id="6f50f-122">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="6f50f-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f50f-123">RELATED LINKS</span></span>

[<span data-ttu-id="6f50f-124">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="6f50f-124">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="6f50f-125">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="6f50f-125">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)


