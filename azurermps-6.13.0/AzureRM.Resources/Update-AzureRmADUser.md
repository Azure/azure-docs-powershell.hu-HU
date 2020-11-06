---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/update-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Update-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Update-AzureRmADUser.md
ms.openlocfilehash: a07d9119d5e83c92d96ab22e98125459945f786b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494934"
---
# <span data-ttu-id="c9d5e-101">Update-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="c9d5e-101">Update-AzureRmADUser</span></span>

## <span data-ttu-id="c9d5e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c9d5e-102">SYNOPSIS</span></span>
<span data-ttu-id="c9d5e-103">Frissít egy meglévő Active Directory-felhasználót.</span><span class="sxs-lookup"><span data-stu-id="c9d5e-103">Updates an existing active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9d5e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c9d5e-104">SYNTAX</span></span>

### <span data-ttu-id="c9d5e-105">UPNOrObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c9d5e-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Update-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9d5e-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9d5e-106">UPNParameterSet</span></span>
```
Update-AzureRmADUser -UserPrincipalName <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9d5e-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9d5e-107">ObjectIdParameterSet</span></span>
```
Update-AzureRmADUser -ObjectId <Guid> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9d5e-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9d5e-108">InputObjectParameterSet</span></span>
```
Update-AzureRmADUser -InputObject <PSADUser> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9d5e-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="c9d5e-109">DESCRIPTION</span></span>
<span data-ttu-id="c9d5e-110">Frissít egy meglévő Active Directory-felhasználó (munkahelyi/iskolai fiók is ismert, mint a szervezeti azonosító).</span><span class="sxs-lookup"><span data-stu-id="c9d5e-110">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="c9d5e-111">További információ: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="c9d5e-111">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="c9d5e-112">Példák</span><span class="sxs-lookup"><span data-stu-id="c9d5e-112">EXAMPLES</span></span>

### <span data-ttu-id="c9d5e-113">Példa 1 – az objektum-azonosítóval rendelkező felhasználó megjelenítendő nevének frissítése</span><span class="sxs-lookup"><span data-stu-id="c9d5e-113">Example 1 - Update the display name of a user using object id</span></span>

```
PS C:\> Update-AzureRmADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 -DisplayName MyNewDisplayName
```

<span data-ttu-id="c9d5e-114">Frissíti a "155a5c10-93a9-4941-a0df-96d83ab5ab24" azonosítójú felhasználó megjelenítendő nevét a "MyNewDisplayName" értékkel.</span><span class="sxs-lookup"><span data-stu-id="c9d5e-114">Updates the display name of the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="c9d5e-115">Példa 2 – a felhasználó megjelenítendő nevének frissítése a felhasználó egyszerű nevével</span><span class="sxs-lookup"><span data-stu-id="c9d5e-115">Example 2 - Update the display name of a user using user principal name</span></span>

```
PS C:\> Update-AzureRmADUser -UserPrincipalName foo@domain.com -DisplayName MyNewDisplayName
```

<span data-ttu-id="c9d5e-116">Frissíti annak a felhasználónak a megjelenítendő nevét, akinek a neve " foo@domain.com MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="c9d5e-116">Updates the display name of the user with user principal name 'foo@domain.com' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="c9d5e-117">3 példa – a felhasználó megjelenítendő nevének frissítése a csővezetékek segítségével</span><span class="sxs-lookup"><span data-stu-id="c9d5e-117">Example 3 - Update the display name of a user using piping</span></span>

```
PS C:\> Get-AzureRmADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 | Update-AzureRmADUser -DisplayName MyNewDisplayName
```

<span data-ttu-id="c9d5e-118">A felhasználó megkapja a "155a5c10-93a9-4941-a0df-96d83ab5ab24" azonosítójú objektumazonosítót, valamint az Update-AzureRmADUser parancsmagot tartalmazó csöveket, hogy a felhasználó megjelenítendő nevét frissítse a "MyNewDisplayName" értékre.</span><span class="sxs-lookup"><span data-stu-id="c9d5e-118">Gets the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' and pipes that to the Update-AzureRmADUser cmdlet to update the display name of that user to 'MyNewDisplayName'.</span></span>

## <span data-ttu-id="c9d5e-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c9d5e-119">PARAMETERS</span></span>

### <span data-ttu-id="c9d5e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9d5e-120">-DefaultProfile</span></span>
<span data-ttu-id="c9d5e-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c9d5e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9d5e-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c9d5e-122">-DisplayName</span></span>
<span data-ttu-id="c9d5e-123">Új megjelenítendő név a felhasználó számára.</span><span class="sxs-lookup"><span data-stu-id="c9d5e-123">New display name for the user.</span></span>

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

### <span data-ttu-id="c9d5e-124">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="c9d5e-124">-EnableAccount</span></span>
<span data-ttu-id="c9d5e-125">True a fiók engedélyezéséhez; egyéb esetben false.</span><span class="sxs-lookup"><span data-stu-id="c9d5e-125">true for enabling the account; otherwise, false.</span></span>

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

### <span data-ttu-id="c9d5e-126">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="c9d5e-126">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="c9d5e-127">Meg kell adni, ha a felhasználó a következő sikeres bejelentkezéskor módosítania kell a jelszót.</span><span class="sxs-lookup"><span data-stu-id="c9d5e-127">It must be specified if the user should change the password on the next successful login.</span></span>
<span data-ttu-id="c9d5e-128">Csak akkor érvényes, ha a jelszó nem jelenik meg, ellenkező esetben figyelmen kívül hagyja.</span><span class="sxs-lookup"><span data-stu-id="c9d5e-128">Only valid if password is updated otherwise it will be ignored.</span></span>

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

### <span data-ttu-id="c9d5e-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9d5e-129">-InputObject</span></span>
<span data-ttu-id="c9d5e-130">A frissítendő felhasználót jelképező objektum.</span><span class="sxs-lookup"><span data-stu-id="c9d5e-130">The object representing the user to be updated.</span></span>

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

### <span data-ttu-id="c9d5e-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c9d5e-131">-ObjectId</span></span>
<span data-ttu-id="c9d5e-132">A frissítendő felhasználó objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c9d5e-132">The object id of the user to be updated.</span></span>

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

### <span data-ttu-id="c9d5e-133">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="c9d5e-133">-Password</span></span>
<span data-ttu-id="c9d5e-134">Új jelszó a felhasználó számára.</span><span class="sxs-lookup"><span data-stu-id="c9d5e-134">New password for the user.</span></span>

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

### <span data-ttu-id="c9d5e-135">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="c9d5e-135">-UPNOrObjectId</span></span>
<span data-ttu-id="c9d5e-136">A frissítendő felhasználó egyszerű felhasználónevét vagy objektum-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="c9d5e-136">The user principal name or object id of the user to be updated.</span></span>

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

### <span data-ttu-id="c9d5e-137">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="c9d5e-137">-UserPrincipalName</span></span>
<span data-ttu-id="c9d5e-138">A frissítendő felhasználó egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="c9d5e-138">The user principal name of the user to be updated.</span></span>

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

### <span data-ttu-id="c9d5e-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c9d5e-139">-Confirm</span></span>
<span data-ttu-id="c9d5e-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c9d5e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9d5e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9d5e-141">-WhatIf</span></span>
<span data-ttu-id="c9d5e-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c9d5e-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9d5e-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c9d5e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9d5e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9d5e-144">CommonParameters</span></span>
<span data-ttu-id="c9d5e-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c9d5e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9d5e-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9d5e-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9d5e-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9d5e-147">INPUTS</span></span>

### <span data-ttu-id="c9d5e-148">System. String</span><span class="sxs-lookup"><span data-stu-id="c9d5e-148">System.String</span></span>

### <span data-ttu-id="c9d5e-149">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c9d5e-149">System.Guid</span></span>

### <span data-ttu-id="c9d5e-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="c9d5e-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>
<span data-ttu-id="c9d5e-151">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c9d5e-151">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="c9d5e-152">System. null ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c9d5e-152">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="c9d5e-153">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="c9d5e-153">System.Security.SecureString</span></span>

## <span data-ttu-id="c9d5e-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9d5e-154">OUTPUTS</span></span>

### <span data-ttu-id="c9d5e-155">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="c9d5e-155">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="c9d5e-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c9d5e-156">NOTES</span></span>

## <span data-ttu-id="c9d5e-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9d5e-157">RELATED LINKS</span></span>
