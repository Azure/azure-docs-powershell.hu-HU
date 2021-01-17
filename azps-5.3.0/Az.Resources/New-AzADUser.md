---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADUser.md
ms.openlocfilehash: c7863e62330dc26d9733d21eb8e4d11753e06d1c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466470"
---
# <span data-ttu-id="27803-101">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="27803-101">New-AzADUser</span></span>

## <span data-ttu-id="27803-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27803-102">SYNOPSIS</span></span>
<span data-ttu-id="27803-103">Új Active Directory-felhasználót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="27803-103">Creates a new active directory user.</span></span>

## <span data-ttu-id="27803-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="27803-104">SYNTAX</span></span>

```
New-AzADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString> [-ImmutableId <String>]
 -MailNickname <String> [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27803-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="27803-105">DESCRIPTION</span></span>
<span data-ttu-id="27803-106">Létrehoz egy új Active Directory-felhasználót (munkahelyi/iskolai fiókot, más néven szervezeti azonosítót).</span><span class="sxs-lookup"><span data-stu-id="27803-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="27803-107">További információ: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="27803-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="27803-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="27803-108">EXAMPLES</span></span>

### <span data-ttu-id="27803-109">1. példa: Új AD-felhasználó létrehozása</span><span class="sxs-lookup"><span data-stu-id="27803-109">Example 1: Create a new AD user</span></span>
```powershell
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADUser -DisplayName "MyDisplayName" -UserPrincipalName "myemail@domain.com" -Password $SecureStringPassword -MailNickname "MyMailNickName"
```

<span data-ttu-id="27803-110">Létrehoz egy új AD-felhasználót a "MyDisplayName" és az egyszerű felhasználónév myemail@domain.com " névvel a bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="27803-110">Creates a new AD user with the name "MyDisplayName" and user principal name "myemail@domain.com" in a tenant.</span></span>

## <span data-ttu-id="27803-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27803-111">PARAMETERS</span></span>

### <span data-ttu-id="27803-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27803-112">-DefaultProfile</span></span>
<span data-ttu-id="27803-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="27803-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27803-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="27803-114">-DisplayName</span></span>
<span data-ttu-id="27803-115">A felhasználó címjegyzékében megjelenítendő név.</span><span class="sxs-lookup"><span data-stu-id="27803-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="27803-116">például "Alex Wu".</span><span class="sxs-lookup"><span data-stu-id="27803-116">example 'Alex Wu'.</span></span>

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

### <span data-ttu-id="27803-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="27803-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="27803-118">Meg kell adni, ha a felhasználónak módosítania kell a jelszót a következő sikeres bejelentkezéskor (igaz).</span><span class="sxs-lookup"><span data-stu-id="27803-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="27803-119">Az alapértelmezett viselkedés (hamis) az, ha nem módosítja a jelszót a következő sikeres bejelentkezéskor.</span><span class="sxs-lookup"><span data-stu-id="27803-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="27803-120">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="27803-120">-ImmutableId</span></span>
<span data-ttu-id="27803-121">Ezt a tulajdonságot csak akkor kell megadni, ha a felhasználó egyszerű felhasználónevének (upn) tulajdonságában összevont tartományt használ.</span><span class="sxs-lookup"><span data-stu-id="27803-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

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

### <span data-ttu-id="27803-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="27803-122">-MailNickname</span></span>
<span data-ttu-id="27803-123">A felhasználó levelezési aliasa.</span><span class="sxs-lookup"><span data-stu-id="27803-123">The mail alias for the user.</span></span>

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

### <span data-ttu-id="27803-124">-Password</span><span class="sxs-lookup"><span data-stu-id="27803-124">-Password</span></span>
<span data-ttu-id="27803-125">A felhasználó jelszava.</span><span class="sxs-lookup"><span data-stu-id="27803-125">Password for the user.</span></span>
<span data-ttu-id="27803-126">Meg kell felelnie a bérlői jelszó összetettségi követelményeinek.</span><span class="sxs-lookup"><span data-stu-id="27803-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="27803-127">Javasoljuk, hogy erős jelszót állítson be.</span><span class="sxs-lookup"><span data-stu-id="27803-127">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="27803-128">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="27803-128">-UserPrincipalName</span></span>
<span data-ttu-id="27803-129">Az egyszerű felhasználónév.</span><span class="sxs-lookup"><span data-stu-id="27803-129">The user principal name.</span></span>
<span data-ttu-id="27803-130">Example-' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="27803-130">Example-'someuser@contoso.com'.</span></span>

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

### <span data-ttu-id="27803-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27803-131">-Confirm</span></span>
<span data-ttu-id="27803-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="27803-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27803-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27803-133">-WhatIf</span></span>
<span data-ttu-id="27803-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="27803-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27803-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="27803-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27803-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27803-136">CommonParameters</span></span>
<span data-ttu-id="27803-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27803-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27803-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27803-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27803-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="27803-139">INPUTS</span></span>

### <span data-ttu-id="27803-140">System.String</span><span class="sxs-lookup"><span data-stu-id="27803-140">System.String</span></span>

### <span data-ttu-id="27803-141">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="27803-141">System.Security.SecureString</span></span>

### <span data-ttu-id="27803-142">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="27803-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="27803-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27803-143">OUTPUTS</span></span>

### <span data-ttu-id="27803-144">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="27803-144">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="27803-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="27803-145">NOTES</span></span>

## <span data-ttu-id="27803-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27803-146">RELATED LINKS</span></span>

[<span data-ttu-id="27803-147">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="27803-147">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="27803-148">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="27803-148">Update-AzADUser</span></span>](./Update-AzADUser.md)

[<span data-ttu-id="27803-149">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="27803-149">Remove-AzADUser</span></span>](./Remove-AzADUser.md)
