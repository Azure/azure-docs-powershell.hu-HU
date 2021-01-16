---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disconnect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
ms.openlocfilehash: 23689d4e84228d4eaeaae82e2efe53b6450d44f9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333234"
---
# <span data-ttu-id="72d76-101">Disconnect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="72d76-101">Disconnect-AzAccount</span></span>

## <span data-ttu-id="72d76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72d76-102">SYNOPSIS</span></span>
<span data-ttu-id="72d76-103">Leválasztja a csatlakoztatott Azure-fiókot, és eltávolítja a fiókkal társított összes hitelesítő adatokat és kontextust.</span><span class="sxs-lookup"><span data-stu-id="72d76-103">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

## <span data-ttu-id="72d76-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="72d76-104">SYNTAX</span></span>

### <span data-ttu-id="72d76-105">ContextName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="72d76-105">ContextName (Default)</span></span>
```
Disconnect-AzAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72d76-106">UserId</span><span class="sxs-lookup"><span data-stu-id="72d76-106">UserId</span></span>
```
Disconnect-AzAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72d76-107">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="72d76-107">ServicePrincipal</span></span>
```
Disconnect-AzAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72d76-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="72d76-108">AccountObject</span></span>
```
Disconnect-AzAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72d76-109">ContextObject</span><span class="sxs-lookup"><span data-stu-id="72d76-109">ContextObject</span></span>
```
Disconnect-AzAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72d76-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="72d76-110">DESCRIPTION</span></span>
<span data-ttu-id="72d76-111">A Disconnect-AzAccount parancsmag leválasztja a csatlakoztatott Azure-fiókot, és eltávolítja a fiókhoz társított összes hitelesítő adatokat és kontextust (előfizetési és bérlői adatokat).</span><span class="sxs-lookup"><span data-stu-id="72d76-111">The Disconnect-AzAccount cmdlet disconnects a connected Azure account and removes all credentials and contexts (subscription and tenant information) associated with that account.</span></span>
<span data-ttu-id="72d76-112">A parancsmag végrehajtása után újból be kell jelentkeznie a Connect-AzAccount használatával.</span><span class="sxs-lookup"><span data-stu-id="72d76-112">After executing this cmdlet, you will need to login again using Connect-AzAccount.</span></span>

## <span data-ttu-id="72d76-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="72d76-113">EXAMPLES</span></span>

### <span data-ttu-id="72d76-114">1. példa: Kijelentkezés az aktuális fiókból</span><span class="sxs-lookup"><span data-stu-id="72d76-114">Example 1: Logout of the current account</span></span>
```powershell
PS C:\> Disconnect-AzAccount
```

<span data-ttu-id="72d76-115">Kijelentkezik az aktuális környezethez társított Azure-fiókból.</span><span class="sxs-lookup"><span data-stu-id="72d76-115">Logs out of the Azure account associated with the current context.</span></span>

### <span data-ttu-id="72d76-116">2. példa: Kijelentkezés egy adott környezethez társított fiókból</span><span class="sxs-lookup"><span data-stu-id="72d76-116">Example 2: Logout of the account associated with a particular context</span></span>
```powershell
PS C:\> Get-AzContext "Work" | Disconnect-AzAccount -Scope CurrentUser
```

<span data-ttu-id="72d76-117">Kijelentkezik a megadott környezethez tartozó ("Munka" nevű) fiókból.</span><span class="sxs-lookup"><span data-stu-id="72d76-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="72d76-118">Mivel ez a "CurrentUser" hatókört használja, minden hitelesítő adat és környezet véglegesen törlődik.</span><span class="sxs-lookup"><span data-stu-id="72d76-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="72d76-119">3. példa: Kijelentkezés egy adott felhasználóból</span><span class="sxs-lookup"><span data-stu-id="72d76-119">Example 3: Log out a particular user</span></span>
```powershell
PS C:\> Disconnect-AzAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="72d76-120">Kijelentkezik a " ' felhasználó – a felhasználóhoz társított összes hitelesítő adat és környezet user1@contoso.org törlődik.</span><span class="sxs-lookup"><span data-stu-id="72d76-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="72d76-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72d76-121">PARAMETERS</span></span>

### <span data-ttu-id="72d76-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="72d76-122">-ApplicationId</span></span>
<span data-ttu-id="72d76-123">ServicePrincipal id (globálisan egyedi azonosító)</span><span class="sxs-lookup"><span data-stu-id="72d76-123">ServicePrincipal id (globally unique id)</span></span>

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

### <span data-ttu-id="72d76-124">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="72d76-124">-AzureContext</span></span>
<span data-ttu-id="72d76-125">Környezet</span><span class="sxs-lookup"><span data-stu-id="72d76-125">Context</span></span>

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

### <span data-ttu-id="72d76-126">-ContextName</span><span class="sxs-lookup"><span data-stu-id="72d76-126">-ContextName</span></span>
<span data-ttu-id="72d76-127">Annak a környezetnek a neve, amelyből ki kell jelentkezni</span><span class="sxs-lookup"><span data-stu-id="72d76-127">Name of the context to log out of</span></span>

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

### <span data-ttu-id="72d76-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72d76-128">-DefaultProfile</span></span>
<span data-ttu-id="72d76-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="72d76-129">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72d76-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72d76-130">-InputObject</span></span>
<span data-ttu-id="72d76-131">Az eltávolítható fiókobjektum</span><span class="sxs-lookup"><span data-stu-id="72d76-131">The account object to remove</span></span>

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

### <span data-ttu-id="72d76-132">-Scope</span><span class="sxs-lookup"><span data-stu-id="72d76-132">-Scope</span></span>
<span data-ttu-id="72d76-133">Meghatározza a környezetváltozások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre vonatkoznak-e.</span><span class="sxs-lookup"><span data-stu-id="72d76-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="72d76-134">-TenantId</span><span class="sxs-lookup"><span data-stu-id="72d76-134">-TenantId</span></span>
<span data-ttu-id="72d76-135">Bérlőazonosító (globálisan egyedi azonosító)</span><span class="sxs-lookup"><span data-stu-id="72d76-135">Tenant id (globally unique id)</span></span>

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

### <span data-ttu-id="72d76-136">-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="72d76-136">-Username</span></span>
<span data-ttu-id="72d76-137">Az űrlap felhasználóneve ' user@contoso.org</span><span class="sxs-lookup"><span data-stu-id="72d76-137">User name of the form 'user@contoso.org'</span></span>

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

### <span data-ttu-id="72d76-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72d76-138">-Confirm</span></span>
<span data-ttu-id="72d76-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="72d76-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72d76-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72d76-140">-WhatIf</span></span>
<span data-ttu-id="72d76-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="72d76-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72d76-142">A parancsmag nem hajtódik végre.</span><span class="sxs-lookup"><span data-stu-id="72d76-142">The cmdlet is not executed.</span></span>

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

### <span data-ttu-id="72d76-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72d76-143">CommonParameters</span></span>
<span data-ttu-id="72d76-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72d76-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72d76-145">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72d76-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72d76-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="72d76-146">INPUTS</span></span>

### <span data-ttu-id="72d76-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="72d76-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

### <span data-ttu-id="72d76-148">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="72d76-148">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="72d76-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72d76-149">OUTPUTS</span></span>

### <span data-ttu-id="72d76-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="72d76-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="72d76-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="72d76-151">NOTES</span></span>

## <span data-ttu-id="72d76-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72d76-152">RELATED LINKS</span></span>
