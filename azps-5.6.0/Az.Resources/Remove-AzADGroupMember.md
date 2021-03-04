---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
ms.openlocfilehash: 7cc64ad6d0f17666ac1e97ae00473907c53a5552
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920449"
---
# <span data-ttu-id="ba251-101">Remove-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="ba251-101">Remove-AzADGroupMember</span></span>

## <span data-ttu-id="ba251-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba251-102">SYNOPSIS</span></span>
<span data-ttu-id="ba251-103">Eltávolít egy felhasználót egy AD-csoportból.</span><span class="sxs-lookup"><span data-stu-id="ba251-103">Removes a user from an AD group.</span></span>

## <span data-ttu-id="ba251-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ba251-104">SYNTAX</span></span>

### <span data-ttu-id="ba251-105">ExplicitParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ba251-105">ExplicitParameterSet (Default)</span></span>
```
Remove-AzADGroupMember [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba251-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="ba251-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba251-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="ba251-107">MemberObjectIdWithGroupObject</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba251-108">MemberObjectIdWithGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="ba251-108">MemberObjectIdWithGroupObjectId</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba251-109">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba251-109">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba251-110">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba251-110">MemberUPNWithGroupObjectParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba251-111">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba251-111">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba251-112">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ba251-112">DESCRIPTION</span></span>
<span data-ttu-id="ba251-113">Eltávolít egy felhasználót egy AD-csoportból.</span><span class="sxs-lookup"><span data-stu-id="ba251-113">Removes a user from an AD group.</span></span>

## <span data-ttu-id="ba251-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ba251-114">EXAMPLES</span></span>

### <span data-ttu-id="ba251-115">1. példa: Felhasználó eltávolítása egy csoportból objektumazonosító alapján</span><span class="sxs-lookup"><span data-stu-id="ba251-115">Example 1: Remove a user from a group by object id</span></span>

```powershell
PS C:\> Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="ba251-116">Eltávolítja a "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" objektumazonosítójú felhasználót a "85F89C90-780E-4AA6-9F4F-6F268D322EEE" objektumazonosítóval.</span><span class="sxs-lookup"><span data-stu-id="ba251-116">Removes the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' from the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="ba251-117">2. példa: Felhasználó eltávolítása egy csoportból pipázás használatával</span><span class="sxs-lookup"><span data-stu-id="ba251-117">Example 2: Remove a user from a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="ba251-118">A (85F89C90-780E-4AA6-9F4F-6F268D322EEE) objektumazonosítót használó csoportot a Remove-AzADGroupMember-parancsmaghoz húzza, hogy a felhasználót eltávolítsa a csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="ba251-118">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Remove-AzADGroupMember cmdlet to remove the user to that group.</span></span>

## <span data-ttu-id="ba251-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba251-119">PARAMETERS</span></span>

### <span data-ttu-id="ba251-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba251-120">-DefaultProfile</span></span>
<span data-ttu-id="ba251-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ba251-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba251-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="ba251-122">-GroupDisplayName</span></span>
<span data-ttu-id="ba251-123">Annak a csoportnak a megjelenítendő neve, amelyből el szeretné távolítani a tag(ak)t.</span><span class="sxs-lookup"><span data-stu-id="ba251-123">The display name of the group to remove the member(s) from.</span></span>

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

### <span data-ttu-id="ba251-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="ba251-124">-GroupObject</span></span>
<span data-ttu-id="ba251-125">Annak a csoportnak az objektum reprezentációja, amelyből el szeretné távolítani a tagokat.</span><span class="sxs-lookup"><span data-stu-id="ba251-125">The object representation of the group to remove the member from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: MemberObjectIdWithGroupObject, MemberUPNWithGroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba251-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="ba251-126">-GroupObjectId</span></span>
<span data-ttu-id="ba251-127">Annak a csoportnak az objektumazonosítója, amelyből el szeretné távolítani a tagokat.</span><span class="sxs-lookup"><span data-stu-id="ba251-127">The object id of the group to remove the member from.</span></span>

```yaml
Type: System.String
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba251-128">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="ba251-128">-MemberObjectId</span></span>
<span data-ttu-id="ba251-129">A tag objektumazonosítója.</span><span class="sxs-lookup"><span data-stu-id="ba251-129">The object id of the member.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject, MemberObjectIdWithGroupObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba251-130">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ba251-130">-MemberUserPrincipalName</span></span>
<span data-ttu-id="ba251-131">Az eltávolítható tag(ak) upn-ja.</span><span class="sxs-lookup"><span data-stu-id="ba251-131">The UPN of the member(s) to remove.</span></span>

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

### <span data-ttu-id="ba251-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba251-132">-PassThru</span></span>
<span data-ttu-id="ba251-133">Ha megadja ezt a parancsot, az igaz értéket ad vissza, ha a parancs sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="ba251-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="ba251-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba251-134">-Confirm</span></span>
<span data-ttu-id="ba251-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ba251-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba251-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba251-136">-WhatIf</span></span>
<span data-ttu-id="ba251-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ba251-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba251-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ba251-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba251-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba251-139">CommonParameters</span></span>
<span data-ttu-id="ba251-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba251-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba251-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba251-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba251-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ba251-142">INPUTS</span></span>

### <span data-ttu-id="ba251-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="ba251-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="ba251-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba251-144">OUTPUTS</span></span>

### <span data-ttu-id="ba251-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ba251-145">System.Boolean</span></span>

## <span data-ttu-id="ba251-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ba251-146">NOTES</span></span>

## <span data-ttu-id="ba251-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba251-147">RELATED LINKS</span></span>
