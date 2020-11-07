---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb5d980efc5f4e4ad7aff13a8f91832589175039
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93840094"
---
# <span data-ttu-id="11805-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="11805-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="11805-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="11805-102">SYNOPSIS</span></span>
<span data-ttu-id="11805-103">Az összes kvóta listázása</span><span class="sxs-lookup"><span data-stu-id="11805-103">List all quotas.</span></span>

## <span data-ttu-id="11805-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="11805-104">SYNTAX</span></span>

### <span data-ttu-id="11805-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="11805-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="11805-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="11805-106">Get</span></span>
```
Get-AzsNetworkQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="11805-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="11805-107">ResourceId</span></span>
```
Get-AzsNetworkQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="11805-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="11805-108">DESCRIPTION</span></span>
<span data-ttu-id="11805-109">Az összes kvóta listázása</span><span class="sxs-lookup"><span data-stu-id="11805-109">List all quotas.</span></span>
<span data-ttu-id="11805-110">A lista korlátozása név vagy szűrő elküldésével.</span><span class="sxs-lookup"><span data-stu-id="11805-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="11805-111">Példák</span><span class="sxs-lookup"><span data-stu-id="11805-111">EXAMPLES</span></span>

### <span data-ttu-id="11805-112">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="11805-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="11805-113">Felsorolja az összes hálózati kvótát.</span><span class="sxs-lookup"><span data-stu-id="11805-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="11805-114">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="11805-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="11805-115">A megadott hálózati kvótát kapja.</span><span class="sxs-lookup"><span data-stu-id="11805-115">Gets the specified network quota.</span></span>

## <span data-ttu-id="11805-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="11805-116">PARAMETERS</span></span>

### <span data-ttu-id="11805-117">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="11805-117">-Filter</span></span>
<span data-ttu-id="11805-118">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="11805-118">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11805-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="11805-119">-Location</span></span>
<span data-ttu-id="11805-120">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="11805-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11805-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="11805-121">-Name</span></span>
<span data-ttu-id="11805-122">Hálózati kvóta-erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="11805-122">Network quota resource name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11805-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11805-123">-ResourceId</span></span>
<span data-ttu-id="11805-124">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="11805-124">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11805-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11805-125">CommonParameters</span></span>
<span data-ttu-id="11805-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="11805-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11805-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11805-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11805-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="11805-128">INPUTS</span></span>

## <span data-ttu-id="11805-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11805-129">OUTPUTS</span></span>

### <span data-ttu-id="11805-130">Microsoft. AzureStack. Management. Network. admin. models. quote</span><span class="sxs-lookup"><span data-stu-id="11805-130">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="11805-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="11805-131">NOTES</span></span>

## <span data-ttu-id="11805-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11805-132">RELATED LINKS</span></span>

