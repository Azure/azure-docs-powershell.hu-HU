---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
ms.openlocfilehash: b3c59fabe648293b6ed92d23e4953cc17190e5e9
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413353"
---
# <span data-ttu-id="6c5f3-101">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="6c5f3-101">Remove-AzADUser</span></span>

## <span data-ttu-id="6c5f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c5f3-102">SYNOPSIS</span></span>
<span data-ttu-id="6c5f3-103">Egy Active Directory-felhasználó törlése.</span><span class="sxs-lookup"><span data-stu-id="6c5f3-103">Deletes an active directory user.</span></span>

## <span data-ttu-id="6c5f3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6c5f3-104">SYNTAX</span></span>

### <span data-ttu-id="6c5f3-105">UPNOrObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6c5f3-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c5f3-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c5f3-106">UPNParameterSet</span></span>
```
Remove-AzADUser -UserPrincipalName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c5f3-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c5f3-107">ObjectIdParameterSet</span></span>
```
Remove-AzADUser -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c5f3-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c5f3-108">DisplayNameParameterSet</span></span>
```
Remove-AzADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c5f3-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c5f3-109">InputObjectParameterSet</span></span>
```
Remove-AzADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c5f3-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6c5f3-110">DESCRIPTION</span></span>
<span data-ttu-id="6c5f3-111">Töröl egy Active Directory-felhasználót (munkahelyi/iskolai fiókot, más néven szervezeti azonosítót).</span><span class="sxs-lookup"><span data-stu-id="6c5f3-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="6c5f3-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6c5f3-112">EXAMPLES</span></span>

### <span data-ttu-id="6c5f3-113">1. példa: Felhasználó eltávolítása egyszerű felhasználónév alapján</span><span class="sxs-lookup"><span data-stu-id="6c5f3-113">Example 1 - Remove a user by user principal name</span></span>

```
PS C:\> Remove-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="6c5f3-114">Eltávolítja a bérlői fiókból a foo@domain.com "" nevű felhasználónevet.</span><span class="sxs-lookup"><span data-stu-id="6c5f3-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="6c5f3-115">2. példa: Felhasználó eltávolítása objektumazonosító alapján</span><span class="sxs-lookup"><span data-stu-id="6c5f3-115">Example 2 - Remove a user by object id</span></span>

```
PS C:\> Remove-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="6c5f3-116">Eltávolítja a bérlői webhelyről a (7a9582cf-88c4-4319-842b-7a5d60967a69) azonosítójú felhasználót.</span><span class="sxs-lookup"><span data-stu-id="6c5f3-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="6c5f3-117">3. példa: Felhasználó eltávolítása pipázás használatával</span><span class="sxs-lookup"><span data-stu-id="6c5f3-117">Example 3 - Remove a user by piping</span></span>

```
PS C:\> Get-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzADUser
```

<span data-ttu-id="6c5f3-118">A (7a9582cf-88c4-4319-842b-7a5d60967a69) azonosítójú felhasználót és a Remove-AzADUser-parancsmagot a felhasználó bérlői webhelyről való eltávolításához bevezető vezetékeket használ.</span><span class="sxs-lookup"><span data-stu-id="6c5f3-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="6c5f3-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c5f3-119">PARAMETERS</span></span>

### <span data-ttu-id="6c5f3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c5f3-120">-DefaultProfile</span></span>
<span data-ttu-id="6c5f3-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6c5f3-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c5f3-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6c5f3-122">-DisplayName</span></span>
<span data-ttu-id="6c5f3-123">A törölendő felhasználó megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="6c5f3-123">The display name of the user to be deleted.</span></span>

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

### <span data-ttu-id="6c5f3-124">-Force</span><span class="sxs-lookup"><span data-stu-id="6c5f3-124">-Force</span></span>
<span data-ttu-id="6c5f3-125">Ha meg van adva, akkor nem kér megerősítést a felhasználó törléséhez.</span><span class="sxs-lookup"><span data-stu-id="6c5f3-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="6c5f3-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c5f3-126">-InputObject</span></span>
<span data-ttu-id="6c5f3-127">A törölni fog egy felhasználói objektumot.</span><span class="sxs-lookup"><span data-stu-id="6c5f3-127">The user object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADUser
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c5f3-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6c5f3-128">-ObjectId</span></span>
<span data-ttu-id="6c5f3-129">A törölt felhasználó objektumazonosítója.</span><span class="sxs-lookup"><span data-stu-id="6c5f3-129">The object id of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c5f3-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c5f3-130">-PassThru</span></span>
<span data-ttu-id="6c5f3-131">Ha megadja ezt a parancsot, az igaz értéket ad vissza, ha a parancs sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="6c5f3-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="6c5f3-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="6c5f3-132">-UPNOrObjectId</span></span>
<span data-ttu-id="6c5f3-133">A törölnie kell a felhasználó egyszerű felhasználónevét vagy objectId azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="6c5f3-133">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="6c5f3-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="6c5f3-134">-UserPrincipalName</span></span>
<span data-ttu-id="6c5f3-135">A törölt felhasználó egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="6c5f3-135">The user principal name of the user to be deleted.</span></span>

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

### <span data-ttu-id="6c5f3-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c5f3-136">-Confirm</span></span>
<span data-ttu-id="6c5f3-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6c5f3-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c5f3-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c5f3-138">-WhatIf</span></span>
<span data-ttu-id="6c5f3-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6c5f3-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c5f3-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6c5f3-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c5f3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c5f3-141">CommonParameters</span></span>
<span data-ttu-id="6c5f3-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c5f3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c5f3-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c5f3-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c5f3-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6c5f3-144">INPUTS</span></span>

### <span data-ttu-id="6c5f3-145">System.String</span><span class="sxs-lookup"><span data-stu-id="6c5f3-145">System.String</span></span>

### <span data-ttu-id="6c5f3-146">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="6c5f3-146">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="6c5f3-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c5f3-147">OUTPUTS</span></span>

### <span data-ttu-id="6c5f3-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6c5f3-148">System.Boolean</span></span>

## <span data-ttu-id="6c5f3-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6c5f3-149">NOTES</span></span>

## <span data-ttu-id="6c5f3-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6c5f3-150">RELATED LINKS</span></span>

[<span data-ttu-id="6c5f3-151">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="6c5f3-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="6c5f3-152">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="6c5f3-152">Get-AzADUser</span></span>](./Get-AzADUser.md)


