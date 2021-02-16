---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
ms.openlocfilehash: 764b2d091b0019cc4231828066b4067c5f054476
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146138"
---
# <span data-ttu-id="57440-101">Get-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="57440-101">Get-AzADGroup</span></span>

## <span data-ttu-id="57440-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57440-102">SYNOPSIS</span></span>
<span data-ttu-id="57440-103">Az Active Directory-csoportok szűrése.</span><span class="sxs-lookup"><span data-stu-id="57440-103">Filters active directory groups.</span></span>

## <span data-ttu-id="57440-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="57440-104">SYNTAX</span></span>

### <span data-ttu-id="57440-105">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="57440-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="57440-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="57440-106">SearchStringParameterSet</span></span>
```
Get-AzADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="57440-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="57440-107">DisplayNameParameterSet</span></span>
```
Get-AzADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="57440-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="57440-108">ObjectIdParameterSet</span></span>
```
Get-AzADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="57440-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="57440-109">DESCRIPTION</span></span>
<span data-ttu-id="57440-110">Az Active Directory-csoportok szűrése.</span><span class="sxs-lookup"><span data-stu-id="57440-110">Filters active directory groups.</span></span>

## <span data-ttu-id="57440-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="57440-111">EXAMPLES</span></span>

### <span data-ttu-id="57440-112">1. példa: Az összes AD-csoport felsorolása</span><span class="sxs-lookup"><span data-stu-id="57440-112">Example 1: List all AD groups</span></span>
```powershell
PS C:\> Get-AzADGroup
```

<span data-ttu-id="57440-113">Egy bérlő összes AD-csoportját felsorolja.</span><span class="sxs-lookup"><span data-stu-id="57440-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="57440-114">2. példa: Az összes AD-csoport felsorolása lapozás használatával</span><span class="sxs-lookup"><span data-stu-id="57440-114">Example 2: List all AD groups using paging</span></span>

```powershell
PS C:\> Get-AzADGroup -First 100
```

<span data-ttu-id="57440-115">A bérlői webhely első 100 AD-csoportjait sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="57440-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="57440-116">3. példa: Az AD-csoport lekérte objektumazonosító szerint</span><span class="sxs-lookup"><span data-stu-id="57440-116">Example 3: Get AD group by object id</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="57440-117">A (85F89C90-780E-4AA6-9F4F-6F268D322EEE) objektumazonosítójú AD-csoportot kapja.</span><span class="sxs-lookup"><span data-stu-id="57440-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="57440-118">4. példa: Csoportok felsorolása keresési karakterlánc alapján</span><span class="sxs-lookup"><span data-stu-id="57440-118">Example 4: List groups by search string</span></span>

```powershell
PS C:\> Get-AzADGroup -SearchString Joe
```

<span data-ttu-id="57440-119">Azokat az AD-csoportokat sorolja fel, amelyeknek a megjelenítendő neve "József" névvel kezdődik.</span><span class="sxs-lookup"><span data-stu-id="57440-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="57440-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57440-120">PARAMETERS</span></span>

### <span data-ttu-id="57440-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57440-121">-DefaultProfile</span></span>
<span data-ttu-id="57440-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="57440-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57440-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="57440-123">-DisplayName</span></span>
<span data-ttu-id="57440-124">A csoport megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="57440-124">The display name of the group.</span></span>

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

### <span data-ttu-id="57440-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="57440-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="57440-126">A megadott karakterláncokkal kezdődik csoportok keresését használja.</span><span class="sxs-lookup"><span data-stu-id="57440-126">Used to find groups that begin with the provided string.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: SearchString

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57440-127">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="57440-127">-ObjectId</span></span>
<span data-ttu-id="57440-128">A csoport objektumazonosítója.</span><span class="sxs-lookup"><span data-stu-id="57440-128">Object id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57440-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="57440-129">-IncludeTotalCount</span></span>
<span data-ttu-id="57440-130">Az adatkészletben lévő objektumok számát jelenti.</span><span class="sxs-lookup"><span data-stu-id="57440-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="57440-131">Ez a paraméter jelenleg nem tesz semmit.</span><span class="sxs-lookup"><span data-stu-id="57440-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="57440-132">-Skip</span><span class="sxs-lookup"><span data-stu-id="57440-132">-Skip</span></span>
<span data-ttu-id="57440-133">Figyelmen kívül hagyja az első N objektumot, majd beveszi a fennmaradó objektumokat.</span><span class="sxs-lookup"><span data-stu-id="57440-133">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="57440-134">-First</span><span class="sxs-lookup"><span data-stu-id="57440-134">-First</span></span>
<span data-ttu-id="57440-135">A vissza nem térhet objektumok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="57440-135">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="57440-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57440-136">CommonParameters</span></span>
<span data-ttu-id="57440-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57440-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57440-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57440-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57440-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57440-139">INPUTS</span></span>

### <span data-ttu-id="57440-140">System.String</span><span class="sxs-lookup"><span data-stu-id="57440-140">System.String</span></span>

### <span data-ttu-id="57440-141">System.Guid</span><span class="sxs-lookup"><span data-stu-id="57440-141">System.Guid</span></span>

## <span data-ttu-id="57440-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="57440-142">OUTPUTS</span></span>

### <span data-ttu-id="57440-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="57440-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="57440-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="57440-144">NOTES</span></span>

## <span data-ttu-id="57440-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="57440-145">RELATED LINKS</span></span>

[<span data-ttu-id="57440-146">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="57440-146">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="57440-147">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="57440-147">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="57440-148">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="57440-148">Get-AzADGroupMember</span></span>](./Get-AzADGroupMember.md)

