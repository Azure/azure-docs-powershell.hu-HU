---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
ms.openlocfilehash: 42c7e2b632b175ef12f34e04ff682020d634ef74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673137"
---
# <span data-ttu-id="22c6e-101">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="22c6e-101">Set-AzureRmContext</span></span>

## <span data-ttu-id="22c6e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="22c6e-102">SYNOPSIS</span></span>
<span data-ttu-id="22c6e-103">A bérlői fiók, az előfizetés és a környezet beállítása az aktuális munkamenetben használható parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="22c6e-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22c6e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="22c6e-104">SYNTAX</span></span>

### <span data-ttu-id="22c6e-105">Környezet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="22c6e-105">Context (Default)</span></span>
```
Set-AzureRmContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22c6e-106">TenantObject</span><span class="sxs-lookup"><span data-stu-id="22c6e-106">TenantObject</span></span>
```
Set-AzureRmContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22c6e-107">SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="22c6e-107">SubscriptionObject</span></span>
```
Set-AzureRmContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22c6e-108">Előfizetés</span><span class="sxs-lookup"><span data-stu-id="22c6e-108">Subscription</span></span>
```
Set-AzureRmContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22c6e-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="22c6e-109">TenantNameOnly</span></span>
```
Set-AzureRmContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22c6e-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="22c6e-110">DESCRIPTION</span></span>
<span data-ttu-id="22c6e-111">A Set-AzureRmContext parancsmag az aktuális munkamenetben futtatott parancsmagok hitelesítési adatait állítja be.</span><span class="sxs-lookup"><span data-stu-id="22c6e-111">The Set-AzureRmContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="22c6e-112">A környezet a bérlői, az előfizetési és a környezeti információkat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="22c6e-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="22c6e-113">Példák</span><span class="sxs-lookup"><span data-stu-id="22c6e-113">EXAMPLES</span></span>

### <span data-ttu-id="22c6e-114">Példa 1: az előfizetés környezetének beállítása</span><span class="sxs-lookup"><span data-stu-id="22c6e-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="22c6e-115">Ez a parancs beállítja a megadott előfizetéshez használt környezetet.</span><span class="sxs-lookup"><span data-stu-id="22c6e-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="22c6e-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="22c6e-116">PARAMETERS</span></span>

### <span data-ttu-id="22c6e-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="22c6e-117">-Context</span></span>
<span data-ttu-id="22c6e-118">Az aktuális munkamenet környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="22c6e-118">Specifies the context for the current session.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: Context
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22c6e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22c6e-119">-DefaultProfile</span></span>
<span data-ttu-id="22c6e-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="22c6e-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22c6e-121">-ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="22c6e-121">-ExtendedProperty</span></span>
<span data-ttu-id="22c6e-122">További környezeti tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="22c6e-122">Additional context properties</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c6e-123">-Force</span><span class="sxs-lookup"><span data-stu-id="22c6e-123">-Force</span></span>
<span data-ttu-id="22c6e-124">Felülírja a meglévő környezetet ugyanazzal a névvel, ha van ilyen.</span><span class="sxs-lookup"><span data-stu-id="22c6e-124">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="22c6e-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="22c6e-125">-Name</span></span>
<span data-ttu-id="22c6e-126">A környezet neve</span><span class="sxs-lookup"><span data-stu-id="22c6e-126">Name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c6e-127">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="22c6e-127">-Scope</span></span>
<span data-ttu-id="22c6e-128">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="22c6e-128">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c6e-129">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="22c6e-129">-Subscription</span></span>
<span data-ttu-id="22c6e-130">Annak az előfizetésnek a neve vagy azonosítója, amelyhez a környezetet be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="22c6e-130">The name or id of the subscription that the context should be set to.</span></span> <span data-ttu-id="22c6e-131">Ez a paraméter aliasokat tartalmaz a-SubscriptionName és a SubscriptionId, így az érthetőség kedvéért az előfizetések helyett a név és azonosító megadásakor is használhatók.</span><span class="sxs-lookup"><span data-stu-id="22c6e-131">This parameter has aliases to -SubscriptionName and -SubscriptionId, so, for clarity, either of these can be used instead of -Subscription when specifying name and id, respectively.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases: SubscriptionId, SubscriptionName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c6e-132">-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="22c6e-132">-SubscriptionObject</span></span>
<span data-ttu-id="22c6e-133">Egy előfizetési objektum</span><span class="sxs-lookup"><span data-stu-id="22c6e-133">A subscription object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription
Parameter Sets: SubscriptionObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22c6e-134">-Bérlő</span><span class="sxs-lookup"><span data-stu-id="22c6e-134">-Tenant</span></span>
<span data-ttu-id="22c6e-135">Bérlő neve vagy azonosítója</span><span class="sxs-lookup"><span data-stu-id="22c6e-135">Tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TenantNameOnly
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c6e-136">-TenantObject</span><span class="sxs-lookup"><span data-stu-id="22c6e-136">-TenantObject</span></span>
<span data-ttu-id="22c6e-137">Bérlői objektum</span><span class="sxs-lookup"><span data-stu-id="22c6e-137">A Tenant Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureTenant
Parameter Sets: TenantObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22c6e-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="22c6e-138">-Confirm</span></span>
<span data-ttu-id="22c6e-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="22c6e-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c6e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22c6e-140">-WhatIf</span></span>
<span data-ttu-id="22c6e-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="22c6e-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22c6e-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="22c6e-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c6e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22c6e-143">CommonParameters</span></span>
<span data-ttu-id="22c6e-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="22c6e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22c6e-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22c6e-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22c6e-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="22c6e-146">INPUTS</span></span>

### <span data-ttu-id="22c6e-147">Microsoft. Azure. Command. profil. models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="22c6e-147">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>
<span data-ttu-id="22c6e-148">Paraméterek: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="22c6e-148">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="22c6e-149">Microsoft. Azure. Command. profil. models. PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="22c6e-149">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>
<span data-ttu-id="22c6e-150">Paraméterek: TenantObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="22c6e-150">Parameters: TenantObject (ByValue)</span></span>

### <span data-ttu-id="22c6e-151">Microsoft. Azure. Command. profil. models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="22c6e-151">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>
<span data-ttu-id="22c6e-152">Paraméterek: SubscriptionObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="22c6e-152">Parameters: SubscriptionObject (ByValue)</span></span>

## <span data-ttu-id="22c6e-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22c6e-153">OUTPUTS</span></span>

### <span data-ttu-id="22c6e-154">Microsoft. Azure. Command. profil. models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="22c6e-154">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="22c6e-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="22c6e-155">NOTES</span></span>

## <span data-ttu-id="22c6e-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22c6e-156">RELATED LINKS</span></span>

[<span data-ttu-id="22c6e-157">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="22c6e-157">Get-AzureRMContext</span></span>](./Get-AzureRMContext.md)

