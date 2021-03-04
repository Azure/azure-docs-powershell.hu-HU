---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
ms.openlocfilehash: 818e76c9ea46b2593b3bdd3871f417dbaca044a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931457"
---
# <span data-ttu-id="4afbe-101">New-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="4afbe-101">New-AzSqlInstancePool</span></span>

## <span data-ttu-id="4afbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4afbe-102">SYNOPSIS</span></span>
<span data-ttu-id="4afbe-103">Létrehoz egy Azure SQL-példánykészletet.</span><span class="sxs-lookup"><span data-stu-id="4afbe-103">Creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="4afbe-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4afbe-104">SYNTAX</span></span>

```
New-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> -Location <String> -SubnetId <String>
 -VCore <Int32> -Edition <String> -ComputeGeneration <String> -LicenseType <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4afbe-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4afbe-105">DESCRIPTION</span></span>
<span data-ttu-id="4afbe-106">A **New-AzSqlInstancePool** parancsmag létrehoz egy Azure SQL-példánykészletet.</span><span class="sxs-lookup"><span data-stu-id="4afbe-106">The **New-AzSqlInstancePool** cmdlet creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="4afbe-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4afbe-107">EXAMPLES</span></span>

### <span data-ttu-id="4afbe-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="4afbe-108">Example 1</span></span>
```powershell
PS C:\> New-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancepool0 -Location canadacentral -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -VCore 8 -Edition GeneralPurpose -ComputeGeneration Gen5 -LicenseType LicenseIncluded
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="4afbe-109">Ez a parancs egy új Azure SQL-példánykészletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4afbe-109">This command creates a new Azure SQL Instance pool.</span></span>

## <span data-ttu-id="4afbe-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4afbe-110">PARAMETERS</span></span>

### <span data-ttu-id="4afbe-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4afbe-111">-AsJob</span></span>
<span data-ttu-id="4afbe-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4afbe-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4afbe-113">-ComputeGeneráció</span><span class="sxs-lookup"><span data-stu-id="4afbe-113">-ComputeGeneration</span></span>
<span data-ttu-id="4afbe-114">A példánykészlet számítási generációja.</span><span class="sxs-lookup"><span data-stu-id="4afbe-114">The compute generation for the instance pool.</span></span>

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

### <span data-ttu-id="4afbe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4afbe-115">-DefaultProfile</span></span>
<span data-ttu-id="4afbe-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4afbe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4afbe-117">-Edition</span><span class="sxs-lookup"><span data-stu-id="4afbe-117">-Edition</span></span>
<span data-ttu-id="4afbe-118">A példánykészlet kiadása.</span><span class="sxs-lookup"><span data-stu-id="4afbe-118">The edition for the instance pool.</span></span>

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

### <span data-ttu-id="4afbe-119">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="4afbe-119">-LicenseType</span></span>
<span data-ttu-id="4afbe-120">Meghatározza, hogy melyik licenctípust kell használni.</span><span class="sxs-lookup"><span data-stu-id="4afbe-120">Determines which License Type to use.</span></span>
<span data-ttu-id="4afbe-121">A lehetséges értékek a BasePrice (HACS árengedménysel) és a LicenseIncluded (ÁRENGEDMÉNY nélkül).</span><span class="sxs-lookup"><span data-stu-id="4afbe-121">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="4afbe-122">-Location</span><span class="sxs-lookup"><span data-stu-id="4afbe-122">-Location</span></span>
<span data-ttu-id="4afbe-123">A példánykészlet létrehozására használt hely.</span><span class="sxs-lookup"><span data-stu-id="4afbe-123">The location to create the instance pool.</span></span>

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

### <span data-ttu-id="4afbe-124">-Name</span><span class="sxs-lookup"><span data-stu-id="4afbe-124">-Name</span></span>
<span data-ttu-id="4afbe-125">A példánykészlet neve.</span><span class="sxs-lookup"><span data-stu-id="4afbe-125">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afbe-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4afbe-126">-ResourceGroupName</span></span>
<span data-ttu-id="4afbe-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4afbe-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afbe-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4afbe-128">-SubnetId</span></span>
<span data-ttu-id="4afbe-129">A példánykészlet létrehozásához használt alhálózati azonosító.</span><span class="sxs-lookup"><span data-stu-id="4afbe-129">The subnet id to use for instance pool creation.</span></span>

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

### <span data-ttu-id="4afbe-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="4afbe-130">-Tag</span></span>
<span data-ttu-id="4afbe-131">A példányhoz társított címkék</span><span class="sxs-lookup"><span data-stu-id="4afbe-131">The tags to associate with the instance</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afbe-132">-VCore</span><span class="sxs-lookup"><span data-stu-id="4afbe-132">-VCore</span></span>
<span data-ttu-id="4afbe-133">Azt határozza meg, hogy mennyi VCore-t társít a példányhoz.</span><span class="sxs-lookup"><span data-stu-id="4afbe-133">Determines how much VCore to associate with instance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: VCores

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afbe-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4afbe-134">-Confirm</span></span>
<span data-ttu-id="4afbe-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4afbe-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4afbe-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4afbe-136">-WhatIf</span></span>
<span data-ttu-id="4afbe-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4afbe-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4afbe-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4afbe-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4afbe-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4afbe-139">CommonParameters</span></span>
<span data-ttu-id="4afbe-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4afbe-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4afbe-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4afbe-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4afbe-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4afbe-142">INPUTS</span></span>

### <span data-ttu-id="4afbe-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="4afbe-143">None</span></span>

## <span data-ttu-id="4afbe-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4afbe-144">OUTPUTS</span></span>

### <span data-ttu-id="4afbe-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="4afbe-145">System.Object</span></span>
## <span data-ttu-id="4afbe-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4afbe-146">NOTES</span></span>

## <span data-ttu-id="4afbe-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4afbe-147">RELATED LINKS</span></span>
