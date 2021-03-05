---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/add-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
ms.openlocfilehash: 7184ee532335d7db84792bf2234d8cbafa9ad201
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999830"
---
# <span data-ttu-id="bc956-101">Add-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="bc956-101">Add-AzADGroupMember</span></span>

## <span data-ttu-id="bc956-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc956-102">SYNOPSIS</span></span>
<span data-ttu-id="bc956-103">Hozzáad egy felhasználót egy meglévő AD-csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="bc956-103">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="bc956-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bc956-104">SYNTAX</span></span>

### <span data-ttu-id="bc956-105">MemberObjectIdWithGroupObjectId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bc956-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc956-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="bc956-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc956-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="bc956-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc956-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc956-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc956-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc956-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc956-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc956-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc956-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bc956-111">DESCRIPTION</span></span>
<span data-ttu-id="bc956-112">Hozzáad egy felhasználót egy meglévő AD-csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="bc956-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="bc956-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bc956-113">EXAMPLES</span></span>

### <span data-ttu-id="bc956-114">1. példa: Felhasználó hozzáadása egy csoporthoz objektumazonosító alapján</span><span class="sxs-lookup"><span data-stu-id="bc956-114">Example 1: Add a user to a group by object id</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="bc956-115">Hozzáadja a "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" objektumazonosítót használó felhasználót a "85F89C90-780E-4AA6-9F4F-6F268D322EEE" objektumazonosítóval.</span><span class="sxs-lookup"><span data-stu-id="bc956-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="bc956-116">2. példa: Felhasználó hozzáadása csoporthoz pipázás használatával</span><span class="sxs-lookup"><span data-stu-id="bc956-116">Example 2: Add a user to a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="bc956-117">A (85F89C90-780E-4AA6-9F4F-6F268D322EEE) objektumazonosítójú csoportot beveszi a Add-AzADGroupMember-parancsmagba, és hozzáadja a felhasználót a csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="bc956-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzADGroupMember cmdlet to add the user to that group.</span></span>

### <span data-ttu-id="bc956-118">3. példa: Felhasználó felvétele egy csoportba egyszerű név alapján</span><span class="sxs-lookup"><span data-stu-id="bc956-118">Example 3: Add a user to a group by principal name</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberUserPrincipalName "myemail@domain.com" -TargetGroupDisplayName "MyGroupDisplayName" 
PS C:\> Get-AzADGroupMember -GroupDisplayName "MyGroupDisplayName"
```

<span data-ttu-id="bc956-119">Hozzáad egy felhasználót egy csoporthoz, és felsorolja a csoport tagjait.</span><span class="sxs-lookup"><span data-stu-id="bc956-119">Adds an user to a group and list the members of the group.</span></span>

## <span data-ttu-id="bc956-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc956-120">PARAMETERS</span></span>

### <span data-ttu-id="bc956-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc956-121">-DefaultProfile</span></span>
<span data-ttu-id="bc956-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bc956-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc956-123">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="bc956-123">-MemberObjectId</span></span>
<span data-ttu-id="bc956-124">A tag objektumazonosítója.</span><span class="sxs-lookup"><span data-stu-id="bc956-124">The object id of the member.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc956-125">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="bc956-125">-MemberUserPrincipalName</span></span>
<span data-ttu-id="bc956-126">A csoporthoz hozzáadni megfelelő tag(ak) upn-ja.</span><span class="sxs-lookup"><span data-stu-id="bc956-126">The UPN of the member(s) to add to the group.</span></span>

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

### <span data-ttu-id="bc956-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc956-127">-PassThru</span></span>
<span data-ttu-id="bc956-128">Ha megadja ezt a parancsot, az igaz értéket ad vissza, ha a parancs sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="bc956-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="bc956-129">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="bc956-129">-TargetGroupDisplayName</span></span>
<span data-ttu-id="bc956-130">Annak a csoportnak a megjelenítendő neve, amelybe fel kell vegye a tagokat.</span><span class="sxs-lookup"><span data-stu-id="bc956-130">The display name of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="bc956-131">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="bc956-131">-TargetGroupObject</span></span>
<span data-ttu-id="bc956-132">Annak a csoportnak az objektum reprezentációja, amelybe fel kell vegye a tagokat.</span><span class="sxs-lookup"><span data-stu-id="bc956-132">The object representation of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="bc956-133">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="bc956-133">-TargetGroupObjectId</span></span>
<span data-ttu-id="bc956-134">Annak a csoportnak az objektumazonosítója, amelybe fel kell vegye a tagokat.</span><span class="sxs-lookup"><span data-stu-id="bc956-134">The object id of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="bc956-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc956-135">-Confirm</span></span>
<span data-ttu-id="bc956-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bc956-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc956-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc956-137">-WhatIf</span></span>
<span data-ttu-id="bc956-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bc956-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc956-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bc956-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc956-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc956-140">CommonParameters</span></span>
<span data-ttu-id="bc956-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc956-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc956-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc956-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc956-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bc956-143">INPUTS</span></span>

### <span data-ttu-id="bc956-144">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="bc956-144">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="bc956-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc956-145">OUTPUTS</span></span>

### <span data-ttu-id="bc956-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bc956-146">System.Boolean</span></span>

## <span data-ttu-id="bc956-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bc956-147">NOTES</span></span>

## <span data-ttu-id="bc956-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc956-148">RELATED LINKS</span></span>
