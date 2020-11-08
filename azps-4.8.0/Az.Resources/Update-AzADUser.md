---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
ms.openlocfilehash: b765e33479c6178d69fb670a2f18ef0169eadf35
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181399"
---
# <span data-ttu-id="a143d-101">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="a143d-101">Update-AzADUser</span></span>

## <span data-ttu-id="a143d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a143d-102">SYNOPSIS</span></span>
<span data-ttu-id="a143d-103">Frissít egy meglévő Active Directory-felhasználót.</span><span class="sxs-lookup"><span data-stu-id="a143d-103">Updates an existing active directory user.</span></span>

## <span data-ttu-id="a143d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a143d-104">SYNTAX</span></span>

### <span data-ttu-id="a143d-105">UPNOrObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a143d-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Update-AzADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a143d-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="a143d-106">UPNParameterSet</span></span>
```
Update-AzADUser -UserPrincipalName <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a143d-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a143d-107">ObjectIdParameterSet</span></span>
```
Update-AzADUser -ObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a143d-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a143d-108">InputObjectParameterSet</span></span>
```
Update-AzADUser -InputObject <PSADUser> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a143d-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="a143d-109">DESCRIPTION</span></span>
<span data-ttu-id="a143d-110">Frissít egy meglévő Active Directory-felhasználó (munkahelyi/iskolai fiók is ismert, mint a szervezeti azonosító).</span><span class="sxs-lookup"><span data-stu-id="a143d-110">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="a143d-111">További információ: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="a143d-111">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="a143d-112">Példák</span><span class="sxs-lookup"><span data-stu-id="a143d-112">EXAMPLES</span></span>

### <span data-ttu-id="a143d-113">Példa 1: a felhasználó megjelenítendő nevének frissítése objektum-azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="a143d-113">Example 1: Update the display name of a user using object id</span></span>

```powershell
PS C:\> Update-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 -DisplayName MyNewDisplayName
```

<span data-ttu-id="a143d-114">Frissíti a "155a5c10-93a9-4941-a0df-96d83ab5ab24" azonosítójú felhasználó megjelenítendő nevét a "MyNewDisplayName" értékkel.</span><span class="sxs-lookup"><span data-stu-id="a143d-114">Updates the display name of the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="a143d-115">2. példa: a felhasználó megjelenítendő nevének frissítése a felhasználó egyszerű nevének használatával</span><span class="sxs-lookup"><span data-stu-id="a143d-115">Example 2: Update the display name of a user using user principal name</span></span>

```powershell
PS C:\> Update-AzADUser -UserPrincipalName foo@domain.com -DisplayName MyNewDisplayName
```

<span data-ttu-id="a143d-116">Frissíti annak a felhasználónak a megjelenítendő nevét, akinek a neve " foo@domain.com MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="a143d-116">Updates the display name of the user with user principal name 'foo@domain.com' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="a143d-117">3. példa: a felhasználó megjelenített nevének frissítése a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="a143d-117">Example 3: Update the display name of a user using piping</span></span>

```powershell
PS C:\> Get-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 | Update-AzADUser -DisplayName MyNewDisplayName
```

<span data-ttu-id="a143d-118">A felhasználó megkapja a "155a5c10-93a9-4941-a0df-96d83ab5ab24" azonosítójú objektumazonosítót, valamint az Update-AzADUser parancsmagot tartalmazó csöveket, hogy a felhasználó megjelenítendő nevét frissítse a "MyNewDisplayName" értékre.</span><span class="sxs-lookup"><span data-stu-id="a143d-118">Gets the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' and pipes that to the Update-AzADUser cmdlet to update the display name of that user to 'MyNewDisplayName'.</span></span>

## <span data-ttu-id="a143d-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a143d-119">PARAMETERS</span></span>

### <span data-ttu-id="a143d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a143d-120">-DefaultProfile</span></span>
<span data-ttu-id="a143d-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a143d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a143d-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a143d-122">-DisplayName</span></span>
<span data-ttu-id="a143d-123">Új megjelenítendő név a felhasználó számára.</span><span class="sxs-lookup"><span data-stu-id="a143d-123">New display name for the user.</span></span>

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

### <span data-ttu-id="a143d-124">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="a143d-124">-EnableAccount</span></span>
<span data-ttu-id="a143d-125">True a fiók engedélyezéséhez; egyéb esetben false.</span><span class="sxs-lookup"><span data-stu-id="a143d-125">true for enabling the account; otherwise, false.</span></span>

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

### <span data-ttu-id="a143d-126">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="a143d-126">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="a143d-127">Meg kell adni, ha a felhasználó a következő sikeres bejelentkezéskor módosítania kell a jelszót.</span><span class="sxs-lookup"><span data-stu-id="a143d-127">It must be specified if the user should change the password on the next successful login.</span></span>
<span data-ttu-id="a143d-128">Csak akkor érvényes, ha a jelszó nem jelenik meg, ellenkező esetben figyelmen kívül hagyja.</span><span class="sxs-lookup"><span data-stu-id="a143d-128">Only valid if password is updated otherwise it will be ignored.</span></span>

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

### <span data-ttu-id="a143d-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a143d-129">-InputObject</span></span>
<span data-ttu-id="a143d-130">A frissítendő felhasználót jelképező objektum.</span><span class="sxs-lookup"><span data-stu-id="a143d-130">The object representing the user to be updated.</span></span>

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

### <span data-ttu-id="a143d-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a143d-131">-ObjectId</span></span>
<span data-ttu-id="a143d-132">A frissítendő felhasználó objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a143d-132">The object id of the user to be updated.</span></span>

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

### <span data-ttu-id="a143d-133">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="a143d-133">-Password</span></span>
<span data-ttu-id="a143d-134">Új jelszó a felhasználó számára.</span><span class="sxs-lookup"><span data-stu-id="a143d-134">New password for the user.</span></span>

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

### <span data-ttu-id="a143d-135">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="a143d-135">-UPNOrObjectId</span></span>
<span data-ttu-id="a143d-136">A frissítendő felhasználó egyszerű felhasználónevét vagy objektum-azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="a143d-136">The user principal name or object id of the user to be updated.</span></span>

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

### <span data-ttu-id="a143d-137">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="a143d-137">-UserPrincipalName</span></span>
<span data-ttu-id="a143d-138">A frissítendő felhasználó egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="a143d-138">The user principal name of the user to be updated.</span></span>

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

### <span data-ttu-id="a143d-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a143d-139">-Confirm</span></span>
<span data-ttu-id="a143d-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a143d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a143d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a143d-141">-WhatIf</span></span>
<span data-ttu-id="a143d-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a143d-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a143d-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a143d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a143d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a143d-144">CommonParameters</span></span>
<span data-ttu-id="a143d-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a143d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a143d-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a143d-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a143d-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a143d-147">INPUTS</span></span>

### <span data-ttu-id="a143d-148">System. String</span><span class="sxs-lookup"><span data-stu-id="a143d-148">System.String</span></span>

### <span data-ttu-id="a143d-149">Microsoft. Azure. Command. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="a143d-149">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

### <span data-ttu-id="a143d-150">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a143d-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a143d-151">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="a143d-151">System.Security.SecureString</span></span>

## <span data-ttu-id="a143d-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a143d-152">OUTPUTS</span></span>

### <span data-ttu-id="a143d-153">Microsoft. Azure. Command. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="a143d-153">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="a143d-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a143d-154">NOTES</span></span>

## <span data-ttu-id="a143d-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a143d-155">RELATED LINKS</span></span>
