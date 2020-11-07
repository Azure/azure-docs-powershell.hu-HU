---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
ms.openlocfilehash: e5fbecea64a15569fbd6319f3f3be5ff4102153e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680307"
---
# <span data-ttu-id="553d6-101">Disconnect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="553d6-101">Disconnect-AzureRmAccount</span></span>

## <span data-ttu-id="553d6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="553d6-102">SYNOPSIS</span></span>
<span data-ttu-id="553d6-103">Leválasztja a csatlakoztatott Azure-fiókot, és eltávolítja az adott fiókkal társított összes hitelesítő adatot és kontextust.</span><span class="sxs-lookup"><span data-stu-id="553d6-103">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="553d6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="553d6-104">SYNTAX</span></span>

### <span data-ttu-id="553d6-105">ContextName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="553d6-105">ContextName (Default)</span></span>
```
Disconnect-AzureRmAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="553d6-106">UserId</span><span class="sxs-lookup"><span data-stu-id="553d6-106">UserId</span></span>
```
Disconnect-AzureRmAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="553d6-107">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="553d6-107">ServicePrincipal</span></span>
```
Disconnect-AzureRmAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="553d6-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="553d6-108">AccountObject</span></span>
```
Disconnect-AzureRmAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="553d6-109">ContextObject</span><span class="sxs-lookup"><span data-stu-id="553d6-109">ContextObject</span></span>
```
Disconnect-AzureRmAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="553d6-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="553d6-110">DESCRIPTION</span></span>
<span data-ttu-id="553d6-111">A Disconnect-AzureRmAccount parancsmag leválasztja a csatlakoztatott Azure-fiókot, és eltávolítja az adott fiókhoz társított összes hitelesítő adatokat és kontextust (előfizetés és bérlői információk).</span><span class="sxs-lookup"><span data-stu-id="553d6-111">The Disconnect-AzureRmAccount cmdlet disconnects a connected Azure account and removes all credentials and contexts (subscription and tenant information) associated with that account.</span></span>
<span data-ttu-id="553d6-112">A parancsmag végrehajtása után ismét be kell jelentkeznie a Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="553d6-112">After executing this cmdlet, you will need to login again using Connect-AzureRmAccount.</span></span>

## <span data-ttu-id="553d6-113">Példák</span><span class="sxs-lookup"><span data-stu-id="553d6-113">EXAMPLES</span></span>

### <span data-ttu-id="553d6-114">Az aktuális fiók kijelentkezése</span><span class="sxs-lookup"><span data-stu-id="553d6-114">Logout of the current account</span></span>
```
PS C:\> Disconnect-AzureRmAccount
```

<span data-ttu-id="553d6-115">Kijelentkezik az aktuális környezethez társított Azure-fiókból.</span><span class="sxs-lookup"><span data-stu-id="553d6-115">Logs out of the Azure account associated with the current context.</span></span>

### <span data-ttu-id="553d6-116">Egy adott környezethez társított fiók kijelentkezése</span><span class="sxs-lookup"><span data-stu-id="553d6-116">Logout of the account associated with a particular context</span></span>
```
PS C:\> Get-AzureRmContext "Work" | Disconnect-AzureRmAccount -Scope CurrentUser
```

<span data-ttu-id="553d6-117">Kinaplózza a megadott környezethez tartozó fiókot ("munka").</span><span class="sxs-lookup"><span data-stu-id="553d6-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="553d6-118">Mivel ez a "CurrentUser" hatókört használja, a hitelesítő adatokat és a környezeteket véglegesen törli a rendszer.</span><span class="sxs-lookup"><span data-stu-id="553d6-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="553d6-119">Adott felhasználó kijelentkezése</span><span class="sxs-lookup"><span data-stu-id="553d6-119">Log out a particular user</span></span>
```
PS C:\> Disconnect-AzureRmAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="553d6-120">Kiszűri a user1@contoso.org felhasználó összes hitelesítő adatait és a felhasználóhoz tartozó összes kontextust.</span><span class="sxs-lookup"><span data-stu-id="553d6-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="553d6-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="553d6-121">PARAMETERS</span></span>

### <span data-ttu-id="553d6-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="553d6-122">-ApplicationId</span></span>
<span data-ttu-id="553d6-123">ServicePrincipal-azonosító (globálisan egyedi azonosító)</span><span class="sxs-lookup"><span data-stu-id="553d6-123">ServicePrincipal id (globally unique id)</span></span>

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

### <span data-ttu-id="553d6-124">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="553d6-124">-AzureContext</span></span>
<span data-ttu-id="553d6-125">Összefüggésben</span><span class="sxs-lookup"><span data-stu-id="553d6-125">Context</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: ContextObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="553d6-126">-ContextName</span><span class="sxs-lookup"><span data-stu-id="553d6-126">-ContextName</span></span>
<span data-ttu-id="553d6-127">A kijelentkezni kívánt környezet neve</span><span class="sxs-lookup"><span data-stu-id="553d6-127">Name of the context to log out of</span></span>

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

### <span data-ttu-id="553d6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="553d6-128">-DefaultProfile</span></span>
<span data-ttu-id="553d6-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="553d6-129">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="553d6-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="553d6-130">-InputObject</span></span>
<span data-ttu-id="553d6-131">Az eltávolítandó fiók objektuma</span><span class="sxs-lookup"><span data-stu-id="553d6-131">The account object to remove</span></span>

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

### <span data-ttu-id="553d6-132">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="553d6-132">-Scope</span></span>
<span data-ttu-id="553d6-133">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="553d6-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="553d6-134">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="553d6-134">-TenantId</span></span>
<span data-ttu-id="553d6-135">Bérlői azonosító (globálisan egyedi azonosító)</span><span class="sxs-lookup"><span data-stu-id="553d6-135">Tenant id (globally unique id)</span></span>

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

### <span data-ttu-id="553d6-136">-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="553d6-136">-Username</span></span>
<span data-ttu-id="553d6-137">Az űrlap felhasználójának neve user@contoso.org</span><span class="sxs-lookup"><span data-stu-id="553d6-137">User name of the form 'user@contoso.org'</span></span>

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

### <span data-ttu-id="553d6-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="553d6-138">-Confirm</span></span>
<span data-ttu-id="553d6-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="553d6-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="553d6-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="553d6-140">-WhatIf</span></span>
<span data-ttu-id="553d6-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="553d6-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="553d6-142">A parancsmag nem hajtható végre.</span><span class="sxs-lookup"><span data-stu-id="553d6-142">The cmdlet is not executed.</span></span>

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

### <span data-ttu-id="553d6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="553d6-143">CommonParameters</span></span>
<span data-ttu-id="553d6-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="553d6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="553d6-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="553d6-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="553d6-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="553d6-146">INPUTS</span></span>

### <span data-ttu-id="553d6-147">Microsoft. Azure. Command. profil. models. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="553d6-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>
<span data-ttu-id="553d6-148">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="553d6-148">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="553d6-149">Microsoft. Azure. Command. profil. models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="553d6-149">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>
<span data-ttu-id="553d6-150">Paraméterek: AzureContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="553d6-150">Parameters: AzureContext (ByValue)</span></span>

## <span data-ttu-id="553d6-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="553d6-151">OUTPUTS</span></span>

### <span data-ttu-id="553d6-152">Microsoft. Azure. Command. profil. models. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="553d6-152">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="553d6-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="553d6-153">NOTES</span></span>

## <span data-ttu-id="553d6-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="553d6-154">RELATED LINKS</span></span>
