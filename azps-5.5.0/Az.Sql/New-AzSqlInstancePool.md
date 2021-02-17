---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
ms.openlocfilehash: 1b4f405e9bf6377855439d1f6d3cad9f0538920f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164930"
---
# <span data-ttu-id="1a1bb-101">New-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="1a1bb-101">New-AzSqlInstancePool</span></span>

## <span data-ttu-id="1a1bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a1bb-102">SYNOPSIS</span></span>
<span data-ttu-id="1a1bb-103">Létrehoz egy Azure SQL-példánykészletet.</span><span class="sxs-lookup"><span data-stu-id="1a1bb-103">Creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="1a1bb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1a1bb-104">SYNTAX</span></span>

```
New-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> -Location <String> -SubnetId <String>
 -VCore <Int32> -Edition <String> -ComputeGeneration <String> -LicenseType <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a1bb-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1a1bb-105">DESCRIPTION</span></span>
<span data-ttu-id="1a1bb-106">A **New-AzSqlInstancePool** parancsmag létrehoz egy Azure SQL-példánykészletet.</span><span class="sxs-lookup"><span data-stu-id="1a1bb-106">The **New-AzSqlInstancePool** cmdlet creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="1a1bb-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1a1bb-107">EXAMPLES</span></span>

### <span data-ttu-id="1a1bb-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="1a1bb-108">Example 1</span></span>
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

<span data-ttu-id="1a1bb-109">Ez a parancs létrehoz egy új Azure SQL-példánykészletet.</span><span class="sxs-lookup"><span data-stu-id="1a1bb-109">This command creates a new Azure SQL Instance pool.</span></span>

## <span data-ttu-id="1a1bb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a1bb-110">PARAMETERS</span></span>

### <span data-ttu-id="1a1bb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a1bb-111">-AsJob</span></span>
<span data-ttu-id="1a1bb-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1a1bb-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a1bb-113">-ComputeGeneráció</span><span class="sxs-lookup"><span data-stu-id="1a1bb-113">-ComputeGeneration</span></span>
<span data-ttu-id="1a1bb-114">A példánykészlet számítási generációja.</span><span class="sxs-lookup"><span data-stu-id="1a1bb-114">The compute generation for the instance pool.</span></span>

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

### <span data-ttu-id="1a1bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a1bb-115">-DefaultProfile</span></span>
<span data-ttu-id="1a1bb-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1a1bb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a1bb-117">-Edition</span><span class="sxs-lookup"><span data-stu-id="1a1bb-117">-Edition</span></span>
<span data-ttu-id="1a1bb-118">A példánykészlet kiadása.</span><span class="sxs-lookup"><span data-stu-id="1a1bb-118">The edition for the instance pool.</span></span>

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

### <span data-ttu-id="1a1bb-119">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="1a1bb-119">-LicenseType</span></span>
<span data-ttu-id="1a1bb-120">Meghatározza, hogy melyik licenctípust kell használni.</span><span class="sxs-lookup"><span data-stu-id="1a1bb-120">Determines which License Type to use.</span></span>
<span data-ttu-id="1a1bb-121">A lehetséges értékek a BasePrice (HAAACS-engedménysel) és a LicenseIncluded (ÁRENGEDMÉNY nélkül).</span><span class="sxs-lookup"><span data-stu-id="1a1bb-121">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="1a1bb-122">-Location</span><span class="sxs-lookup"><span data-stu-id="1a1bb-122">-Location</span></span>
<span data-ttu-id="1a1bb-123">A példánykészlet létrehozására használt hely.</span><span class="sxs-lookup"><span data-stu-id="1a1bb-123">The location to create the instance pool.</span></span>

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

### <span data-ttu-id="1a1bb-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1a1bb-124">-Name</span></span>
<span data-ttu-id="1a1bb-125">A példánykészlet neve.</span><span class="sxs-lookup"><span data-stu-id="1a1bb-125">The name of the instance pool.</span></span>

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

### <span data-ttu-id="1a1bb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a1bb-126">-ResourceGroupName</span></span>
<span data-ttu-id="1a1bb-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1a1bb-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="1a1bb-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="1a1bb-128">-SubnetId</span></span>
<span data-ttu-id="1a1bb-129">A példánykészlet létrehozásához használt alhálózati azonosító.</span><span class="sxs-lookup"><span data-stu-id="1a1bb-129">The subnet id to use for instance pool creation.</span></span>

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

### <span data-ttu-id="1a1bb-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="1a1bb-130">-Tag</span></span>
<span data-ttu-id="1a1bb-131">A példányhoz társított címkék</span><span class="sxs-lookup"><span data-stu-id="1a1bb-131">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="1a1bb-132">-VCore</span><span class="sxs-lookup"><span data-stu-id="1a1bb-132">-VCore</span></span>
<span data-ttu-id="1a1bb-133">Azt határozza meg, hogy mennyi VCore-t társít a példányhoz.</span><span class="sxs-lookup"><span data-stu-id="1a1bb-133">Determines how much VCore to associate with instance.</span></span>

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

### <span data-ttu-id="1a1bb-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a1bb-134">-Confirm</span></span>
<span data-ttu-id="1a1bb-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1a1bb-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a1bb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a1bb-136">-WhatIf</span></span>
<span data-ttu-id="1a1bb-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1a1bb-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a1bb-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1a1bb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a1bb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a1bb-139">CommonParameters</span></span>
<span data-ttu-id="1a1bb-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a1bb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a1bb-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a1bb-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a1bb-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1a1bb-142">INPUTS</span></span>

### <span data-ttu-id="1a1bb-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="1a1bb-143">None</span></span>

## <span data-ttu-id="1a1bb-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a1bb-144">OUTPUTS</span></span>

### <span data-ttu-id="1a1bb-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="1a1bb-145">System.Object</span></span>
## <span data-ttu-id="1a1bb-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1a1bb-146">NOTES</span></span>

## <span data-ttu-id="1a1bb-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1a1bb-147">RELATED LINKS</span></span>
