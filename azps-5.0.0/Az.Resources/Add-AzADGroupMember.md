---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/add-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
ms.openlocfilehash: bf64c2fd139a4174496ba48cdb94aab89486a62a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302480"
---
# <span data-ttu-id="0eb5d-101">Add-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="0eb5d-101">Add-AzADGroupMember</span></span>

## <span data-ttu-id="0eb5d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0eb5d-102">SYNOPSIS</span></span>
<span data-ttu-id="0eb5d-103">Felhasználó felvétele egy meglévő HIRDETÉSCSOPORT-csoportba.</span><span class="sxs-lookup"><span data-stu-id="0eb5d-103">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="0eb5d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0eb5d-104">SYNTAX</span></span>

### <span data-ttu-id="0eb5d-105">MemberObjectIdWithGroupObjectId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0eb5d-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eb5d-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="0eb5d-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eb5d-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="0eb5d-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eb5d-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0eb5d-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eb5d-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0eb5d-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eb5d-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0eb5d-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0eb5d-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="0eb5d-111">DESCRIPTION</span></span>
<span data-ttu-id="0eb5d-112">Felhasználó felvétele egy meglévő HIRDETÉSCSOPORT-csoportba.</span><span class="sxs-lookup"><span data-stu-id="0eb5d-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="0eb5d-113">Példák</span><span class="sxs-lookup"><span data-stu-id="0eb5d-113">EXAMPLES</span></span>

### <span data-ttu-id="0eb5d-114">1. példa: felhasználó felvétele objektum-azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="0eb5d-114">Example 1: Add a user to a group by object id</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="0eb5d-115">A "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" azonosítójú felhasználó felvétele a "85F89C90-780E-4AA6-9F4F-6F268D322EEE" azonosítójú csoportba.</span><span class="sxs-lookup"><span data-stu-id="0eb5d-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="0eb5d-116">2. példa: felhasználó felvétele egy csoportba csővezetékekkel</span><span class="sxs-lookup"><span data-stu-id="0eb5d-116">Example 2: Add a user to a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="0eb5d-117">Beilleszti az "85F89C90-780E-4AA6-9F4F-6F268D322EEE" azonosítójú csoportot, és a Add-AzADGroupMember parancsmagba beilleszti a felhasználót a csoportba.</span><span class="sxs-lookup"><span data-stu-id="0eb5d-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzADGroupMember cmdlet to add the user to that group.</span></span>

### <span data-ttu-id="0eb5d-118">3. példa: felhasználó felvétele a csoportba elsődleges név szerint</span><span class="sxs-lookup"><span data-stu-id="0eb5d-118">Example 3: Add a user to a group by principal name</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberUserPrincipalName "myemail@domain.com" -TargetGroupDisplayName "MyGroupDisplayName" 
PS C:\> Get-AzADGroupMember -GroupDisplayName "MyGroupDisplayName"
```

<span data-ttu-id="0eb5d-119">Felvesz egy felhasználót egy csoportba, és felsorolja a csoport tagjait.</span><span class="sxs-lookup"><span data-stu-id="0eb5d-119">Adds an user to a group and list the members of the group.</span></span>

## <span data-ttu-id="0eb5d-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0eb5d-120">PARAMETERS</span></span>

### <span data-ttu-id="0eb5d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eb5d-121">-DefaultProfile</span></span>
<span data-ttu-id="0eb5d-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0eb5d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0eb5d-123">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="0eb5d-123">-MemberObjectId</span></span>
<span data-ttu-id="0eb5d-124">A tag objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0eb5d-124">The object id of the member.</span></span>

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

### <span data-ttu-id="0eb5d-125">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="0eb5d-125">-MemberUserPrincipalName</span></span>
<span data-ttu-id="0eb5d-126">A csoportba felvenni kívánt tag (ok) UPN-címe.</span><span class="sxs-lookup"><span data-stu-id="0eb5d-126">The UPN of the member(s) to add to the group.</span></span>

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

### <span data-ttu-id="0eb5d-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0eb5d-127">-PassThru</span></span>
<span data-ttu-id="0eb5d-128">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="0eb5d-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="0eb5d-129">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="0eb5d-129">-TargetGroupDisplayName</span></span>
<span data-ttu-id="0eb5d-130">Annak a csoportnak a megjelenítendő neve, amelybe fel szeretné venni a tag (oka) t.</span><span class="sxs-lookup"><span data-stu-id="0eb5d-130">The display name of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="0eb5d-131">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="0eb5d-131">-TargetGroupObject</span></span>
<span data-ttu-id="0eb5d-132">A csoport objektum-ábrázolása a tagok (ok) hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="0eb5d-132">The object representation of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="0eb5d-133">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="0eb5d-133">-TargetGroupObjectId</span></span>
<span data-ttu-id="0eb5d-134">Annak a csoportnak az objektum azonosítója, amelyhez hozzá szeretné adni a tag (oka) t.</span><span class="sxs-lookup"><span data-stu-id="0eb5d-134">The object id of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="0eb5d-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0eb5d-135">-Confirm</span></span>
<span data-ttu-id="0eb5d-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0eb5d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0eb5d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eb5d-137">-WhatIf</span></span>
<span data-ttu-id="0eb5d-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0eb5d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0eb5d-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0eb5d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0eb5d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eb5d-140">CommonParameters</span></span>
<span data-ttu-id="0eb5d-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0eb5d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eb5d-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0eb5d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eb5d-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0eb5d-143">INPUTS</span></span>

### <span data-ttu-id="0eb5d-144">Microsoft. Azure. Command. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="0eb5d-144">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="0eb5d-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0eb5d-145">OUTPUTS</span></span>

### <span data-ttu-id="0eb5d-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0eb5d-146">System.Boolean</span></span>

## <span data-ttu-id="0eb5d-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0eb5d-147">NOTES</span></span>

## <span data-ttu-id="0eb5d-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0eb5d-148">RELATED LINKS</span></span>
