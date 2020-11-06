---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 13d8be80411e39124ab29d9a31e44edd0ebd95e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493396"
---
# <span data-ttu-id="3da59-101">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="3da59-101">Set-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="3da59-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3da59-102">SYNOPSIS</span></span>
<span data-ttu-id="3da59-103">Frissít egy adatforrást.</span><span class="sxs-lookup"><span data-stu-id="3da59-103">Updates a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3da59-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3da59-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsDataSource [-DataSource] <PSDataSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3da59-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3da59-105">DESCRIPTION</span></span>
<span data-ttu-id="3da59-106">A **set-AzureRmOperationalInsightsDataSource** parancsmag frissíti az adatforrást.</span><span class="sxs-lookup"><span data-stu-id="3da59-106">The **Set-AzureRmOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="3da59-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3da59-107">EXAMPLES</span></span>

## <span data-ttu-id="3da59-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3da59-108">PARAMETERS</span></span>

### <span data-ttu-id="3da59-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="3da59-109">-DataSource</span></span>
<span data-ttu-id="3da59-110">A parancsmag által frissített adatforrást adja meg.</span><span class="sxs-lookup"><span data-stu-id="3da59-110">Specifies the data source that this cmdlet updates.</span></span>

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

### <span data-ttu-id="3da59-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3da59-111">-DefaultProfile</span></span>
<span data-ttu-id="3da59-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3da59-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3da59-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3da59-113">CommonParameters</span></span>
<span data-ttu-id="3da59-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3da59-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3da59-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3da59-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3da59-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3da59-116">INPUTS</span></span>

### <span data-ttu-id="3da59-117">PSDataSource</span><span class="sxs-lookup"><span data-stu-id="3da59-117">PSDataSource</span></span>
<span data-ttu-id="3da59-118">A "DataSource" paraméter az "PSDataSource" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="3da59-118">Parameter 'DataSource' accepts value of type 'PSDataSource' from the pipeline</span></span>

## <span data-ttu-id="3da59-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3da59-119">OUTPUTS</span></span>

### <span data-ttu-id="3da59-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="3da59-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="3da59-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3da59-121">NOTES</span></span>
* <span data-ttu-id="3da59-122">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, működési, betekintések</span><span class="sxs-lookup"><span data-stu-id="3da59-122">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="3da59-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3da59-123">RELATED LINKS</span></span>

[<span data-ttu-id="3da59-124">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="3da59-124">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="3da59-125">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="3da59-125">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)


