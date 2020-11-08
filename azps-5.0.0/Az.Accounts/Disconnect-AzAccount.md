---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disconnect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
ms.openlocfilehash: 23689d4e84228d4eaeaae82e2efe53b6450d44f9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193978"
---
# <span data-ttu-id="bbc14-101">Disconnect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="bbc14-101">Disconnect-AzAccount</span></span>

## <span data-ttu-id="bbc14-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bbc14-102">SYNOPSIS</span></span>
<span data-ttu-id="bbc14-103">Leválasztja a csatlakoztatott Azure-fiókot, és eltávolítja az adott fiókkal társított összes hitelesítő adatot és kontextust.</span><span class="sxs-lookup"><span data-stu-id="bbc14-103">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

## <span data-ttu-id="bbc14-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bbc14-104">SYNTAX</span></span>

### <span data-ttu-id="bbc14-105">ContextName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bbc14-105">ContextName (Default)</span></span>
```
Disconnect-AzAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbc14-106">UserId</span><span class="sxs-lookup"><span data-stu-id="bbc14-106">UserId</span></span>
```
Disconnect-AzAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbc14-107">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="bbc14-107">ServicePrincipal</span></span>
```
Disconnect-AzAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbc14-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="bbc14-108">AccountObject</span></span>
```
Disconnect-AzAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbc14-109">ContextObject</span><span class="sxs-lookup"><span data-stu-id="bbc14-109">ContextObject</span></span>
```
Disconnect-AzAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbc14-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="bbc14-110">DESCRIPTION</span></span>
<span data-ttu-id="bbc14-111">A Disconnect-AzAccount parancsmag leválasztja a csatlakoztatott Azure-fiókot, és eltávolítja az adott fiókhoz társított összes hitelesítő adatokat és kontextust (előfizetés és bérlői információk).</span><span class="sxs-lookup"><span data-stu-id="bbc14-111">The Disconnect-AzAccount cmdlet disconnects a connected Azure account and removes all credentials and contexts (subscription and tenant information) associated with that account.</span></span>
<span data-ttu-id="bbc14-112">A parancsmag végrehajtása után ismét be kell jelentkeznie a Connect-AzAccount.</span><span class="sxs-lookup"><span data-stu-id="bbc14-112">After executing this cmdlet, you will need to login again using Connect-AzAccount.</span></span>

## <span data-ttu-id="bbc14-113">Példák</span><span class="sxs-lookup"><span data-stu-id="bbc14-113">EXAMPLES</span></span>

### <span data-ttu-id="bbc14-114">1. példa: az aktuális fiók kijelentkezése</span><span class="sxs-lookup"><span data-stu-id="bbc14-114">Example 1: Logout of the current account</span></span>
```powershell
PS C:\> Disconnect-AzAccount
```

<span data-ttu-id="bbc14-115">Kijelentkezik az aktuális környezethez társított Azure-fiókból.</span><span class="sxs-lookup"><span data-stu-id="bbc14-115">Logs out of the Azure account associated with the current context.</span></span>

### <span data-ttu-id="bbc14-116">2. példa: az adott környezethez társított fiók kijelentkezése</span><span class="sxs-lookup"><span data-stu-id="bbc14-116">Example 2: Logout of the account associated with a particular context</span></span>
```powershell
PS C:\> Get-AzContext "Work" | Disconnect-AzAccount -Scope CurrentUser
```

<span data-ttu-id="bbc14-117">Kinaplózza a megadott környezethez tartozó fiókot ("munka").</span><span class="sxs-lookup"><span data-stu-id="bbc14-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="bbc14-118">Mivel ez a "CurrentUser" hatókört használja, a hitelesítő adatokat és a környezeteket véglegesen törli a rendszer.</span><span class="sxs-lookup"><span data-stu-id="bbc14-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="bbc14-119">3. példa: adott felhasználó kijelentkezése</span><span class="sxs-lookup"><span data-stu-id="bbc14-119">Example 3: Log out a particular user</span></span>
```powershell
PS C:\> Disconnect-AzAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="bbc14-120">Kiszűri a user1@contoso.org felhasználó összes hitelesítő adatait és a felhasználóhoz tartozó összes kontextust.</span><span class="sxs-lookup"><span data-stu-id="bbc14-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="bbc14-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bbc14-121">PARAMETERS</span></span>

### <span data-ttu-id="bbc14-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="bbc14-122">-ApplicationId</span></span>
<span data-ttu-id="bbc14-123">ServicePrincipal-azonosító (globálisan egyedi azonosító)</span><span class="sxs-lookup"><span data-stu-id="bbc14-123">ServicePrincipal id (globally unique id)</span></span>

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

### <span data-ttu-id="bbc14-124">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="bbc14-124">-AzureContext</span></span>
<span data-ttu-id="bbc14-125">Összefüggésben</span><span class="sxs-lookup"><span data-stu-id="bbc14-125">Context</span></span>

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

### <span data-ttu-id="bbc14-126">-ContextName</span><span class="sxs-lookup"><span data-stu-id="bbc14-126">-ContextName</span></span>
<span data-ttu-id="bbc14-127">A kijelentkezni kívánt környezet neve</span><span class="sxs-lookup"><span data-stu-id="bbc14-127">Name of the context to log out of</span></span>

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

### <span data-ttu-id="bbc14-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbc14-128">-DefaultProfile</span></span>
<span data-ttu-id="bbc14-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bbc14-129">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bbc14-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbc14-130">-InputObject</span></span>
<span data-ttu-id="bbc14-131">Az eltávolítandó fiók objektuma</span><span class="sxs-lookup"><span data-stu-id="bbc14-131">The account object to remove</span></span>

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

### <span data-ttu-id="bbc14-132">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="bbc14-132">-Scope</span></span>
<span data-ttu-id="bbc14-133">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="bbc14-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="bbc14-134">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="bbc14-134">-TenantId</span></span>
<span data-ttu-id="bbc14-135">Bérlői azonosító (globálisan egyedi azonosító)</span><span class="sxs-lookup"><span data-stu-id="bbc14-135">Tenant id (globally unique id)</span></span>

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

### <span data-ttu-id="bbc14-136">-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="bbc14-136">-Username</span></span>
<span data-ttu-id="bbc14-137">Az űrlap felhasználójának neve user@contoso.org</span><span class="sxs-lookup"><span data-stu-id="bbc14-137">User name of the form 'user@contoso.org'</span></span>

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

### <span data-ttu-id="bbc14-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bbc14-138">-Confirm</span></span>
<span data-ttu-id="bbc14-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bbc14-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbc14-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbc14-140">-WhatIf</span></span>
<span data-ttu-id="bbc14-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bbc14-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbc14-142">A parancsmag nem hajtható végre.</span><span class="sxs-lookup"><span data-stu-id="bbc14-142">The cmdlet is not executed.</span></span>

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

### <span data-ttu-id="bbc14-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbc14-143">CommonParameters</span></span>
<span data-ttu-id="bbc14-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bbc14-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbc14-145">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbc14-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbc14-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbc14-146">INPUTS</span></span>

### <span data-ttu-id="bbc14-147">Microsoft. Azure. Command. profil. models. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="bbc14-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

### <span data-ttu-id="bbc14-148">Microsoft. Azure. Command. profil. models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="bbc14-148">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="bbc14-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bbc14-149">OUTPUTS</span></span>

### <span data-ttu-id="bbc14-150">Microsoft. Azure. Command. profil. models. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="bbc14-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="bbc14-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bbc14-151">NOTES</span></span>

## <span data-ttu-id="bbc14-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bbc14-152">RELATED LINKS</span></span>
