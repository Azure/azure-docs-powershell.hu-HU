---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
ms.openlocfilehash: 5d54f90c6ed16c95f19a8df6ef32a95c15ce501b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012030"
---
# <span data-ttu-id="a294d-101">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="a294d-101">Get-AzADGroupMember</span></span>

## <span data-ttu-id="a294d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a294d-102">SYNOPSIS</span></span>
<span data-ttu-id="a294d-103">Az aktuális bérlői fiókban lévő HIRDETÉSCSOPORT tagjainak listája.</span><span class="sxs-lookup"><span data-stu-id="a294d-103">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="a294d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a294d-104">SYNTAX</span></span>

### <span data-ttu-id="a294d-105">ObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a294d-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADGroupMember [-GroupObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a294d-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a294d-106">DisplayNameParameterSet</span></span>
```
Get-AzADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a294d-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a294d-107">GroupObjectParameterSet</span></span>
```
Get-AzADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="a294d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a294d-108">DESCRIPTION</span></span>
<span data-ttu-id="a294d-109">Az aktuális bérlői fiókban lévő HIRDETÉSCSOPORT tagjainak listája.</span><span class="sxs-lookup"><span data-stu-id="a294d-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="a294d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a294d-110">EXAMPLES</span></span>

### <span data-ttu-id="a294d-111">Példa 1 – HIRDETÉSCSOPORT-objektum azonosítójának listázása</span><span class="sxs-lookup"><span data-stu-id="a294d-111">Example 1 - List members by AD group object id</span></span>

```
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="a294d-112">Felsorolja az "85F89C90-780E-4AA6-9F4F-6F268D322EEE" azonosítójú HIRDETÉSCSOPORT tagjait.</span><span class="sxs-lookup"><span data-stu-id="a294d-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="a294d-113">Példa: 2 – a tagokat a HIRDETÉSCSOPORT-azonosítók listája a lapozással</span><span class="sxs-lookup"><span data-stu-id="a294d-113">Example 2 - List members by AD group object id using paging</span></span>

```
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="a294d-114">A "85F89C90-780E-4AA6-9F4F-6F268D322EEE" azonosítójú HIRDETÉSCSOPORT első 100-tagjainak listája.</span><span class="sxs-lookup"><span data-stu-id="a294d-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="a294d-115">Példa: 3 – a tagok listája csővezetékek szerint</span><span class="sxs-lookup"><span data-stu-id="a294d-115">Example 3 - List members by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzADGroupMember
```

<span data-ttu-id="a294d-116">Megkapja a "85F89C90-780E-4AA6-9F4F-6F268D322EEE" azonosítójú HIRDETÉSCSOPORTOT, és a csoport összes tagjának listázásához a Get-AzADGroupMember parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="a294d-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="a294d-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a294d-117">PARAMETERS</span></span>

### <span data-ttu-id="a294d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a294d-118">-DefaultProfile</span></span>
<span data-ttu-id="a294d-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a294d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a294d-120">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="a294d-120">-GroupDisplayName</span></span>
<span data-ttu-id="a294d-121">A csoport megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="a294d-121">The display name of the group.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a294d-122">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="a294d-122">-GroupObject</span></span>
<span data-ttu-id="a294d-123">Annak a csoportnak az objektuma, amelyből a tagokat listázni kívánja.</span><span class="sxs-lookup"><span data-stu-id="a294d-123">The group object that you are listing members from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: GroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a294d-124">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="a294d-124">-GroupObjectId</span></span>
<span data-ttu-id="a294d-125">A csoport objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a294d-125">Object Id of the group.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: Id, ObjectId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a294d-126">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="a294d-126">-IncludeTotalCount</span></span>
<span data-ttu-id="a294d-127">Az adathalmaz objektumainak számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="a294d-127">Reports the number of objects in the data set.</span></span> <span data-ttu-id="a294d-128">Ez a paraméter jelenleg nem tesz semmit.</span><span class="sxs-lookup"><span data-stu-id="a294d-128">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="a294d-129">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="a294d-129">-Skip</span></span>
<span data-ttu-id="a294d-130">Figyelmen kívül hagyja az első N objektumokat, és a fennmaradó objektumokat kapja.</span><span class="sxs-lookup"><span data-stu-id="a294d-130">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a294d-131">– Első</span><span class="sxs-lookup"><span data-stu-id="a294d-131">-First</span></span>
<span data-ttu-id="a294d-132">A visszaadni kívánt objektumok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="a294d-132">The maximum number of objects to return.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a294d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a294d-133">CommonParameters</span></span>
<span data-ttu-id="a294d-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a294d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a294d-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a294d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a294d-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a294d-136">INPUTS</span></span>

### <span data-ttu-id="a294d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a294d-137">System.String</span></span>

### <span data-ttu-id="a294d-138">Microsoft. Azure. Command. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="a294d-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="a294d-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a294d-139">OUTPUTS</span></span>

### <span data-ttu-id="a294d-140">Microsoft. Azure. Command. ActiveDirectory. PSADObject</span><span class="sxs-lookup"><span data-stu-id="a294d-140">Microsoft.Azure.Commands.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="a294d-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a294d-141">NOTES</span></span>

## <span data-ttu-id="a294d-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a294d-142">RELATED LINKS</span></span>

[<span data-ttu-id="a294d-143">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="a294d-143">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="a294d-144">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a294d-144">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

