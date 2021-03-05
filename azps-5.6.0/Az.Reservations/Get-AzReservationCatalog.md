---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/get-azreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
ms.openlocfilehash: 77fb1806ba2cbdd2e0398bcdf8289aed62c085fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000309"
---
# <span data-ttu-id="d4dc5-101">Get-AzReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="d4dc5-101">Get-AzReservationCatalog</span></span>

## <span data-ttu-id="d4dc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4dc5-102">SYNOPSIS</span></span>
<span data-ttu-id="d4dc5-103">Az elérhető foglalások katalógusának lekérhetők</span><span class="sxs-lookup"><span data-stu-id="d4dc5-103">Get the catalog of available reservations</span></span>

## <span data-ttu-id="d4dc5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d4dc5-104">SYNTAX</span></span>

```
Get-AzReservationCatalog [-SubscriptionId <Guid>] -ReservedResourceType <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4dc5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d4dc5-105">DESCRIPTION</span></span>
<span data-ttu-id="d4dc5-106">Szerezze be a foglalt példányok vásárlásához a megadott Azure-előfizetéshez elérhető régiókat és terméksokokat.</span><span class="sxs-lookup"><span data-stu-id="d4dc5-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="d4dc5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d4dc5-107">EXAMPLES</span></span>

### <span data-ttu-id="d4dc5-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="d4dc5-108">Example 1</span></span>
```
PS C:\> Get-AzReservationCatalog -ReservedResourceType VirtualMachines -Location westus
```

<span data-ttu-id="d4dc5-109">A VirtualMachines katalógusának lekérte az alapértelmezett előfizetést a WestUsban</span><span class="sxs-lookup"><span data-stu-id="d4dc5-109">Get the VirtualMachines catalog in westus for the default subscription</span></span>

### <span data-ttu-id="d4dc5-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="d4dc5-110">Example 2</span></span>
```
PS C:\> Get-AzReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservedResourceType SuseLinux
```

<span data-ttu-id="d4dc5-111">A SuseLinux katalógusának lekérte a megadott előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="d4dc5-111">Get the SuseLinux catalog for the specified subscription</span></span>

## <span data-ttu-id="d4dc5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4dc5-112">PARAMETERS</span></span>

### <span data-ttu-id="d4dc5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4dc5-113">-DefaultProfile</span></span>
<span data-ttu-id="d4dc5-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4dc5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4dc5-115">-Location</span><span class="sxs-lookup"><span data-stu-id="d4dc5-115">-Location</span></span>
<span data-ttu-id="d4dc5-116">Megadja a fenntartott erőforrások helyét a katalógusban.</span><span class="sxs-lookup"><span data-stu-id="d4dc5-116">Specifies the location of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="d4dc5-117">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="d4dc5-117">-ReservedResourceType</span></span>
<span data-ttu-id="d4dc5-118">A katalógusban foglalt erőforrások típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="d4dc5-118">Specifies the type of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="d4dc5-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4dc5-119">-SubscriptionId</span></span>
<span data-ttu-id="d4dc5-120">Az előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="d4dc5-120">Id of the subscription</span></span>

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

### <span data-ttu-id="d4dc5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4dc5-121">CommonParameters</span></span>
<span data-ttu-id="d4dc5-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4dc5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4dc5-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4dc5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4dc5-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4dc5-124">INPUTS</span></span>

### <span data-ttu-id="d4dc5-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="d4dc5-125">None</span></span>

## <span data-ttu-id="d4dc5-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4dc5-126">OUTPUTS</span></span>

### <span data-ttu-id="d4dc5-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span><span class="sxs-lookup"><span data-stu-id="d4dc5-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span></span>

## <span data-ttu-id="d4dc5-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d4dc5-128">NOTES</span></span>

## <span data-ttu-id="d4dc5-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4dc5-129">RELATED LINKS</span></span>
