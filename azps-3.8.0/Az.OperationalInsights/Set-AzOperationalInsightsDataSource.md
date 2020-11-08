---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
ms.openlocfilehash: ef90211ccca53a94db2651f17b3a666a725ce8b1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014525"
---
# <span data-ttu-id="a81b1-101">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="a81b1-101">Set-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="a81b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a81b1-102">SYNOPSIS</span></span>
<span data-ttu-id="a81b1-103">Frissít egy adatforrást.</span><span class="sxs-lookup"><span data-stu-id="a81b1-103">Updates a data source.</span></span>

## <span data-ttu-id="a81b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a81b1-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsDataSource [-DataSource] <PSDataSource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a81b1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a81b1-105">DESCRIPTION</span></span>
<span data-ttu-id="a81b1-106">A **set-AzOperationalInsightsDataSource** parancsmag frissíti az adatforrást.</span><span class="sxs-lookup"><span data-stu-id="a81b1-106">The **Set-AzOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="a81b1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a81b1-107">EXAMPLES</span></span>

## <span data-ttu-id="a81b1-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a81b1-108">PARAMETERS</span></span>

### <span data-ttu-id="a81b1-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="a81b1-109">-DataSource</span></span>
<span data-ttu-id="a81b1-110">A parancsmag által frissített adatforrást adja meg.</span><span class="sxs-lookup"><span data-stu-id="a81b1-110">Specifies the data source that this cmdlet updates.</span></span>

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

### <span data-ttu-id="a81b1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a81b1-111">-DefaultProfile</span></span>
<span data-ttu-id="a81b1-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a81b1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a81b1-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a81b1-113">CommonParameters</span></span>
<span data-ttu-id="a81b1-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a81b1-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a81b1-115">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a81b1-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a81b1-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a81b1-116">INPUTS</span></span>

### <span data-ttu-id="a81b1-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="a81b1-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="a81b1-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a81b1-118">OUTPUTS</span></span>

### <span data-ttu-id="a81b1-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="a81b1-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="a81b1-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a81b1-120">NOTES</span></span>
* <span data-ttu-id="a81b1-121">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, működési, betekintések</span><span class="sxs-lookup"><span data-stu-id="a81b1-121">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="a81b1-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a81b1-122">RELATED LINKS</span></span>

[<span data-ttu-id="a81b1-123">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="a81b1-123">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="a81b1-124">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="a81b1-124">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)


