---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermaduser
schema: 2.0.0
ms.openlocfilehash: 51758c5b51c358a60be310405a89666cc56bac2e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848385"
---
# <span data-ttu-id="9c2be-101">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="9c2be-101">Remove-AzureRmADUser</span></span>

## <span data-ttu-id="9c2be-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9c2be-102">SYNOPSIS</span></span>
<span data-ttu-id="9c2be-103">Active Directory-felhasználó törlése</span><span class="sxs-lookup"><span data-stu-id="9c2be-103">Deletes an active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c2be-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9c2be-104">SYNTAX</span></span>

### <span data-ttu-id="9c2be-105">UPNOrObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9c2be-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c2be-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c2be-106">UPNParameterSet</span></span>
```
Remove-AzureRmADUser -UserPrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c2be-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c2be-107">ObjectIdParameterSet</span></span>
```
Remove-AzureRmADUser -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c2be-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c2be-108">DisplayNameParameterSet</span></span>
```
Remove-AzureRmADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c2be-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c2be-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c2be-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="9c2be-110">DESCRIPTION</span></span>
<span data-ttu-id="9c2be-111">Egy Active Directory-felhasználó törlése (munkahelyi/iskolai fiók is ismert a szervezeti azonosító néven ismert).</span><span class="sxs-lookup"><span data-stu-id="9c2be-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="9c2be-112">Példák</span><span class="sxs-lookup"><span data-stu-id="9c2be-112">EXAMPLES</span></span>

### <span data-ttu-id="9c2be-113">Példa 1 – felhasználó eltávolítása a felhasználó egyszerű nevével</span><span class="sxs-lookup"><span data-stu-id="9c2be-113">Example 1 - Remove a user by user principal name</span></span>

```
PS C:\> Remove-AzureRmADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="9c2be-114">A felhasználó eltávolítása a "" "nevű felhasználó nevéből foo@domain.com a bérlői webhelyről.</span><span class="sxs-lookup"><span data-stu-id="9c2be-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="9c2be-115">2. példa – egy felhasználó objektum-azonosítóval való eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9c2be-115">Example 2 - Remove a user by object id</span></span>

```
PS C:\> Remove-AzureRmADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="9c2be-116">Eltávolítja az "7a9582cf-88c4-4319-842b-7a5d60967a69" azonosítójú felhasználót a bérlői webhelyről.</span><span class="sxs-lookup"><span data-stu-id="9c2be-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="9c2be-117">3 példa – felhasználó eltávolítása csővezetékről</span><span class="sxs-lookup"><span data-stu-id="9c2be-117">Example 3 - Remove a user by piping</span></span>

```
PS C:\> Get-AzureRmADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzureRmADUser
```

<span data-ttu-id="9c2be-118">A felhasználót a "7a9582cf-88c4-4319-842b-7a5d60967a69" azonosítójú objektummal, a Remove-AzureRmADUser parancsmagot tartalmazó csövekkel pedig eltávolítja a felhasználót a bérlői fiókból.</span><span class="sxs-lookup"><span data-stu-id="9c2be-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzureRmADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="9c2be-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9c2be-119">PARAMETERS</span></span>

### <span data-ttu-id="9c2be-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c2be-120">-DefaultProfile</span></span>
<span data-ttu-id="9c2be-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9c2be-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c2be-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9c2be-122">-DisplayName</span></span>
<span data-ttu-id="9c2be-123">A törlendő felhasználó megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="9c2be-123">The display name of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c2be-124">-Force</span><span class="sxs-lookup"><span data-stu-id="9c2be-124">-Force</span></span>
<span data-ttu-id="9c2be-125">Ha meg van adva, nem kér megerősítést a felhasználó törléséhez.</span><span class="sxs-lookup"><span data-stu-id="9c2be-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="9c2be-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c2be-126">-InputObject</span></span>
<span data-ttu-id="9c2be-127">A törlendő felhasználói objektum.</span><span class="sxs-lookup"><span data-stu-id="9c2be-127">The user object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c2be-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="9c2be-128">-ObjectId</span></span>
<span data-ttu-id="9c2be-129">A törlendő felhasználó objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9c2be-129">The object id of the user to be deleted.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c2be-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c2be-130">-PassThru</span></span>
<span data-ttu-id="9c2be-131">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="9c2be-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="9c2be-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="9c2be-132">-UPNOrObjectId</span></span>
<span data-ttu-id="9c2be-133">A törölni kívánt felhasználó egyszerű felhasználónevét vagy objectId.</span><span class="sxs-lookup"><span data-stu-id="9c2be-133">The user principal name or the objectId of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNOrObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c2be-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="9c2be-134">-UserPrincipalName</span></span>
<span data-ttu-id="9c2be-135">A törlendő felhasználó egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="9c2be-135">The user principal name of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c2be-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9c2be-136">-Confirm</span></span>
<span data-ttu-id="9c2be-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9c2be-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c2be-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c2be-138">-WhatIf</span></span>
<span data-ttu-id="9c2be-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9c2be-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c2be-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9c2be-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c2be-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c2be-141">CommonParameters</span></span>
<span data-ttu-id="9c2be-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9c2be-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c2be-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c2be-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c2be-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c2be-144">INPUTS</span></span>

### <span data-ttu-id="9c2be-145">System. String</span><span class="sxs-lookup"><span data-stu-id="9c2be-145">System.String</span></span>

### <span data-ttu-id="9c2be-146">System. GUID</span><span class="sxs-lookup"><span data-stu-id="9c2be-146">System.Guid</span></span>

### <span data-ttu-id="9c2be-147">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="9c2be-147">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>
<span data-ttu-id="9c2be-148">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9c2be-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="9c2be-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c2be-149">OUTPUTS</span></span>

### <span data-ttu-id="9c2be-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9c2be-150">System.Boolean</span></span>

## <span data-ttu-id="9c2be-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9c2be-151">NOTES</span></span>

## <span data-ttu-id="9c2be-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c2be-152">RELATED LINKS</span></span>

[<span data-ttu-id="9c2be-153">Új – AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="9c2be-153">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="9c2be-154">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="9c2be-154">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)



