---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
ms.openlocfilehash: 155310764ea540d9062df8ae8f37171bc6f73066
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493969"
---
# <span data-ttu-id="f46fd-101">Get-AzureRmReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="f46fd-101">Get-AzureRmReservationCatalog</span></span>

## <span data-ttu-id="f46fd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f46fd-102">SYNOPSIS</span></span>
<span data-ttu-id="f46fd-103">A rendelkezésre álló foglalások katalógusának beszerzése</span><span class="sxs-lookup"><span data-stu-id="f46fd-103">Get the catalog of available reservations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f46fd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f46fd-104">SYNTAX</span></span>

```
Get-AzureRmReservationCatalog [-SubscriptionId <Guid>] -ReservedResourceType <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f46fd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f46fd-105">DESCRIPTION</span></span>
<span data-ttu-id="f46fd-106">A megadott Azure-előfizetéshez lefoglalt példányok vásárlásához rendelkezésre álló régiók és SKU-ók beszerzése.</span><span class="sxs-lookup"><span data-stu-id="f46fd-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="f46fd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f46fd-107">EXAMPLES</span></span>

### <span data-ttu-id="f46fd-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f46fd-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationCatalog -ReservedResourceType VirtualMachines -Location westus
```

<span data-ttu-id="f46fd-109">A VirtualMachines katalógus beszerzése az alapértelmezett előfizetés westus</span><span class="sxs-lookup"><span data-stu-id="f46fd-109">Get the VirtualMachines catalog in westus for the default subscription</span></span>

### <span data-ttu-id="f46fd-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="f46fd-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservedResourceType SuseLinux
```

<span data-ttu-id="f46fd-111">A megadott előfizetés SuseLinux katalógusának beszerzése</span><span class="sxs-lookup"><span data-stu-id="f46fd-111">Get the SuseLinux catalog for the specified subscription</span></span>

## <span data-ttu-id="f46fd-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f46fd-112">PARAMETERS</span></span>

### <span data-ttu-id="f46fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f46fd-113">-DefaultProfile</span></span>
<span data-ttu-id="f46fd-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f46fd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f46fd-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="f46fd-115">-Location</span></span>
<span data-ttu-id="f46fd-116">A katalógusban lévő foglalt erőforrások helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f46fd-116">Specifies the location of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="f46fd-117">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="f46fd-117">-ReservedResourceType</span></span>
<span data-ttu-id="f46fd-118">A katalógusban lévő foglalt erőforrások típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f46fd-118">Specifies the type of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="f46fd-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f46fd-119">-SubscriptionId</span></span>
<span data-ttu-id="f46fd-120">Az előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="f46fd-120">Id of the subscription</span></span>

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

### <span data-ttu-id="f46fd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f46fd-121">CommonParameters</span></span>
<span data-ttu-id="f46fd-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f46fd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f46fd-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f46fd-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f46fd-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f46fd-124">INPUTS</span></span>

### <span data-ttu-id="f46fd-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="f46fd-125">None</span></span>

## <span data-ttu-id="f46fd-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f46fd-126">OUTPUTS</span></span>

### <span data-ttu-id="f46fd-127">Microsoft. Azure. commands. Reservations. models. PSCatalog</span><span class="sxs-lookup"><span data-stu-id="f46fd-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span></span>

## <span data-ttu-id="f46fd-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f46fd-128">NOTES</span></span>

## <span data-ttu-id="f46fd-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f46fd-129">RELATED LINKS</span></span>
