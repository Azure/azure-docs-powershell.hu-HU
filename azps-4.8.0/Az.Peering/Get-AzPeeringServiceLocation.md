---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservicelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
ms.openlocfilehash: 6f869cee7258c38e941ca8fbb7c8ac31b47171af
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181477"
---
# <span data-ttu-id="aac8d-101">Get-AzPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="aac8d-101">Get-AzPeeringServiceLocation</span></span>

## <span data-ttu-id="aac8d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aac8d-102">SYNOPSIS</span></span>
<span data-ttu-id="aac8d-103">A Microsoft által kínált társközi szolgáltatási helyek listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="aac8d-103">Gets a list of peering service locations offered by Microsoft.</span></span>

## <span data-ttu-id="aac8d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aac8d-104">SYNTAX</span></span>

```
Get-AzPeeringServiceLocation [-Country <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aac8d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aac8d-105">DESCRIPTION</span></span>
<span data-ttu-id="aac8d-106">A partnerek listájának listázása</span><span class="sxs-lookup"><span data-stu-id="aac8d-106">List peering locations.</span></span>

## <span data-ttu-id="aac8d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="aac8d-107">EXAMPLES</span></span>

### <span data-ttu-id="aac8d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="aac8d-108">Example 1</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States" | Where-Object { $_.State -match "Washington"}

Country     : United States
State       : Washington
AzureRegion : West US
Name        : Washington
Id          :
Type        : Microsoft.Peering/peeringServiceLocations
```

<span data-ttu-id="aac8d-109">Kikeresi a washingtoni peer-helyeket.</span><span class="sxs-lookup"><span data-stu-id="aac8d-109">Retrieves the peering locations for washington.</span></span>

### <span data-ttu-id="aac8d-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="aac8d-110">Example 2</span></span>
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

<span data-ttu-id="aac8d-111">Kikeresi a washingtoni peer-helyeket.</span><span class="sxs-lookup"><span data-stu-id="aac8d-111">Retrieves the peering locations for washington.</span></span>

## <span data-ttu-id="aac8d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aac8d-112">PARAMETERS</span></span>

### <span data-ttu-id="aac8d-113">-Ország</span><span class="sxs-lookup"><span data-stu-id="aac8d-113">-Country</span></span>
<span data-ttu-id="aac8d-114">Az ország szűrő</span><span class="sxs-lookup"><span data-stu-id="aac8d-114">The country filter</span></span>

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

### <span data-ttu-id="aac8d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aac8d-115">-DefaultProfile</span></span>
<span data-ttu-id="aac8d-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aac8d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aac8d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aac8d-117">CommonParameters</span></span>
<span data-ttu-id="aac8d-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aac8d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aac8d-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="aac8d-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aac8d-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aac8d-120">INPUTS</span></span>

### <span data-ttu-id="aac8d-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="aac8d-121">None</span></span>

## <span data-ttu-id="aac8d-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aac8d-122">OUTPUTS</span></span>

### <span data-ttu-id="aac8d-123">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="aac8d-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span></span>

## <span data-ttu-id="aac8d-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aac8d-124">NOTES</span></span>

## <span data-ttu-id="aac8d-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aac8d-125">RELATED LINKS</span></span>
