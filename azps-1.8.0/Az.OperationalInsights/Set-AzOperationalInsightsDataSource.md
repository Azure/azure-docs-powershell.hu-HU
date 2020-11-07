---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 607da2e6478d72915497f1476e04ae11f9a69b9b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669838"
---
# <span data-ttu-id="a2e93-101">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="a2e93-101">Set-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="a2e93-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a2e93-102">SYNOPSIS</span></span>
<span data-ttu-id="a2e93-103">Frissít egy adatforrást.</span><span class="sxs-lookup"><span data-stu-id="a2e93-103">Updates a data source.</span></span>

## <span data-ttu-id="a2e93-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a2e93-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsDataSource [-DataSource] <PSDataSource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2e93-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a2e93-105">DESCRIPTION</span></span>
<span data-ttu-id="a2e93-106">A **set-AzOperationalInsightsDataSource** parancsmag frissíti az adatforrást.</span><span class="sxs-lookup"><span data-stu-id="a2e93-106">The **Set-AzOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="a2e93-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a2e93-107">EXAMPLES</span></span>

## <span data-ttu-id="a2e93-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a2e93-108">PARAMETERS</span></span>

### <span data-ttu-id="a2e93-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="a2e93-109">-DataSource</span></span>
<span data-ttu-id="a2e93-110">A parancsmag által frissített adatforrást adja meg.</span><span class="sxs-lookup"><span data-stu-id="a2e93-110">Specifies the data source that this cmdlet updates.</span></span>

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

### <span data-ttu-id="a2e93-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2e93-111">-DefaultProfile</span></span>
<span data-ttu-id="a2e93-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a2e93-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2e93-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2e93-113">CommonParameters</span></span>
<span data-ttu-id="a2e93-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a2e93-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2e93-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2e93-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2e93-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2e93-116">INPUTS</span></span>

### <span data-ttu-id="a2e93-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="a2e93-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="a2e93-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2e93-118">OUTPUTS</span></span>

### <span data-ttu-id="a2e93-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="a2e93-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="a2e93-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a2e93-120">NOTES</span></span>
* <span data-ttu-id="a2e93-121">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, működési, betekintések</span><span class="sxs-lookup"><span data-stu-id="a2e93-121">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="a2e93-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2e93-122">RELATED LINKS</span></span>

[<span data-ttu-id="a2e93-123">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="a2e93-123">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="a2e93-124">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="a2e93-124">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)


