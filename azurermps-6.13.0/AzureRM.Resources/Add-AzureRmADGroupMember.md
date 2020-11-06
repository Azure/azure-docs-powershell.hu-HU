---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/add-azurermadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Add-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Add-AzureRmADGroupMember.md
ms.openlocfilehash: 333a56a59c28482c2da228e3e9c0f8c2f1c21f06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493962"
---
# <span data-ttu-id="9638e-101">Add-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="9638e-101">Add-AzureRmADGroupMember</span></span>

## <span data-ttu-id="9638e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9638e-102">SYNOPSIS</span></span>
<span data-ttu-id="9638e-103">Felhasználó felvétele egy meglévő HIRDETÉSCSOPORT-csoportba.</span><span class="sxs-lookup"><span data-stu-id="9638e-103">Adds a user to an existing AD group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9638e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9638e-104">SYNTAX</span></span>

### <span data-ttu-id="9638e-105">MemberObjectIdWithGroupObjectId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9638e-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzureRmADGroupMember -MemberObjectId <Guid[]> -TargetGroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9638e-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="9638e-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzureRmADGroupMember -MemberObjectId <Guid[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9638e-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="9638e-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzureRmADGroupMember -MemberObjectId <Guid[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9638e-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9638e-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9638e-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9638e-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9638e-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9638e-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9638e-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="9638e-111">DESCRIPTION</span></span>
<span data-ttu-id="9638e-112">Felhasználó felvétele egy meglévő HIRDETÉSCSOPORT-csoportba.</span><span class="sxs-lookup"><span data-stu-id="9638e-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="9638e-113">Példák</span><span class="sxs-lookup"><span data-stu-id="9638e-113">EXAMPLES</span></span>

### <span data-ttu-id="9638e-114">Példa 1 – felhasználó felvétele a csoportba objektum-azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="9638e-114">Example 1 - Add a user to a group by object id</span></span>

```
PS C:\> Add-AzureRmADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="9638e-115">A "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" azonosítójú felhasználó felvétele a "85F89C90-780E-4AA6-9F4F-6F268D322EEE" azonosítójú csoportba.</span><span class="sxs-lookup"><span data-stu-id="9638e-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="9638e-116">2. példa – felhasználó felvétele egy csoportba csővezetékekkel</span><span class="sxs-lookup"><span data-stu-id="9638e-116">Example 2 - Add a user to a group by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzureRmADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="9638e-117">Beilleszti az "85F89C90-780E-4AA6-9F4F-6F268D322EEE" azonosítójú csoportot, és a Add-AzureRmADGroupMember parancsmagba beilleszti a felhasználót a csoportba.</span><span class="sxs-lookup"><span data-stu-id="9638e-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzureRmADGroupMember cmdlet to add the user to that group.</span></span>

## <span data-ttu-id="9638e-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9638e-118">PARAMETERS</span></span>

### <span data-ttu-id="9638e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9638e-119">-DefaultProfile</span></span>
<span data-ttu-id="9638e-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9638e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9638e-121">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="9638e-121">-MemberObjectId</span></span>
<span data-ttu-id="9638e-122">A tag objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9638e-122">The object id of the member.</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9638e-123">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="9638e-123">-MemberUserPrincipalName</span></span>
<span data-ttu-id="9638e-124">A csoportba felvenni kívánt tag (ok) UPN-címe.</span><span class="sxs-lookup"><span data-stu-id="9638e-124">The UPN of the member(s) to add to the group.</span></span>

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

### <span data-ttu-id="9638e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9638e-125">-PassThru</span></span>
<span data-ttu-id="9638e-126">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="9638e-126">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="9638e-127">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="9638e-127">-TargetGroupDisplayName</span></span>
<span data-ttu-id="9638e-128">Annak a csoportnak a megjelenítendő neve, amelybe fel szeretné venni a tag (oka) t.</span><span class="sxs-lookup"><span data-stu-id="9638e-128">The display name of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="9638e-129">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="9638e-129">-TargetGroupObject</span></span>
<span data-ttu-id="9638e-130">A csoport objektum-ábrázolása a tagok (ok) hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="9638e-130">The object representation of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="9638e-131">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="9638e-131">-TargetGroupObjectId</span></span>
<span data-ttu-id="9638e-132">Annak a csoportnak az objektum azonosítója, amelyhez hozzá szeretné adni a tag (oka) t.</span><span class="sxs-lookup"><span data-stu-id="9638e-132">The object id of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="9638e-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9638e-133">-Confirm</span></span>
<span data-ttu-id="9638e-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9638e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9638e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9638e-135">-WhatIf</span></span>
<span data-ttu-id="9638e-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9638e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9638e-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9638e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9638e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9638e-138">CommonParameters</span></span>
<span data-ttu-id="9638e-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9638e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9638e-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9638e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9638e-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9638e-141">INPUTS</span></span>

### <span data-ttu-id="9638e-142">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="9638e-142">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="9638e-143">Paraméterek: TargetGroupObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9638e-143">Parameters: TargetGroupObject (ByValue)</span></span>

## <span data-ttu-id="9638e-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9638e-144">OUTPUTS</span></span>

### <span data-ttu-id="9638e-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9638e-145">System.Boolean</span></span>

## <span data-ttu-id="9638e-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9638e-146">NOTES</span></span>

## <span data-ttu-id="9638e-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9638e-147">RELATED LINKS</span></span>
