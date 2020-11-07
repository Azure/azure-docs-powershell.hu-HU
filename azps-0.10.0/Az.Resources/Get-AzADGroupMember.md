---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADGroupMember.md
ms.openlocfilehash: f083498860f3f2b9e19280b41d953032796e0eb9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843478"
---
# <span data-ttu-id="fd103-101">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="fd103-101">Get-AzADGroupMember</span></span>

## <span data-ttu-id="fd103-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd103-102">SYNOPSIS</span></span>
<span data-ttu-id="fd103-103">Az aktuális bérlői fiókban lévő HIRDETÉSCSOPORT tagjainak listája.</span><span class="sxs-lookup"><span data-stu-id="fd103-103">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="fd103-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd103-104">SYNTAX</span></span>

### <span data-ttu-id="fd103-105">ObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fd103-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADGroupMember [-GroupObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="fd103-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd103-106">DisplayNameParameterSet</span></span>
```
Get-AzADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="fd103-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd103-107">GroupObjectParameterSet</span></span>
```
Get-AzADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="fd103-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd103-108">DESCRIPTION</span></span>
<span data-ttu-id="fd103-109">Az aktuális bérlői fiókban lévő HIRDETÉSCSOPORT tagjainak listája.</span><span class="sxs-lookup"><span data-stu-id="fd103-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="fd103-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fd103-110">EXAMPLES</span></span>

### <span data-ttu-id="fd103-111">Példa 1 – HIRDETÉSCSOPORT-objektum azonosítójának listázása</span><span class="sxs-lookup"><span data-stu-id="fd103-111">Example 1 - List members by AD group object id</span></span>

```
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="fd103-112">Felsorolja az "85F89C90-780E-4AA6-9F4F-6F268D322EEE" azonosítójú HIRDETÉSCSOPORT tagjait.</span><span class="sxs-lookup"><span data-stu-id="fd103-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="fd103-113">Példa: 2 – a tagokat a HIRDETÉSCSOPORT-azonosítók listája a lapozással</span><span class="sxs-lookup"><span data-stu-id="fd103-113">Example 2 - List members by AD group object id using paging</span></span>

```
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="fd103-114">A "85F89C90-780E-4AA6-9F4F-6F268D322EEE" azonosítójú HIRDETÉSCSOPORT első 100-tagjainak listája.</span><span class="sxs-lookup"><span data-stu-id="fd103-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="fd103-115">Példa: 3 – a tagok listája csővezetékek szerint</span><span class="sxs-lookup"><span data-stu-id="fd103-115">Example 3 - List members by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzADGroupMember
```

<span data-ttu-id="fd103-116">Megkapja a "85F89C90-780E-4AA6-9F4F-6F268D322EEE" azonosítójú HIRDETÉSCSOPORTOT, és a csoport összes tagjának listázásához a Get-AzADGroupMember parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="fd103-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="fd103-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd103-117">PARAMETERS</span></span>

### <span data-ttu-id="fd103-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd103-118">-DefaultProfile</span></span>
<span data-ttu-id="fd103-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fd103-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd103-120">– Első</span><span class="sxs-lookup"><span data-stu-id="fd103-120">-First</span></span>
<span data-ttu-id="fd103-121">A visszaadni kívánt objektumok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="fd103-121">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="fd103-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="fd103-122">-GroupDisplayName</span></span>
<span data-ttu-id="fd103-123">A csoport megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="fd103-123">The display name of the group.</span></span>

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

### <span data-ttu-id="fd103-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="fd103-124">-GroupObject</span></span>
<span data-ttu-id="fd103-125">Annak a csoportnak az objektuma, amelyből a tagokat listázni kívánja.</span><span class="sxs-lookup"><span data-stu-id="fd103-125">The group object that you are listing members from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: GroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd103-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="fd103-126">-GroupObjectId</span></span>
<span data-ttu-id="fd103-127">A csoport objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fd103-127">Object Id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: Id, ObjectId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd103-128">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="fd103-128">-IncludeTotalCount</span></span>
<span data-ttu-id="fd103-129">Az adathalmaz objektumainak számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="fd103-129">Reports the number of objects in the data set.</span></span> <span data-ttu-id="fd103-130">Ez a paraméter jelenleg nem tesz semmit.</span><span class="sxs-lookup"><span data-stu-id="fd103-130">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="fd103-131">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="fd103-131">-Skip</span></span>
<span data-ttu-id="fd103-132">Figyelmen kívül hagyja az első N objektumokat, és a fennmaradó objektumokat kapja.</span><span class="sxs-lookup"><span data-stu-id="fd103-132">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="fd103-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd103-133">CommonParameters</span></span>
<span data-ttu-id="fd103-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd103-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd103-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd103-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd103-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd103-136">INPUTS</span></span>

### <span data-ttu-id="fd103-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="fd103-137">System.Guid</span></span>

### <span data-ttu-id="fd103-138">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="fd103-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="fd103-139">Paraméterek: GroupObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fd103-139">Parameters: GroupObject (ByValue)</span></span>

## <span data-ttu-id="fd103-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd103-140">OUTPUTS</span></span>

### <span data-ttu-id="fd103-141">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADObject</span><span class="sxs-lookup"><span data-stu-id="fd103-141">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="fd103-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd103-142">NOTES</span></span>

## <span data-ttu-id="fd103-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd103-143">RELATED LINKS</span></span>

[<span data-ttu-id="fd103-144">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="fd103-144">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="fd103-145">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="fd103-145">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

