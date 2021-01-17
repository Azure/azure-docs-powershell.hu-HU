---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
ms.openlocfilehash: 6f1eb79b7c740cae437e28af8153a4c14532871e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370144"
---
# <span data-ttu-id="ab8be-101">Get-AzReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="ab8be-101">Get-AzReservationCatalog</span></span>

## <span data-ttu-id="ab8be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab8be-102">SYNOPSIS</span></span>
<span data-ttu-id="ab8be-103">Az elérhető foglalások katalógusának lekérhetők</span><span class="sxs-lookup"><span data-stu-id="ab8be-103">Get the catalog of available reservations</span></span>

## <span data-ttu-id="ab8be-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ab8be-104">SYNTAX</span></span>

```
Get-AzReservationCatalog [-SubscriptionId <Guid>] -ReservedResourceType <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab8be-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ab8be-105">DESCRIPTION</span></span>
<span data-ttu-id="ab8be-106">Szerezze be a foglalt példányok vásárlásához a megadott Azure-előfizetéshez elérhető régiókat és termék terméksokokat.</span><span class="sxs-lookup"><span data-stu-id="ab8be-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="ab8be-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ab8be-107">EXAMPLES</span></span>

### <span data-ttu-id="ab8be-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="ab8be-108">Example 1</span></span>
```
PS C:\> Get-AzReservationCatalog -ReservedResourceType VirtualMachines -Location westus
```

<span data-ttu-id="ab8be-109">A VirtualMachines katalógusának lekérte az alapértelmezett előfizetést a WestUsban</span><span class="sxs-lookup"><span data-stu-id="ab8be-109">Get the VirtualMachines catalog in westus for the default subscription</span></span>

### <span data-ttu-id="ab8be-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="ab8be-110">Example 2</span></span>
```
PS C:\> Get-AzReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservedResourceType SuseLinux
```

<span data-ttu-id="ab8be-111">A SuseLinux katalógusának lekérte a megadott előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="ab8be-111">Get the SuseLinux catalog for the specified subscription</span></span>

## <span data-ttu-id="ab8be-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab8be-112">PARAMETERS</span></span>

### <span data-ttu-id="ab8be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab8be-113">-DefaultProfile</span></span>
<span data-ttu-id="ab8be-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ab8be-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab8be-115">-Location</span><span class="sxs-lookup"><span data-stu-id="ab8be-115">-Location</span></span>
<span data-ttu-id="ab8be-116">Megadja a fenntartott erőforrások helyét a katalógusban.</span><span class="sxs-lookup"><span data-stu-id="ab8be-116">Specifies the location of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="ab8be-117">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="ab8be-117">-ReservedResourceType</span></span>
<span data-ttu-id="ab8be-118">A katalógusban foglalt erőforrások típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="ab8be-118">Specifies the type of the reserved resources in the catalog</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab8be-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ab8be-119">-SubscriptionId</span></span>
<span data-ttu-id="ab8be-120">Az előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="ab8be-120">Id of the subscription</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab8be-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab8be-121">CommonParameters</span></span>
<span data-ttu-id="ab8be-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab8be-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab8be-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab8be-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab8be-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ab8be-124">INPUTS</span></span>

### <span data-ttu-id="ab8be-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="ab8be-125">None</span></span>

## <span data-ttu-id="ab8be-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab8be-126">OUTPUTS</span></span>

### <span data-ttu-id="ab8be-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span><span class="sxs-lookup"><span data-stu-id="ab8be-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span></span>

## <span data-ttu-id="ab8be-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ab8be-128">NOTES</span></span>

## <span data-ttu-id="ab8be-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab8be-129">RELATED LINKS</span></span>
