---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadgroupmember
schema: 2.0.0
ms.openlocfilehash: 3b1af5134147ad099547d95fdf5dbf79850e464a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848089"
---
# <span data-ttu-id="1ba3e-101">Remove-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="1ba3e-101">Remove-AzureRmADGroupMember</span></span>

## <span data-ttu-id="1ba3e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1ba3e-102">SYNOPSIS</span></span>
<span data-ttu-id="1ba3e-103">Felhasználó eltávolítása egy HIRDETÉSCSOPORT-csoportból.</span><span class="sxs-lookup"><span data-stu-id="1ba3e-103">Removes a user from an AD group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ba3e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1ba3e-104">SYNTAX</span></span>

### <span data-ttu-id="1ba3e-105">ExplicitParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1ba3e-105">ExplicitParameterSet (Default)</span></span>
```
Remove-AzureRmADGroupMember [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1ba3e-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="1ba3e-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Remove-AzureRmADGroupMember -MemberObjectId <Guid[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ba3e-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="1ba3e-107">MemberObjectIdWithGroupObject</span></span>
```
Remove-AzureRmADGroupMember -MemberObjectId <Guid[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ba3e-108">MemberObjectIdWithGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="1ba3e-108">MemberObjectIdWithGroupObjectId</span></span>
```
Remove-AzureRmADGroupMember -MemberObjectId <Guid[]> -GroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ba3e-109">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ba3e-109">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Remove-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ba3e-110">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ba3e-110">MemberUPNWithGroupObjectParameterSet</span></span>
```
Remove-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ba3e-111">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ba3e-111">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Remove-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -GroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ba3e-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="1ba3e-112">DESCRIPTION</span></span>
<span data-ttu-id="1ba3e-113">Felhasználó eltávolítása egy HIRDETÉSCSOPORT-csoportból.</span><span class="sxs-lookup"><span data-stu-id="1ba3e-113">Removes a user from an AD group.</span></span>

## <span data-ttu-id="1ba3e-114">Példák</span><span class="sxs-lookup"><span data-stu-id="1ba3e-114">EXAMPLES</span></span>

### <span data-ttu-id="1ba3e-115">Példa 1 – felhasználó eltávolítása a csoportból objektum-azonosító alapján</span><span class="sxs-lookup"><span data-stu-id="1ba3e-115">Example 1 - Remove a user from a group by object id</span></span>

```
PS C:\> Remove-AzureRmADGroup -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="1ba3e-116">A "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" azonosítójú felhasználó eltávolítása a "85F89C90-780E-4AA6-9F4F-6F268D322EEE" azonosítójú csoportból.</span><span class="sxs-lookup"><span data-stu-id="1ba3e-116">Removes the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' from the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="1ba3e-117">2. példa – felhasználó eltávolítása egy csoportból csővezetékről</span><span class="sxs-lookup"><span data-stu-id="1ba3e-117">Example 2 - Remove a user from a group by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzureRmADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="1ba3e-118">Beilleszti az "85F89C90-780E-4AA6-9F4F-6F268D322EEE" azonosítójú csoportot, és a Remove-AzureRmADGroupMember parancsmaghoz illeszti a felhasználót a csoportba.</span><span class="sxs-lookup"><span data-stu-id="1ba3e-118">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Remove-AzureRmADGroupMember cmdlet to remove the user to that group.</span></span>

## <span data-ttu-id="1ba3e-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1ba3e-119">PARAMETERS</span></span>

### <span data-ttu-id="1ba3e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ba3e-120">-DefaultProfile</span></span>
<span data-ttu-id="1ba3e-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1ba3e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ba3e-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="1ba3e-122">-GroupDisplayName</span></span>
<span data-ttu-id="1ba3e-123">Annak a csoportnak a megjelenítendő neve, amelyből el szeretné távolítani a tagot (ka) t.</span><span class="sxs-lookup"><span data-stu-id="1ba3e-123">The display name of the group to remove the member(s) from.</span></span>

```yaml
Type: System.String
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberUPNWithGroupDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ba3e-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="1ba3e-124">-GroupObject</span></span>
<span data-ttu-id="1ba3e-125">A Csoport objektumát ábrázoló objektum a tagok eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="1ba3e-125">The object representation of the group to remove the member from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: MemberObjectIdWithGroupObject, MemberUPNWithGroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ba3e-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="1ba3e-126">-GroupObjectId</span></span>
<span data-ttu-id="1ba3e-127">Annak a csoportnak az objektum azonosítója, amelyből a tagot el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="1ba3e-127">The object id of the group to remove the member from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ba3e-128">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="1ba3e-128">-MemberObjectId</span></span>
<span data-ttu-id="1ba3e-129">A tag objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1ba3e-129">The object id of the member.</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject, MemberObjectIdWithGroupObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ba3e-130">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="1ba3e-130">-MemberUserPrincipalName</span></span>
<span data-ttu-id="1ba3e-131">Az eltávolítandó tag (ok) UPN-címe.</span><span class="sxs-lookup"><span data-stu-id="1ba3e-131">The UPN of the member(s) to remove.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberUPNWithGroupDisplayNameParameterSet, MemberUPNWithGroupObjectParameterSet, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ba3e-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ba3e-132">-PassThru</span></span>
<span data-ttu-id="1ba3e-133">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="1ba3e-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="1ba3e-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1ba3e-134">-Confirm</span></span>
<span data-ttu-id="1ba3e-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1ba3e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ba3e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ba3e-136">-WhatIf</span></span>
<span data-ttu-id="1ba3e-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1ba3e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ba3e-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1ba3e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ba3e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ba3e-139">CommonParameters</span></span>
<span data-ttu-id="1ba3e-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1ba3e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ba3e-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ba3e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ba3e-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ba3e-142">INPUTS</span></span>

### <span data-ttu-id="1ba3e-143">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="1ba3e-143">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="1ba3e-144">Paraméterek: GroupObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1ba3e-144">Parameters: GroupObject (ByValue)</span></span>

## <span data-ttu-id="1ba3e-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ba3e-145">OUTPUTS</span></span>

### <span data-ttu-id="1ba3e-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1ba3e-146">System.Boolean</span></span>

## <span data-ttu-id="1ba3e-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1ba3e-147">NOTES</span></span>

## <span data-ttu-id="1ba3e-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ba3e-148">RELATED LINKS</span></span>
