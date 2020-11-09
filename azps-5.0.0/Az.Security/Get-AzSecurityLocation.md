---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityLocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
ms.openlocfilehash: 77f9283b16aa605da066780165c2fe7b42b1830b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302435"
---
# <span data-ttu-id="4e44e-101">Get-AzSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="4e44e-101">Get-AzSecurityLocation</span></span>

## <span data-ttu-id="4e44e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4e44e-102">SYNOPSIS</span></span>
<span data-ttu-id="4e44e-103">Annak a helynek a helye, ahol az Azure Security Center automatikusan menti az adott előfizetéshez tartozó adatot</span><span class="sxs-lookup"><span data-stu-id="4e44e-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

## <span data-ttu-id="4e44e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4e44e-104">SYNTAX</span></span>

### <span data-ttu-id="4e44e-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4e44e-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e44e-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="4e44e-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e44e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e44e-107">ResourceId</span></span>
```
Get-AzSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e44e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4e44e-108">DESCRIPTION</span></span>
<span data-ttu-id="4e44e-109">Az Azure Security Center automatikusan úgy dönt, hogy egy helyre menti az adatait.</span><span class="sxs-lookup"><span data-stu-id="4e44e-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="4e44e-110">Ezzel a parancsmaggal felfedezheti ezt a helyet.</span><span class="sxs-lookup"><span data-stu-id="4e44e-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="4e44e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="4e44e-111">EXAMPLES</span></span>

### <span data-ttu-id="4e44e-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4e44e-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="4e44e-113">Megkapja azt a helyet, ahol az Azure Security Center menti a számított biztonsági adatmennyiséget.</span><span class="sxs-lookup"><span data-stu-id="4e44e-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="4e44e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4e44e-114">PARAMETERS</span></span>

### <span data-ttu-id="4e44e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e44e-115">-DefaultProfile</span></span>
<span data-ttu-id="4e44e-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4e44e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e44e-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4e44e-117">-Name</span></span>
<span data-ttu-id="4e44e-118">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="4e44e-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e44e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e44e-119">-ResourceId</span></span>
<span data-ttu-id="4e44e-120">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="4e44e-120">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e44e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e44e-121">CommonParameters</span></span>
<span data-ttu-id="4e44e-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4e44e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e44e-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4e44e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e44e-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e44e-124">INPUTS</span></span>

### <span data-ttu-id="4e44e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4e44e-125">System.String</span></span>

## <span data-ttu-id="4e44e-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e44e-126">OUTPUTS</span></span>

### <span data-ttu-id="4e44e-127">Microsoft. Azure. commands. Security. models. Locations. PSSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="4e44e-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="4e44e-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4e44e-128">NOTES</span></span>

## <span data-ttu-id="4e44e-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e44e-129">RELATED LINKS</span></span>
