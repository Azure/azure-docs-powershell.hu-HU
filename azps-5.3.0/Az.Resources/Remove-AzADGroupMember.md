---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
ms.openlocfilehash: 7450588905deeb900efbffffa253f5c06ae63272
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466418"
---
# <span data-ttu-id="6f821-101">Remove-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="6f821-101">Remove-AzADGroupMember</span></span>

## <span data-ttu-id="6f821-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f821-102">SYNOPSIS</span></span>
<span data-ttu-id="6f821-103">Eltávolít egy felhasználót egy AD-csoportból.</span><span class="sxs-lookup"><span data-stu-id="6f821-103">Removes a user from an AD group.</span></span>

## <span data-ttu-id="6f821-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6f821-104">SYNTAX</span></span>

### <span data-ttu-id="6f821-105">ExplicitParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6f821-105">ExplicitParameterSet (Default)</span></span>
```
Remove-AzADGroupMember [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f821-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="6f821-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f821-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="6f821-107">MemberObjectIdWithGroupObject</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f821-108">MemberObjectIdWithGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="6f821-108">MemberObjectIdWithGroupObjectId</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f821-109">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f821-109">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f821-110">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f821-110">MemberUPNWithGroupObjectParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f821-111">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f821-111">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f821-112">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6f821-112">DESCRIPTION</span></span>
<span data-ttu-id="6f821-113">Eltávolít egy felhasználót egy AD-csoportból.</span><span class="sxs-lookup"><span data-stu-id="6f821-113">Removes a user from an AD group.</span></span>

## <span data-ttu-id="6f821-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6f821-114">EXAMPLES</span></span>

### <span data-ttu-id="6f821-115">1. példa: Felhasználó eltávolítása egy csoportból objektumazonosító alapján</span><span class="sxs-lookup"><span data-stu-id="6f821-115">Example 1: Remove a user from a group by object id</span></span>

```powershell
PS C:\> Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="6f821-116">Eltávolítja a "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" objektumazonosítójú felhasználót a "85F89C90-780E-4AA6-9F4F-6F268D322EEE" objektumazonosítóval.</span><span class="sxs-lookup"><span data-stu-id="6f821-116">Removes the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' from the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="6f821-117">2. példa: Felhasználó eltávolítása egy csoportból pipázás használatával</span><span class="sxs-lookup"><span data-stu-id="6f821-117">Example 2: Remove a user from a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="6f821-118">A (85F89C90-780E-4AA6-9F4F-6F268D322EEE) objektumazonosítót használó csoportot a Remove-AzADGroupMember-parancsmaghoz húzza, hogy eltávolítsa a felhasználót a csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="6f821-118">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Remove-AzADGroupMember cmdlet to remove the user to that group.</span></span>

## <span data-ttu-id="6f821-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f821-119">PARAMETERS</span></span>

### <span data-ttu-id="6f821-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f821-120">-DefaultProfile</span></span>
<span data-ttu-id="6f821-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6f821-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f821-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="6f821-122">-GroupDisplayName</span></span>
<span data-ttu-id="6f821-123">Annak a csoportnak a megjelenítendő neve, amelyből el szeretné távolítani a tag(ak)t.</span><span class="sxs-lookup"><span data-stu-id="6f821-123">The display name of the group to remove the member(s) from.</span></span>

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

### <span data-ttu-id="6f821-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="6f821-124">-GroupObject</span></span>
<span data-ttu-id="6f821-125">Annak a csoportnak az objektum reprezentációja, amelyből el szeretné távolítani a tagokat.</span><span class="sxs-lookup"><span data-stu-id="6f821-125">The object representation of the group to remove the member from.</span></span>

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

### <span data-ttu-id="6f821-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="6f821-126">-GroupObjectId</span></span>
<span data-ttu-id="6f821-127">Annak a csoportnak az objektumazonosítója, amelyből el szeretné távolítani a tagokat.</span><span class="sxs-lookup"><span data-stu-id="6f821-127">The object id of the group to remove the member from.</span></span>

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

### <span data-ttu-id="6f821-128">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="6f821-128">-MemberObjectId</span></span>
<span data-ttu-id="6f821-129">A tag objektumazonosítója.</span><span class="sxs-lookup"><span data-stu-id="6f821-129">The object id of the member.</span></span>

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

### <span data-ttu-id="6f821-130">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="6f821-130">-MemberUserPrincipalName</span></span>
<span data-ttu-id="6f821-131">Az eltávolítható tag(ak) upn-ja.</span><span class="sxs-lookup"><span data-stu-id="6f821-131">The UPN of the member(s) to remove.</span></span>

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

### <span data-ttu-id="6f821-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f821-132">-PassThru</span></span>
<span data-ttu-id="6f821-133">Ha megadja ezt a parancsot, az igaz értéket ad vissza, ha a parancs sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="6f821-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="6f821-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f821-134">-Confirm</span></span>
<span data-ttu-id="6f821-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6f821-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f821-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f821-136">-WhatIf</span></span>
<span data-ttu-id="6f821-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6f821-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f821-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6f821-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f821-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f821-139">CommonParameters</span></span>
<span data-ttu-id="6f821-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f821-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f821-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f821-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f821-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6f821-142">INPUTS</span></span>

### <span data-ttu-id="6f821-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="6f821-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="6f821-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f821-144">OUTPUTS</span></span>

### <span data-ttu-id="6f821-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6f821-145">System.Boolean</span></span>

## <span data-ttu-id="6f821-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6f821-146">NOTES</span></span>

## <span data-ttu-id="6f821-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f821-147">RELATED LINKS</span></span>
