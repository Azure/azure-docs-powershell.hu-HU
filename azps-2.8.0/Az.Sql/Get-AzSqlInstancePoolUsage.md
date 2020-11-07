---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancepoolusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePoolUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePoolUsage.md
ms.openlocfilehash: 594b1902a408268d82f4bf50cfe61cb1b78c82d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839461"
---
# <span data-ttu-id="4bcee-101">Get-AzSqlInstancePoolUsage</span><span class="sxs-lookup"><span data-stu-id="4bcee-101">Get-AzSqlInstancePoolUsage</span></span>

## <span data-ttu-id="4bcee-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4bcee-102">SYNOPSIS</span></span>
<span data-ttu-id="4bcee-103">Egy Azure SQL-példány használatáról szóló információt ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="4bcee-103">Returns information about an Azure SQL Instance pool's usage.</span></span>

## <span data-ttu-id="4bcee-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4bcee-104">SYNTAX</span></span>

### <span data-ttu-id="4bcee-105">InstancePoolUsageDefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4bcee-105">InstancePoolUsageDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstancePoolUsage [-ResourceGroupName] <String> [-Name] <String> [-ExpandChildren]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bcee-106">InstancePoolUsageParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4bcee-106">InstancePoolUsageParentObjectParameterSet</span></span>
```
Get-AzSqlInstancePoolUsage [-InstancePool] <AzureSqlInstancePoolModel> [-ExpandChildren]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bcee-107">InstancePoolUsageResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4bcee-107">InstancePoolUsageResourceIdParameterSet</span></span>
```
Get-AzSqlInstancePoolUsage [-ResourceId] <String> [-ExpandChildren] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4bcee-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4bcee-108">DESCRIPTION</span></span>
<span data-ttu-id="4bcee-109">A **Get-AzSqlInstancePoolUsage** parancsmag az Azure SQL instance Pool használatáról ad információt.</span><span class="sxs-lookup"><span data-stu-id="4bcee-109">The **Get-AzSqlInstancePoolUsage** cmdlet returns information an Azure SQL Instance pool's usage.</span></span>

## <span data-ttu-id="4bcee-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4bcee-110">EXAMPLES</span></span>

### <span data-ttu-id="4bcee-111">1. példa: egy Azure SQL-példány-készlet használatba kapja</span><span class="sxs-lookup"><span data-stu-id="4bcee-111">Example 1 : Gets the usage of an Azure SQL Instance pool</span></span>
```powershell
PS C:\> Get-AzSqlInstancePoolUsage -ResourceGroupName resourcegroup01 -Name instancepool0

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages
```

<span data-ttu-id="4bcee-112">Megkapja az Azure SQL instance Pool instancepool0 használatát.</span><span class="sxs-lookup"><span data-stu-id="4bcee-112">Gets the usage for the Azure SQL Instance pool instancepool0.</span></span>

### <span data-ttu-id="4bcee-113">2. példa: egy Azure SQL-példány alkalmazáskészletének beolvasása egy példány-alkalmazáskészlet objektum használatával</span><span class="sxs-lookup"><span data-stu-id="4bcee-113">Example 2: Gets the usage of an Azure SQL Instance pool using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancepool0
PS C:\> Get-AzSqlInstancePoolUsage -InstancePool $instancePool

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages
```

<span data-ttu-id="4bcee-114">Beolvassa az Azure SQL instance Pool instancepool0 használatát egy példány Pool-objektummal.</span><span class="sxs-lookup"><span data-stu-id="4bcee-114">Gets the usage for the Azure SQL Instance pool instancepool0 using an instance pool object.</span></span>

### <span data-ttu-id="4bcee-115">3. példa: egy Azure SQL-példány alkalmazáskészletének beszerzése egy példány erőforráskészlet-erőforrás-azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="4bcee-115">Example 3: Gets the usage of an Azure SQL Instance pool using an instance pool resource id</span></span>
```powershell
PS C:\> Get-AzSqlInstancePoolUsage -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages
```

<span data-ttu-id="4bcee-116">Az Azure SQL instance Pool instancepool0 használatát adja meg a példány-erőforrás-azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="4bcee-116">Gets the usage for the Azure SQL Instance pool instancepool0 using an instance pool resource identifier.</span></span>

### <span data-ttu-id="4bcee-117">3. példa: egy Azure SQL-példány-készlet használatát kapja meg, és lebontja a kezelt példány használatát a készleten belül.</span><span class="sxs-lookup"><span data-stu-id="4bcee-117">Example 3: Gets the usage of an Azure SQL Instance pool with a breakdown of the managed instance usages within the pool.</span></span>
```powershell
PS C:\> Get-AzSqlInstancePoolUsage -ResourceGroupName resourcegroup01 -Name instancepool0 -ExpandChildren

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/2e7fe4bd-90c7-454e-8bb6-dc44649f27b2/resourceGroups/poolsPS/providers/Microsoft.Sql/instancePools/instancepool0/managedInstances/managedinstance0/usages/vcore_utilization
CurrentValue   :
Limit          : 2
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/managedInstances/usages

