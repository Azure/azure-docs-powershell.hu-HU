---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disconnect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
ms.openlocfilehash: 23689d4e84228d4eaeaae82e2efe53b6450d44f9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145362"
---
# <span data-ttu-id="09120-101">Disconnect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="09120-101">Disconnect-AzAccount</span></span>

## <span data-ttu-id="09120-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09120-102">SYNOPSIS</span></span>
<span data-ttu-id="09120-103">Leválasztja a csatlakoztatott Azure-fiókot, és eltávolítja a fiókkal társított összes hitelesítő adatokat és kontextust.</span><span class="sxs-lookup"><span data-stu-id="09120-103">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

## <span data-ttu-id="09120-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="09120-104">SYNTAX</span></span>

### <span data-ttu-id="09120-105">ContextName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="09120-105">ContextName (Default)</span></span>
```
Disconnect-AzAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09120-106">UserId</span><span class="sxs-lookup"><span data-stu-id="09120-106">UserId</span></span>
```
Disconnect-AzAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09120-107">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="09120-107">ServicePrincipal</span></span>
```
Disconnect-AzAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09120-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="09120-108">AccountObject</span></span>
```
Disconnect-AzAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09120-109">ContextObject</span><span class="sxs-lookup"><span data-stu-id="09120-109">ContextObject</span></span>
```
Disconnect-AzAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09120-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="09120-110">DESCRIPTION</span></span>
<span data-ttu-id="09120-111">A Disconnect-AzAccount parancsmag leválasztja a csatlakoztatott Azure-fiókot, és eltávolítja a fiókhoz társított összes hitelesítő adatokat és kontextust (előfizetési és bérlői adatokat).</span><span class="sxs-lookup"><span data-stu-id="09120-111">The Disconnect-AzAccount cmdlet disconnects a connected Azure account and removes all credentials and contexts (subscription and tenant information) associated with that account.</span></span>
<span data-ttu-id="09120-112">A parancsmag végrehajtása után újból be kell jelentkeznie a Connect-AzAccount használatával.</span><span class="sxs-lookup"><span data-stu-id="09120-112">After executing this cmdlet, you will need to login again using Connect-AzAccount.</span></span>

## <span data-ttu-id="09120-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="09120-113">EXAMPLES</span></span>

### <span data-ttu-id="09120-114">1. példa: Kijelentkezés az aktuális fiókból</span><span class="sxs-lookup"><span data-stu-id="09120-114">Example 1: Logout of the current account</span></span>
```powershell
PS C:\> Disconnect-AzAccount
```

<span data-ttu-id="09120-115">Kijelentkezik az aktuális környezethez társított Azure-fiókból.</span><span class="sxs-lookup"><span data-stu-id="09120-115">Logs out of the Azure account associated with the current context.</span></span>

### <span data-ttu-id="09120-116">2. példa: Kijelentkezés egy adott környezethez társított fiókból</span><span class="sxs-lookup"><span data-stu-id="09120-116">Example 2: Logout of the account associated with a particular context</span></span>
```powershell
PS C:\> Get-AzContext "Work" | Disconnect-AzAccount -Scope CurrentUser
```

<span data-ttu-id="09120-117">Kijelentkezik a megadott környezethez tartozó ("Munka" nevű) fiókból.</span><span class="sxs-lookup"><span data-stu-id="09120-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="09120-118">Mivel ez a "CurrentUser" hatókört használja, minden hitelesítő adat és környezet véglegesen törlődik.</span><span class="sxs-lookup"><span data-stu-id="09120-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="09120-119">3. példa: Kijelentkezés egy adott felhasználóból</span><span class="sxs-lookup"><span data-stu-id="09120-119">Example 3: Log out a particular user</span></span>
```powershell
PS C:\> Disconnect-AzAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="09120-120">Kijelentkezik a " ' felhasználó – a felhasználóhoz társított összes hitelesítő adat és környezet user1@contoso.org törlődik.</span><span class="sxs-lookup"><span data-stu-id="09120-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="09120-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09120-121">PARAMETERS</span></span>

### <span data-ttu-id="09120-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="09120-122">-ApplicationId</span></span>
<span data-ttu-id="09120-123">ServicePrincipal id (globálisan egyedi azonosító)</span><span class="sxs-lookup"><span data-stu-id="09120-123">ServicePrincipal id (globally unique id)</span></span>

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

### <span data-ttu-id="09120-124">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="09120-124">-AzureContext</span></span>
<span data-ttu-id="09120-125">Környezet</span><span class="sxs-lookup"><span data-stu-id="09120-125">Context</span></span>

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

### <span data-ttu-id="09120-126">-ContextName</span><span class="sxs-lookup"><span data-stu-id="09120-126">-ContextName</span></span>
<span data-ttu-id="09120-127">Annak a környezetnek a neve, amelyből ki kell jelentkezni</span><span class="sxs-lookup"><span data-stu-id="09120-127">Name of the context to log out of</span></span>

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

### <span data-ttu-id="09120-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09120-128">-DefaultProfile</span></span>
<span data-ttu-id="09120-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="09120-129">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09120-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09120-130">-InputObject</span></span>
<span data-ttu-id="09120-131">Az eltávolítható fiókobjektum</span><span class="sxs-lookup"><span data-stu-id="09120-131">The account object to remove</span></span>

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

### <span data-ttu-id="09120-132">-Scope</span><span class="sxs-lookup"><span data-stu-id="09120-132">-Scope</span></span>
<span data-ttu-id="09120-133">Meghatározza a környezetváltozások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre vonatkoznak-e.</span><span class="sxs-lookup"><span data-stu-id="09120-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="09120-134">-TenantId</span><span class="sxs-lookup"><span data-stu-id="09120-134">-TenantId</span></span>
<span data-ttu-id="09120-135">Bérlőazonosító (globálisan egyedi azonosító)</span><span class="sxs-lookup"><span data-stu-id="09120-135">Tenant id (globally unique id)</span></span>

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

### <span data-ttu-id="09120-136">-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="09120-136">-Username</span></span>
<span data-ttu-id="09120-137">Az űrlap felhasználóneve ' user@contoso.org</span><span class="sxs-lookup"><span data-stu-id="09120-137">User name of the form 'user@contoso.org'</span></span>

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

### <span data-ttu-id="09120-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09120-138">-Confirm</span></span>
<span data-ttu-id="09120-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="09120-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09120-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09120-140">-WhatIf</span></span>
<span data-ttu-id="09120-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="09120-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09120-142">A parancsmag nem hajtódik végre.</span><span class="sxs-lookup"><span data-stu-id="09120-142">The cmdlet is not executed.</span></span>

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

### <span data-ttu-id="09120-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09120-143">CommonParameters</span></span>
<span data-ttu-id="09120-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09120-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09120-145">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09120-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09120-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="09120-146">INPUTS</span></span>

### <span data-ttu-id="09120-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="09120-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

### <span data-ttu-id="09120-148">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="09120-148">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="09120-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09120-149">OUTPUTS</span></span>

### <span data-ttu-id="09120-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="09120-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="09120-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="09120-151">NOTES</span></span>

## <span data-ttu-id="09120-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09120-152">RELATED LINKS</span></span>
