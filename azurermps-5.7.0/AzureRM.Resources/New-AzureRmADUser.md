---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
ms.openlocfilehash: 80a35ac1a1087d9e74cb47c3297af3ded491e701
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495262"
---
# <span data-ttu-id="815b6-101">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="815b6-101">New-AzureRmADUser</span></span>

## <span data-ttu-id="815b6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="815b6-102">SYNOPSIS</span></span>
<span data-ttu-id="815b6-103">Új Active Directory-felhasználó létrehozása.</span><span class="sxs-lookup"><span data-stu-id="815b6-103">Creates a new active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="815b6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="815b6-104">SYNTAX</span></span>

```
New-AzureRmADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString>
 [-ImmutableId <String>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="815b6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="815b6-105">DESCRIPTION</span></span>
<span data-ttu-id="815b6-106">Új Active Directory-felhasználó létrehozása (munkahelyi/iskolai fiók is ismert a szervezeti azonosító néven ismert).</span><span class="sxs-lookup"><span data-stu-id="815b6-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="815b6-107">További információ: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="815b6-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="815b6-108">Példák</span><span class="sxs-lookup"><span data-stu-id="815b6-108">EXAMPLES</span></span>

### <span data-ttu-id="815b6-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="815b6-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="815b6-110">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="815b6-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="815b6-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="815b6-111">PARAMETERS</span></span>

### <span data-ttu-id="815b6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="815b6-112">-DefaultProfile</span></span>
<span data-ttu-id="815b6-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="815b6-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="815b6-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="815b6-114">-DisplayName</span></span>
<span data-ttu-id="815b6-115">A felhasználó címjegyzékében megjelenítendő név.</span><span class="sxs-lookup"><span data-stu-id="815b6-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="815b6-116">Példa: ' Alex Wu '.</span><span class="sxs-lookup"><span data-stu-id="815b6-116">example 'Alex Wu'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="815b6-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="815b6-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="815b6-118">Meg kell adni, ha a felhasználónak módosítania kell a jelszavát a következő sikeres bejelentkezéskor (igaz).</span><span class="sxs-lookup"><span data-stu-id="815b6-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="815b6-119">Az alapértelmezett viselkedés (hamis) a következő sikeres bejelentkezéskor nem módosíthatja a jelszót.</span><span class="sxs-lookup"><span data-stu-id="815b6-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="815b6-120">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="815b6-120">-ImmutableId</span></span>
<span data-ttu-id="815b6-121">Csak akkor kell megadni, ha a felhasználó egyszerű felhasználónevét (UPN-tulajdonságát) összevont tartománnyal használja.</span><span class="sxs-lookup"><span data-stu-id="815b6-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="815b6-122">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="815b6-122">-Password</span></span>
<span data-ttu-id="815b6-123">A felhasználó jelszava.</span><span class="sxs-lookup"><span data-stu-id="815b6-123">Password for the user.</span></span>
<span data-ttu-id="815b6-124">Meg kell felelnie a bérlő jelszó-bonyolultsági követelményeinek.</span><span class="sxs-lookup"><span data-stu-id="815b6-124">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="815b6-125">Ajánlott egy erős jelszó beállítása.</span><span class="sxs-lookup"><span data-stu-id="815b6-125">It is recommended to set a strong password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="815b6-126">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="815b6-126">-UserPrincipalName</span></span>
<span data-ttu-id="815b6-127">A felhasználó egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="815b6-127">The user principal name.</span></span>
<span data-ttu-id="815b6-128">Példa-' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="815b6-128">Example-'someuser@contoso.com'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="815b6-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="815b6-129">-Confirm</span></span>
<span data-ttu-id="815b6-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="815b6-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="815b6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="815b6-131">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="815b6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="815b6-132">CommonParameters</span></span>
<span data-ttu-id="815b6-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="815b6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="815b6-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="815b6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="815b6-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="815b6-135">INPUTS</span></span>

### <span data-ttu-id="815b6-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="815b6-136">None</span></span>
<span data-ttu-id="815b6-137">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="815b6-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="815b6-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="815b6-138">OUTPUTS</span></span>

### <span data-ttu-id="815b6-139">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="815b6-139">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="815b6-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="815b6-140">NOTES</span></span>

## <span data-ttu-id="815b6-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="815b6-141">RELATED LINKS</span></span>

[<span data-ttu-id="815b6-142">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="815b6-142">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="815b6-143">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="815b6-143">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="815b6-144">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="815b6-144">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)
