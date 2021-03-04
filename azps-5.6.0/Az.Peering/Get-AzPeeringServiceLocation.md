---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringservicelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
ms.openlocfilehash: 84cc6f2e8e51de6176b4ab8a04296aab8516a967
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937721"
---
# <span data-ttu-id="9e82b-101">Get-AzPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="9e82b-101">Get-AzPeeringServiceLocation</span></span>

## <span data-ttu-id="9e82b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e82b-102">SYNOPSIS</span></span>
<span data-ttu-id="9e82b-103">A Microsoft által kínált társviszony-létesítő szolgáltatási helyek listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="9e82b-103">Gets a list of peering service locations offered by Microsoft.</span></span>

## <span data-ttu-id="9e82b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9e82b-104">SYNTAX</span></span>

```
Get-AzPeeringServiceLocation [-Country <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e82b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9e82b-105">DESCRIPTION</span></span>
<span data-ttu-id="9e82b-106">Társviszony-létesítés helyeinek felsorolása.</span><span class="sxs-lookup"><span data-stu-id="9e82b-106">List peering locations.</span></span>

## <span data-ttu-id="9e82b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9e82b-107">EXAMPLES</span></span>

### <span data-ttu-id="9e82b-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="9e82b-108">Example 1</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States" | Where-Object { $_.State -match "Washington"}

Country     : United States
State       : Washington
AzureRegion : West US
Name        : Washington
Id          :
Type        : Microsoft.Peering/peeringServiceLocations
```

<span data-ttu-id="9e82b-109">Beolvassa a washingtoni társviszony-létesítő helyeket.</span><span class="sxs-lookup"><span data-stu-id="9e82b-109">Retrieves the peering locations for washington.</span></span>

### <span data-ttu-id="9e82b-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="9e82b-110">Example 2</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States"

Country     : United States
State       : Alabama
AzureRegion : East US
Name        : Alabama
Id          :
Type        : Microsoft.Peering/peeringServiceLocations

Country     : United States
State       : Arizona
AzureRegion : West US
Name        : Arizona
Id          :
Type        : Microsoft.Peering/peeringServiceLocations

...
```

<span data-ttu-id="9e82b-111">Beolvassa a washingtoni társviszony-létesítő helyeket.</span><span class="sxs-lookup"><span data-stu-id="9e82b-111">Retrieves the peering locations for washington.</span></span>

## <span data-ttu-id="9e82b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e82b-112">PARAMETERS</span></span>

### <span data-ttu-id="9e82b-113">-Country</span><span class="sxs-lookup"><span data-stu-id="9e82b-113">-Country</span></span>
<span data-ttu-id="9e82b-114">Az országszűrő</span><span class="sxs-lookup"><span data-stu-id="9e82b-114">The country filter</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e82b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e82b-115">-DefaultProfile</span></span>
<span data-ttu-id="9e82b-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9e82b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e82b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e82b-117">CommonParameters</span></span>
<span data-ttu-id="9e82b-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e82b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e82b-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e82b-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e82b-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9e82b-120">INPUTS</span></span>

### <span data-ttu-id="9e82b-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="9e82b-121">None</span></span>

## <span data-ttu-id="9e82b-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e82b-122">OUTPUTS</span></span>

### <span data-ttu-id="9e82b-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="9e82b-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span></span>

## <span data-ttu-id="9e82b-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9e82b-124">NOTES</span></span>

## <span data-ttu-id="9e82b-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e82b-125">RELATED LINKS</span></span>
