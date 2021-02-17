---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADUser.md
ms.openlocfilehash: c7863e62330dc26d9733d21eb8e4d11753e06d1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208471"
---
# <span data-ttu-id="4aaf7-101">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="4aaf7-101">New-AzADUser</span></span>

## <span data-ttu-id="4aaf7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4aaf7-102">SYNOPSIS</span></span>
<span data-ttu-id="4aaf7-103">Új Active Directory-felhasználót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4aaf7-103">Creates a new active directory user.</span></span>

## <span data-ttu-id="4aaf7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4aaf7-104">SYNTAX</span></span>

```
New-AzADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString> [-ImmutableId <String>]
 -MailNickname <String> [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4aaf7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4aaf7-105">DESCRIPTION</span></span>
<span data-ttu-id="4aaf7-106">Létrehoz egy új Active Directory-felhasználót (munkahelyi/iskolai fiókot, más néven szervezeti azonosítót).</span><span class="sxs-lookup"><span data-stu-id="4aaf7-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="4aaf7-107">További információ: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="4aaf7-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="4aaf7-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4aaf7-108">EXAMPLES</span></span>

### <span data-ttu-id="4aaf7-109">1. példa: Új AD-felhasználó létrehozása</span><span class="sxs-lookup"><span data-stu-id="4aaf7-109">Example 1: Create a new AD user</span></span>
```powershell
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADUser -DisplayName "MyDisplayName" -UserPrincipalName "myemail@domain.com" -Password $SecureStringPassword -MailNickname "MyMailNickName"
```

<span data-ttu-id="4aaf7-110">Létrehoz egy új AD-felhasználót a "MyDisplayName" és az egyszerű felhasználónév myemail@domain.com " névvel a bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="4aaf7-110">Creates a new AD user with the name "MyDisplayName" and user principal name "myemail@domain.com" in a tenant.</span></span>

## <span data-ttu-id="4aaf7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4aaf7-111">PARAMETERS</span></span>

### <span data-ttu-id="4aaf7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aaf7-112">-DefaultProfile</span></span>
<span data-ttu-id="4aaf7-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4aaf7-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4aaf7-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4aaf7-114">-DisplayName</span></span>
<span data-ttu-id="4aaf7-115">A felhasználó címjegyzékében megjelenítendő név.</span><span class="sxs-lookup"><span data-stu-id="4aaf7-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="4aaf7-116">például "Alex Wu".</span><span class="sxs-lookup"><span data-stu-id="4aaf7-116">example 'Alex Wu'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aaf7-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="4aaf7-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="4aaf7-118">Meg kell adni, ha a felhasználónak módosítania kell a jelszót a következő sikeres bejelentkezéskor (igaz).</span><span class="sxs-lookup"><span data-stu-id="4aaf7-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="4aaf7-119">Az alapértelmezett viselkedés (hamis) az, ha nem módosítja a jelszót a következő sikeres bejelentkezéskor.</span><span class="sxs-lookup"><span data-stu-id="4aaf7-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aaf7-120">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="4aaf7-120">-ImmutableId</span></span>
<span data-ttu-id="4aaf7-121">Ezt a tulajdonságot csak akkor kell megadni, ha összevont tartományt használ a felhasználó egyszerű felhasználónév (upn) tulajdonságában.</span><span class="sxs-lookup"><span data-stu-id="4aaf7-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aaf7-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="4aaf7-122">-MailNickname</span></span>
<span data-ttu-id="4aaf7-123">A felhasználó levelezési aliasa.</span><span class="sxs-lookup"><span data-stu-id="4aaf7-123">The mail alias for the user.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aaf7-124">-Password</span><span class="sxs-lookup"><span data-stu-id="4aaf7-124">-Password</span></span>
<span data-ttu-id="4aaf7-125">A felhasználó jelszava.</span><span class="sxs-lookup"><span data-stu-id="4aaf7-125">Password for the user.</span></span>
<span data-ttu-id="4aaf7-126">Meg kell felelnie a bérlői jelszó összetettségi követelményeinek.</span><span class="sxs-lookup"><span data-stu-id="4aaf7-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="4aaf7-127">Javasoljuk, hogy erős jelszót állítson be.</span><span class="sxs-lookup"><span data-stu-id="4aaf7-127">It is recommended to set a strong password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aaf7-128">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="4aaf7-128">-UserPrincipalName</span></span>
<span data-ttu-id="4aaf7-129">Az egyszerű felhasználó neve.</span><span class="sxs-lookup"><span data-stu-id="4aaf7-129">The user principal name.</span></span>
<span data-ttu-id="4aaf7-130">Example-' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="4aaf7-130">Example-'someuser@contoso.com'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aaf7-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4aaf7-131">-Confirm</span></span>
<span data-ttu-id="4aaf7-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4aaf7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4aaf7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4aaf7-133">-WhatIf</span></span>
<span data-ttu-id="4aaf7-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4aaf7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4aaf7-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4aaf7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4aaf7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aaf7-136">CommonParameters</span></span>
<span data-ttu-id="4aaf7-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4aaf7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aaf7-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4aaf7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aaf7-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4aaf7-139">INPUTS</span></span>

### <span data-ttu-id="4aaf7-140">System.String</span><span class="sxs-lookup"><span data-stu-id="4aaf7-140">System.String</span></span>

### <span data-ttu-id="4aaf7-141">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="4aaf7-141">System.Security.SecureString</span></span>

### <span data-ttu-id="4aaf7-142">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4aaf7-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4aaf7-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4aaf7-143">OUTPUTS</span></span>

### <span data-ttu-id="4aaf7-144">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="4aaf7-144">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="4aaf7-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4aaf7-145">NOTES</span></span>

## <span data-ttu-id="4aaf7-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4aaf7-146">RELATED LINKS</span></span>

[<span data-ttu-id="4aaf7-147">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="4aaf7-147">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="4aaf7-148">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="4aaf7-148">Update-AzADUser</span></span>](./Update-AzADUser.md)

[<span data-ttu-id="4aaf7-149">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="4aaf7-149">Remove-AzADUser</span></span>](./Remove-AzADUser.md)
