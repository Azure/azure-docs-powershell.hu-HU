---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 388D4173-A937-42FA-81CB-C4A27F9D0B04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
ms.openlocfilehash: 9d65ed2f6bbc2e26c4e91916cc42bf2954c08252
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672195"
---
# <span data-ttu-id="642a6-101">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="642a6-101">Set-AzureRmADUser</span></span>

## <span data-ttu-id="642a6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="642a6-102">SYNOPSIS</span></span>
<span data-ttu-id="642a6-103">Frissít egy meglévő Active Directory-felhasználót.</span><span class="sxs-lookup"><span data-stu-id="642a6-103">Updates an existing active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="642a6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="642a6-104">SYNTAX</span></span>

```
Set-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <String>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="642a6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="642a6-105">DESCRIPTION</span></span>
<span data-ttu-id="642a6-106">Frissít egy meglévő Active Directory-felhasználó (munkahelyi/iskolai fiók is ismert, mint a szervezeti azonosító).</span><span class="sxs-lookup"><span data-stu-id="642a6-106">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="642a6-107">További információ: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="642a6-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="642a6-108">Példák</span><span class="sxs-lookup"><span data-stu-id="642a6-108">EXAMPLES</span></span>

### <span data-ttu-id="642a6-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="642a6-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="642a6-110">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="642a6-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="642a6-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="642a6-111">PARAMETERS</span></span>

### <span data-ttu-id="642a6-112">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="642a6-112">-DisplayName</span></span>
<span data-ttu-id="642a6-113">A felhasználó címjegyzékében megjelenítendő új név.</span><span class="sxs-lookup"><span data-stu-id="642a6-113">New name to display in the address book for the user.</span></span>
<span data-ttu-id="642a6-114">Példa – 'Alex Wu '.</span><span class="sxs-lookup"><span data-stu-id="642a6-114">Example-'Alex Wu'.</span></span>

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

### <span data-ttu-id="642a6-115">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="642a6-115">-EnableAccount</span></span>
<span data-ttu-id="642a6-116">True a fiók engedélyezéséhez; egyéb esetben false.</span><span class="sxs-lookup"><span data-stu-id="642a6-116">True for enabling the account; otherwise, false.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="642a6-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="642a6-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="642a6-118">A jelszót csak a jelszó frissítésekor kell megadni.</span><span class="sxs-lookup"><span data-stu-id="642a6-118">It must be specified only when you are updating the password.</span></span>
<span data-ttu-id="642a6-119">Egyéb esetben a program figyelmen kívül hagyja.</span><span class="sxs-lookup"><span data-stu-id="642a6-119">Otherwise it will be ignored.</span></span>
<span data-ttu-id="642a6-120">Meg kell adni, ha a felhasználónak módosítania kell a jelszavát a következő sikeres bejelentkezéskor (igaz).</span><span class="sxs-lookup"><span data-stu-id="642a6-120">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="642a6-121">Az alapértelmezett viselkedés (hamis) a következő sikeres bejelentkezéskor nem módosíthatja a jelszót.</span><span class="sxs-lookup"><span data-stu-id="642a6-121">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="642a6-122">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="642a6-122">-Password</span></span>
<span data-ttu-id="642a6-123">Új jelszó a felhasználó számára.</span><span class="sxs-lookup"><span data-stu-id="642a6-123">New password for the user.</span></span>
<span data-ttu-id="642a6-124">Meg kell felelnie a bérlő jelszó-bonyolultsági követelményeinek.</span><span class="sxs-lookup"><span data-stu-id="642a6-124">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="642a6-125">Ajánlott egy erős jelszó beállítása.</span><span class="sxs-lookup"><span data-stu-id="642a6-125">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="642a6-126">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="642a6-126">-UPNOrObjectId</span></span>
<span data-ttu-id="642a6-127">A felhasználó egyszerű felhasználóneve (például ' someuser@contoso.com ') vagy annak a felhasználónak a objectId, akinek a tulajdonságokat frissíteni kell.</span><span class="sxs-lookup"><span data-stu-id="642a6-127">The user principal name (e.g. 'someuser@contoso.com') or the objectId of the user for which the properties need to be updated.</span></span>

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

### <span data-ttu-id="642a6-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="642a6-128">-Confirm</span></span>
<span data-ttu-id="642a6-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="642a6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="642a6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="642a6-130">-WhatIf</span></span>
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

### <span data-ttu-id="642a6-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="642a6-131">-DefaultProfile</span></span>
<span data-ttu-id="642a6-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="642a6-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="642a6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="642a6-133">CommonParameters</span></span>
<span data-ttu-id="642a6-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="642a6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="642a6-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="642a6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="642a6-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="642a6-136">INPUTS</span></span>

## <span data-ttu-id="642a6-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="642a6-137">OUTPUTS</span></span>

### <span data-ttu-id="642a6-138">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="642a6-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="642a6-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="642a6-139">NOTES</span></span>

## <span data-ttu-id="642a6-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="642a6-140">RELATED LINKS</span></span>

[<span data-ttu-id="642a6-141">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="642a6-141">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="642a6-142">Új – AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="642a6-142">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="642a6-143">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="642a6-143">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

