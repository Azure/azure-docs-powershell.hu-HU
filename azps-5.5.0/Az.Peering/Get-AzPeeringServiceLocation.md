---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservicelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
ms.openlocfilehash: 6f869cee7258c38e941ca8fbb7c8ac31b47171af
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146410"
---
# <span data-ttu-id="292b8-101">Get-AzPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="292b8-101">Get-AzPeeringServiceLocation</span></span>

## <span data-ttu-id="292b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="292b8-102">SYNOPSIS</span></span>
<span data-ttu-id="292b8-103">A Microsoft által kínált társviszony-létesítő szolgáltatási helyek listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="292b8-103">Gets a list of peering service locations offered by Microsoft.</span></span>

## <span data-ttu-id="292b8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="292b8-104">SYNTAX</span></span>

```
Get-AzPeeringServiceLocation [-Country <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="292b8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="292b8-105">DESCRIPTION</span></span>
<span data-ttu-id="292b8-106">Társviszony-létesítés helyeinek felsorolása.</span><span class="sxs-lookup"><span data-stu-id="292b8-106">List peering locations.</span></span>

## <span data-ttu-id="292b8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="292b8-107">EXAMPLES</span></span>

### <span data-ttu-id="292b8-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="292b8-108">Example 1</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States" | Where-Object { $_.State -match "Washington"}

Country     : United States
State       : Washington
AzureRegion : West US
Name        : Washington
Id          :
Type        : Microsoft.Peering/peeringServiceLocations
```

<span data-ttu-id="292b8-109">Beolvassa a washingtoni társviszony-létesítő helyeket.</span><span class="sxs-lookup"><span data-stu-id="292b8-109">Retrieves the peering locations for washington.</span></span>

### <span data-ttu-id="292b8-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="292b8-110">Example 2</span></span>
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

<span data-ttu-id="292b8-111">Beolvassa a washingtoni társviszony-létesítő helyeket.</span><span class="sxs-lookup"><span data-stu-id="292b8-111">Retrieves the peering locations for washington.</span></span>

## <span data-ttu-id="292b8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="292b8-112">PARAMETERS</span></span>

### <span data-ttu-id="292b8-113">-Country</span><span class="sxs-lookup"><span data-stu-id="292b8-113">-Country</span></span>
<span data-ttu-id="292b8-114">Az országszűrő</span><span class="sxs-lookup"><span data-stu-id="292b8-114">The country filter</span></span>

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

### <span data-ttu-id="292b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="292b8-115">-DefaultProfile</span></span>
<span data-ttu-id="292b8-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="292b8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="292b8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="292b8-117">CommonParameters</span></span>
<span data-ttu-id="292b8-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="292b8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="292b8-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="292b8-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="292b8-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="292b8-120">INPUTS</span></span>

### <span data-ttu-id="292b8-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="292b8-121">None</span></span>

## <span data-ttu-id="292b8-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="292b8-122">OUTPUTS</span></span>

### <span data-ttu-id="292b8-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="292b8-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span></span>

## <span data-ttu-id="292b8-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="292b8-124">NOTES</span></span>

## <span data-ttu-id="292b8-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="292b8-125">RELATED LINKS</span></span>
