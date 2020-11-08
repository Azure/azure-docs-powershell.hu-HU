---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
ms.openlocfilehash: 984b5ef9a1ff19142ef044e1f3c919f8fb2a3dce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188215"
---
# <span data-ttu-id="d641a-101">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="d641a-101">Get-AzADGroupMember</span></span>

## <span data-ttu-id="d641a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d641a-102">SYNOPSIS</span></span>
<span data-ttu-id="d641a-103">Az aktuális bérlői fiókban lévő HIRDETÉSCSOPORT tagjainak listája.</span><span class="sxs-lookup"><span data-stu-id="d641a-103">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="d641a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d641a-104">SYNTAX</span></span>

### <span data-ttu-id="d641a-105">ObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d641a-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADGroupMember [-GroupObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d641a-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d641a-106">DisplayNameParameterSet</span></span>
```
Get-AzADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d641a-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d641a-107">GroupObjectParameterSet</span></span>
```
Get-AzADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="d641a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d641a-108">DESCRIPTION</span></span>
<span data-ttu-id="d641a-109">Az aktuális bérlői fiókban lévő HIRDETÉSCSOPORT tagjainak listája.</span><span class="sxs-lookup"><span data-stu-id="d641a-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="d641a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d641a-110">EXAMPLES</span></span>

### <span data-ttu-id="d641a-111">1. példa: HIRDETÉSCSOPORT-objektum azonosítója alapján listázhatja a tagokat</span><span class="sxs-lookup"><span data-stu-id="d641a-111">Example 1: List members by AD group object id</span></span>

```powershell
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="d641a-112">Felsorolja az "85F89C90-780E-4AA6-9F4F-6F268D322EEE" azonosítójú HIRDETÉSCSOPORT tagjait.</span><span class="sxs-lookup"><span data-stu-id="d641a-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="d641a-113">2. példa: a tagokat a HIRDETÉSCSOPORT-azonosítók alapján listázhatja a személyhívóval</span><span class="sxs-lookup"><span data-stu-id="d641a-113">Example 2: List members by AD group object id using paging</span></span>

```powershell
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="d641a-114">A "85F89C90-780E-4AA6-9F4F-6F268D322EEE" azonosítójú HIRDETÉSCSOPORT első 100-tagjainak listája.</span><span class="sxs-lookup"><span data-stu-id="d641a-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="d641a-115">3. példa: a tagok kilistázása csővezetékekkel</span><span class="sxs-lookup"><span data-stu-id="d641a-115">Example 3: List members by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzADGroupMember
```

<span data-ttu-id="d641a-116">Megkapja a "85F89C90-780E-4AA6-9F4F-6F268D322EEE" azonosítójú HIRDETÉSCSOPORTOT, és a csoport összes tagjának listázásához a Get-AzADGroupMember parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="d641a-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="d641a-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d641a-117">PARAMETERS</span></span>

### <span data-ttu-id="d641a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d641a-118">-DefaultProfile</span></span>
<span data-ttu-id="d641a-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d641a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d641a-120">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="d641a-120">-GroupDisplayName</span></span>
<span data-ttu-id="d641a-121">A csoport megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="d641a-121">The display name of the group.</span></span>

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

### <span data-ttu-id="d641a-122">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="d641a-122">-GroupObject</span></span>
<span data-ttu-id="d641a-123">Annak a csoportnak az objektuma, amelyből a tagokat listázni kívánja.</span><span class="sxs-lookup"><span data-stu-id="d641a-123">The group object that you are listing members from.</span></span>

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

### <span data-ttu-id="d641a-124">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="d641a-124">-GroupObjectId</span></span>
<span data-ttu-id="d641a-125">A csoport objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d641a-125">Object Id of the group.</span></span>

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

### <span data-ttu-id="d641a-126">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="d641a-126">-IncludeTotalCount</span></span>
<span data-ttu-id="d641a-127">Az adathalmaz objektumainak számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="d641a-127">Reports the number of objects in the data set.</span></span> <span data-ttu-id="d641a-128">Ez a paraméter jelenleg nem tesz semmit.</span><span class="sxs-lookup"><span data-stu-id="d641a-128">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="d641a-129">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="d641a-129">-Skip</span></span>
<span data-ttu-id="d641a-130">Figyelmen kívül hagyja az első N objektumokat, és a fennmaradó objektumokat kapja.</span><span class="sxs-lookup"><span data-stu-id="d641a-130">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="d641a-131">– Első</span><span class="sxs-lookup"><span data-stu-id="d641a-131">-First</span></span>
<span data-ttu-id="d641a-132">A visszaadni kívánt objektumok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="d641a-132">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="d641a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d641a-133">CommonParameters</span></span>
<span data-ttu-id="d641a-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d641a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d641a-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d641a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d641a-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d641a-136">INPUTS</span></span>

### <span data-ttu-id="d641a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d641a-137">System.String</span></span>

### <span data-ttu-id="d641a-138">Microsoft. Azure. Command. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="d641a-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="d641a-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d641a-139">OUTPUTS</span></span>

### <span data-ttu-id="d641a-140">Microsoft. Azure. Command. ActiveDirectory. PSADObject</span><span class="sxs-lookup"><span data-stu-id="d641a-140">Microsoft.Azure.Commands.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="d641a-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d641a-141">NOTES</span></span>

## <span data-ttu-id="d641a-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d641a-142">RELATED LINKS</span></span>

[<span data-ttu-id="d641a-143">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="d641a-143">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="d641a-144">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d641a-144">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

