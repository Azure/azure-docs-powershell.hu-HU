---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
ms.openlocfilehash: 49805dee2bff967da294fda228b5426e2652e209
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145354"
---
# <span data-ttu-id="d858c-101">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="d858c-101">Set-AzContext</span></span>

## <span data-ttu-id="d858c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d858c-102">SYNOPSIS</span></span>
<span data-ttu-id="d858c-103">Beállítja a parancsmagok aktuális munkamenetben használt bérlői, előfizetési és környezetét.</span><span class="sxs-lookup"><span data-stu-id="d858c-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

## <span data-ttu-id="d858c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d858c-104">SYNTAX</span></span>

### <span data-ttu-id="d858c-105">Környezet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d858c-105">Context (Default)</span></span>
```
Set-AzContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d858c-106">TenantObject</span><span class="sxs-lookup"><span data-stu-id="d858c-106">TenantObject</span></span>
```
Set-AzContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d858c-107">SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="d858c-107">SubscriptionObject</span></span>
```
Set-AzContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d858c-108">Előfizetés</span><span class="sxs-lookup"><span data-stu-id="d858c-108">Subscription</span></span>
```
Set-AzContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d858c-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="d858c-109">TenantNameOnly</span></span>
```
Set-AzContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d858c-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d858c-110">DESCRIPTION</span></span>
<span data-ttu-id="d858c-111">A Set-AzContext parancsmag beállítja az aktuális munkamenetben futtatott parancsmagok hitelesítési adatait.</span><span class="sxs-lookup"><span data-stu-id="d858c-111">The Set-AzContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="d858c-112">A környezet bérlői, előfizetési és környezeti információkat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="d858c-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="d858c-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d858c-113">EXAMPLES</span></span>

### <span data-ttu-id="d858c-114">1. példa: Az előfizetés környezetének beállítása</span><span class="sxs-lookup"><span data-stu-id="d858c-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzContext -Subscription "xxxx-xxxx-xxxx-xxxx"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="d858c-115">Ez a parancs beállítja a környezetét a megadott előfizetés használatára.</span><span class="sxs-lookup"><span data-stu-id="d858c-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="d858c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d858c-116">PARAMETERS</span></span>

### <span data-ttu-id="d858c-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="d858c-117">-Context</span></span>
<span data-ttu-id="d858c-118">Az aktuális munkamenet környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="d858c-118">Specifies the context for the current session.</span></span>

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

### <span data-ttu-id="d858c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d858c-119">-DefaultProfile</span></span>
<span data-ttu-id="d858c-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d858c-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d858c-121">-ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="d858c-121">-ExtendedProperty</span></span>
<span data-ttu-id="d858c-122">További környezettulajdonságok</span><span class="sxs-lookup"><span data-stu-id="d858c-122">Additional context properties</span></span>

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

### <span data-ttu-id="d858c-123">-Force</span><span class="sxs-lookup"><span data-stu-id="d858c-123">-Force</span></span>
<span data-ttu-id="d858c-124">Ha van ilyen, felülírja a meglévő környezetét ugyanazokkal a névvel.</span><span class="sxs-lookup"><span data-stu-id="d858c-124">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="d858c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d858c-125">-Name</span></span>
<span data-ttu-id="d858c-126">A környezet neve</span><span class="sxs-lookup"><span data-stu-id="d858c-126">Name of the context</span></span>

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

### <span data-ttu-id="d858c-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="d858c-127">-Scope</span></span>
<span data-ttu-id="d858c-128">Meghatározza a környezetváltozások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre vonatkoznak-e.</span><span class="sxs-lookup"><span data-stu-id="d858c-128">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="d858c-129">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="d858c-129">-Subscription</span></span>
<span data-ttu-id="d858c-130">Annak az előfizetésnek a neve vagy azonosítója, amelybe be kell állítani a kontextust.</span><span class="sxs-lookup"><span data-stu-id="d858c-130">The name or id of the subscription that the context should be set to.</span></span> <span data-ttu-id="d858c-131">Ez a paraméter -SubscriptionName és -SubscriptionId aliasokkal rendelkezik, így az átláthatóság érdekében ezek bármelyike használható a -Subscription helyett a név és az azonosító megadásakor.</span><span class="sxs-lookup"><span data-stu-id="d858c-131">This parameter has aliases to -SubscriptionName and -SubscriptionId, so, for clarity, either of these can be used instead of -Subscription when specifying name and id, respectively.</span></span>

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

### <span data-ttu-id="d858c-132">-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="d858c-132">-SubscriptionObject</span></span>
<span data-ttu-id="d858c-133">Előfizetési objektum</span><span class="sxs-lookup"><span data-stu-id="d858c-133">A subscription object</span></span>

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

### <span data-ttu-id="d858c-134">-Tenant</span><span class="sxs-lookup"><span data-stu-id="d858c-134">-Tenant</span></span>
<span data-ttu-id="d858c-135">Bérlő neve vagy azonosítója</span><span class="sxs-lookup"><span data-stu-id="d858c-135">Tenant name or ID</span></span>

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

### <span data-ttu-id="d858c-136">-TenantObject</span><span class="sxs-lookup"><span data-stu-id="d858c-136">-TenantObject</span></span>
<span data-ttu-id="d858c-137">Bérlői objektum</span><span class="sxs-lookup"><span data-stu-id="d858c-137">A Tenant Object</span></span>

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

### <span data-ttu-id="d858c-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d858c-138">-Confirm</span></span>
<span data-ttu-id="d858c-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d858c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d858c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d858c-140">-WhatIf</span></span>
<span data-ttu-id="d858c-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d858c-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d858c-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d858c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d858c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d858c-143">CommonParameters</span></span>
<span data-ttu-id="d858c-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d858c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d858c-145">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d858c-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d858c-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d858c-146">INPUTS</span></span>

### <span data-ttu-id="d858c-147">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="d858c-147">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

### <span data-ttu-id="d858c-148">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="d858c-148">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

### <span data-ttu-id="d858c-149">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="d858c-149">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="d858c-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d858c-150">OUTPUTS</span></span>

### <span data-ttu-id="d858c-151">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="d858c-151">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="d858c-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d858c-152">NOTES</span></span>

## <span data-ttu-id="d858c-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d858c-153">RELATED LINKS</span></span>

[<span data-ttu-id="d858c-154">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="d858c-154">Get-AzContext</span></span>](./Get-AzContext.md)

