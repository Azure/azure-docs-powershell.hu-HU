---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disconnect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
ms.openlocfilehash: a55844251e7d84ef24d62195b96b9bd4c3934317
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668268"
---
# <span data-ttu-id="7afdf-101">Disconnect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="7afdf-101">Disconnect-AzAccount</span></span>

## <span data-ttu-id="7afdf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7afdf-102">SYNOPSIS</span></span>
<span data-ttu-id="7afdf-103">Leválasztja a csatlakoztatott Azure-fiókot, és eltávolítja az adott fiókkal társított összes hitelesítő adatot és kontextust.</span><span class="sxs-lookup"><span data-stu-id="7afdf-103">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

## <span data-ttu-id="7afdf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7afdf-104">SYNTAX</span></span>

### <span data-ttu-id="7afdf-105">ContextName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7afdf-105">ContextName (Default)</span></span>
```
Disconnect-AzAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7afdf-106">UserId</span><span class="sxs-lookup"><span data-stu-id="7afdf-106">UserId</span></span>
```
Disconnect-AzAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7afdf-107">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7afdf-107">ServicePrincipal</span></span>
```
Disconnect-AzAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7afdf-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="7afdf-108">AccountObject</span></span>
```
Disconnect-AzAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7afdf-109">ContextObject</span><span class="sxs-lookup"><span data-stu-id="7afdf-109">ContextObject</span></span>
```
Disconnect-AzAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7afdf-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="7afdf-110">DESCRIPTION</span></span>
<span data-ttu-id="7afdf-111">A Disconnect-AzAccount parancsmag leválasztja a csatlakoztatott Azure-fiókot, és eltávolítja az adott fiókhoz társított összes hitelesítő adatokat és kontextust (előfizetés és bérlői információk).</span><span class="sxs-lookup"><span data-stu-id="7afdf-111">The Disconnect-AzAccount cmdlet disconnects a connected Azure account and removes all credentials and contexts (subscription and tenant information) associated with that account.</span></span>
<span data-ttu-id="7afdf-112">A parancsmag végrehajtása után ismét be kell jelentkeznie a Connect-AzAccount.</span><span class="sxs-lookup"><span data-stu-id="7afdf-112">After executing this cmdlet, you will need to login again using Connect-AzAccount.</span></span>

## <span data-ttu-id="7afdf-113">Példák</span><span class="sxs-lookup"><span data-stu-id="7afdf-113">EXAMPLES</span></span>

### <span data-ttu-id="7afdf-114">Az aktuális fiók kijelentkezése</span><span class="sxs-lookup"><span data-stu-id="7afdf-114">Logout of the current account</span></span>
```
PS C:\> Disconnect-AzAccount
```

<span data-ttu-id="7afdf-115">Kijelentkezik az aktuális környezethez társított Azure-fiókból.</span><span class="sxs-lookup"><span data-stu-id="7afdf-115">Logs out of the Azure account associated with the current context.</span></span>

### <span data-ttu-id="7afdf-116">Egy adott környezethez társított fiók kijelentkezése</span><span class="sxs-lookup"><span data-stu-id="7afdf-116">Logout of the account associated with a particular context</span></span>
```
PS C:\> Get-AzContext "Work" | Disconnect-AzAccount -Scope CurrentUser
```

<span data-ttu-id="7afdf-117">Kinaplózza a megadott környezethez tartozó fiókot ("munka").</span><span class="sxs-lookup"><span data-stu-id="7afdf-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="7afdf-118">Mivel ez a "CurrentUser" hatókört használja, a hitelesítő adatokat és a környezeteket véglegesen törli a rendszer.</span><span class="sxs-lookup"><span data-stu-id="7afdf-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="7afdf-119">Adott felhasználó kijelentkezése</span><span class="sxs-lookup"><span data-stu-id="7afdf-119">Log out a particular user</span></span>
```
PS C:\> Disconnect-AzAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="7afdf-120">Kiszűri a user1@contoso.org felhasználó összes hitelesítő adatait és a felhasználóhoz tartozó összes kontextust.</span><span class="sxs-lookup"><span data-stu-id="7afdf-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="7afdf-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7afdf-121">PARAMETERS</span></span>

### <span data-ttu-id="7afdf-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7afdf-122">-ApplicationId</span></span>
<span data-ttu-id="7afdf-123">ServicePrincipal-azonosító (globálisan egyedi azonosító)</span><span class="sxs-lookup"><span data-stu-id="7afdf-123">ServicePrincipal id (globally unique id)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipal
Aliases: SPN, ServicePrincipal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7afdf-124">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="7afdf-124">-AzureContext</span></span>
<span data-ttu-id="7afdf-125">Összefüggésben</span><span class="sxs-lookup"><span data-stu-id="7afdf-125">Context</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: ContextObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7afdf-126">-ContextName</span><span class="sxs-lookup"><span data-stu-id="7afdf-126">-ContextName</span></span>
<span data-ttu-id="7afdf-127">A kijelentkezni kívánt környezet neve</span><span class="sxs-lookup"><span data-stu-id="7afdf-127">Name of the context to log out of</span></span>

```yaml
Type: System.String
Parameter Sets: ContextName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7afdf-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7afdf-128">-DefaultProfile</span></span>
<span data-ttu-id="7afdf-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7afdf-129">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7afdf-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7afdf-130">-InputObject</span></span>
<span data-ttu-id="7afdf-131">Az eltávolítandó fiók objektuma</span><span class="sxs-lookup"><span data-stu-id="7afdf-131">The account object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7afdf-132">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="7afdf-132">-Scope</span></span>
<span data-ttu-id="7afdf-133">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="7afdf-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="7afdf-134">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="7afdf-134">-TenantId</span></span>
<span data-ttu-id="7afdf-135">Bérlői azonosító (globálisan egyedi azonosító)</span><span class="sxs-lookup"><span data-stu-id="7afdf-135">Tenant id (globally unique id)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipal
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7afdf-136">-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="7afdf-136">-Username</span></span>
<span data-ttu-id="7afdf-137">Az űrlap felhasználójának neve user@contoso.org</span><span class="sxs-lookup"><span data-stu-id="7afdf-137">User name of the form 'user@contoso.org'</span></span>

```yaml
Type: System.String
Parameter Sets: UserId
Aliases: Id, UserId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7afdf-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7afdf-138">-Confirm</span></span>
<span data-ttu-id="7afdf-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7afdf-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7afdf-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7afdf-140">-WhatIf</span></span>
<span data-ttu-id="7afdf-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7afdf-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7afdf-142">A parancsmag nem hajtható végre.</span><span class="sxs-lookup"><span data-stu-id="7afdf-142">The cmdlet is not executed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7afdf-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7afdf-143">CommonParameters</span></span>
<span data-ttu-id="7afdf-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7afdf-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7afdf-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7afdf-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7afdf-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7afdf-146">INPUTS</span></span>

### <span data-ttu-id="7afdf-147">Microsoft. Azure. Command. profil. models. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="7afdf-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

### <span data-ttu-id="7afdf-148">Microsoft. Azure. Command. profil. models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="7afdf-148">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="7afdf-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7afdf-149">OUTPUTS</span></span>

### <span data-ttu-id="7afdf-150">Microsoft. Azure. Command. profil. models. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="7afdf-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="7afdf-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7afdf-151">NOTES</span></span>

## <span data-ttu-id="7afdf-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7afdf-152">RELATED LINKS</span></span>
