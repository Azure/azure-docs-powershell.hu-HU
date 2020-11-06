---
external help file: Microsoft.Azure.Commands.ManagedServiceIdentity.dll-Help.xml
Module Name: AzureRM.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.managedserviceidentity/new-azurermuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/New-AzureRmUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/New-AzureRmUserAssignedIdentity.md
ms.openlocfilehash: 9f4bea5ce1eaad0096ed36628704d9406047d5f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497592"
---
# <span data-ttu-id="da335-101">New-AzureRmUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="da335-101">New-AzureRmUserAssignedIdentity</span></span>

## <span data-ttu-id="da335-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da335-102">SYNOPSIS</span></span>
<span data-ttu-id="da335-103">Egy új felhasználó által kiosztott identitást hoz létre, vagy egy meglévő, felhasználó által kiosztott identitást frissít.</span><span class="sxs-lookup"><span data-stu-id="da335-103">Creates a new User Assigned Identity or updates an existing User Assigned Identity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da335-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da335-104">SYNTAX</span></span>

```
New-AzureRmUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da335-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="da335-105">DESCRIPTION</span></span>
<span data-ttu-id="da335-106">A **New-AzureRmUserAssignedIdentity** parancsmag új felhasználó által kiosztott identitást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="da335-106">The **New-AzureRmUserAssignedIdentity** cmdlet creates a new User Assigned Identity.</span></span> <span data-ttu-id="da335-107">Ha egy már meglévő identitással használja, frissítette az identitást.</span><span class="sxs-lookup"><span data-stu-id="da335-107">When used with an already existing identity, it updated the identity.</span></span>
<span data-ttu-id="da335-108">Ha Azure Resource Manager címkét szeretne hozzáadni az identitáshoz, használja az Set-AzureRmResource parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="da335-108">To add Azure Resource Manager tags to the identity, please use the Set-AzureRmResource cmdlet.</span></span>

## <span data-ttu-id="da335-109">Példák</span><span class="sxs-lookup"><span data-stu-id="da335-109">EXAMPLES</span></span>

### <span data-ttu-id="da335-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="da335-110">Example 1</span></span>
<span data-ttu-id="da335-111">Ez a példa parancsmag létrehoz egy új felhasználóhoz rendelt identitást, amelynek neve **ID1** az erőforráscsoport **PSRG** a ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="da335-111">This example cmdlet creates a new User Assigned Identity with name **ID1** under resource group **PSRG** in the location of the ResourceGroup.</span></span>

```powershell
PS C:\> New-AzureRmUserAssignedIdentity -ResourceGroupName PSRG -Name ID1

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : centralus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

### <span data-ttu-id="da335-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="da335-112">Example 2</span></span>
<span data-ttu-id="da335-113">Ez a példa parancsmag létrehoz egy új felhasználóhoz rendelt identitást, amelynek neve **ID1** a westus terület erőforráscsoport **PSRG** .</span><span class="sxs-lookup"><span data-stu-id="da335-113">This example cmdlet creates a new User Assigned Identity with name **ID1** under the resource group **PSRG** in the westus region.</span></span>

```powershell
PS C:\> New-AzureRmUserAssignedIdentity -ResourceGroupName PSRG -Name ID1 -Location westus

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

## <span data-ttu-id="da335-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da335-114">PARAMETERS</span></span>

### <span data-ttu-id="da335-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da335-115">-AsJob</span></span>
<span data-ttu-id="da335-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="da335-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da335-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da335-117">-DefaultProfile</span></span>
<span data-ttu-id="da335-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da335-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da335-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="da335-119">-Location</span></span>
<span data-ttu-id="da335-120">Az Azure-régió neve, ahol az identitást létre kell tenni.</span><span class="sxs-lookup"><span data-stu-id="da335-120">The Azure region name where the Identity should be created.</span></span>

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

### <span data-ttu-id="da335-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="da335-121">-Name</span></span>
<span data-ttu-id="da335-122">Az identitás neve.</span><span class="sxs-lookup"><span data-stu-id="da335-122">The Identity name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da335-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da335-123">-ResourceGroupName</span></span>
<span data-ttu-id="da335-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="da335-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da335-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="da335-125">-Tag</span></span>
<span data-ttu-id="da335-126">Az Azure Resource Manager címkéi az identitáshoz társítva.</span><span class="sxs-lookup"><span data-stu-id="da335-126">The Azure Resource Manager tags associated with the identity.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da335-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="da335-127">-Confirm</span></span>
<span data-ttu-id="da335-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="da335-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da335-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da335-129">-WhatIf</span></span>
<span data-ttu-id="da335-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="da335-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da335-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="da335-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da335-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da335-132">CommonParameters</span></span>
<span data-ttu-id="da335-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da335-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da335-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da335-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da335-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da335-135">INPUTS</span></span>

### <span data-ttu-id="da335-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="da335-136">None</span></span>

## <span data-ttu-id="da335-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da335-137">OUTPUTS</span></span>

### <span data-ttu-id="da335-138">Microsoft. Azure. Command. ManagedServiceIdentity. models. PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="da335-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

## <span data-ttu-id="da335-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da335-139">NOTES</span></span>

## <span data-ttu-id="da335-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da335-140">RELATED LINKS</span></span>
