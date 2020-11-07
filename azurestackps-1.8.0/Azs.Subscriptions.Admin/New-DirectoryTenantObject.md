---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20b70e2eeb1aa2d98f595dfe7bbe3075174c1f64
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840168"
---
# <span data-ttu-id="2600e-101">New-DirectoryTenantObject</span><span class="sxs-lookup"><span data-stu-id="2600e-101">New-DirectoryTenantObject</span></span>

## <span data-ttu-id="2600e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2600e-102">SYNOPSIS</span></span>
<span data-ttu-id="2600e-103">Címtár-bérlő.</span><span class="sxs-lookup"><span data-stu-id="2600e-103">Directory tenant.</span></span>

## <span data-ttu-id="2600e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2600e-104">SYNTAX</span></span>

```
New-DirectoryTenantObject [[-Id] <String>] [[-Type] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [[-Name] <String>]
 [[-TenantId] <String>] [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="2600e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2600e-105">DESCRIPTION</span></span>
<span data-ttu-id="2600e-106">Címtár-bérlő.</span><span class="sxs-lookup"><span data-stu-id="2600e-106">Directory tenant.</span></span>

## <span data-ttu-id="2600e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2600e-107">EXAMPLES</span></span>

### <span data-ttu-id="2600e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2600e-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="2600e-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="2600e-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="2600e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2600e-110">PARAMETERS</span></span>

### <span data-ttu-id="2600e-111">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="2600e-111">-Id</span></span>
<span data-ttu-id="2600e-112">Az erőforrás URI-ja.</span><span class="sxs-lookup"><span data-stu-id="2600e-112">URI of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2600e-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="2600e-113">-Location</span></span>
<span data-ttu-id="2600e-114">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="2600e-114">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2600e-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2600e-115">-Name</span></span>
<span data-ttu-id="2600e-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="2600e-116">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2600e-117">-Címkék</span><span class="sxs-lookup"><span data-stu-id="2600e-117">-Tags</span></span>
<span data-ttu-id="2600e-118">A kulcs-érték párok listája.</span><span class="sxs-lookup"><span data-stu-id="2600e-118">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2600e-119">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="2600e-119">-TenantId</span></span>
<span data-ttu-id="2600e-120">Bérlői egyedi azonosító.</span><span class="sxs-lookup"><span data-stu-id="2600e-120">Tenant unique identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2600e-121">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="2600e-121">-Type</span></span>
<span data-ttu-id="2600e-122">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="2600e-122">Type of resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2600e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2600e-123">CommonParameters</span></span>
<span data-ttu-id="2600e-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2600e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2600e-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2600e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2600e-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2600e-126">INPUTS</span></span>

## <span data-ttu-id="2600e-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2600e-127">OUTPUTS</span></span>

## <span data-ttu-id="2600e-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2600e-128">NOTES</span></span>

## <span data-ttu-id="2600e-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2600e-129">RELATED LINKS</span></span>

