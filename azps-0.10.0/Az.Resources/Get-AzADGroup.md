---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADGroup.md
ms.openlocfilehash: 42696be07c560d24d1d87542873b6795497c370c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843477"
---
# <span data-ttu-id="f10cc-101">Get-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="f10cc-101">Get-AzADGroup</span></span>

## <span data-ttu-id="f10cc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f10cc-102">SYNOPSIS</span></span>
<span data-ttu-id="f10cc-103">Szűri az Active Directory-csoportokat.</span><span class="sxs-lookup"><span data-stu-id="f10cc-103">Filters active directory groups.</span></span>

## <span data-ttu-id="f10cc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f10cc-104">SYNTAX</span></span>

### <span data-ttu-id="f10cc-105">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f10cc-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f10cc-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="f10cc-106">SearchStringParameterSet</span></span>
```
Get-AzADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f10cc-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f10cc-107">DisplayNameParameterSet</span></span>
```
Get-AzADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f10cc-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f10cc-108">ObjectIdParameterSet</span></span>
```
Get-AzADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="f10cc-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="f10cc-109">DESCRIPTION</span></span>
<span data-ttu-id="f10cc-110">Szűri az Active Directory-csoportokat.</span><span class="sxs-lookup"><span data-stu-id="f10cc-110">Filters active directory groups.</span></span>

## <span data-ttu-id="f10cc-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f10cc-111">EXAMPLES</span></span>

### <span data-ttu-id="f10cc-112">Példa 1 – az összes HIRDETÉSCSOPORT listázása</span><span class="sxs-lookup"><span data-stu-id="f10cc-112">Example 1 - List all AD groups</span></span>
```
PS C:\> Get-AzADGroup
```

<span data-ttu-id="f10cc-113">A bérlői fiók összes HIRDETÉSCSOPORT-listája.</span><span class="sxs-lookup"><span data-stu-id="f10cc-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="f10cc-114">Példa 2 – minden HIRDETÉSCSOPORT listázása a lapozással</span><span class="sxs-lookup"><span data-stu-id="f10cc-114">Example 2 - List all AD groups using paging</span></span>

```
PS C:\> Get-AzADGroup -First 100
```

<span data-ttu-id="f10cc-115">Az első 100-HIRDETÉSCSOPORTOK listája a bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="f10cc-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="f10cc-116">Példa 3 – HIRDETÉSCSOPORT-azonosító beolvasása</span><span class="sxs-lookup"><span data-stu-id="f10cc-116">Example 3 - Get AD group by object id</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="f10cc-117">A "85F89C90-780E-4AA6-9F4F-6F268D322EEE" azonosítójú HIRDETÉSCSOPORTOT kapja.</span><span class="sxs-lookup"><span data-stu-id="f10cc-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="f10cc-118">Példa 4 – keresési karakterlánc szerint csoportosított listák</span><span class="sxs-lookup"><span data-stu-id="f10cc-118">Example 4 - List groups by search string</span></span>

```
PS C:\> Get-AzADGroup -SearchString Joe
```

<span data-ttu-id="f10cc-119">Felsorolja az összes olyan HIRDETÉSCSOPORTOT, amelynek a megjelenítendő neve "Joe"-val kezdődik.</span><span class="sxs-lookup"><span data-stu-id="f10cc-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="f10cc-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f10cc-120">PARAMETERS</span></span>

### <span data-ttu-id="f10cc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f10cc-121">-DefaultProfile</span></span>
<span data-ttu-id="f10cc-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f10cc-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f10cc-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f10cc-123">-DisplayName</span></span>
<span data-ttu-id="f10cc-124">A csoport megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="f10cc-124">The display name of the group.</span></span>

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

### <span data-ttu-id="f10cc-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="f10cc-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="f10cc-126">A megadott karakterlánccal kezdődő csoportok megkeresésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="f10cc-126">Used to find groups that begin with the provided string.</span></span>

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

### <span data-ttu-id="f10cc-127">– Első</span><span class="sxs-lookup"><span data-stu-id="f10cc-127">-First</span></span>
<span data-ttu-id="f10cc-128">A visszaadni kívánt objektumok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="f10cc-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="f10cc-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="f10cc-129">-IncludeTotalCount</span></span>
<span data-ttu-id="f10cc-130">Az adathalmaz objektumainak számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="f10cc-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="f10cc-131">Ez a paraméter jelenleg nem tesz semmit.</span><span class="sxs-lookup"><span data-stu-id="f10cc-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="f10cc-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f10cc-132">-ObjectId</span></span>
<span data-ttu-id="f10cc-133">A csoport objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f10cc-133">Object id of the group.</span></span>

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

### <span data-ttu-id="f10cc-134">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="f10cc-134">-Skip</span></span>
<span data-ttu-id="f10cc-135">Figyelmen kívül hagyja az első N objektumokat, és a fennmaradó objektumokat kapja.</span><span class="sxs-lookup"><span data-stu-id="f10cc-135">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="f10cc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f10cc-136">CommonParameters</span></span>
<span data-ttu-id="f10cc-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f10cc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f10cc-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f10cc-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f10cc-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f10cc-139">INPUTS</span></span>

### <span data-ttu-id="f10cc-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f10cc-140">System.String</span></span>

### <span data-ttu-id="f10cc-141">System. GUID</span><span class="sxs-lookup"><span data-stu-id="f10cc-141">System.Guid</span></span>

## <span data-ttu-id="f10cc-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f10cc-142">OUTPUTS</span></span>

### <span data-ttu-id="f10cc-143">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="f10cc-143">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="f10cc-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f10cc-144">NOTES</span></span>

## <span data-ttu-id="f10cc-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f10cc-145">RELATED LINKS</span></span>

[<span data-ttu-id="f10cc-146">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="f10cc-146">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="f10cc-147">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f10cc-147">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="f10cc-148">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="f10cc-148">Get-AzADGroupMember</span></span>](./Get-AzADGroupMember.md)