Id             : /subscriptions/2e7fe4bd-90c7-454e-8bb6-dc44649f27b2/resourceGroups/poolsPS/providers/Microsoft.Sql/instancePools/instancepool0/managedInstances/managedinstance0/usages/storage_utilization
CurrentValue   :
Limit          : 32
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/managedInstances/usages

Id             : /subscriptions/2e7fe4bd-90c7-454e-8bb6-dc44649f27b2/resourceGroups/poolsPS/providers/Microsoft.Sql/instancePools/instancepool0/managedInstances/managedinstance0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/managedInstances/usages
```

<span data-ttu-id="4bcee-118">Beolvassa az Azure SQL instance Pool instancepool0 használatát, valamint a kezelt példányok használatát a instancepool0 belül.</span><span class="sxs-lookup"><span data-stu-id="4bcee-118">Gets the usage for the Azure SQL Instance pool instancepool0 along with the usages of the managed instances within instancepool0.</span></span>

## <span data-ttu-id="4bcee-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4bcee-119">PARAMETERS</span></span>

### <span data-ttu-id="4bcee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bcee-120">-DefaultProfile</span></span>
<span data-ttu-id="4bcee-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4bcee-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bcee-122">-ExpandChildren</span><span class="sxs-lookup"><span data-stu-id="4bcee-122">-ExpandChildren</span></span>
<span data-ttu-id="4bcee-123">Annak jelzése, hogy ki kell-e terjeszteni a példányleírás használatát a gyermekek használatáról.</span><span class="sxs-lookup"><span data-stu-id="4bcee-123">Flag indicating whether to expand this instance pool's usage with its children's usage.</span></span>

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

### <span data-ttu-id="4bcee-124">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="4bcee-124">-InstancePool</span></span>
<span data-ttu-id="4bcee-125">A szülő-példány alkalmazáskészlet-objektuma.</span><span class="sxs-lookup"><span data-stu-id="4bcee-125">The parent instance pool object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: InstancePoolUsageParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bcee-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4bcee-126">-Name</span></span>
<span data-ttu-id="4bcee-127">A felügyelt példányok készletének neve.</span><span class="sxs-lookup"><span data-stu-id="4bcee-127">The managed instance pool name.</span></span>

```yaml
Type: System.String
Parameter Sets: InstancePoolUsageDefaultParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bcee-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bcee-128">-ResourceGroupName</span></span>
<span data-ttu-id="4bcee-129">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="4bcee-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: InstancePoolUsageDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bcee-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bcee-130">-ResourceId</span></span>
<span data-ttu-id="4bcee-131">A szülő erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="4bcee-131">The parent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: InstancePoolUsageResourceIdParameterSet
Aliases: InstancePoolResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bcee-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bcee-132">CommonParameters</span></span>
<span data-ttu-id="4bcee-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4bcee-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bcee-134">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4bcee-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bcee-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4bcee-135">INPUTS</span></span>

### <span data-ttu-id="4bcee-136">Microsoft.Azure.Commands.Sql.Instance_Pools. Model. AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="4bcee-136">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="4bcee-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4bcee-137">System.String</span></span>

## <span data-ttu-id="4bcee-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4bcee-138">OUTPUTS</span></span>

### <span data-ttu-id="4bcee-139">Microsoft. Azure. Command. SQL. használat. models. AzureSqlUsageModel</span><span class="sxs-lookup"><span data-stu-id="4bcee-139">Microsoft.Azure.Commands.Sql.Usages.Models.AzureSqlUsageModel</span></span>

## <span data-ttu-id="4bcee-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4bcee-140">NOTES</span></span>

## <span data-ttu-id="4bcee-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4bcee-141">RELATED LINKS</span></span>
