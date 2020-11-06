---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmAccount.md
ms.openlocfilehash: d1b401c1ae806d48b9cb9969c36ef72d104076eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496951"
---
# <span data-ttu-id="341aa-101">Remove-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="341aa-101">Remove-AzureRmAccount</span></span>

## <span data-ttu-id="341aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="341aa-102">SYNOPSIS</span></span>
<span data-ttu-id="341aa-103">Az adott fiókkal társított összes hitelesítő adat és környezet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="341aa-103">Remove all credentials and contexts associated with the given account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="341aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="341aa-104">SYNTAX</span></span>

### <span data-ttu-id="341aa-105">ContextName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="341aa-105">ContextName (Default)</span></span>
```
Remove-AzureRmAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="341aa-106">UserId</span><span class="sxs-lookup"><span data-stu-id="341aa-106">UserId</span></span>
```
Remove-AzureRmAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="341aa-107">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="341aa-107">ServicePrincipal</span></span>
```
Remove-AzureRmAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="341aa-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="341aa-108">AccountObject</span></span>
```
Remove-AzureRmAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="341aa-109">ContextObject</span><span class="sxs-lookup"><span data-stu-id="341aa-109">ContextObject</span></span>
```
Remove-AzureRmAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="341aa-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="341aa-110">DESCRIPTION</span></span>
<span data-ttu-id="341aa-111">Az adott fiókhoz társított összes hitelesítő adat és környezet (előfizetés és bérlői információ) eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="341aa-111">Remove all credentials, and contexts (subscription and tenant information) associated with the given account.</span></span>  <span data-ttu-id="341aa-112">A parancsmag végrehajtása után ismét be kell jelentkeznie a Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="341aa-112">After executing this cmdlet, you will need to login again using Add-AzureRmAccount</span></span>

## <span data-ttu-id="341aa-113">Példák</span><span class="sxs-lookup"><span data-stu-id="341aa-113">EXAMPLES</span></span>

### <span data-ttu-id="341aa-114">Az curent-fiók kijelentkezése</span><span class="sxs-lookup"><span data-stu-id="341aa-114">Log out the curent account</span></span>
```
PS C:\> Remove-AzureRmAccount
```

<span data-ttu-id="341aa-115">Az aktuális környezethez társított fiók kinaplózása.</span><span class="sxs-lookup"><span data-stu-id="341aa-115">Logs out the account associated with the current context.</span></span>

### <span data-ttu-id="341aa-116">Az adott környezethez társított fiók kijelentkezése</span><span class="sxs-lookup"><span data-stu-id="341aa-116">Log out the account associated with a particular context</span></span>
```
PS C:\> Get-AzureRmContext "Work" | Remove-AzureRmAccount -Scope CurrentUser
```

<span data-ttu-id="341aa-117">Kinaplózza a megadott környezethez tartozó fiókot ("munka").</span><span class="sxs-lookup"><span data-stu-id="341aa-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="341aa-118">Mivel ez a "CurrentUser" hatókört használja, a hitelesítő adatokat és a környezeteket véglegesen törli a rendszer.</span><span class="sxs-lookup"><span data-stu-id="341aa-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="341aa-119">Adott felhasználó kijelentkezése</span><span class="sxs-lookup"><span data-stu-id="341aa-119">Log out a particular user</span></span>
```
PS C:\> Remove-AzureRmAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="341aa-120">Kiszűri a user1@contoso.org felhasználó összes hitelesítő adatait és a felhasználóhoz tartozó összes kontextust.</span><span class="sxs-lookup"><span data-stu-id="341aa-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="341aa-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="341aa-121">PARAMETERS</span></span>

### <span data-ttu-id="341aa-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="341aa-122">-ApplicationId</span></span>
<span data-ttu-id="341aa-123">ServicePrincipal-azonosító (globálisan egyedi azonosító)</span><span class="sxs-lookup"><span data-stu-id="341aa-123">ServicePrincipal id (globally unique id)</span></span>

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

### <span data-ttu-id="341aa-124">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="341aa-124">-AzureContext</span></span>
<span data-ttu-id="341aa-125">Összefüggésben</span><span class="sxs-lookup"><span data-stu-id="341aa-125">Context</span></span>

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

### <span data-ttu-id="341aa-126">-ContextName</span><span class="sxs-lookup"><span data-stu-id="341aa-126">-ContextName</span></span>
<span data-ttu-id="341aa-127">A kijelentkezni kívánt környezet neve</span><span class="sxs-lookup"><span data-stu-id="341aa-127">Name of the context to log out of</span></span>

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

### <span data-ttu-id="341aa-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="341aa-128">-DefaultProfile</span></span>
<span data-ttu-id="341aa-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="341aa-129">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="341aa-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="341aa-130">-InputObject</span></span>
<span data-ttu-id="341aa-131">Az eltávolítandó fiók objektuma</span><span class="sxs-lookup"><span data-stu-id="341aa-131">The account object to remove</span></span>

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

### <span data-ttu-id="341aa-132">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="341aa-132">-Scope</span></span>
<span data-ttu-id="341aa-133">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="341aa-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="341aa-134">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="341aa-134">-TenantId</span></span>
<span data-ttu-id="341aa-135">Bérlői azonosító (globálisan egyedi azonosító)</span><span class="sxs-lookup"><span data-stu-id="341aa-135">Tenant id (globally unique id)</span></span>

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

### <span data-ttu-id="341aa-136">-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="341aa-136">-Username</span></span>
<span data-ttu-id="341aa-137">Az űrlap felhasználójának neve user@contoso.org</span><span class="sxs-lookup"><span data-stu-id="341aa-137">User name of the form 'user@contoso.org'</span></span>

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

### <span data-ttu-id="341aa-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="341aa-138">-Confirm</span></span>
<span data-ttu-id="341aa-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="341aa-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="341aa-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="341aa-140">-WhatIf</span></span>
<span data-ttu-id="341aa-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="341aa-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="341aa-142">A parancsmag nem hajtható végre.</span><span class="sxs-lookup"><span data-stu-id="341aa-142">The cmdlet is not executed.</span></span>

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

### <span data-ttu-id="341aa-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="341aa-143">CommonParameters</span></span>
<span data-ttu-id="341aa-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="341aa-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="341aa-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="341aa-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="341aa-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="341aa-146">INPUTS</span></span>

### <span data-ttu-id="341aa-147">Microsoft. Azure. Command. profil. models. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="341aa-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

### <span data-ttu-id="341aa-148">Microsoft. Azure. Command. profil. models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="341aa-148">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="341aa-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="341aa-149">OUTPUTS</span></span>

### <span data-ttu-id="341aa-150">Microsoft. Azure. Command. profil. models. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="341aa-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="341aa-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="341aa-151">NOTES</span></span>

## <span data-ttu-id="341aa-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="341aa-152">RELATED LINKS</span></span>

