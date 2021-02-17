---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
ms.openlocfilehash: 98c41f8e9e1592cf0405f42701fc19f3badd9553
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205111"
---
# <span data-ttu-id="017a1-101">Get-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="017a1-101">Get-AzCdnOriginGroup</span></span>

## <span data-ttu-id="017a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="017a1-102">SYNOPSIS</span></span>
<span data-ttu-id="017a1-103">CDN-forráscsoportot kap</span><span class="sxs-lookup"><span data-stu-id="017a1-103">Gets a CDN origin group</span></span>

## <span data-ttu-id="017a1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="017a1-104">SYNTAX</span></span>

### <span data-ttu-id="017a1-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="017a1-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="017a1-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="017a1-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOriginGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="017a1-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="017a1-107">DESCRIPTION</span></span>
<span data-ttu-id="017a1-108">A Get-AzCdnOriginGroup parancsmag lekéri a CDN-forráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="017a1-108">The Get-AzCdnOriginGroup cmdlet retrieves a CDN origin group.</span></span>

## <span data-ttu-id="017a1-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="017a1-109">EXAMPLES</span></span>

### <span data-ttu-id="017a1-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="017a1-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="017a1-111">Ez a parancs a megadott végponton belül be fogja szerezni a forráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="017a1-111">This command will get the origin group within the specified endpoint.</span></span>

## <span data-ttu-id="017a1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="017a1-112">PARAMETERS</span></span>

### <span data-ttu-id="017a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="017a1-113">-DefaultProfile</span></span>
<span data-ttu-id="017a1-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="017a1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="017a1-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="017a1-115">-EndpointName</span></span>
<span data-ttu-id="017a1-116">Azure CDN-végpont neve.</span><span class="sxs-lookup"><span data-stu-id="017a1-116">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="017a1-117">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="017a1-117">-OriginGroupName</span></span>
<span data-ttu-id="017a1-118">Azure CDN-forráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="017a1-118">Azure CDN origin group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="017a1-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="017a1-119">-ProfileName</span></span>
<span data-ttu-id="017a1-120">Azure CDN-profil neve.</span><span class="sxs-lookup"><span data-stu-id="017a1-120">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="017a1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="017a1-121">-ResourceGroupName</span></span>
<span data-ttu-id="017a1-122">Az Azure CDN-profil erőforráscsoportja.</span><span class="sxs-lookup"><span data-stu-id="017a1-122">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="017a1-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="017a1-123">-ResourceId</span></span>
<span data-ttu-id="017a1-124">A forráscsoport erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="017a1-124">Resource Id for the the origin group</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="017a1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="017a1-125">CommonParameters</span></span>
<span data-ttu-id="017a1-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="017a1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="017a1-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="017a1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="017a1-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="017a1-128">INPUTS</span></span>

### <span data-ttu-id="017a1-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="017a1-129">None</span></span>

## <span data-ttu-id="017a1-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="017a1-130">OUTPUTS</span></span>

### <span data-ttu-id="017a1-131">System.Object</span><span class="sxs-lookup"><span data-stu-id="017a1-131">System.Object</span></span>

## <span data-ttu-id="017a1-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="017a1-132">NOTES</span></span>

## <span data-ttu-id="017a1-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="017a1-133">RELATED LINKS</span></span>
