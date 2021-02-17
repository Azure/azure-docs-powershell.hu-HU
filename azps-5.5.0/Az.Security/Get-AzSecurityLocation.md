---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityLocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
ms.openlocfilehash: 77f9283b16aa605da066780165c2fe7b42b1830b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156419"
---
# <span data-ttu-id="0ab33-101">Get-AzSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="0ab33-101">Get-AzSecurityLocation</span></span>

## <span data-ttu-id="0ab33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ab33-102">SYNOPSIS</span></span>
<span data-ttu-id="0ab33-103">Az a hely, ahová az Azure Security Center automatikusan menti az adott előfizetés adatait</span><span class="sxs-lookup"><span data-stu-id="0ab33-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

## <span data-ttu-id="0ab33-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0ab33-104">SYNTAX</span></span>

### <span data-ttu-id="0ab33-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0ab33-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ab33-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="0ab33-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ab33-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ab33-107">ResourceId</span></span>
```
Get-AzSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ab33-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0ab33-108">DESCRIPTION</span></span>
<span data-ttu-id="0ab33-109">Az Azure Biztonsági központ automatikusan kiválasztja az adatok mentésének helyét.</span><span class="sxs-lookup"><span data-stu-id="0ab33-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="0ab33-110">Ezzel a parancsmagot használva felderítheti ezt a helyet.</span><span class="sxs-lookup"><span data-stu-id="0ab33-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="0ab33-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0ab33-111">EXAMPLES</span></span>

### <span data-ttu-id="0ab33-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="0ab33-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="0ab33-113">Lekérte azt a helyet, ahová az Azure Biztonsági központ a számított biztonsági adatokat menti.</span><span class="sxs-lookup"><span data-stu-id="0ab33-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="0ab33-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ab33-114">PARAMETERS</span></span>

### <span data-ttu-id="0ab33-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ab33-115">-DefaultProfile</span></span>
<span data-ttu-id="0ab33-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ab33-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ab33-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0ab33-117">-Name</span></span>
<span data-ttu-id="0ab33-118">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="0ab33-118">Resource name.</span></span>

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

### <span data-ttu-id="0ab33-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ab33-119">-ResourceId</span></span>
<span data-ttu-id="0ab33-120">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="0ab33-120">Resource ID.</span></span>

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

### <span data-ttu-id="0ab33-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ab33-121">CommonParameters</span></span>
<span data-ttu-id="0ab33-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ab33-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ab33-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ab33-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ab33-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0ab33-124">INPUTS</span></span>

### <span data-ttu-id="0ab33-125">System.String</span><span class="sxs-lookup"><span data-stu-id="0ab33-125">System.String</span></span>

## <span data-ttu-id="0ab33-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ab33-126">OUTPUTS</span></span>

### <span data-ttu-id="0ab33-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="0ab33-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="0ab33-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0ab33-128">NOTES</span></span>

## <span data-ttu-id="0ab33-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ab33-129">RELATED LINKS</span></span>
