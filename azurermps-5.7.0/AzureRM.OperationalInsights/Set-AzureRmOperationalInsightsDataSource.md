---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: e45dcbfad9b4b92695f310d7d2c56fc46fc57bd7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492253"
---
# <span data-ttu-id="25729-101">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="25729-101">Set-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="25729-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="25729-102">SYNOPSIS</span></span>
<span data-ttu-id="25729-103">Frissít egy adatforrást.</span><span class="sxs-lookup"><span data-stu-id="25729-103">Updates a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25729-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="25729-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsDataSource [-DataSource] <PSDataSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25729-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="25729-105">DESCRIPTION</span></span>
<span data-ttu-id="25729-106">A **set-AzureRmOperationalInsightsDataSource** parancsmag frissíti az adatforrást.</span><span class="sxs-lookup"><span data-stu-id="25729-106">The **Set-AzureRmOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="25729-107">Példák</span><span class="sxs-lookup"><span data-stu-id="25729-107">EXAMPLES</span></span>

## <span data-ttu-id="25729-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="25729-108">PARAMETERS</span></span>

### <span data-ttu-id="25729-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="25729-109">-DataSource</span></span>
<span data-ttu-id="25729-110">A parancsmag által frissített adatforrást adja meg.</span><span class="sxs-lookup"><span data-stu-id="25729-110">Specifies the data source that this cmdlet updates.</span></span>

```yaml
Type: PSDataSource
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25729-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25729-111">-DefaultProfile</span></span>
<span data-ttu-id="25729-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="25729-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25729-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25729-113">CommonParameters</span></span>
<span data-ttu-id="25729-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="25729-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25729-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25729-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25729-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="25729-116">INPUTS</span></span>

### <span data-ttu-id="25729-117">PSDataSource</span><span class="sxs-lookup"><span data-stu-id="25729-117">PSDataSource</span></span>
<span data-ttu-id="25729-118">A "DataSource" paraméter az "PSDataSource" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="25729-118">Parameter 'DataSource' accepts value of type 'PSDataSource' from the pipeline</span></span>

## <span data-ttu-id="25729-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25729-119">OUTPUTS</span></span>

### <span data-ttu-id="25729-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="25729-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="25729-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="25729-121">NOTES</span></span>
* <span data-ttu-id="25729-122">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, működési, betekintések</span><span class="sxs-lookup"><span data-stu-id="25729-122">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="25729-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25729-123">RELATED LINKS</span></span>

[<span data-ttu-id="25729-124">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="25729-124">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="25729-125">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="25729-125">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)


