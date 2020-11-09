---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
ms.openlocfilehash: f7d6c1fcfe4a74601a8a27e85bd1520912b26350
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300014"
---
# <span data-ttu-id="00f80-101">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="00f80-101">Set-AzContext</span></span>

## <span data-ttu-id="00f80-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="00f80-102">SYNOPSIS</span></span>
<span data-ttu-id="00f80-103">A bérlői fiók, az előfizetés és a környezet beállítása az aktuális munkamenetben használható parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="00f80-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

## <span data-ttu-id="00f80-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="00f80-104">SYNTAX</span></span>

### <span data-ttu-id="00f80-105">Környezet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="00f80-105">Context (Default)</span></span>
```
Set-AzContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00f80-106">TenantObject</span><span class="sxs-lookup"><span data-stu-id="00f80-106">TenantObject</span></span>
```
Set-AzContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00f80-107">SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="00f80-107">SubscriptionObject</span></span>
```
Set-AzContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00f80-108">Előfizetés</span><span class="sxs-lookup"><span data-stu-id="00f80-108">Subscription</span></span>
```
Set-AzContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00f80-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="00f80-109">TenantNameOnly</span></span>
```
Set-AzContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="00f80-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="00f80-110">DESCRIPTION</span></span>
<span data-ttu-id="00f80-111">A Set-AzContext parancsmag az aktuális munkamenetben futtatott parancsmagok hitelesítési adatait állítja be.</span><span class="sxs-lookup"><span data-stu-id="00f80-111">The Set-AzContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="00f80-112">A környezet a bérlői, az előfizetési és a környezeti információkat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="00f80-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="00f80-113">Példák</span><span class="sxs-lookup"><span data-stu-id="00f80-113">EXAMPLES</span></span>

### <span data-ttu-id="00f80-114">Példa 1: az előfizetés környezetének beállítása</span><span class="sxs-lookup"><span data-stu-id="00f80-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="00f80-115">Ez a parancs beállítja a megadott előfizetéshez használt környezetet.</span><span class="sxs-lookup"><span data-stu-id="00f80-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="00f80-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="00f80-116">PARAMETERS</span></span>

### <span data-ttu-id="00f80-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="00f80-117">-Context</span></span>
<span data-ttu-id="00f80-118">Az aktuális munkamenet környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="00f80-118">Specifies the context for the current session.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: Context
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00f80-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00f80-119">-DefaultProfile</span></span>
<span data-ttu-id="00f80-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00f80-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00f80-121">-ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="00f80-121">-ExtendedProperty</span></span>
<span data-ttu-id="00f80-122">További környezeti tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="00f80-122">Additional context properties</span></span>

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

### <span data-ttu-id="00f80-123">-Force</span><span class="sxs-lookup"><span data-stu-id="00f80-123">-Force</span></span>
<span data-ttu-id="00f80-124">Felülírja a meglévő környezetet ugyanazzal a névvel, ha van ilyen.</span><span class="sxs-lookup"><span data-stu-id="00f80-124">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="00f80-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="00f80-125">-Name</span></span>
<span data-ttu-id="00f80-126">A környezet neve</span><span class="sxs-lookup"><span data-stu-id="00f80-126">Name of the context</span></span>

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

### <span data-ttu-id="00f80-127">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="00f80-127">-Scope</span></span>
<span data-ttu-id="00f80-128">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="00f80-128">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="00f80-129">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="00f80-129">-Subscription</span></span>
<span data-ttu-id="00f80-130">Annak az előfizetésnek a neve vagy azonosítója, amelyhez a környezetet be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="00f80-130">The name or id of the subscription that the context should be set to.</span></span> <span data-ttu-id="00f80-131">Ez a paraméter aliasokat tartalmaz a-SubscriptionName és a SubscriptionId, így az érthetőség kedvéért az előfizetések helyett a név és azonosító megadásakor is használhatók.</span><span class="sxs-lookup"><span data-stu-id="00f80-131">This parameter has aliases to -SubscriptionName and -SubscriptionId, so, for clarity, either of these can be used instead of -Subscription when specifying name and id, respectively.</span></span>

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

### <span data-ttu-id="00f80-132">-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="00f80-132">-SubscriptionObject</span></span>
<span data-ttu-id="00f80-133">Egy előfizetési objektum</span><span class="sxs-lookup"><span data-stu-id="00f80-133">A subscription object</span></span>

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

### <span data-ttu-id="00f80-134">-Bérlő</span><span class="sxs-lookup"><span data-stu-id="00f80-134">-Tenant</span></span>
<span data-ttu-id="00f80-135">Bérlő neve vagy azonosítója</span><span class="sxs-lookup"><span data-stu-id="00f80-135">Tenant name or ID</span></span>

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

### <span data-ttu-id="00f80-136">-TenantObject</span><span class="sxs-lookup"><span data-stu-id="00f80-136">-TenantObject</span></span>
<span data-ttu-id="00f80-137">Bérlői objektum</span><span class="sxs-lookup"><span data-stu-id="00f80-137">A Tenant Object</span></span>

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

### <span data-ttu-id="00f80-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="00f80-138">-Confirm</span></span>
<span data-ttu-id="00f80-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="00f80-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00f80-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00f80-140">-WhatIf</span></span>
<span data-ttu-id="00f80-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="00f80-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="00f80-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="00f80-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00f80-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00f80-143">CommonParameters</span></span>
<span data-ttu-id="00f80-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="00f80-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00f80-145">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00f80-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00f80-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="00f80-146">INPUTS</span></span>

### <span data-ttu-id="00f80-147">Microsoft. Azure. Command. profil. models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="00f80-147">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

### <span data-ttu-id="00f80-148">Microsoft. Azure. Command. profil. models. PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="00f80-148">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

### <span data-ttu-id="00f80-149">Microsoft. Azure. Command. profil. models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="00f80-149">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="00f80-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00f80-150">OUTPUTS</span></span>

### <span data-ttu-id="00f80-151">Microsoft. Azure. Command. profil. models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="00f80-151">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="00f80-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="00f80-152">NOTES</span></span>

## <span data-ttu-id="00f80-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00f80-153">RELATED LINKS</span></span>

[<span data-ttu-id="00f80-154">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="00f80-154">Get-AzContext</span></span>](./Get-AzContext.md)

