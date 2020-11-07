---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3def97a3e02e77efd6ec21768b30c855f1ceb34e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840373"
---
# <span data-ttu-id="0e286-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="0e286-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="0e286-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0e286-102">SYNOPSIS</span></span>
<span data-ttu-id="0e286-103">Az összes kvóta listázása</span><span class="sxs-lookup"><span data-stu-id="0e286-103">List all quotas.</span></span>

## <span data-ttu-id="0e286-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0e286-104">SYNTAX</span></span>

### <span data-ttu-id="0e286-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0e286-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="0e286-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="0e286-106">Get</span></span>
```
Get-AzsNetworkQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="0e286-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e286-107">ResourceId</span></span>
```
Get-AzsNetworkQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="0e286-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0e286-108">DESCRIPTION</span></span>
<span data-ttu-id="0e286-109">Az összes kvóta listázása</span><span class="sxs-lookup"><span data-stu-id="0e286-109">List all quotas.</span></span>
<span data-ttu-id="0e286-110">A lista korlátozása név vagy szűrő elküldésével.</span><span class="sxs-lookup"><span data-stu-id="0e286-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="0e286-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0e286-111">EXAMPLES</span></span>

### <span data-ttu-id="0e286-112">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="0e286-112">EXAMPLE 1</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="0e286-113">Felsorolja az összes hálózati kvótát.</span><span class="sxs-lookup"><span data-stu-id="0e286-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="0e286-114">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="0e286-114">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="0e286-115">A megadott hálózati kvótát kapja.</span><span class="sxs-lookup"><span data-stu-id="0e286-115">Gets the specified network quota.</span></span>

## <span data-ttu-id="0e286-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0e286-116">PARAMETERS</span></span>

### <span data-ttu-id="0e286-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0e286-117">-Name</span></span>
<span data-ttu-id="0e286-118">Hálózati kvóta-erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="0e286-118">Network quota resource name.</span></span>

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

### <span data-ttu-id="0e286-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="0e286-119">-Location</span></span>
<span data-ttu-id="0e286-120">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="0e286-120">Location of the resource.</span></span>

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

### <span data-ttu-id="0e286-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e286-121">-ResourceId</span></span>
<span data-ttu-id="0e286-122">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="0e286-122">The resource id.</span></span>

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

### <span data-ttu-id="0e286-123">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="0e286-123">-Filter</span></span>
<span data-ttu-id="0e286-124">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="0e286-124">OData filter parameter.</span></span>

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

### <span data-ttu-id="0e286-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e286-125">CommonParameters</span></span>
<span data-ttu-id="0e286-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0e286-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e286-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e286-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e286-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e286-128">INPUTS</span></span>

## <span data-ttu-id="0e286-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e286-129">OUTPUTS</span></span>

### <span data-ttu-id="0e286-130">Microsoft. AzureStack. Management. Network. admin. models. quote</span><span class="sxs-lookup"><span data-stu-id="0e286-130">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="0e286-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0e286-131">NOTES</span></span>

## <span data-ttu-id="0e286-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e286-132">RELATED LINKS</span></span>
