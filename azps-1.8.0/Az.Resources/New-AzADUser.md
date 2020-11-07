---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADUser.md
ms.openlocfilehash: ac2dfb864733d7bcb2b46e17d557fca57c7bb4b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669395"
---
# <span data-ttu-id="ed22d-101">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="ed22d-101">New-AzADUser</span></span>

## <span data-ttu-id="ed22d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ed22d-102">SYNOPSIS</span></span>
<span data-ttu-id="ed22d-103">Új Active Directory-felhasználó létrehozása.</span><span class="sxs-lookup"><span data-stu-id="ed22d-103">Creates a new active directory user.</span></span>

## <span data-ttu-id="ed22d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ed22d-104">SYNTAX</span></span>

```
New-AzADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString> [-ImmutableId <String>]
 -MailNickname <String> [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed22d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ed22d-105">DESCRIPTION</span></span>
<span data-ttu-id="ed22d-106">Új Active Directory-felhasználó létrehozása (munkahelyi/iskolai fiók is ismert a szervezeti azonosító néven ismert).</span><span class="sxs-lookup"><span data-stu-id="ed22d-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="ed22d-107">További információ: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="ed22d-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="ed22d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ed22d-108">EXAMPLES</span></span>

### <span data-ttu-id="ed22d-109">Példa 1 – új AD-felhasználó létrehozása</span><span class="sxs-lookup"><span data-stu-id="ed22d-109">Example 1 - Create a new AD user</span></span>
```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADUser -DisplayName "MyDisplayName" -UserPrincipalName "myemail@domain.com" -Password $SecureStringPassword -MailNickname "MyMailNickName"
```

<span data-ttu-id="ed22d-110">Új AD-felhasználó létrehozása a "MyDisplayName" és a "" "nevű felhasználó nevében a myemail@domain.com bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="ed22d-110">Creates a new AD user with the name "MyDisplayName" and user principal name "myemail@domain.com" in a tenant.</span></span>

## <span data-ttu-id="ed22d-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ed22d-111">PARAMETERS</span></span>

### <span data-ttu-id="ed22d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed22d-112">-DefaultProfile</span></span>
<span data-ttu-id="ed22d-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ed22d-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed22d-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ed22d-114">-DisplayName</span></span>
<span data-ttu-id="ed22d-115">A felhasználó címjegyzékében megjelenítendő név.</span><span class="sxs-lookup"><span data-stu-id="ed22d-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="ed22d-116">Példa: ' Alex Wu '.</span><span class="sxs-lookup"><span data-stu-id="ed22d-116">example 'Alex Wu'.</span></span>

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

### <span data-ttu-id="ed22d-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="ed22d-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="ed22d-118">Meg kell adni, ha a felhasználónak módosítania kell a jelszavát a következő sikeres bejelentkezéskor (igaz).</span><span class="sxs-lookup"><span data-stu-id="ed22d-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="ed22d-119">Az alapértelmezett viselkedés (hamis) a következő sikeres bejelentkezéskor nem módosíthatja a jelszót.</span><span class="sxs-lookup"><span data-stu-id="ed22d-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="ed22d-120">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="ed22d-120">-ImmutableId</span></span>
<span data-ttu-id="ed22d-121">Csak akkor kell megadni, ha a felhasználó egyszerű felhasználónevét (UPN-tulajdonságát) összevont tartománnyal használja.</span><span class="sxs-lookup"><span data-stu-id="ed22d-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

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

### <span data-ttu-id="ed22d-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="ed22d-122">-MailNickname</span></span>
<span data-ttu-id="ed22d-123">A felhasználó levelezési aliasa.</span><span class="sxs-lookup"><span data-stu-id="ed22d-123">The mail alias for the user.</span></span>

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

### <span data-ttu-id="ed22d-124">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="ed22d-124">-Password</span></span>
<span data-ttu-id="ed22d-125">A felhasználó jelszava.</span><span class="sxs-lookup"><span data-stu-id="ed22d-125">Password for the user.</span></span>
<span data-ttu-id="ed22d-126">Meg kell felelnie a bérlő jelszó-bonyolultsági követelményeinek.</span><span class="sxs-lookup"><span data-stu-id="ed22d-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="ed22d-127">Ajánlott egy erős jelszó beállítása.</span><span class="sxs-lookup"><span data-stu-id="ed22d-127">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="ed22d-128">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ed22d-128">-UserPrincipalName</span></span>
<span data-ttu-id="ed22d-129">A felhasználó egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="ed22d-129">The user principal name.</span></span>
<span data-ttu-id="ed22d-130">Példa-' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="ed22d-130">Example-'someuser@contoso.com'.</span></span>

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

### <span data-ttu-id="ed22d-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ed22d-131">-Confirm</span></span>
<span data-ttu-id="ed22d-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ed22d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed22d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed22d-133">-WhatIf</span></span>
<span data-ttu-id="ed22d-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ed22d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed22d-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ed22d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed22d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed22d-136">CommonParameters</span></span>
<span data-ttu-id="ed22d-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ed22d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed22d-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed22d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed22d-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed22d-139">INPUTS</span></span>

### <span data-ttu-id="ed22d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ed22d-140">System.String</span></span>

### <span data-ttu-id="ed22d-141">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="ed22d-141">System.Security.SecureString</span></span>

### <span data-ttu-id="ed22d-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ed22d-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ed22d-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed22d-143">OUTPUTS</span></span>

### <span data-ttu-id="ed22d-144">Microsoft. Azure. Command. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="ed22d-144">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="ed22d-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ed22d-145">NOTES</span></span>

## <span data-ttu-id="ed22d-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed22d-146">RELATED LINKS</span></span>

[<span data-ttu-id="ed22d-147">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="ed22d-147">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="ed22d-148">Set-AzADUser</span><span class="sxs-lookup"><span data-stu-id="ed22d-148">Set-AzADUser</span></span>](./Set-AzADUser.md)

[<span data-ttu-id="ed22d-149">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="ed22d-149">Remove-AzADUser</span></span>](./Remove-AzADUser.md)
