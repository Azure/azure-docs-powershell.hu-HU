---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
ms.openlocfilehash: ec9c234a03180f20b1b0cf6a4f5004923f3eab51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504755"
---
# <span data-ttu-id="6d3cc-101">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="6d3cc-101">New-AzureRmADUser</span></span>

## <span data-ttu-id="6d3cc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6d3cc-102">SYNOPSIS</span></span>
<span data-ttu-id="6d3cc-103">Új Active Directory-felhasználó létrehozása.</span><span class="sxs-lookup"><span data-stu-id="6d3cc-103">Creates a new active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d3cc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6d3cc-104">SYNTAX</span></span>

```
New-AzureRmADUser -DisplayName <String> -UserPrincipalName <String> -Password <String> [-ImmutableId <String>]
 [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d3cc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6d3cc-105">DESCRIPTION</span></span>
<span data-ttu-id="6d3cc-106">Új Active Directory-felhasználó létrehozása (munkahelyi/iskolai fiók is ismert a szervezeti azonosító néven ismert).</span><span class="sxs-lookup"><span data-stu-id="6d3cc-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="6d3cc-107">További információ: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="6d3cc-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="6d3cc-108">Példák</span><span class="sxs-lookup"><span data-stu-id="6d3cc-108">EXAMPLES</span></span>

### <span data-ttu-id="6d3cc-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6d3cc-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="6d3cc-110">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="6d3cc-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="6d3cc-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6d3cc-111">PARAMETERS</span></span>

### <span data-ttu-id="6d3cc-112">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6d3cc-112">-DisplayName</span></span>
<span data-ttu-id="6d3cc-113">A felhasználó címjegyzékében megjelenítendő név.</span><span class="sxs-lookup"><span data-stu-id="6d3cc-113">The name to display in the address book for the user.</span></span>
<span data-ttu-id="6d3cc-114">Példa: ' Alex Wu '.</span><span class="sxs-lookup"><span data-stu-id="6d3cc-114">example 'Alex Wu'.</span></span>

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

### <span data-ttu-id="6d3cc-115">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="6d3cc-115">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="6d3cc-116">Meg kell adni, ha a felhasználónak módosítania kell a jelszavát a következő sikeres bejelentkezéskor (igaz).</span><span class="sxs-lookup"><span data-stu-id="6d3cc-116">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="6d3cc-117">Az alapértelmezett viselkedés (hamis) a következő sikeres bejelentkezéskor nem módosíthatja a jelszót.</span><span class="sxs-lookup"><span data-stu-id="6d3cc-117">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="6d3cc-118">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="6d3cc-118">-ImmutableId</span></span>
<span data-ttu-id="6d3cc-119">Csak akkor kell megadni, ha a felhasználó egyszerű felhasználónevét (UPN-tulajdonságát) összevont tartománnyal használja.</span><span class="sxs-lookup"><span data-stu-id="6d3cc-119">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

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

### <span data-ttu-id="6d3cc-120">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="6d3cc-120">-Password</span></span>
<span data-ttu-id="6d3cc-121">A felhasználó jelszava.</span><span class="sxs-lookup"><span data-stu-id="6d3cc-121">Password for the user.</span></span>
<span data-ttu-id="6d3cc-122">Meg kell felelnie a bérlő jelszó-bonyolultsági követelményeinek.</span><span class="sxs-lookup"><span data-stu-id="6d3cc-122">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="6d3cc-123">Ajánlott egy erős jelszó beállítása.</span><span class="sxs-lookup"><span data-stu-id="6d3cc-123">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="6d3cc-124">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="6d3cc-124">-UserPrincipalName</span></span>
<span data-ttu-id="6d3cc-125">A felhasználó egyszerű felhasználóneve.</span><span class="sxs-lookup"><span data-stu-id="6d3cc-125">The user principal name.</span></span>
<span data-ttu-id="6d3cc-126">Példa-' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="6d3cc-126">Example-'someuser@contoso.com'.</span></span>

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

### <span data-ttu-id="6d3cc-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6d3cc-127">-Confirm</span></span>
<span data-ttu-id="6d3cc-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6d3cc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d3cc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d3cc-129">-WhatIf</span></span>
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

### <span data-ttu-id="6d3cc-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d3cc-130">-DefaultProfile</span></span>
<span data-ttu-id="6d3cc-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6d3cc-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d3cc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d3cc-132">CommonParameters</span></span>
<span data-ttu-id="6d3cc-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6d3cc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d3cc-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d3cc-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d3cc-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d3cc-135">INPUTS</span></span>

## <span data-ttu-id="6d3cc-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d3cc-136">OUTPUTS</span></span>

### <span data-ttu-id="6d3cc-137">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="6d3cc-137">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="6d3cc-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6d3cc-138">NOTES</span></span>

## <span data-ttu-id="6d3cc-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d3cc-139">RELATED LINKS</span></span>

[<span data-ttu-id="6d3cc-140">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="6d3cc-140">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="6d3cc-141">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="6d3cc-141">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="6d3cc-142">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="6d3cc-142">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)
