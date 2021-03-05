---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePool.md
ms.openlocfilehash: 524d9ff479355f511b9039e1ea64a8234e37e021
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999318"
---
# <span data-ttu-id="68633-101">Get-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="68633-101">Get-AzSqlInstancePool</span></span>

## <span data-ttu-id="68633-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68633-102">SYNOPSIS</span></span>
<span data-ttu-id="68633-103">Az Azure SQL-példánykészletre vonatkozó információkat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="68633-103">Returns information about the Azure SQL Instance pool.</span></span>

## <span data-ttu-id="68633-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="68633-104">SYNTAX</span></span>

### <span data-ttu-id="68633-105">ListBySubOrResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="68633-105">ListBySubOrResourceGroupParameterSet (Default)</span></span>
```
Get-AzSqlInstancePool [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="68633-106">ListByInstancePoolDefaultsParameterSet</span><span class="sxs-lookup"><span data-stu-id="68633-106">ListByInstancePoolDefaultsParameterSet</span></span>
```
Get-AzSqlInstancePool -ResourceGroupName <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="68633-107">GetInstancePoolByInstancePoolResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="68633-107">GetInstancePoolByInstancePoolResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68633-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="68633-108">DESCRIPTION</span></span>
<span data-ttu-id="68633-109">A **Get-AzSqlInstancePool** parancsmag egy vagy több Azure SQL-példánykészlet adatait adja vissza.</span><span class="sxs-lookup"><span data-stu-id="68633-109">The **Get-AzSqlInstancePool** cmdlet returns information about one or more Azure SQL Instance pool.</span></span>
<span data-ttu-id="68633-110">Adja meg egy példánykészlet nevét, hogy csak az adott példánykészlet adatait lássa.</span><span class="sxs-lookup"><span data-stu-id="68633-110">Specify the name of an instance pool to see information for only that instance pool.</span></span>

## <span data-ttu-id="68633-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="68633-111">EXAMPLES</span></span>

### <span data-ttu-id="68633-112">1. példa: Az összes példánykészlet lekérte egy ügyfél-előfizetésben</span><span class="sxs-lookup"><span data-stu-id="68633-112">Example 1: Get all instance pools across a customer subscription</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool
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

ResourceGroupName : resourcegroup02
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup02/providers/Microsoft.Sql/instancePools/ps-instancepool-1
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup02/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="68633-113">Ez a parancs információkat kap az ügyfél-előfizetésben található összes példánykészletről.</span><span class="sxs-lookup"><span data-stu-id="68633-113">This command gets information about all instance pools within the customer subscription.</span></span>

### <span data-ttu-id="68633-114">2. példa: Az erőforráscsoport összes példánykészletének lekérte</span><span class="sxs-lookup"><span data-stu-id="68633-114">Example 2: Get all instance pools across a resource group</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroupName resourcegroup01
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

<span data-ttu-id="68633-115">Ez a parancs információkat kap az erőforráscsoport erőforráscsoport01-ében található összes példánykészletről.</span><span class="sxs-lookup"><span data-stu-id="68633-115">This command gets information about all instance pools within the resource group resourcegroup01.</span></span>

### <span data-ttu-id="68633-116">3. példa: Információ lekérte egy példánykészletről</span><span class="sxs-lookup"><span data-stu-id="68633-116">Example 3: Get information about an instance pool</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0
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

<span data-ttu-id="68633-117">Ez a parancs információkat kap a példánykészlet PéldánySor0 mappáról.</span><span class="sxs-lookup"><span data-stu-id="68633-117">This command gets information about the instance pool instancePool0.</span></span>

### <span data-ttu-id="68633-118">4. példa: Információ lekérte egy példánykészletről a példánykészlet erőforrás-azonosítóját használva</span><span class="sxs-lookup"><span data-stu-id="68633-118">Example 4: Get information about an instance pool using instance pool resource id</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
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

<span data-ttu-id="68633-119">Ez a parancs információt kap a példánykészletről az erőforrás-azonosítóval együtt.</span><span class="sxs-lookup"><span data-stu-id="68633-119">This command gets information about the instance pool with its resource identifier.</span></span>

## <span data-ttu-id="68633-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68633-120">PARAMETERS</span></span>

### <span data-ttu-id="68633-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68633-121">-DefaultProfile</span></span>
<span data-ttu-id="68633-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="68633-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68633-123">-Name</span><span class="sxs-lookup"><span data-stu-id="68633-123">-Name</span></span>
<span data-ttu-id="68633-124">A példánykészlet neve.</span><span class="sxs-lookup"><span data-stu-id="68633-124">The instance pool name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolDefaultsParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68633-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68633-125">-ResourceGroupName</span></span>
<span data-ttu-id="68633-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="68633-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListBySubOrResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolDefaultsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68633-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68633-127">-ResourceId</span></span>
<span data-ttu-id="68633-128">A példánykészlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="68633-128">The instance pool resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstancePoolByInstancePoolResourceIdentifierParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68633-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68633-129">CommonParameters</span></span>
<span data-ttu-id="68633-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68633-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68633-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="68633-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68633-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="68633-132">INPUTS</span></span>

### <span data-ttu-id="68633-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="68633-133">None</span></span>

## <span data-ttu-id="68633-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="68633-134">OUTPUTS</span></span>

### <span data-ttu-id="68633-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="68633-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

## <span data-ttu-id="68633-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="68633-136">NOTES</span></span>

## <span data-ttu-id="68633-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="68633-137">RELATED LINKS</span></span>
