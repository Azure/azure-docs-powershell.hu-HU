---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADGroup.md
ms.openlocfilehash: 4d285471632c9c4bc952b2dcdc0e4ce5147fac12
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843302"
---
# <span data-ttu-id="885a4-101">Remove-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="885a4-101">Remove-AzADGroup</span></span>

## <span data-ttu-id="885a4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="885a4-102">SYNOPSIS</span></span>
<span data-ttu-id="885a4-103">Active Directory-csoport törlése</span><span class="sxs-lookup"><span data-stu-id="885a4-103">Deletes an active directory group.</span></span>

## <span data-ttu-id="885a4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="885a4-104">SYNTAX</span></span>

### <span data-ttu-id="885a4-105">ObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="885a4-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADGroup -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="885a4-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="885a4-106">DisplayNameParameterSet</span></span>
```
Remove-AzADGroup -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="885a4-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="885a4-107">InputObjectParameterSet</span></span>
```
Remove-AzADGroup -InputObject <PSADGroup> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="885a4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="885a4-108">DESCRIPTION</span></span>
<span data-ttu-id="885a4-109">Active Directory-csoport törlése</span><span class="sxs-lookup"><span data-stu-id="885a4-109">Deletes an active directory group.</span></span>

## <span data-ttu-id="885a4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="885a4-110">EXAMPLES</span></span>

### <span data-ttu-id="885a4-111">Példa 1 – csoport objektum-azonosítójának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="885a4-111">Example 1 - Remove a group by object id</span></span>

```
PS C:\> Remove-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="885a4-112">Eltávolítja az "85F89C90-780E-4AA6-9F4F-6F268D322EEE" azonosítójú csoportot a bérlői webhelyről.</span><span class="sxs-lookup"><span data-stu-id="885a4-112">Removes the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' from the tenant.</span></span>

### <span data-ttu-id="885a4-113">2. példa – csoport eltávolítása csővezetékről</span><span class="sxs-lookup"><span data-stu-id="885a4-113">Example 2 - Remove a group by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroup
```

<span data-ttu-id="885a4-114">Megkapja a csoportot a "85F89C90-780E-4AA6-9F4F-6F268D322EEE" azonosítójú azonosítójú objektummal, és a csöveket, amelyek Remove-AzADGroup a csoport eltávolítását a bérlői fiókból.</span><span class="sxs-lookup"><span data-stu-id="885a4-114">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes that to Remove-AzADGroup to remove the group from the tenant.</span></span>

## <span data-ttu-id="885a4-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="885a4-115">PARAMETERS</span></span>

### <span data-ttu-id="885a4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="885a4-116">-DefaultProfile</span></span>
<span data-ttu-id="885a4-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="885a4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="885a4-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="885a4-118">-DisplayName</span></span>
<span data-ttu-id="885a4-119">Annak a csoportnak a megjelenítendő neve, amelyet el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="885a4-119">The display name of the group to be removed.</span></span>

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

### <span data-ttu-id="885a4-120">-Force</span><span class="sxs-lookup"><span data-stu-id="885a4-120">-Force</span></span>
<span data-ttu-id="885a4-121">Ha meg van adva, nem kér megerősítést a csoport törléséhez.</span><span class="sxs-lookup"><span data-stu-id="885a4-121">If specified, doesn't ask for confirmation for deleting the group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="885a4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="885a4-122">-InputObject</span></span>
<span data-ttu-id="885a4-123">Az eltávolítandó csoport objektum-ábrázolása.</span><span class="sxs-lookup"><span data-stu-id="885a4-123">The object representation of the group to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="885a4-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="885a4-124">-ObjectId</span></span>
<span data-ttu-id="885a4-125">Az eltávolítandó csoport objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="885a4-125">The object id of the group to be removed.</span></span>

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

### <span data-ttu-id="885a4-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="885a4-126">-PassThru</span></span>
<span data-ttu-id="885a4-127">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="885a4-127">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="885a4-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="885a4-128">-Confirm</span></span>
<span data-ttu-id="885a4-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="885a4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="885a4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="885a4-130">-WhatIf</span></span>
<span data-ttu-id="885a4-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="885a4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="885a4-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="885a4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="885a4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="885a4-133">CommonParameters</span></span>
<span data-ttu-id="885a4-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="885a4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="885a4-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="885a4-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="885a4-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="885a4-136">INPUTS</span></span>

### <span data-ttu-id="885a4-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="885a4-137">System.Guid</span></span>

### <span data-ttu-id="885a4-138">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="885a4-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="885a4-139">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="885a4-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="885a4-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="885a4-140">OUTPUTS</span></span>

### <span data-ttu-id="885a4-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="885a4-141">System.Boolean</span></span>

## <span data-ttu-id="885a4-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="885a4-142">NOTES</span></span>

## <span data-ttu-id="885a4-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="885a4-143">RELATED LINKS</span></span>
