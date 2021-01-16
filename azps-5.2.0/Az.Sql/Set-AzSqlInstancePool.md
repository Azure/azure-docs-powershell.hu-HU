---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
ms.openlocfilehash: db7d9165b8aec6a69f31850f7a37eddb2450e53b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360610"
---
# <span data-ttu-id="64f82-101">Set-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="64f82-101">Set-AzSqlInstancePool</span></span>

## <span data-ttu-id="64f82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64f82-102">SYNOPSIS</span></span>
<span data-ttu-id="64f82-103">Beállítja egy Azure SQL-példánykészlet tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="64f82-103">Sets properties for an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="64f82-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="64f82-104">SYNTAX</span></span>

### <span data-ttu-id="64f82-105">DefaultSetInstancePoolParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="64f82-105">DefaultSetInstancePoolParameterSet (Default)</span></span>
```
Set-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64f82-106">InputObjectSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="64f82-106">InputObjectSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64f82-107">ResourceIdSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="64f82-107">ResourceIdSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-ResourceId] <String> [-LicenseType <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64f82-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="64f82-108">DESCRIPTION</span></span>
<span data-ttu-id="64f82-109">A **Set-AzSqlInstancePool** parancsmag módosítja egy Azure SQL-példánykészlet tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="64f82-109">The **Set-AzSqlInstancePool** cmdlet modifies properties of an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="64f82-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="64f82-110">EXAMPLES</span></span>

### <span data-ttu-id="64f82-111">1. példa: Példánykészlet licenctípusának beállítása</span><span class="sxs-lookup"><span data-stu-id="64f82-111">Example 1 : Set an instance pool license type</span></span>
```powershell
PS C:\> Set-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0 -LicenseType LicenseIncluded
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

<span data-ttu-id="64f82-112">Ez a parancs beállítja egy példányPool0 nevű példánykészlet licenctípusát és/vagy címkéit.</span><span class="sxs-lookup"><span data-stu-id="64f82-112">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

### <span data-ttu-id="64f82-113">2. példa: Példánykészlet licenctípusának beállítása egy példánykészlet-objektum használatával</span><span class="sxs-lookup"><span data-stu-id="64f82-113">Example 2 : Set an instance pool license type using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0
PS C:\> Set-AzSqlInstancePool -InputObject $instancePool -LicenseType LicenseIncluded
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

<span data-ttu-id="64f82-114">Ez a parancs egy példánykészlet-objektum használatával beállítja egy példánykészlet licenctípusát és/vagy címkéit.</span><span class="sxs-lookup"><span data-stu-id="64f82-114">This command sets the license type and/or tags for an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="64f82-115">3. példa: Példánykészlet licenctípusának beállítása egy példánykészlet erőforrás-azonosítójával</span><span class="sxs-lookup"><span data-stu-id="64f82-115">Example 3 : Set an instance pool license type using an instance pool resource id</span></span>
```powershell
PS C:\> Set-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0" -LicenseType LicenseIncluded
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

<span data-ttu-id="64f82-116">Ez a parancs beállítja egy példányPool0 nevű példánykészlet licenctípusát és/vagy címkéit.</span><span class="sxs-lookup"><span data-stu-id="64f82-116">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

## <span data-ttu-id="64f82-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64f82-117">PARAMETERS</span></span>

### <span data-ttu-id="64f82-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64f82-118">-AsJob</span></span>
<span data-ttu-id="64f82-119">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="64f82-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="64f82-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64f82-120">-DefaultProfile</span></span>
<span data-ttu-id="64f82-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64f82-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64f82-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64f82-122">-InputObject</span></span>
<span data-ttu-id="64f82-123">A példánykészlet bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="64f82-123">The instance pool input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: InputObjectSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64f82-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="64f82-124">-LicenseType</span></span>
<span data-ttu-id="64f82-125">Meghatározza, hogy melyik licenctípust kell használni.</span><span class="sxs-lookup"><span data-stu-id="64f82-125">Determines which License Type to use.</span></span>
<span data-ttu-id="64f82-126">A lehetséges értékek a BasePrice (HACS árengedménysel) és a LicenseIncluded (ÁRENGEDMÉNY nélkül).</span><span class="sxs-lookup"><span data-stu-id="64f82-126">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64f82-127">-Name</span><span class="sxs-lookup"><span data-stu-id="64f82-127">-Name</span></span>
<span data-ttu-id="64f82-128">A példánykészlet neve.</span><span class="sxs-lookup"><span data-stu-id="64f82-128">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSetInstancePoolParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64f82-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64f82-129">-ResourceGroupName</span></span>
<span data-ttu-id="64f82-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="64f82-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64f82-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64f82-131">-ResourceId</span></span>
<span data-ttu-id="64f82-132">A példánykészlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="64f82-132">The instance pool resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64f82-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="64f82-133">-Tag</span></span>
<span data-ttu-id="64f82-134">A példányhoz társított címkék</span><span class="sxs-lookup"><span data-stu-id="64f82-134">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="64f82-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64f82-135">-Confirm</span></span>
<span data-ttu-id="64f82-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="64f82-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64f82-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64f82-137">-WhatIf</span></span>
<span data-ttu-id="64f82-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="64f82-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64f82-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="64f82-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64f82-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64f82-140">CommonParameters</span></span>
<span data-ttu-id="64f82-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64f82-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64f82-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64f82-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64f82-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="64f82-143">INPUTS</span></span>

### <span data-ttu-id="64f82-144">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="64f82-144">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="64f82-145">System.String</span><span class="sxs-lookup"><span data-stu-id="64f82-145">System.String</span></span>

## <span data-ttu-id="64f82-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64f82-146">OUTPUTS</span></span>

### <span data-ttu-id="64f82-147">System.Object</span><span class="sxs-lookup"><span data-stu-id="64f82-147">System.Object</span></span>
## <span data-ttu-id="64f82-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="64f82-148">NOTES</span></span>

## <span data-ttu-id="64f82-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64f82-149">RELATED LINKS</span></span>
