---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
ms.openlocfilehash: 98c41f8e9e1592cf0405f42701fc19f3badd9553
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195244"
---
# <span data-ttu-id="acdde-101">Get-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="acdde-101">Get-AzCdnOriginGroup</span></span>

## <span data-ttu-id="acdde-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="acdde-102">SYNOPSIS</span></span>
<span data-ttu-id="acdde-103">Bekapja a CDN-származási csoportot</span><span class="sxs-lookup"><span data-stu-id="acdde-103">Gets a CDN origin group</span></span>

## <span data-ttu-id="acdde-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="acdde-104">SYNTAX</span></span>

### <span data-ttu-id="acdde-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="acdde-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acdde-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="acdde-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOriginGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acdde-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="acdde-107">DESCRIPTION</span></span>
<span data-ttu-id="acdde-108">A Get-AzCdnOriginGroup parancsmag egy CDN-származási csoportot keres.</span><span class="sxs-lookup"><span data-stu-id="acdde-108">The Get-AzCdnOriginGroup cmdlet retrieves a CDN origin group.</span></span>

## <span data-ttu-id="acdde-109">Példák</span><span class="sxs-lookup"><span data-stu-id="acdde-109">EXAMPLES</span></span>

### <span data-ttu-id="acdde-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="acdde-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="acdde-111">Ez a parancs a megadott végponton belül a kezdőpont csoportot fogja kapni.</span><span class="sxs-lookup"><span data-stu-id="acdde-111">This command will get the origin group within the specified endpoint.</span></span>

## <span data-ttu-id="acdde-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="acdde-112">PARAMETERS</span></span>

### <span data-ttu-id="acdde-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acdde-113">-DefaultProfile</span></span>
<span data-ttu-id="acdde-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="acdde-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acdde-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="acdde-115">-EndpointName</span></span>
<span data-ttu-id="acdde-116">Azure CDN végpont neve.</span><span class="sxs-lookup"><span data-stu-id="acdde-116">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="acdde-117">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="acdde-117">-OriginGroupName</span></span>
<span data-ttu-id="acdde-118">Azure CDN származási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="acdde-118">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="acdde-119">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="acdde-119">-ProfileName</span></span>
<span data-ttu-id="acdde-120">Azure CDN-profil neve.</span><span class="sxs-lookup"><span data-stu-id="acdde-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="acdde-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acdde-121">-ResourceGroupName</span></span>
<span data-ttu-id="acdde-122">Az Azure CDN-profil erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="acdde-122">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="acdde-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="acdde-123">-ResourceId</span></span>
<span data-ttu-id="acdde-124">A származási csoport erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="acdde-124">Resource Id for the the origin group</span></span>

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

### <span data-ttu-id="acdde-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acdde-125">CommonParameters</span></span>
<span data-ttu-id="acdde-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="acdde-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acdde-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="acdde-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acdde-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="acdde-128">INPUTS</span></span>

### <span data-ttu-id="acdde-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="acdde-129">None</span></span>

## <span data-ttu-id="acdde-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="acdde-130">OUTPUTS</span></span>

### <span data-ttu-id="acdde-131">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="acdde-131">System.Object</span></span>

## <span data-ttu-id="acdde-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="acdde-132">NOTES</span></span>

## <span data-ttu-id="acdde-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="acdde-133">RELATED LINKS</span></span>
