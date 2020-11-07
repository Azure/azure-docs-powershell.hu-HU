---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroup
schema: 2.0.0
ms.openlocfilehash: 9ddc9658d6d18cc7a08df33f1f976521656c9234
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849050"
---
# <span data-ttu-id="1ef3e-101">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="1ef3e-101">Get-AzureRmADGroup</span></span>

## <span data-ttu-id="1ef3e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1ef3e-102">SYNOPSIS</span></span>
<span data-ttu-id="1ef3e-103">Szűri az Active Directory-csoportokat.</span><span class="sxs-lookup"><span data-stu-id="1ef3e-103">Filters active directory groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ef3e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1ef3e-104">SYNTAX</span></span>

### <span data-ttu-id="1ef3e-105">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1ef3e-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="1ef3e-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ef3e-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="1ef3e-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ef3e-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="1ef3e-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ef3e-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="1ef3e-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="1ef3e-109">DESCRIPTION</span></span>
<span data-ttu-id="1ef3e-110">Szűri az Active Directory-csoportokat.</span><span class="sxs-lookup"><span data-stu-id="1ef3e-110">Filters active directory groups.</span></span>

## <span data-ttu-id="1ef3e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="1ef3e-111">EXAMPLES</span></span>

### <span data-ttu-id="1ef3e-112">Példa 1 – az összes HIRDETÉSCSOPORT listázása</span><span class="sxs-lookup"><span data-stu-id="1ef3e-112">Example 1 - List all AD groups</span></span>
```
PS C:\> Get-AzureRmADGroup
```

<span data-ttu-id="1ef3e-113">A bérlői fiók összes HIRDETÉSCSOPORT-listája.</span><span class="sxs-lookup"><span data-stu-id="1ef3e-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="1ef3e-114">Példa 2 – minden HIRDETÉSCSOPORT listázása a lapozással</span><span class="sxs-lookup"><span data-stu-id="1ef3e-114">Example 2 - List all AD groups using paging</span></span>

```
PS C:\> Get-AzureRmADGroup -First 100
```

<span data-ttu-id="1ef3e-115">Az első 100-HIRDETÉSCSOPORTOK listája a bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="1ef3e-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="1ef3e-116">Példa 3 – HIRDETÉSCSOPORT-azonosító beolvasása</span><span class="sxs-lookup"><span data-stu-id="1ef3e-116">Example 3 - Get AD group by object id</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="1ef3e-117">A "85F89C90-780E-4AA6-9F4F-6F268D322EEE" azonosítójú HIRDETÉSCSOPORTOT kapja.</span><span class="sxs-lookup"><span data-stu-id="1ef3e-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="1ef3e-118">Példa 4 – keresési karakterlánc szerint csoportosított listák</span><span class="sxs-lookup"><span data-stu-id="1ef3e-118">Example 4 - List groups by search string</span></span>

```
PS C:\> Get-AzureRmADGroup -SearchString Joe
```

<span data-ttu-id="1ef3e-119">Felsorolja az összes olyan HIRDETÉSCSOPORTOT, amelynek a megjelenítendő neve "Joe"-val kezdődik.</span><span class="sxs-lookup"><span data-stu-id="1ef3e-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="1ef3e-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1ef3e-120">PARAMETERS</span></span>

### <span data-ttu-id="1ef3e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ef3e-121">-DefaultProfile</span></span>
<span data-ttu-id="1ef3e-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1ef3e-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ef3e-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1ef3e-123">-DisplayName</span></span>
<span data-ttu-id="1ef3e-124">A csoport megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="1ef3e-124">The display name of the group.</span></span>

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

### <span data-ttu-id="1ef3e-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="1ef3e-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="1ef3e-126">A megadott karakterlánccal kezdődő csoportok megkeresésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="1ef3e-126">Used to find groups that begin with the provided string.</span></span>

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

### <span data-ttu-id="1ef3e-127">– Első</span><span class="sxs-lookup"><span data-stu-id="1ef3e-127">-First</span></span>
<span data-ttu-id="1ef3e-128">A visszaadni kívánt objektumok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="1ef3e-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="1ef3e-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="1ef3e-129">-IncludeTotalCount</span></span>
<span data-ttu-id="1ef3e-130">Az adathalmaz objektumainak számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="1ef3e-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="1ef3e-131">Ez a paraméter jelenleg nem tesz semmit.</span><span class="sxs-lookup"><span data-stu-id="1ef3e-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="1ef3e-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1ef3e-132">-ObjectId</span></span>
<span data-ttu-id="1ef3e-133">A csoport objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1ef3e-133">Object id of the group.</span></span>

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

### <span data-ttu-id="1ef3e-134">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="1ef3e-134">-Skip</span></span>
<span data-ttu-id="1ef3e-135">Figyelmen kívül hagyja az első N objektumokat, és a fennmaradó objektumokat kapja.</span><span class="sxs-lookup"><span data-stu-id="1ef3e-135">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="1ef3e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ef3e-136">CommonParameters</span></span>
<span data-ttu-id="1ef3e-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1ef3e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ef3e-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ef3e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ef3e-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ef3e-139">INPUTS</span></span>

### <span data-ttu-id="1ef3e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1ef3e-140">System.String</span></span>

### <span data-ttu-id="1ef3e-141">System. GUID</span><span class="sxs-lookup"><span data-stu-id="1ef3e-141">System.Guid</span></span>

## <span data-ttu-id="1ef3e-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ef3e-142">OUTPUTS</span></span>

### <span data-ttu-id="1ef3e-143">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="1ef3e-143">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="1ef3e-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1ef3e-144">NOTES</span></span>

## <span data-ttu-id="1ef3e-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ef3e-145">RELATED LINKS</span></span>

[<span data-ttu-id="1ef3e-146">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="1ef3e-146">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="1ef3e-147">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1ef3e-147">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="1ef3e-148">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="1ef3e-148">Get-AzureRmADGroupMember</span></span>](./Get-AzureRmADGroupMember.md)

