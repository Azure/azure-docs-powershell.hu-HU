---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3def97a3e02e77efd6ec21768b30c855f1ceb34e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840729"
---
# <span data-ttu-id="f0b8f-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="f0b8f-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="f0b8f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f0b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="f0b8f-103">Az összes kvóta listázása</span><span class="sxs-lookup"><span data-stu-id="f0b8f-103">List all quotas.</span></span>

## <span data-ttu-id="f0b8f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f0b8f-104">SYNTAX</span></span>

### <span data-ttu-id="f0b8f-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f0b8f-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="f0b8f-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="f0b8f-106">Get</span></span>
```
Get-AzsNetworkQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="f0b8f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0b8f-107">ResourceId</span></span>
```
Get-AzsNetworkQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="f0b8f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f0b8f-108">DESCRIPTION</span></span>
<span data-ttu-id="f0b8f-109">Az összes kvóta listázása</span><span class="sxs-lookup"><span data-stu-id="f0b8f-109">List all quotas.</span></span>
<span data-ttu-id="f0b8f-110">A lista korlátozása név vagy szűrő elküldésével.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="f0b8f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f0b8f-111">EXAMPLES</span></span>

### <span data-ttu-id="f0b8f-112">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="f0b8f-112">EXAMPLE 1</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="f0b8f-113">Felsorolja az összes hálózati kvótát.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="f0b8f-114">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="f0b8f-114">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="f0b8f-115">A megadott hálózati kvótát kapja.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-115">Gets the specified network quota.</span></span>

## <span data-ttu-id="f0b8f-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f0b8f-116">PARAMETERS</span></span>

### <span data-ttu-id="f0b8f-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f0b8f-117">-Name</span></span>
<span data-ttu-id="f0b8f-118">Hálózati kvóta-erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="f0b8f-118">Network quota resource name.</span></span>

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

### <span data-ttu-id="f0b8f-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="f0b8f-119">-Location</span></span>
<span data-ttu-id="f0b8f-120">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-120">Location of the resource.</span></span>

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

### <span data-ttu-id="f0b8f-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0b8f-121">-ResourceId</span></span>
<span data-ttu-id="f0b8f-122">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="f0b8f-122">The resource id.</span></span>

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

### <span data-ttu-id="f0b8f-123">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="f0b8f-123">-Filter</span></span>
<span data-ttu-id="f0b8f-124">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="f0b8f-124">OData filter parameter.</span></span>

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

### <span data-ttu-id="f0b8f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0b8f-125">CommonParameters</span></span>
<span data-ttu-id="f0b8f-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f0b8f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0b8f-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0b8f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0b8f-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0b8f-128">INPUTS</span></span>

## <span data-ttu-id="f0b8f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0b8f-129">OUTPUTS</span></span>

### <span data-ttu-id="f0b8f-130">Microsoft. AzureStack. Management. Network. admin. models. quote</span><span class="sxs-lookup"><span data-stu-id="f0b8f-130">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="f0b8f-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f0b8f-131">NOTES</span></span>

## <span data-ttu-id="f0b8f-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f0b8f-132">RELATED LINKS</span></span>
