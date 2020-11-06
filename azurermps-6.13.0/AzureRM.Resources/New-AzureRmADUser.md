---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
ms.openlocfilehash: 27b52e6b3cf58f530e15b2ddd2ff3873087dfc2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493956"
---
# <span data-ttu-id="d637b-101">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="d637b-101">New-AzureRmADUser</span></span>

## <span data-ttu-id="d637b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d637b-102">SYNOPSIS</span></span>
<span data-ttu-id="d637b-103">Új Active Directory-felhasználó létrehozása.</span><span class="sxs-lookup"><span data-stu-id="d637b-103">Creates a new active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d637b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d637b-104">SYNTAX</span></span>

```
New-AzureRmADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString>
 [-ImmutableId <String>] [-MailNickname <String>] [-ForceChangePasswordNextLogin]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d637b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d637b-105">DESCRIPTION</span></span>
<span data-ttu-id="d637b-106">Új Active Directory-felhasználó létrehozása (munkahelyi/iskolai fiók is ismert a szervezeti azonosító néven ismert).</span><span class="sxs-lookup"><span data-stu-id="d637b-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="d637b-107">További információ: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="d637b-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="d637b-108">Példák</span><span class="sxs-lookup"><span data-stu-id="d637b-108">EXAMPLES</span></span>

### <span data-ttu-id="d637b-109">Példa 1 – új AD-felhasználó létrehozása</span><span class="sxs-lookup"><span data-stu-id="d637b-109">Example 1 - Create a new AD user</span></span>
```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzureRmADUser -DisplayName "MyDisplayName" -UserPrincipalName "myemail@domain.com" -Password $SecureStringPassword -MailNickname "MyMailNickName"
```

<span data-ttu-id="d637b-110">Új AD-felhasználó létrehozása a "MyDisplayName" és a "" "nevű felhasználó nevében a myemail@domain.com bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="d637b-110">Creates a new AD user with the name "MyDisplayName" and user principal name "myemail@domain.com" in a tenant.</span></span>

## <span data-ttu-id="d637b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d637b-111">PARAMETERS</span></span>

### <span data-ttu-id="d637b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d637b-112">-DefaultProfile</span></span>
<span data-ttu-id="d637b-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d637b-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d637b-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d637b-114">-DisplayName</span></span>
<span data-ttu-id="d637b-115">A felhasználó címjegyzékében megjelenítendő név.</span><span class="sxs-lookup"><span data-stu-id="d637b-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="d637b-116">Példa: ' Alex Wu '.</span><span class="sxs-lookup"><span data-stu-id="d637b-116">example 'Alex Wu'.</span></span>

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

### <span data-ttu-id="d637b-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="d637b-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="d637b-118">Meg kell adni, ha a felhasználónak módosítania kell a jelszavát a következő sikeres bejelentkezéskor (igaz).</span><span class="sxs-lookup"><span data-stu-id="d637b-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="d637b-119">Az alapértelmezett viselkedés (hamis) a következő sikeres bejelentkezéskor nem módosíthatja a jelszót.</span><span class="sxs-lookup"><span data-stu-id="d637b-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="d637b-120">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="d637b-120">-ImmutableId</span></span>
<span data-ttu-id="d637b-121">Csak akkor kell megadni, ha a felhasználó egyszerű felhasználónevét (UPN-tulajdonságát) összevont tartománnyal használja.</span><span class="sxs-lookup"><span data-stu-id="d637b-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

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

### <span data-ttu-id="d637b-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="d637b-122">-MailNickname</span></span>
<span data-ttu-id="d637b-123">A felhasználó levelezési aliasa.</span><span class="sxs-lookup"><span data-stu-id="d637b-123">The mail alias for the user.</span></span>

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

### <span data-ttu-id="d637b-124">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="d637b-124">-Password</span></span>
<span data-ttu-id="d637b-125">A felhasználó jelszava.</span><span class="sxs-lookup"><span data-stu-id="d637b-125">Password for the user.</span></span>
<span data-ttu-id="d637b-126">Meg kell felelnie a bérlő jelszó-bonyolultsági követelményeinek.</span><span class="sxs-lookup"><span data-stu-id="d637b-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="d637b-127">Ajánlott egy erős jelszó beállítása.</span><span class="sxs-lookup"><span data-stu-id="d637b-127">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="d637b-128">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d637b-128">-UserPrincipalName</span></span>
<span data-ttu-id="d637b-129">A felhasználó egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="d637b-129">The user principal name.</span></span>
<span data-ttu-id="d637b-130">Példa-' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="d637b-130">Example-'someuser@contoso.com'.</span></span>

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

### <span data-ttu-id="d637b-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d637b-131">-Confirm</span></span>
<span data-ttu-id="d637b-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d637b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d637b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d637b-133">-WhatIf</span></span>
<span data-ttu-id="d637b-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d637b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d637b-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d637b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d637b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d637b-136">CommonParameters</span></span>
<span data-ttu-id="d637b-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d637b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d637b-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d637b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d637b-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d637b-139">INPUTS</span></span>

### <span data-ttu-id="d637b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d637b-140">System.String</span></span>

### <span data-ttu-id="d637b-141">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="d637b-141">System.Security.SecureString</span></span>

### <span data-ttu-id="d637b-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d637b-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d637b-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d637b-143">OUTPUTS</span></span>

### <span data-ttu-id="d637b-144">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="d637b-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="d637b-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d637b-145">NOTES</span></span>

## <span data-ttu-id="d637b-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d637b-146">RELATED LINKS</span></span>

[<span data-ttu-id="d637b-147">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="d637b-147">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="d637b-148">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="d637b-148">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="d637b-149">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="d637b-149">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)
