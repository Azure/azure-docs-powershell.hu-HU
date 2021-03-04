---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
ms.openlocfilehash: d351ee85c36b9f5f8493879cded058fd7220450f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936121"
---
# <span data-ttu-id="008ed-101">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="008ed-101">Get-AzADGroupMember</span></span>

## <span data-ttu-id="008ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="008ed-102">SYNOPSIS</span></span>
<span data-ttu-id="008ed-103">Az aktuális bérlői webhely AD-csoportjának tagjait sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="008ed-103">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="008ed-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="008ed-104">SYNTAX</span></span>

### <span data-ttu-id="008ed-105">ObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="008ed-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADGroupMember [-GroupObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="008ed-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="008ed-106">DisplayNameParameterSet</span></span>
```
Get-AzADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="008ed-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="008ed-107">GroupObjectParameterSet</span></span>
```
Get-AzADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="008ed-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="008ed-108">DESCRIPTION</span></span>
<span data-ttu-id="008ed-109">Az aktuális bérlői webhely AD-csoportjának tagjait sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="008ed-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="008ed-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="008ed-110">EXAMPLES</span></span>

### <span data-ttu-id="008ed-111">1. példa: Tagok listába sorolása AD-csoportobjektum-azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="008ed-111">Example 1: List members by AD group object id</span></span>

```powershell
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="008ed-112">Az AD-csoport tagjainak listája a következő objektumazonosítóval: '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span><span class="sxs-lookup"><span data-stu-id="008ed-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="008ed-113">2. példa: Listatagok felsorolása az AD-csoport objektumazonosítója alapján lapozás használatával</span><span class="sxs-lookup"><span data-stu-id="008ed-113">Example 2: List members by AD group object id using paging</span></span>

```powershell
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="008ed-114">A (85F89C90-780E-4AA6-9F4F-6F268D322EEE) objektumazonosítóval az AD csoport első 100 tagját sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="008ed-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="008ed-115">3. példa: Tagok listázása pipával</span><span class="sxs-lookup"><span data-stu-id="008ed-115">Example 3: List members by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzADGroupMember
```

<span data-ttu-id="008ed-116">A (85F89C90-780E-4AA6-9F4F-6F268D322EEE) objektumazonosítóval jelölt AD-csoportot a Get-AzADGroupMember-parancsmaghoz és a csoport összes tagjának listához.</span><span class="sxs-lookup"><span data-stu-id="008ed-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="008ed-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="008ed-117">PARAMETERS</span></span>

### <span data-ttu-id="008ed-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="008ed-118">-DefaultProfile</span></span>
<span data-ttu-id="008ed-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="008ed-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="008ed-120">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="008ed-120">-GroupDisplayName</span></span>
<span data-ttu-id="008ed-121">A csoport megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="008ed-121">The display name of the group.</span></span>

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

### <span data-ttu-id="008ed-122">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="008ed-122">-GroupObject</span></span>
<span data-ttu-id="008ed-123">Az a csoportobjektum, amelyből tagokat sorol fel.</span><span class="sxs-lookup"><span data-stu-id="008ed-123">The group object that you are listing members from.</span></span>

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

### <span data-ttu-id="008ed-124">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="008ed-124">-GroupObjectId</span></span>
<span data-ttu-id="008ed-125">A csoport objektumazonosítója.</span><span class="sxs-lookup"><span data-stu-id="008ed-125">Object Id of the group.</span></span>

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

### <span data-ttu-id="008ed-126">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="008ed-126">-IncludeTotalCount</span></span>
<span data-ttu-id="008ed-127">Az adatkészletben lévő objektumok számát jelenti.</span><span class="sxs-lookup"><span data-stu-id="008ed-127">Reports the number of objects in the data set.</span></span> <span data-ttu-id="008ed-128">Ez a paraméter jelenleg nem tesz semmit.</span><span class="sxs-lookup"><span data-stu-id="008ed-128">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="008ed-129">-Skip</span><span class="sxs-lookup"><span data-stu-id="008ed-129">-Skip</span></span>
<span data-ttu-id="008ed-130">Figyelmen kívül hagyja az első N objektumot, majd beveszi a fennmaradó objektumokat.</span><span class="sxs-lookup"><span data-stu-id="008ed-130">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="008ed-131">-First</span><span class="sxs-lookup"><span data-stu-id="008ed-131">-First</span></span>
<span data-ttu-id="008ed-132">A vissza nem térhet objektumok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="008ed-132">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="008ed-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="008ed-133">CommonParameters</span></span>
<span data-ttu-id="008ed-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="008ed-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="008ed-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="008ed-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="008ed-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="008ed-136">INPUTS</span></span>

### <span data-ttu-id="008ed-137">System.String</span><span class="sxs-lookup"><span data-stu-id="008ed-137">System.String</span></span>

### <span data-ttu-id="008ed-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="008ed-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="008ed-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="008ed-139">OUTPUTS</span></span>

### <span data-ttu-id="008ed-140">Microsoft.Azure.Commands.ActiveDirectory.PSADObject</span><span class="sxs-lookup"><span data-stu-id="008ed-140">Microsoft.Azure.Commands.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="008ed-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="008ed-141">NOTES</span></span>

## <span data-ttu-id="008ed-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="008ed-142">RELATED LINKS</span></span>

[<span data-ttu-id="008ed-143">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="008ed-143">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="008ed-144">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="008ed-144">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

