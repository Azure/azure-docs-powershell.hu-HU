---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/new-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsInstance.md
ms.openlocfilehash: d6a748897b956759ad64056b0d9b83a6e82e91fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167611"
---
# <span data-ttu-id="04fc2-101">New-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="04fc2-101">New-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="04fc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04fc2-102">SYNOPSIS</span></span>
<span data-ttu-id="04fc2-103">Létrehozhatja vagy frissítheti a DigitalTwinsInstance metaadatait.</span><span class="sxs-lookup"><span data-stu-id="04fc2-103">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="04fc2-104">A tulajdonság módosításának szokásos sémája az, hogy beolvassa a DigitalTwinsInstance és a biztonsági metaadatokat, majd kombinálja őket a módosított értékekkel egy új törzsben a DigitalTwinsInstance frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="04fc2-104">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="04fc2-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="04fc2-105">SYNTAX</span></span>

### <span data-ttu-id="04fc2-106">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="04fc2-106">CreateExpanded (Default)</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> -Location <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="04fc2-107">Létrehozás</span><span class="sxs-lookup"><span data-stu-id="04fc2-107">Create</span></span>
```
New-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsCreate <IDigitalTwinsDescription> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="04fc2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="04fc2-108">DESCRIPTION</span></span>
<span data-ttu-id="04fc2-109">Létrehozhatja vagy frissítheti a DigitalTwinsInstance metaadatait.</span><span class="sxs-lookup"><span data-stu-id="04fc2-109">Create or update the metadata of a DigitalTwinsInstance.</span></span>
<span data-ttu-id="04fc2-110">A tulajdonság módosításának szokásos sémája az, hogy beolvassa a DigitalTwinsInstance és a biztonsági metaadatokat, majd kombinálja őket a módosított értékekkel egy új törzsben a DigitalTwinsInstance frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="04fc2-110">The usual pattern to modify a property is to retrieve the DigitalTwinsInstance and security metadata, and then combine them with the modified values in a new body to update the DigitalTwinsInstance.</span></span>

## <span data-ttu-id="04fc2-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="04fc2-111">EXAMPLES</span></span>

### <span data-ttu-id="04fc2-112">1. példa: AzDigitalTwinsInstance alapértelmezés szerint.</span><span class="sxs-lookup"><span data-stu-id="04fc2-112">Example 1: Create an AzDigitalTwinsInstance by default.</span></span>
```powershell
PS C:\> New-AzDigitalTwinsInstance -ResourceGroupName youritest -ResourceName youriDigitalTwin -Location eastus

Location Name             SkuName Type
-------- ----             ------- ----
eastus   youriDigitalTwin S1      Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="04fc2-113">AzDigitalTwinsInstance alapértelmezés szerint</span><span class="sxs-lookup"><span data-stu-id="04fc2-113">Create an AzDigitalTwinsInstance by default</span></span>

### <span data-ttu-id="04fc2-114">2. példa: AzDigitalTwinsInstance by AzDigitalTwins objektum létrehozása.</span><span class="sxs-lookup"><span data-stu-id="04fc2-114">Example 2: Create an AzDigitalTwinsInstance by AzDigitalTwins Object.</span></span>
```powershell
PS C:\> $GetAzDigTwin = Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
New-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest01 -DigitalTwinsCreate $getAzdigitalTwins

Location Name                    Type
-------- ----                    ----
eastus   youriDigitalTwinsTest01 Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="04fc2-115">AzDigitalTwinsInstance by AzDigitalTwins objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="04fc2-115">Create an AzDigitalTwinsInstance by AzDigitalTwins Object</span></span>

## <span data-ttu-id="04fc2-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04fc2-116">PARAMETERS</span></span>

### <span data-ttu-id="04fc2-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04fc2-117">-AsJob</span></span>
<span data-ttu-id="04fc2-118">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="04fc2-118">Run the command as a job</span></span>

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

### <span data-ttu-id="04fc2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04fc2-119">-DefaultProfile</span></span>
<span data-ttu-id="04fc2-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="04fc2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04fc2-121">-DigitalTwinsCreate</span><span class="sxs-lookup"><span data-stu-id="04fc2-121">-DigitalTwinsCreate</span></span>
<span data-ttu-id="04fc2-122">A DigitalTwins szolgáltatás leírása.</span><span class="sxs-lookup"><span data-stu-id="04fc2-122">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="04fc2-123">Ennek létrehozásáról a DIGITALTWINSCREATE tulajdonságokat és a hash táblázatot hoz létre a NOTES (JEGYZETEK) című szakaszban található.</span><span class="sxs-lookup"><span data-stu-id="04fc2-123">To construct, see NOTES section for DIGITALTWINSCREATE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04fc2-124">-Location</span><span class="sxs-lookup"><span data-stu-id="04fc2-124">-Location</span></span>
<span data-ttu-id="04fc2-125">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="04fc2-125">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04fc2-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="04fc2-126">-NoWait</span></span>
<span data-ttu-id="04fc2-127">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="04fc2-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="04fc2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04fc2-128">-ResourceGroupName</span></span>
<span data-ttu-id="04fc2-129">A DigitalTwinsInstance erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="04fc2-129">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04fc2-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="04fc2-130">-ResourceName</span></span>
<span data-ttu-id="04fc2-131">A DigitalTwinsInstance név.</span><span class="sxs-lookup"><span data-stu-id="04fc2-131">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04fc2-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="04fc2-132">-SubscriptionId</span></span>
<span data-ttu-id="04fc2-133">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="04fc2-133">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04fc2-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="04fc2-134">-Tag</span></span>
<span data-ttu-id="04fc2-135">Az erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="04fc2-135">The resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04fc2-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04fc2-136">-Confirm</span></span>
<span data-ttu-id="04fc2-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="04fc2-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04fc2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04fc2-138">-WhatIf</span></span>
<span data-ttu-id="04fc2-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="04fc2-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04fc2-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="04fc2-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04fc2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04fc2-141">CommonParameters</span></span>
<span data-ttu-id="04fc2-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04fc2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04fc2-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04fc2-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04fc2-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="04fc2-144">INPUTS</span></span>

### <span data-ttu-id="04fc2-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="04fc2-145">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="04fc2-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04fc2-146">OUTPUTS</span></span>

### <span data-ttu-id="04fc2-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="04fc2-147">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="04fc2-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="04fc2-148">NOTES</span></span>

<span data-ttu-id="04fc2-149">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="04fc2-149">ALIASES</span></span>

<span data-ttu-id="04fc2-150">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="04fc2-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="04fc2-151">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="04fc2-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="04fc2-152">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="04fc2-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="04fc2-153">DIGITALTWINSCREATE: <IDigitalTwinsDescription> A DigitalTwins szolgáltatás leírása.</span><span class="sxs-lookup"><span data-stu-id="04fc2-153">DIGITALTWINSCREATE <IDigitalTwinsDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="04fc2-154">`Location <String>`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="04fc2-154">`Location <String>`: The resource location.</span></span>
  - <span data-ttu-id="04fc2-155">`[Tag <IDigitalTwinsResourceTags>]`: Az erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="04fc2-155">`[Tag <IDigitalTwinsResourceTags>]`: The resource tags.</span></span>
    - <span data-ttu-id="04fc2-156">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.</span><span class="sxs-lookup"><span data-stu-id="04fc2-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="04fc2-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04fc2-157">RELATED LINKS</span></span>

