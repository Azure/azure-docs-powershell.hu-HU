---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
ms.openlocfilehash: ef90211ccca53a94db2651f17b3a666a725ce8b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151290"
---
# <span data-ttu-id="a4f6f-101">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="a4f6f-101">Set-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="a4f6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4f6f-102">SYNOPSIS</span></span>
<span data-ttu-id="a4f6f-103">Frissíti az adatforrást.</span><span class="sxs-lookup"><span data-stu-id="a4f6f-103">Updates a data source.</span></span>

## <span data-ttu-id="a4f6f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a4f6f-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsDataSource [-DataSource] <PSDataSource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4f6f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a4f6f-105">DESCRIPTION</span></span>
<span data-ttu-id="a4f6f-106">A **Set-AzOperationalInsightsDataSource** parancsmag frissíti az adatforrást.</span><span class="sxs-lookup"><span data-stu-id="a4f6f-106">The **Set-AzOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="a4f6f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a4f6f-107">EXAMPLES</span></span>

## <span data-ttu-id="a4f6f-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4f6f-108">PARAMETERS</span></span>

### <span data-ttu-id="a4f6f-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="a4f6f-109">-DataSource</span></span>
<span data-ttu-id="a4f6f-110">A parancsmag által frissülő adatforrást adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4f6f-110">Specifies the data source that this cmdlet updates.</span></span>

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

### <span data-ttu-id="a4f6f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4f6f-111">-DefaultProfile</span></span>
<span data-ttu-id="a4f6f-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a4f6f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4f6f-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4f6f-113">CommonParameters</span></span>
<span data-ttu-id="a4f6f-114">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4f6f-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4f6f-115">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4f6f-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4f6f-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a4f6f-116">INPUTS</span></span>

### <span data-ttu-id="a4f6f-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="a4f6f-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="a4f6f-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4f6f-118">OUTPUTS</span></span>

### <span data-ttu-id="a4f6f-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="a4f6f-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="a4f6f-120">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a4f6f-120">NOTES</span></span>
* <span data-ttu-id="a4f6f-121">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, műveleti, betekintések</span><span class="sxs-lookup"><span data-stu-id="a4f6f-121">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="a4f6f-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4f6f-122">RELATED LINKS</span></span>

[<span data-ttu-id="a4f6f-123">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="a4f6f-123">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="a4f6f-124">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="a4f6f-124">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)


