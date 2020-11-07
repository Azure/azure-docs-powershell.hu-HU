---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
ms.openlocfilehash: 1b863b0bc9cb90caca4d7431ec6835cb75836609
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679519"
---
# <span data-ttu-id="7f31c-101">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="7f31c-101">Remove-AzureRmADUser</span></span>

## <span data-ttu-id="7f31c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7f31c-102">SYNOPSIS</span></span>
<span data-ttu-id="7f31c-103">Active Directory-felhasználó törlése</span><span class="sxs-lookup"><span data-stu-id="7f31c-103">Deletes an active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f31c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7f31c-104">SYNTAX</span></span>

### <span data-ttu-id="7f31c-105">UPNOrObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7f31c-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f31c-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f31c-106">UPNParameterSet</span></span>
```
Remove-AzureRmADUser -UserPrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f31c-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f31c-107">ObjectIdParameterSet</span></span>
```
Remove-AzureRmADUser -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f31c-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f31c-108">DisplayNameParameterSet</span></span>
```
Remove-AzureRmADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f31c-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f31c-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f31c-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="7f31c-110">DESCRIPTION</span></span>
<span data-ttu-id="7f31c-111">Egy Active Directory-felhasználó törlése (munkahelyi/iskolai fiók is ismert a szervezeti azonosító néven ismert).</span><span class="sxs-lookup"><span data-stu-id="7f31c-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="7f31c-112">Példák</span><span class="sxs-lookup"><span data-stu-id="7f31c-112">EXAMPLES</span></span>

### <span data-ttu-id="7f31c-113">Példa 1 – felhasználó eltávolítása a felhasználó egyszerű nevével</span><span class="sxs-lookup"><span data-stu-id="7f31c-113">Example 1 - Remove a user by user principal name</span></span>

```
PS C:\> Remove-AzureRmADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="7f31c-114">A felhasználó eltávolítása a "" "nevű felhasználó nevéből foo@domain.com a bérlői webhelyről.</span><span class="sxs-lookup"><span data-stu-id="7f31c-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="7f31c-115">2. példa – egy felhasználó objektum-azonosítóval való eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7f31c-115">Example 2 - Remove a user by object id</span></span>

```
PS C:\> Remove-AzureRmADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="7f31c-116">Eltávolítja az "7a9582cf-88c4-4319-842b-7a5d60967a69" azonosítójú felhasználót a bérlői webhelyről.</span><span class="sxs-lookup"><span data-stu-id="7f31c-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="7f31c-117">3 példa – felhasználó eltávolítása csővezetékről</span><span class="sxs-lookup"><span data-stu-id="7f31c-117">Example 3 - Remove a user by piping</span></span>

```
PS C:\> Get-AzureRmADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzureRmADUser
```

<span data-ttu-id="7f31c-118">A felhasználót a "7a9582cf-88c4-4319-842b-7a5d60967a69" azonosítójú objektummal, a Remove-AzureRmADUser parancsmagot tartalmazó csövekkel pedig eltávolítja a felhasználót a bérlői fiókból.</span><span class="sxs-lookup"><span data-stu-id="7f31c-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzureRmADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="7f31c-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7f31c-119">PARAMETERS</span></span>

### <span data-ttu-id="7f31c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f31c-120">-DefaultProfile</span></span>
<span data-ttu-id="7f31c-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7f31c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f31c-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7f31c-122">-DisplayName</span></span>
<span data-ttu-id="7f31c-123">A törlendő felhasználó megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="7f31c-123">The display name of the user to be deleted.</span></span>

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

### <span data-ttu-id="7f31c-124">-Force</span><span class="sxs-lookup"><span data-stu-id="7f31c-124">-Force</span></span>
<span data-ttu-id="7f31c-125">Ha meg van adva, nem kér megerősítést a felhasználó törléséhez.</span><span class="sxs-lookup"><span data-stu-id="7f31c-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="7f31c-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f31c-126">-InputObject</span></span>
<span data-ttu-id="7f31c-127">A törlendő felhasználói objektum.</span><span class="sxs-lookup"><span data-stu-id="7f31c-127">The user object to be deleted.</span></span>

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

### <span data-ttu-id="7f31c-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7f31c-128">-ObjectId</span></span>
<span data-ttu-id="7f31c-129">A törlendő felhasználó objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7f31c-129">The object id of the user to be deleted.</span></span>

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

### <span data-ttu-id="7f31c-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f31c-130">-PassThru</span></span>
<span data-ttu-id="7f31c-131">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="7f31c-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="7f31c-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="7f31c-132">-UPNOrObjectId</span></span>
<span data-ttu-id="7f31c-133">A törölni kívánt felhasználó egyszerű felhasználónevét vagy objectId.</span><span class="sxs-lookup"><span data-stu-id="7f31c-133">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="7f31c-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="7f31c-134">-UserPrincipalName</span></span>
<span data-ttu-id="7f31c-135">A törlendő felhasználó egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="7f31c-135">The user principal name of the user to be deleted.</span></span>

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

### <span data-ttu-id="7f31c-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7f31c-136">-Confirm</span></span>
<span data-ttu-id="7f31c-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7f31c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f31c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f31c-138">-WhatIf</span></span>
<span data-ttu-id="7f31c-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7f31c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f31c-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7f31c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f31c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f31c-141">CommonParameters</span></span>
<span data-ttu-id="7f31c-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7f31c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f31c-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f31c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f31c-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f31c-144">INPUTS</span></span>

### <span data-ttu-id="7f31c-145">System. String</span><span class="sxs-lookup"><span data-stu-id="7f31c-145">System.String</span></span>

### <span data-ttu-id="7f31c-146">System. GUID</span><span class="sxs-lookup"><span data-stu-id="7f31c-146">System.Guid</span></span>

### <span data-ttu-id="7f31c-147">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="7f31c-147">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>
<span data-ttu-id="7f31c-148">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7f31c-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="7f31c-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f31c-149">OUTPUTS</span></span>

### <span data-ttu-id="7f31c-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7f31c-150">System.Boolean</span></span>

## <span data-ttu-id="7f31c-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7f31c-151">NOTES</span></span>

## <span data-ttu-id="7f31c-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f31c-152">RELATED LINKS</span></span>

[<span data-ttu-id="7f31c-153">Új – AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="7f31c-153">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="7f31c-154">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="7f31c-154">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="7f31c-155">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="7f31c-155">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

