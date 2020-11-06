---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
ms.openlocfilehash: 62f3e1b357c0a85f30ba4eeba6a92d9b8dfc9dd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495791"
---
# <span data-ttu-id="85f59-101">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="85f59-101">Get-AzureRmSubscription</span></span>

## <span data-ttu-id="85f59-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="85f59-102">SYNOPSIS</span></span>
<span data-ttu-id="85f59-103">Az aktuális fiók által elérhető előfizetések beszerzése.</span><span class="sxs-lookup"><span data-stu-id="85f59-103">Get subscriptions that the current account can access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85f59-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="85f59-104">SYNTAX</span></span>

### <span data-ttu-id="85f59-105">ListByIdInTenant (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="85f59-105">ListByIdInTenant (Default)</span></span>
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85f59-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="85f59-106">ListByNameInTenant</span></span>
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85f59-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="85f59-107">DESCRIPTION</span></span>
<span data-ttu-id="85f59-108">A Get-AzureRmSubscription parancsmag az előfizetés AZONOSÍTÓját, az előfizetés nevét és az otthoni bérlőt kapja meg az aktuális fiók által elérhető előfizetésekhez.</span><span class="sxs-lookup"><span data-stu-id="85f59-108">The Get-AzureRmSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="85f59-109">Példák</span><span class="sxs-lookup"><span data-stu-id="85f59-109">EXAMPLES</span></span>

### <span data-ttu-id="85f59-110">Példa 1: összes előfizetés lekérése az összes bérlői fiókban</span><span class="sxs-lookup"><span data-stu-id="85f59-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzureRmSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription3                      zzzz-zzzz-zzzz-zzzz     bbbb-bbbb-bbbb-bbbb             Enabled
```

<span data-ttu-id="85f59-111">Ez a parancs minden előfizetést beolvassa az aktuális fiókhoz engedéllyel rendelkező bérlői fiókokban.</span><span class="sxs-lookup"><span data-stu-id="85f59-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="85f59-112">2. példa: adott bérlői előfizetések lekérése</span><span class="sxs-lookup"><span data-stu-id="85f59-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="85f59-113">Az adott bérlői fiók összes előfizetésének listázása, amely az aktuális fiókhoz van engedélyezve.</span><span class="sxs-lookup"><span data-stu-id="85f59-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="85f59-114">3. példa: a jelenlegi bérlő összes előfizetésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="85f59-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzureRmSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="85f59-115">Ez a parancs beilleszti az aktuális felhasználó által engedélyezett összes előfizetést az aktuális bérlői fiókba.</span><span class="sxs-lookup"><span data-stu-id="85f59-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="85f59-116">Példa 4: az aktuális környezet módosítása adott előfizetés használatára</span><span class="sxs-lookup"><span data-stu-id="85f59-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxx-xxxx-xxxx-xxxx)      azureuser@micros... Subscription1       AzureCloud          yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="85f59-117">Ez a parancs beilleszti a megadott előfizetést, majd az aktuális környezetet a használatára állítja be.</span><span class="sxs-lookup"><span data-stu-id="85f59-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="85f59-118">A munkamenet minden további parancsmagja alapértelmezés szerint az új előfizetést használja (contoso-előfizetés 1).</span><span class="sxs-lookup"><span data-stu-id="85f59-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="85f59-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="85f59-119">PARAMETERS</span></span>

### <span data-ttu-id="85f59-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85f59-120">-AsJob</span></span>
<span data-ttu-id="85f59-121">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="85f59-121">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85f59-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85f59-122">-DefaultProfile</span></span>
<span data-ttu-id="85f59-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="85f59-123">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85f59-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="85f59-124">-SubscriptionId</span></span>
<span data-ttu-id="85f59-125">Megadja a beszerzéshez tartozó előfizetés AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="85f59-125">Specifies the ID of the subscription to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByIdInTenant
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85f59-126">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="85f59-126">-SubscriptionName</span></span>
<span data-ttu-id="85f59-127">A beolvasott előfizetés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="85f59-127">Specifies the name of the subscription to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByNameInTenant
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85f59-128">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="85f59-128">-TenantId</span></span>
<span data-ttu-id="85f59-129">Az előfizetéseket tartalmazó bérlő AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="85f59-129">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85f59-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85f59-130">CommonParameters</span></span>
<span data-ttu-id="85f59-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="85f59-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85f59-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85f59-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85f59-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="85f59-133">INPUTS</span></span>

### <span data-ttu-id="85f59-134">System. String</span><span class="sxs-lookup"><span data-stu-id="85f59-134">System.String</span></span>

## <span data-ttu-id="85f59-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="85f59-135">OUTPUTS</span></span>

### <span data-ttu-id="85f59-136">Microsoft. Azure. Command. profil. models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="85f59-136">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="85f59-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="85f59-137">NOTES</span></span>

## <span data-ttu-id="85f59-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="85f59-138">RELATED LINKS</span></span>
