---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: e141e2af2dea2a07a9a64ab25c2417ffb6842837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491323"
---
# <span data-ttu-id="ffdd9-101">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="ffdd9-101">Set-AzureRmContext</span></span>

## <span data-ttu-id="ffdd9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ffdd9-102">SYNOPSIS</span></span>
<span data-ttu-id="ffdd9-103">A bérlői fiók, az előfizetés és a környezet beállítása az aktuális munkamenetben használható parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

## <span data-ttu-id="ffdd9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ffdd9-104">SYNTAX</span></span>

### <span data-ttu-id="ffdd9-105">SubscriptionName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ffdd9-105">SubscriptionName (Default)</span></span>
```
Set-AzureRmContext [-SubscriptionName <String>] [-TenantId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffdd9-106">Összefüggésben</span><span class="sxs-lookup"><span data-stu-id="ffdd9-106">Context</span></span>
```
Set-AzureRmContext -Context <PSAzureContext> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffdd9-107">SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ffdd9-107">SubscriptionId</span></span>
```
Set-AzureRmContext [-TenantId <String>] [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffdd9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ffdd9-108">DESCRIPTION</span></span>
<span data-ttu-id="ffdd9-109">A Set-AzureRmContext parancsmag az aktuális munkamenetben futtatott parancsmagok hitelesítési adatait állítja be.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-109">The Set-AzureRmContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="ffdd9-110">A környezet a bérlői, az előfizetési és a környezeti információkat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-110">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="ffdd9-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ffdd9-111">EXAMPLES</span></span>

### <span data-ttu-id="ffdd9-112">Példa 1: az előfizetés környezetének beállítása</span><span class="sxs-lookup"><span data-stu-id="ffdd9-112">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Account      : PFuller@contoso.com
Environment  : AzureCloud
Subscription : xxxx-xxxx-xxxx-xxxx
Tenant       : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="ffdd9-113">Ez a parancs beállítja a megadott előfizetéshez használt környezetet.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-113">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="ffdd9-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ffdd9-114">PARAMETERS</span></span>

### <span data-ttu-id="ffdd9-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ffdd9-115">-Context</span></span>
<span data-ttu-id="ffdd9-116">Az aktuális munkamenet környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-116">Specifies the context for the current session.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: Context
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffdd9-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ffdd9-117">-SubscriptionId</span></span>
<span data-ttu-id="ffdd9-118">Annak a környezetnek az előfizetési AZONOSÍTÓját adja meg, amelyhez az adott parancsmag az aktuális munkamenetet állítja be.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-118">Specifies the subscription ID for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffdd9-119">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ffdd9-119">-SubscriptionName</span></span>
<span data-ttu-id="ffdd9-120">Annak az előfizetésnek a nevét adja meg, amely az aktuális munkamenethez a parancsmag által beállított környezethez tartozik.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-120">Specifies the subscription name for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffdd9-121">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="ffdd9-121">-TenantId</span></span>
<span data-ttu-id="ffdd9-122">Annak a környezetnek az AZONOSÍTÓját adja meg a bérlői fiók számára, amelyre a parancsmag az aktuális munkamenetet állítja be.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-122">Specifies the ID of the tenant for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionName, SubscriptionId
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffdd9-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ffdd9-123">-Confirm</span></span>
<span data-ttu-id="ffdd9-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffdd9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffdd9-125">-WhatIf</span></span>
<span data-ttu-id="ffdd9-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ffdd9-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ffdd9-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffdd9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffdd9-128">CommonParameters</span></span>
<span data-ttu-id="ffdd9-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ffdd9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffdd9-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffdd9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffdd9-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffdd9-131">INPUTS</span></span>

## <span data-ttu-id="ffdd9-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffdd9-132">OUTPUTS</span></span>

### <span data-ttu-id="ffdd9-133">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="ffdd9-133">PSAzureContext</span></span>

## <span data-ttu-id="ffdd9-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ffdd9-134">NOTES</span></span>

## <span data-ttu-id="ffdd9-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ffdd9-135">RELATED LINKS</span></span>

[<span data-ttu-id="ffdd9-136">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="ffdd9-136">Get-AzureRMContext</span></span>]()

