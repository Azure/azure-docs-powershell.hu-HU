---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 388D4173-A937-42FA-81CB-C4A27F9D0B04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
ms.openlocfilehash: 325f134baf860b728aec3f144d9c9cf455c6b4ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492195"
---
# <span data-ttu-id="10b24-101">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="10b24-101">Set-AzureRmADUser</span></span>

## <span data-ttu-id="10b24-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="10b24-102">SYNOPSIS</span></span>
<span data-ttu-id="10b24-103">Frissít egy meglévő Active Directory-felhasználót.</span><span class="sxs-lookup"><span data-stu-id="10b24-103">Updates an existing active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10b24-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="10b24-104">SYNTAX</span></span>

```
Set-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10b24-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="10b24-105">DESCRIPTION</span></span>
<span data-ttu-id="10b24-106">Frissít egy meglévő Active Directory-felhasználó (munkahelyi/iskolai fiók is ismert, mint a szervezeti azonosító).</span><span class="sxs-lookup"><span data-stu-id="10b24-106">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="10b24-107">További információ: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="10b24-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="10b24-108">Példák</span><span class="sxs-lookup"><span data-stu-id="10b24-108">EXAMPLES</span></span>

### <span data-ttu-id="10b24-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="10b24-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="10b24-110">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="10b24-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="10b24-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="10b24-111">PARAMETERS</span></span>

### <span data-ttu-id="10b24-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10b24-112">-DefaultProfile</span></span>
<span data-ttu-id="10b24-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="10b24-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10b24-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="10b24-114">-DisplayName</span></span>
<span data-ttu-id="10b24-115">A felhasználó címjegyzékében megjelenítendő új név.</span><span class="sxs-lookup"><span data-stu-id="10b24-115">New name to display in the address book for the user.</span></span>
<span data-ttu-id="10b24-116">Példa – 'Alex Wu '.</span><span class="sxs-lookup"><span data-stu-id="10b24-116">Example-'Alex Wu'.</span></span>

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

### <span data-ttu-id="10b24-117">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="10b24-117">-EnableAccount</span></span>
<span data-ttu-id="10b24-118">True a fiók engedélyezéséhez; egyéb esetben false.</span><span class="sxs-lookup"><span data-stu-id="10b24-118">True for enabling the account; otherwise, false.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10b24-119">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="10b24-119">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="10b24-120">A jelszót csak a jelszó frissítésekor kell megadni.</span><span class="sxs-lookup"><span data-stu-id="10b24-120">It must be specified only when you are updating the password.</span></span>
<span data-ttu-id="10b24-121">Egyéb esetben a program figyelmen kívül hagyja.</span><span class="sxs-lookup"><span data-stu-id="10b24-121">Otherwise it will be ignored.</span></span>
<span data-ttu-id="10b24-122">Meg kell adni, ha a felhasználónak módosítania kell a jelszavát a következő sikeres bejelentkezéskor (igaz).</span><span class="sxs-lookup"><span data-stu-id="10b24-122">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="10b24-123">Az alapértelmezett viselkedés (hamis) a következő sikeres bejelentkezéskor nem módosíthatja a jelszót.</span><span class="sxs-lookup"><span data-stu-id="10b24-123">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="10b24-124">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="10b24-124">-Password</span></span>
<span data-ttu-id="10b24-125">Új jelszó a felhasználó számára.</span><span class="sxs-lookup"><span data-stu-id="10b24-125">New password for the user.</span></span>
<span data-ttu-id="10b24-126">Meg kell felelnie a bérlő jelszó-bonyolultsági követelményeinek.</span><span class="sxs-lookup"><span data-stu-id="10b24-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="10b24-127">Ajánlott egy erős jelszó beállítása.</span><span class="sxs-lookup"><span data-stu-id="10b24-127">It is recommended to set a strong password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10b24-128">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="10b24-128">-UPNOrObjectId</span></span>
<span data-ttu-id="10b24-129">A felhasználó egyszerű felhasználóneve (például ' someuser@contoso.com ') vagy annak a felhasználónak a objectId, akinek a tulajdonságokat frissíteni kell.</span><span class="sxs-lookup"><span data-stu-id="10b24-129">The user principal name (e.g. 'someuser@contoso.com') or the objectId of the user for which the properties need to be updated.</span></span>

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

### <span data-ttu-id="10b24-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="10b24-130">-Confirm</span></span>
<span data-ttu-id="10b24-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="10b24-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10b24-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10b24-132">-WhatIf</span></span>
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

### <span data-ttu-id="10b24-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10b24-133">CommonParameters</span></span>
<span data-ttu-id="10b24-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="10b24-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10b24-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10b24-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10b24-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="10b24-136">INPUTS</span></span>

### <span data-ttu-id="10b24-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="10b24-137">None</span></span>
<span data-ttu-id="10b24-138">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="10b24-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="10b24-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10b24-139">OUTPUTS</span></span>

### <span data-ttu-id="10b24-140">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="10b24-140">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="10b24-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="10b24-141">NOTES</span></span>

## <span data-ttu-id="10b24-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10b24-142">RELATED LINKS</span></span>

[<span data-ttu-id="10b24-143">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="10b24-143">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="10b24-144">Új – AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="10b24-144">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="10b24-145">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="10b24-145">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

