---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePool.md
ms.openlocfilehash: afbd74953f876ede2a03e94c4db46937470a92dc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845190"
---
# <span data-ttu-id="ef5b8-101">Get-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="ef5b8-101">Get-AzSqlInstancePool</span></span>

## <span data-ttu-id="ef5b8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef5b8-102">SYNOPSIS</span></span>
<span data-ttu-id="ef5b8-103">Információt ad az Azure SQL-példány-készletről.</span><span class="sxs-lookup"><span data-stu-id="ef5b8-103">Returns information about the Azure SQL Instance pool.</span></span>

## <span data-ttu-id="ef5b8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef5b8-104">SYNTAX</span></span>

### <span data-ttu-id="ef5b8-105">ListBySubOrResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ef5b8-105">ListBySubOrResourceGroupParameterSet (Default)</span></span>
```
Get-AzSqlInstancePool [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ef5b8-106">ListByInstancePoolDefaultsParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef5b8-106">ListByInstancePoolDefaultsParameterSet</span></span>
```
Get-AzSqlInstancePool -ResourceGroupName <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ef5b8-107">GetInstancePoolByInstancePoolResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef5b8-107">GetInstancePoolByInstancePoolResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef5b8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef5b8-108">DESCRIPTION</span></span>
<span data-ttu-id="ef5b8-109">A **Get-AzSqlInstancePool** parancsmag egy vagy több Azure SQL-kiszolgálópéldány-készletről ad információt.</span><span class="sxs-lookup"><span data-stu-id="ef5b8-109">The **Get-AzSqlInstancePool** cmdlet returns information about one or more Azure SQL Instance pool.</span></span>
<span data-ttu-id="ef5b8-110">Adja meg a példányleírás nevét, hogy csak az adott példányhoz tartozó készlet adatait lássa.</span><span class="sxs-lookup"><span data-stu-id="ef5b8-110">Specify the name of an instance pool to see information for only that instance pool.</span></span>

## <span data-ttu-id="ef5b8-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ef5b8-111">EXAMPLES</span></span>

### <span data-ttu-id="ef5b8-112">Példa 1: az összes példány beolvasása az ügyfél-előfizetésbe</span><span class="sxs-lookup"><span data-stu-id="ef5b8-112">Example 1: Get all instance pools across a customer subscription</span></span>
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

<span data-ttu-id="ef5b8-113">Ez a parancs információt kap az ügyfél-előfizetésben lévő összes példányról.</span><span class="sxs-lookup"><span data-stu-id="ef5b8-113">This command gets information about all instance pools within the customer subscription.</span></span>

### <span data-ttu-id="ef5b8-114">2. példa: az összes példány készletének beolvasása egy erőforráscsoport között</span><span class="sxs-lookup"><span data-stu-id="ef5b8-114">Example 2: Get all instance pools across a resource group</span></span>
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

<span data-ttu-id="ef5b8-115">Ez a parancs információkat kap az erőforráscsoport resourcegroup01 található összes példányról.</span><span class="sxs-lookup"><span data-stu-id="ef5b8-115">This command gets information about all instance pools within the resource group resourcegroup01.</span></span>

### <span data-ttu-id="ef5b8-116">3. példa: a példány adatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="ef5b8-116">Example 3: Get information about an instance pool</span></span>
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

<span data-ttu-id="ef5b8-117">Ez a parancs információkat kap a példány instancePool0.</span><span class="sxs-lookup"><span data-stu-id="ef5b8-117">This command gets information about the instance pool instancePool0.</span></span>

### <span data-ttu-id="ef5b8-118">4. példa: a példányokra vonatkozó információk beolvasása a példány-készlet erőforrás-azonosítójával</span><span class="sxs-lookup"><span data-stu-id="ef5b8-118">Example 4: Get information about an instance pool using instance pool resource id</span></span>
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

<span data-ttu-id="ef5b8-119">Ez a parancs információt kap a példány-készletről az erőforrás-azonosítóval együtt.</span><span class="sxs-lookup"><span data-stu-id="ef5b8-119">This command gets information about the instance pool with its resource identifier.</span></span>

## <span data-ttu-id="ef5b8-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef5b8-120">PARAMETERS</span></span>

### <span data-ttu-id="ef5b8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef5b8-121">-DefaultProfile</span></span>
<span data-ttu-id="ef5b8-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef5b8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef5b8-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ef5b8-123">-Name</span></span>
<span data-ttu-id="ef5b8-124">A példány-gyűjtő neve.</span><span class="sxs-lookup"><span data-stu-id="ef5b8-124">The instance pool name.</span></span>

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

### <span data-ttu-id="ef5b8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef5b8-125">-ResourceGroupName</span></span>
<span data-ttu-id="ef5b8-126">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="ef5b8-126">The resource group name.</span></span>

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

### <span data-ttu-id="ef5b8-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef5b8-127">-ResourceId</span></span>
<span data-ttu-id="ef5b8-128">A példány erőforráskészlet-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ef5b8-128">The instance pool resource identifier.</span></span>

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

### <span data-ttu-id="ef5b8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef5b8-129">CommonParameters</span></span>
<span data-ttu-id="ef5b8-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ef5b8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef5b8-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ef5b8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef5b8-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef5b8-132">INPUTS</span></span>

### <span data-ttu-id="ef5b8-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="ef5b8-133">None</span></span>

## <span data-ttu-id="ef5b8-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef5b8-134">OUTPUTS</span></span>

### <span data-ttu-id="ef5b8-135">Microsoft.Azure.Commands.Sql.Instance_Pools. Model. AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="ef5b8-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

## <span data-ttu-id="ef5b8-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef5b8-136">NOTES</span></span>

## <span data-ttu-id="ef5b8-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef5b8-137">RELATED LINKS</span></span>
