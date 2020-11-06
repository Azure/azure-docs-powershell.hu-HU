---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
ms.openlocfilehash: ffc04a6b1560845a0c29db4d000270fe91aa8ff4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505728"
---
# <span data-ttu-id="20e66-101">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="20e66-101">Get-AzureRmADGroupMember</span></span>

## <span data-ttu-id="20e66-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="20e66-102">SYNOPSIS</span></span>
<span data-ttu-id="20e66-103">Az aktuális bérlői fiókban lévő HIRDETÉSCSOPORT tagjainak listája.</span><span class="sxs-lookup"><span data-stu-id="20e66-103">Lists members of an AD group in the current tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20e66-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="20e66-104">SYNTAX</span></span>

### <span data-ttu-id="20e66-105">ObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="20e66-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADGroupMember [-GroupObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="20e66-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="20e66-106">DisplayNameParameterSet</span></span>
```
Get-AzureRmADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="20e66-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20e66-107">GroupObjectParameterSet</span></span>
```
Get-AzureRmADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="20e66-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="20e66-108">DESCRIPTION</span></span>
<span data-ttu-id="20e66-109">Az aktuális bérlői fiókban lévő HIRDETÉSCSOPORT tagjainak listája.</span><span class="sxs-lookup"><span data-stu-id="20e66-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="20e66-110">Példák</span><span class="sxs-lookup"><span data-stu-id="20e66-110">EXAMPLES</span></span>

### <span data-ttu-id="20e66-111">Példa 1 – HIRDETÉSCSOPORT-objektum azonosítójának listázása</span><span class="sxs-lookup"><span data-stu-id="20e66-111">Example 1 - List members by AD group object id</span></span>

```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="20e66-112">Felsorolja az "85F89C90-780E-4AA6-9F4F-6F268D322EEE" azonosítójú HIRDETÉSCSOPORT tagjait.</span><span class="sxs-lookup"><span data-stu-id="20e66-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="20e66-113">Példa: 2 – a tagokat a HIRDETÉSCSOPORT-azonosítók listája a lapozással</span><span class="sxs-lookup"><span data-stu-id="20e66-113">Example 2 - List members by AD group object id using paging</span></span>

```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="20e66-114">A "85F89C90-780E-4AA6-9F4F-6F268D322EEE" azonosítójú HIRDETÉSCSOPORT első 100-tagjainak listája.</span><span class="sxs-lookup"><span data-stu-id="20e66-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="20e66-115">Példa: 3 – a tagok listája csővezetékek szerint</span><span class="sxs-lookup"><span data-stu-id="20e66-115">Example 3 - List members by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzureRmADGroupMember
```

<span data-ttu-id="20e66-116">Megkapja a "85F89C90-780E-4AA6-9F4F-6F268D322EEE" azonosítójú HIRDETÉSCSOPORTOT, és a csoport összes tagjának listázásához a Get-AzureRmADGroupMember parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="20e66-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzureRmADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="20e66-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="20e66-117">PARAMETERS</span></span>

### <span data-ttu-id="20e66-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20e66-118">-DefaultProfile</span></span>
<span data-ttu-id="20e66-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="20e66-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20e66-120">– Első</span><span class="sxs-lookup"><span data-stu-id="20e66-120">-First</span></span>
<span data-ttu-id="20e66-121">A visszaadni kívánt objektumok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="20e66-121">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="20e66-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="20e66-122">-GroupDisplayName</span></span>
<span data-ttu-id="20e66-123">A csoport megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="20e66-123">The display name of the group.</span></span>

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

### <span data-ttu-id="20e66-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="20e66-124">-GroupObject</span></span>
<span data-ttu-id="20e66-125">Annak a csoportnak az objektuma, amelyből a tagokat listázni kívánja.</span><span class="sxs-lookup"><span data-stu-id="20e66-125">The group object that you are listing members from.</span></span>

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

### <span data-ttu-id="20e66-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="20e66-126">-GroupObjectId</span></span>
<span data-ttu-id="20e66-127">A csoport objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="20e66-127">Object Id of the group.</span></span>

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

### <span data-ttu-id="20e66-128">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="20e66-128">-IncludeTotalCount</span></span>
<span data-ttu-id="20e66-129">Az adathalmaz objektumainak számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="20e66-129">Reports the number of objects in the data set.</span></span> <span data-ttu-id="20e66-130">Ez a paraméter jelenleg nem tesz semmit.</span><span class="sxs-lookup"><span data-stu-id="20e66-130">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="20e66-131">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="20e66-131">-Skip</span></span>
<span data-ttu-id="20e66-132">Figyelmen kívül hagyja az első N objektumokat, és a fennmaradó objektumokat kapja.</span><span class="sxs-lookup"><span data-stu-id="20e66-132">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="20e66-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20e66-133">CommonParameters</span></span>
<span data-ttu-id="20e66-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="20e66-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20e66-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20e66-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20e66-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="20e66-136">INPUTS</span></span>

### <span data-ttu-id="20e66-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="20e66-137">System.Guid</span></span>

### <span data-ttu-id="20e66-138">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="20e66-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="20e66-139">Paraméterek: GroupObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="20e66-139">Parameters: GroupObject (ByValue)</span></span>

## <span data-ttu-id="20e66-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20e66-140">OUTPUTS</span></span>

### <span data-ttu-id="20e66-141">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADObject</span><span class="sxs-lookup"><span data-stu-id="20e66-141">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="20e66-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="20e66-142">NOTES</span></span>

## <span data-ttu-id="20e66-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20e66-143">RELATED LINKS</span></span>

[<span data-ttu-id="20e66-144">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="20e66-144">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="20e66-145">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="20e66-145">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

