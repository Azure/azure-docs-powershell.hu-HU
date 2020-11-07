---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzSubscription.md
ms.openlocfilehash: ac699d3a52271652682f22a8f4c94961e4a921d2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841053"
---
# <span data-ttu-id="14ec9-101">Get-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="14ec9-101">Get-AzSubscription</span></span>

## <span data-ttu-id="14ec9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="14ec9-102">SYNOPSIS</span></span>
<span data-ttu-id="14ec9-103">Az aktuális fiók által elérhető előfizetések beszerzése.</span><span class="sxs-lookup"><span data-stu-id="14ec9-103">Get subscriptions that the current account can access.</span></span>

## <span data-ttu-id="14ec9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="14ec9-104">SYNTAX</span></span>

### <span data-ttu-id="14ec9-105">ListByIdInTenant (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="14ec9-105">ListByIdInTenant (Default)</span></span>
```
Get-AzSubscription [-SubscriptionId <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14ec9-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="14ec9-106">ListByNameInTenant</span></span>
```
Get-AzSubscription [-SubscriptionName <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14ec9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="14ec9-107">DESCRIPTION</span></span>
<span data-ttu-id="14ec9-108">A Get-AzSubscription parancsmag az előfizetés AZONOSÍTÓját, az előfizetés nevét és az otthoni bérlőt kapja meg az aktuális fiók által elérhető előfizetésekhez.</span><span class="sxs-lookup"><span data-stu-id="14ec9-108">The Get-AzSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="14ec9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="14ec9-109">EXAMPLES</span></span>

### <span data-ttu-id="14ec9-110">Példa 1: összes előfizetés lekérése az összes bérlői fiókban</span><span class="sxs-lookup"><span data-stu-id="14ec9-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription3                      zzzz-zzzz-zzzz-zzzz     bbbb-bbbb-bbbb-bbbb             Enabled
```

<span data-ttu-id="14ec9-111">Ez a parancs minden előfizetést beolvassa az aktuális fiókhoz engedéllyel rendelkező bérlői fiókokban.</span><span class="sxs-lookup"><span data-stu-id="14ec9-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="14ec9-112">2. példa: adott bérlői előfizetések lekérése</span><span class="sxs-lookup"><span data-stu-id="14ec9-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzSubscription -TenantId "aaaa-aaaa-aaaa-aaaa"

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="14ec9-113">Az adott bérlői fiók összes előfizetésének listázása, amely az aktuális fiókhoz van engedélyezve.</span><span class="sxs-lookup"><span data-stu-id="14ec9-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="14ec9-114">3. példa: a jelenlegi bérlő összes előfizetésének beszerzése</span><span class="sxs-lookup"><span data-stu-id="14ec9-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="14ec9-115">Ez a parancs beilleszti az aktuális felhasználó által engedélyezett összes előfizetést az aktuális bérlői fiókba.</span><span class="sxs-lookup"><span data-stu-id="14ec9-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="14ec9-116">Példa 4: az aktuális környezet módosítása adott előfizetés használatára</span><span class="sxs-lookup"><span data-stu-id="14ec9-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxx-xxxx-xxxx-xxxx)      azureuser@micros... Subscription1       AzureCloud          yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="14ec9-117">Ez a parancs beilleszti a megadott előfizetést, majd az aktuális környezetet a használatára állítja be.</span><span class="sxs-lookup"><span data-stu-id="14ec9-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="14ec9-118">A munkamenet minden további parancsmagja alapértelmezés szerint az új előfizetést használja (contoso-előfizetés 1).</span><span class="sxs-lookup"><span data-stu-id="14ec9-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="14ec9-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="14ec9-119">PARAMETERS</span></span>

### <span data-ttu-id="14ec9-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14ec9-120">-AsJob</span></span>
<span data-ttu-id="14ec9-121">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="14ec9-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="14ec9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14ec9-122">-DefaultProfile</span></span>
<span data-ttu-id="14ec9-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="14ec9-123">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14ec9-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="14ec9-124">-SubscriptionId</span></span>
<span data-ttu-id="14ec9-125">Megadja a beszerzéshez tartozó előfizetés AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="14ec9-125">Specifies the ID of the subscription to get.</span></span>

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

### <span data-ttu-id="14ec9-126">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="14ec9-126">-SubscriptionName</span></span>
<span data-ttu-id="14ec9-127">A beolvasott előfizetés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="14ec9-127">Specifies the name of the subscription to get.</span></span>

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

### <span data-ttu-id="14ec9-128">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="14ec9-128">-TenantId</span></span>
<span data-ttu-id="14ec9-129">Az előfizetéseket tartalmazó bérlő AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="14ec9-129">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

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

### <span data-ttu-id="14ec9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14ec9-130">CommonParameters</span></span>
<span data-ttu-id="14ec9-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="14ec9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14ec9-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="14ec9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14ec9-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="14ec9-133">INPUTS</span></span>

### <span data-ttu-id="14ec9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="14ec9-134">System.String</span></span>

## <span data-ttu-id="14ec9-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14ec9-135">OUTPUTS</span></span>

### <span data-ttu-id="14ec9-136">Microsoft. Azure. Command. profil. models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="14ec9-136">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="14ec9-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="14ec9-137">NOTES</span></span>

## <span data-ttu-id="14ec9-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14ec9-138">RELATED LINKS</span></span>
