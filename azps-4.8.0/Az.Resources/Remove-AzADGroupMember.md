---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
ms.openlocfilehash: 7450588905deeb900efbffffa253f5c06ae63272
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181419"
---
# <span data-ttu-id="cf8b4-101">Remove-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="cf8b4-101">Remove-AzADGroupMember</span></span>

## <span data-ttu-id="cf8b4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf8b4-102">SYNOPSIS</span></span>
<span data-ttu-id="cf8b4-103">Felhasználó eltávolítása egy HIRDETÉSCSOPORT-csoportból.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-103">Removes a user from an AD group.</span></span>

## <span data-ttu-id="cf8b4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf8b4-104">SYNTAX</span></span>

### <span data-ttu-id="cf8b4-105">ExplicitParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cf8b4-105">ExplicitParameterSet (Default)</span></span>
```
Remove-AzADGroupMember [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf8b4-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="cf8b4-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf8b4-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="cf8b4-107">MemberObjectIdWithGroupObject</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf8b4-108">MemberObjectIdWithGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="cf8b4-108">MemberObjectIdWithGroupObjectId</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf8b4-109">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf8b4-109">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf8b4-110">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf8b4-110">MemberUPNWithGroupObjectParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf8b4-111">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf8b4-111">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf8b4-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf8b4-112">DESCRIPTION</span></span>
<span data-ttu-id="cf8b4-113">Felhasználó eltávolítása egy HIRDETÉSCSOPORT-csoportból.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-113">Removes a user from an AD group.</span></span>

## <span data-ttu-id="cf8b4-114">Példák</span><span class="sxs-lookup"><span data-stu-id="cf8b4-114">EXAMPLES</span></span>

### <span data-ttu-id="cf8b4-115">1. példa: felhasználó eltávolítása a csoportból objektum-azonosító alapján</span><span class="sxs-lookup"><span data-stu-id="cf8b4-115">Example 1: Remove a user from a group by object id</span></span>

```powershell
PS C:\> Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="cf8b4-116">A "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" azonosítójú felhasználó eltávolítása a "85F89C90-780E-4AA6-9F4F-6F268D322EEE" azonosítójú csoportból.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-116">Removes the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' from the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="cf8b4-117">2. példa: felhasználó eltávolítása egy csoportból csővezetékről</span><span class="sxs-lookup"><span data-stu-id="cf8b4-117">Example 2: Remove a user from a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="cf8b4-118">Beilleszti az "85F89C90-780E-4AA6-9F4F-6F268D322EEE" azonosítójú csoportot, és a Remove-AzADGroupMember parancsmaghoz illeszti a felhasználót a csoportba.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-118">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Remove-AzADGroupMember cmdlet to remove the user to that group.</span></span>

## <span data-ttu-id="cf8b4-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf8b4-119">PARAMETERS</span></span>

### <span data-ttu-id="cf8b4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf8b4-120">-DefaultProfile</span></span>
<span data-ttu-id="cf8b4-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf8b4-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="cf8b4-122">-GroupDisplayName</span></span>
<span data-ttu-id="cf8b4-123">Annak a csoportnak a megjelenítendő neve, amelyből el szeretné távolítani a tagot (ka) t.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-123">The display name of the group to remove the member(s) from.</span></span>

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

### <span data-ttu-id="cf8b4-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="cf8b4-124">-GroupObject</span></span>
<span data-ttu-id="cf8b4-125">A Csoport objektumát ábrázoló objektum a tagok eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-125">The object representation of the group to remove the member from.</span></span>

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

### <span data-ttu-id="cf8b4-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="cf8b4-126">-GroupObjectId</span></span>
<span data-ttu-id="cf8b4-127">Annak a csoportnak az objektum azonosítója, amelyből a tagot el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-127">The object id of the group to remove the member from.</span></span>

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

### <span data-ttu-id="cf8b4-128">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="cf8b4-128">-MemberObjectId</span></span>
<span data-ttu-id="cf8b4-129">A tag objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-129">The object id of the member.</span></span>

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

### <span data-ttu-id="cf8b4-130">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="cf8b4-130">-MemberUserPrincipalName</span></span>
<span data-ttu-id="cf8b4-131">Az eltávolítandó tag (ok) UPN-címe.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-131">The UPN of the member(s) to remove.</span></span>

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

### <span data-ttu-id="cf8b4-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf8b4-132">-PassThru</span></span>
<span data-ttu-id="cf8b4-133">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="cf8b4-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cf8b4-134">-Confirm</span></span>
<span data-ttu-id="cf8b4-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf8b4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf8b4-136">-WhatIf</span></span>
<span data-ttu-id="cf8b4-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf8b4-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf8b4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf8b4-139">CommonParameters</span></span>
<span data-ttu-id="cf8b4-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf8b4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf8b4-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cf8b4-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf8b4-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf8b4-142">INPUTS</span></span>

### <span data-ttu-id="cf8b4-143">Microsoft. Azure. Command. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="cf8b4-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="cf8b4-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf8b4-144">OUTPUTS</span></span>

### <span data-ttu-id="cf8b4-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cf8b4-145">System.Boolean</span></span>

## <span data-ttu-id="cf8b4-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf8b4-146">NOTES</span></span>

## <span data-ttu-id="cf8b4-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf8b4-147">RELATED LINKS</span></span>
