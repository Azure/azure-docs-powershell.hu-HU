---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3def97a3e02e77efd6ec21768b30c855f1ceb34e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016991"
---
# <span data-ttu-id="b5e4c-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="b5e4c-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="b5e4c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b5e4c-102">SYNOPSIS</span></span>
<span data-ttu-id="b5e4c-103">Az összes kvóta listázása</span><span class="sxs-lookup"><span data-stu-id="b5e4c-103">List all quotas.</span></span>

## <span data-ttu-id="b5e4c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b5e4c-104">SYNTAX</span></span>

### <span data-ttu-id="b5e4c-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b5e4c-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="b5e4c-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="b5e4c-106">Get</span></span>
```
Get-AzsNetworkQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="b5e4c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5e4c-107">ResourceId</span></span>
```
Get-AzsNetworkQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b5e4c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b5e4c-108">DESCRIPTION</span></span>
<span data-ttu-id="b5e4c-109">Az összes kvóta listázása</span><span class="sxs-lookup"><span data-stu-id="b5e4c-109">List all quotas.</span></span>
<span data-ttu-id="b5e4c-110">A lista korlátozása név vagy szűrő elküldésével.</span><span class="sxs-lookup"><span data-stu-id="b5e4c-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="b5e4c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b5e4c-111">EXAMPLES</span></span>

### <span data-ttu-id="b5e4c-112">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="b5e4c-112">EXAMPLE 1</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="b5e4c-113">Felsorolja az összes hálózati kvótát.</span><span class="sxs-lookup"><span data-stu-id="b5e4c-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="b5e4c-114">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="b5e4c-114">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="b5e4c-115">A megadott hálózati kvótát kapja.</span><span class="sxs-lookup"><span data-stu-id="b5e4c-115">Gets the specified network quota.</span></span>

## <span data-ttu-id="b5e4c-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b5e4c-116">PARAMETERS</span></span>

### <span data-ttu-id="b5e4c-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b5e4c-117">-Name</span></span>
<span data-ttu-id="b5e4c-118">Hálózati kvóta-erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="b5e4c-118">Network quota resource name.</span></span>

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

### <span data-ttu-id="b5e4c-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="b5e4c-119">-Location</span></span>
<span data-ttu-id="b5e4c-120">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="b5e4c-120">Location of the resource.</span></span>

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

### <span data-ttu-id="b5e4c-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5e4c-121">-ResourceId</span></span>
<span data-ttu-id="b5e4c-122">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="b5e4c-122">The resource id.</span></span>

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

### <span data-ttu-id="b5e4c-123">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="b5e4c-123">-Filter</span></span>
<span data-ttu-id="b5e4c-124">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="b5e4c-124">OData filter parameter.</span></span>

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

### <span data-ttu-id="b5e4c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5e4c-125">CommonParameters</span></span>
<span data-ttu-id="b5e4c-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b5e4c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5e4c-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5e4c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5e4c-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5e4c-128">INPUTS</span></span>

## <span data-ttu-id="b5e4c-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5e4c-129">OUTPUTS</span></span>

### <span data-ttu-id="b5e4c-130">Microsoft. AzureStack. Management. Network. admin. models. quote</span><span class="sxs-lookup"><span data-stu-id="b5e4c-130">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="b5e4c-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b5e4c-131">NOTES</span></span>

## <span data-ttu-id="b5e4c-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5e4c-132">RELATED LINKS</span></span>
