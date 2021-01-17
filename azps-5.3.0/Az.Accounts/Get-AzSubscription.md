---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzSubscription.md
ms.openlocfilehash: aecdd4a0b5f0ef4465f08441841fb923a273afdf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479158"
---
# <span data-ttu-id="48db9-101">Get-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="48db9-101">Get-AzSubscription</span></span>

## <span data-ttu-id="48db9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48db9-102">SYNOPSIS</span></span>
<span data-ttu-id="48db9-103">Szerezze be az aktuális fiók által elérhető előfizetéseket.</span><span class="sxs-lookup"><span data-stu-id="48db9-103">Get subscriptions that the current account can access.</span></span>

## <span data-ttu-id="48db9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="48db9-104">SYNTAX</span></span>

### <span data-ttu-id="48db9-105">ListByIdInTenant (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="48db9-105">ListByIdInTenant (Default)</span></span>
```
Get-AzSubscription [-SubscriptionId <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48db9-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="48db9-106">ListByNameInTenant</span></span>
```
Get-AzSubscription [-SubscriptionName <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48db9-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="48db9-107">DESCRIPTION</span></span>
<span data-ttu-id="48db9-108">A Get-AzSubscription parancsmag az aktuális fiók által elérhető előfizetések előfizetésazonosítóját, előfizetés nevét és otthoni bérlői webhelyét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="48db9-108">The Get-AzSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="48db9-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="48db9-109">EXAMPLES</span></span>

### <span data-ttu-id="48db9-110">1. példa: Az összes bérlői webhely összes előfizetésének lekérte</span><span class="sxs-lookup"><span data-stu-id="48db9-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription3                      zzzz-zzzz-zzzz-zzzz     bbbb-bbbb-bbbb-bbbb             Enabled
```

<span data-ttu-id="48db9-111">Ez a parancs az aktuális fiókhoz engedélyezett összes bérlő összes előfizetését beveszi.</span><span class="sxs-lookup"><span data-stu-id="48db9-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="48db9-112">2. példa: Egy adott bérlő összes előfizetésének lekérte</span><span class="sxs-lookup"><span data-stu-id="48db9-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzSubscription -TenantId "aaaa-aaaa-aaaa-aaaa"

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="48db9-113">List all subscriptions in the given tenant that are authorized for the current account.</span><span class="sxs-lookup"><span data-stu-id="48db9-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="48db9-114">3. példa: Az aktuális bérlő összes előfizetésének lekérte</span><span class="sxs-lookup"><span data-stu-id="48db9-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="48db9-115">Ez a parancs az aktuális bérlő összes olyan előfizetését megkapja, amely jogosult az aktuális felhasználóra.</span><span class="sxs-lookup"><span data-stu-id="48db9-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="48db9-116">4. példa: Az aktuális környezet módosítása adott előfizetés használatára</span><span class="sxs-lookup"><span data-stu-id="48db9-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxx-xxxx-xxxx-xxxx)      azureuser@micros... Subscription1       AzureCloud          yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="48db9-117">Ez a parancs beállítja a megadott előfizetést, majd beállítja a jelenlegi környezet használatát.</span><span class="sxs-lookup"><span data-stu-id="48db9-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="48db9-118">A munkamenet minden ezt követő parancsmagja alapértelmezés szerint az új előfizetést (Contoso-előfizetés 1) használja.</span><span class="sxs-lookup"><span data-stu-id="48db9-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="48db9-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48db9-119">PARAMETERS</span></span>

### <span data-ttu-id="48db9-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48db9-120">-AsJob</span></span>
<span data-ttu-id="48db9-121">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="48db9-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="48db9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48db9-122">-DefaultProfile</span></span>
<span data-ttu-id="48db9-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="48db9-123">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48db9-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="48db9-124">-SubscriptionId</span></span>
<span data-ttu-id="48db9-125">A lekért előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="48db9-125">Specifies the ID of the subscription to get.</span></span>

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

### <span data-ttu-id="48db9-126">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="48db9-126">-SubscriptionName</span></span>
<span data-ttu-id="48db9-127">A lekért előfizetés neve.</span><span class="sxs-lookup"><span data-stu-id="48db9-127">Specifies the name of the subscription to get.</span></span>

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

### <span data-ttu-id="48db9-128">-TenantId</span><span class="sxs-lookup"><span data-stu-id="48db9-128">-TenantId</span></span>
<span data-ttu-id="48db9-129">Annak a bérlőnek az azonosítója, amely a behozni kívánt előfizetéseket tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="48db9-129">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

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

### <span data-ttu-id="48db9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48db9-130">CommonParameters</span></span>
<span data-ttu-id="48db9-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48db9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48db9-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48db9-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48db9-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="48db9-133">INPUTS</span></span>

### <span data-ttu-id="48db9-134">System.String</span><span class="sxs-lookup"><span data-stu-id="48db9-134">System.String</span></span>

## <span data-ttu-id="48db9-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48db9-135">OUTPUTS</span></span>

### <span data-ttu-id="48db9-136">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="48db9-136">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="48db9-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="48db9-137">NOTES</span></span>

## <span data-ttu-id="48db9-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48db9-138">RELATED LINKS</span></span>
