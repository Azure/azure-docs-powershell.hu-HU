---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
ms.openlocfilehash: b765e33479c6178d69fb670a2f18ef0169eadf35
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467209"
---
# <span data-ttu-id="ec608-101">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="ec608-101">Update-AzADUser</span></span>

## <span data-ttu-id="ec608-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec608-102">SYNOPSIS</span></span>
<span data-ttu-id="ec608-103">Egy meglévő Active Directory-felhasználó frissítése.</span><span class="sxs-lookup"><span data-stu-id="ec608-103">Updates an existing active directory user.</span></span>

## <span data-ttu-id="ec608-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ec608-104">SYNTAX</span></span>

### <span data-ttu-id="ec608-105">UPNOrObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ec608-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Update-AzADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec608-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec608-106">UPNParameterSet</span></span>
```
Update-AzADUser -UserPrincipalName <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec608-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec608-107">ObjectIdParameterSet</span></span>
```
Update-AzADUser -ObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec608-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec608-108">InputObjectParameterSet</span></span>
```
Update-AzADUser -InputObject <PSADUser> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec608-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ec608-109">DESCRIPTION</span></span>
<span data-ttu-id="ec608-110">Egy meglévő Active Directory-felhasználó (munkahelyi/iskolai fiók, más néven szervezeti azonosító) frissítése.</span><span class="sxs-lookup"><span data-stu-id="ec608-110">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="ec608-111">További információ: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="ec608-111">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="ec608-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ec608-112">EXAMPLES</span></span>

### <span data-ttu-id="ec608-113">1. példa: Felhasználó megjelenítendő nevének frissítése objektumazonosító használatával</span><span class="sxs-lookup"><span data-stu-id="ec608-113">Example 1: Update the display name of a user using object id</span></span>

```powershell
PS C:\> Update-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 -DisplayName MyNewDisplayName
```

<span data-ttu-id="ec608-114">Frissíti a felhasználó megjelenítendő nevét a (155a5c10-93a9-4941-a0df-96d83ab5ab24) azonosítóval "MyNewDisplayName" azonosítóra.</span><span class="sxs-lookup"><span data-stu-id="ec608-114">Updates the display name of the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="ec608-115">2. példa: Felhasználó megjelenített nevének frissítése egyszerű felhasználónévvel</span><span class="sxs-lookup"><span data-stu-id="ec608-115">Example 2: Update the display name of a user using user principal name</span></span>

```powershell
PS C:\> Update-AzADUser -UserPrincipalName foo@domain.com -DisplayName MyNewDisplayName
```

<span data-ttu-id="ec608-116">Frissíti a felhasználó megjelenítendő nevét egyszerű felhasználónévvel ' ' úgy, hogy foo@domain.com "MyNewDisplayName" legyen.</span><span class="sxs-lookup"><span data-stu-id="ec608-116">Updates the display name of the user with user principal name 'foo@domain.com' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="ec608-117">3. példa: Felhasználó megjelenítendő nevének frissítése pipázás használatával</span><span class="sxs-lookup"><span data-stu-id="ec608-117">Example 3: Update the display name of a user using piping</span></span>

```powershell
PS C:\> Get-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 | Update-AzADUser -DisplayName MyNewDisplayName
```

<span data-ttu-id="ec608-118">A (155a5c10-93a9-4941-a0df-96d83ab5ab24) objektumazonosítóval és a Update-AzADUser-parancsmaghoz a felhasználó megjelenítendő nevének "MyNewDisplayName" névre való frissítéséhez bevezető vezetékeket használ.</span><span class="sxs-lookup"><span data-stu-id="ec608-118">Gets the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' and pipes that to the Update-AzADUser cmdlet to update the display name of that user to 'MyNewDisplayName'.</span></span>

## <span data-ttu-id="ec608-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec608-119">PARAMETERS</span></span>

### <span data-ttu-id="ec608-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec608-120">-DefaultProfile</span></span>
<span data-ttu-id="ec608-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ec608-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec608-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ec608-122">-DisplayName</span></span>
<span data-ttu-id="ec608-123">A felhasználó új megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="ec608-123">New display name for the user.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec608-124">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="ec608-124">-EnableAccount</span></span>
<span data-ttu-id="ec608-125">true for enabling the account; ellenkező esetben hamis.</span><span class="sxs-lookup"><span data-stu-id="ec608-125">true for enabling the account; otherwise, false.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec608-126">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="ec608-126">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="ec608-127">Meg kell adni, ha a felhasználónak módosítania kell a jelszót a következő sikeres bejelentkezéskor.</span><span class="sxs-lookup"><span data-stu-id="ec608-127">It must be specified if the user should change the password on the next successful login.</span></span>
<span data-ttu-id="ec608-128">Csak akkor érvényes, ha a jelszó frissül, ellenkező esetben a rendszer figyelmen kívül hagyja.</span><span class="sxs-lookup"><span data-stu-id="ec608-128">Only valid if password is updated otherwise it will be ignored.</span></span>

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

### <span data-ttu-id="ec608-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec608-129">-InputObject</span></span>
<span data-ttu-id="ec608-130">A frissíthető felhasználót képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="ec608-130">The object representing the user to be updated.</span></span>

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

### <span data-ttu-id="ec608-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ec608-131">-ObjectId</span></span>
<span data-ttu-id="ec608-132">A frissíthető felhasználó objektumazonosítója.</span><span class="sxs-lookup"><span data-stu-id="ec608-132">The object id of the user to be updated.</span></span>

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

### <span data-ttu-id="ec608-133">-Password</span><span class="sxs-lookup"><span data-stu-id="ec608-133">-Password</span></span>
<span data-ttu-id="ec608-134">A felhasználó új jelszava.</span><span class="sxs-lookup"><span data-stu-id="ec608-134">New password for the user.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec608-135">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="ec608-135">-UPNOrObjectId</span></span>
<span data-ttu-id="ec608-136">A frissíthető felhasználó egyszerű felhasználóneve vagy objektumazonosítója.</span><span class="sxs-lookup"><span data-stu-id="ec608-136">The user principal name or object id of the user to be updated.</span></span>

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

### <span data-ttu-id="ec608-137">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ec608-137">-UserPrincipalName</span></span>
<span data-ttu-id="ec608-138">A frissíthető felhasználó egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="ec608-138">The user principal name of the user to be updated.</span></span>

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

### <span data-ttu-id="ec608-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ec608-139">-Confirm</span></span>
<span data-ttu-id="ec608-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ec608-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec608-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec608-141">-WhatIf</span></span>
<span data-ttu-id="ec608-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ec608-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec608-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ec608-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec608-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec608-144">CommonParameters</span></span>
<span data-ttu-id="ec608-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec608-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec608-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec608-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec608-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ec608-147">INPUTS</span></span>

### <span data-ttu-id="ec608-148">System.String</span><span class="sxs-lookup"><span data-stu-id="ec608-148">System.String</span></span>

### <span data-ttu-id="ec608-149">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="ec608-149">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

### <span data-ttu-id="ec608-150">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ec608-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ec608-151">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="ec608-151">System.Security.SecureString</span></span>

## <span data-ttu-id="ec608-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec608-152">OUTPUTS</span></span>

### <span data-ttu-id="ec608-153">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="ec608-153">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="ec608-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ec608-154">NOTES</span></span>

## <span data-ttu-id="ec608-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec608-155">RELATED LINKS</span></span>
