---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 13dd14f59b28e3b5730f207c675771e1275392d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491167"
---
# <span data-ttu-id="b506e-101">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="b506e-101">Get-AzureRmSubscription</span></span>

## <span data-ttu-id="b506e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b506e-102">SYNOPSIS</span></span>
<span data-ttu-id="b506e-103">Az aktuális fiók által elérhető előfizetések beszerzése.</span><span class="sxs-lookup"><span data-stu-id="b506e-103">Get subscriptions that the current account can access.</span></span>

## <span data-ttu-id="b506e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b506e-104">SYNTAX</span></span>

### <span data-ttu-id="b506e-105">ListByIdInTenant (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b506e-105">ListByIdInTenant (Default)</span></span>
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>] [<CommonParameters>]
```

### <span data-ttu-id="b506e-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="b506e-106">ListByNameInTenant</span></span>
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>] [<CommonParameters>]
```

## <span data-ttu-id="b506e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b506e-107">DESCRIPTION</span></span>
<span data-ttu-id="b506e-108">A Get-AzureRmSubscription parancsmag az előfizetés AZONOSÍTÓját, az előfizetés nevét és az otthoni bérlőt kapja meg az aktuális fiók által elérhető előfizetésekhez.</span><span class="sxs-lookup"><span data-stu-id="b506e-108">The Get-AzureRmSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="b506e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b506e-109">EXAMPLES</span></span>

### <span data-ttu-id="b506e-110">Példa 1: összes előfizetés lekérése az összes bérlői fiókban</span><span class="sxs-lookup"><span data-stu-id="b506e-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzureRmSubscription -All

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="b506e-111">Ez a parancs minden előfizetést beolvassa az aktuális fiókhoz engedéllyel rendelkező bérlői fiókokban.</span><span class="sxs-lookup"><span data-stu-id="b506e-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="b506e-112">2. példa: adott bérlői előfizetések lekérése</span><span class="sxs-lookup"><span data-stu-id="b506e-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="b506e-113">Az adott bérlői fiók összes előfizetésének listázása, amely az aktuális fiókhoz van engedélyezve.</span><span class="sxs-lookup"><span data-stu-id="b506e-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="b506e-114">3. példa: a jelenlegi bérlő összes előfizetésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="b506e-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzureRmSubscription

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="b506e-115">Ez a parancs beilleszti az aktuális felhasználó által engedélyezett összes előfizetést az aktuális bérlői fiókba.</span><span class="sxs-lookup"><span data-stu-id="b506e-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="b506e-116">Példa 4: az aktuális környezet módosítása adott előfizetés használatára</span><span class="sxs-lookup"><span data-stu-id="b506e-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="b506e-117">Ez a parancs beilleszti a megadott előfizetést, majd az aktuális környezetet a használatára állítja be.</span><span class="sxs-lookup"><span data-stu-id="b506e-117">This command gets the specified subscription, and then sets the current context to use it.</span></span>
<span data-ttu-id="b506e-118">A munkamenet minden további parancsmagja alapértelmezés szerint az új előfizetést használja (contoso-előfizetés 1).</span><span class="sxs-lookup"><span data-stu-id="b506e-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="b506e-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b506e-119">PARAMETERS</span></span>

### <span data-ttu-id="b506e-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b506e-120">-SubscriptionId</span></span>
<span data-ttu-id="b506e-121">Megadja a beszerzéshez tartozó előfizetés AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="b506e-121">Specifies the ID of the subscription to get.</span></span>

```yaml
Type: String
Parameter Sets: ListByIdInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b506e-122">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="b506e-122">-SubscriptionName</span></span>
<span data-ttu-id="b506e-123">A beolvasott előfizetés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b506e-123">Specifies the name of the subscription to get.</span></span>

```yaml
Type: String
Parameter Sets: ListByNameInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b506e-124">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="b506e-124">-TenantId</span></span>
<span data-ttu-id="b506e-125">Az előfizetéseket tartalmazó bérlő AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b506e-125">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b506e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b506e-126">CommonParameters</span></span>
<span data-ttu-id="b506e-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b506e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b506e-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b506e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b506e-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b506e-129">INPUTS</span></span>

## <span data-ttu-id="b506e-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b506e-130">OUTPUTS</span></span>

### <span data-ttu-id="b506e-131">PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="b506e-131">PSAzureSubscription</span></span>

## <span data-ttu-id="b506e-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b506e-132">NOTES</span></span>

## <span data-ttu-id="b506e-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b506e-133">RELATED LINKS</span></span>

