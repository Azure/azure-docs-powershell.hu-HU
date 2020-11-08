---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
ms.openlocfilehash: 6f1eb79b7c740cae437e28af8153a4c14532871e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184690"
---
# <span data-ttu-id="889d0-101">Get-AzReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="889d0-101">Get-AzReservationCatalog</span></span>

## <span data-ttu-id="889d0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="889d0-102">SYNOPSIS</span></span>
<span data-ttu-id="889d0-103">A rendelkezésre álló foglalások katalógusának beszerzése</span><span class="sxs-lookup"><span data-stu-id="889d0-103">Get the catalog of available reservations</span></span>

## <span data-ttu-id="889d0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="889d0-104">SYNTAX</span></span>

```
Get-AzReservationCatalog [-SubscriptionId <Guid>] -ReservedResourceType <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="889d0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="889d0-105">DESCRIPTION</span></span>
<span data-ttu-id="889d0-106">A megadott Azure-előfizetéshez lefoglalt példányok vásárlásához rendelkezésre álló régiók és SKU-ók beszerzése.</span><span class="sxs-lookup"><span data-stu-id="889d0-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="889d0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="889d0-107">EXAMPLES</span></span>

### <span data-ttu-id="889d0-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="889d0-108">Example 1</span></span>
```
PS C:\> Get-AzReservationCatalog -ReservedResourceType VirtualMachines -Location westus
```

<span data-ttu-id="889d0-109">A VirtualMachines katalógus beszerzése az alapértelmezett előfizetés westus</span><span class="sxs-lookup"><span data-stu-id="889d0-109">Get the VirtualMachines catalog in westus for the default subscription</span></span>

### <span data-ttu-id="889d0-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="889d0-110">Example 2</span></span>
```
PS C:\> Get-AzReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservedResourceType SuseLinux
```

<span data-ttu-id="889d0-111">A megadott előfizetés SuseLinux katalógusának beszerzése</span><span class="sxs-lookup"><span data-stu-id="889d0-111">Get the SuseLinux catalog for the specified subscription</span></span>

## <span data-ttu-id="889d0-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="889d0-112">PARAMETERS</span></span>

### <span data-ttu-id="889d0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="889d0-113">-DefaultProfile</span></span>
<span data-ttu-id="889d0-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="889d0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="889d0-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="889d0-115">-Location</span></span>
<span data-ttu-id="889d0-116">A katalógusban lévő foglalt erőforrások helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="889d0-116">Specifies the location of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="889d0-117">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="889d0-117">-ReservedResourceType</span></span>
<span data-ttu-id="889d0-118">A katalógusban lévő foglalt erőforrások típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="889d0-118">Specifies the type of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="889d0-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="889d0-119">-SubscriptionId</span></span>
<span data-ttu-id="889d0-120">Az előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="889d0-120">Id of the subscription</span></span>

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

### <span data-ttu-id="889d0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="889d0-121">CommonParameters</span></span>
<span data-ttu-id="889d0-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="889d0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="889d0-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="889d0-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="889d0-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="889d0-124">INPUTS</span></span>

### <span data-ttu-id="889d0-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="889d0-125">None</span></span>

## <span data-ttu-id="889d0-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="889d0-126">OUTPUTS</span></span>

### <span data-ttu-id="889d0-127">Microsoft. Azure. commands. Reservations. models. PSCatalog</span><span class="sxs-lookup"><span data-stu-id="889d0-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span></span>

## <span data-ttu-id="889d0-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="889d0-128">NOTES</span></span>

## <span data-ttu-id="889d0-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="889d0-129">RELATED LINKS</span></span>
