---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
ms.openlocfilehash: db7d9165b8aec6a69f31850f7a37eddb2450e53b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183871"
---
# <span data-ttu-id="a1d3c-101">Set-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="a1d3c-101">Set-AzSqlInstancePool</span></span>

## <span data-ttu-id="a1d3c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a1d3c-102">SYNOPSIS</span></span>
<span data-ttu-id="a1d3c-103">Az Azure SQL-példányok tulajdonságainak beállítása.</span><span class="sxs-lookup"><span data-stu-id="a1d3c-103">Sets properties for an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="a1d3c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a1d3c-104">SYNTAX</span></span>

### <span data-ttu-id="a1d3c-105">DefaultSetInstancePoolParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a1d3c-105">DefaultSetInstancePoolParameterSet (Default)</span></span>
```
Set-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1d3c-106">InputObjectSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1d3c-106">InputObjectSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1d3c-107">ResourceIdSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1d3c-107">ResourceIdSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-ResourceId] <String> [-LicenseType <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1d3c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a1d3c-108">DESCRIPTION</span></span>
<span data-ttu-id="a1d3c-109">A **set-AzSqlInstancePool** parancsmag egy Azure SQL-példány-készlet tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="a1d3c-109">The **Set-AzSqlInstancePool** cmdlet modifies properties of an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="a1d3c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a1d3c-110">EXAMPLES</span></span>

### <span data-ttu-id="a1d3c-111">1. példa: a példányleírás-licenc típusának beállítása</span><span class="sxs-lookup"><span data-stu-id="a1d3c-111">Example 1 : Set an instance pool license type</span></span>
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

<span data-ttu-id="a1d3c-112">Ezzel a paranccsal beállíthatja a instancePool0 nevű példány licencének típusát és/vagy címkéit.</span><span class="sxs-lookup"><span data-stu-id="a1d3c-112">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

### <span data-ttu-id="a1d3c-113">2. példa: egy példány alkalmazáskészlet-típusának beállítása példány-gyűjtő objektummal</span><span class="sxs-lookup"><span data-stu-id="a1d3c-113">Example 2 : Set an instance pool license type using an instance pool object</span></span>
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

<span data-ttu-id="a1d3c-114">Ez a parancs a példányleírás típusát és/vagy címkéit a példány-gyűjtő objektum segítségével állítja be.</span><span class="sxs-lookup"><span data-stu-id="a1d3c-114">This command sets the license type and/or tags for an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="a1d3c-115">3. példa: a példányleírás-típus beállítása a példány-készlet erőforrás-azonosítójának használatával</span><span class="sxs-lookup"><span data-stu-id="a1d3c-115">Example 3 : Set an instance pool license type using an instance pool resource id</span></span>
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

<span data-ttu-id="a1d3c-116">Ezzel a paranccsal beállíthatja a instancePool0 nevű példány licencének típusát és/vagy címkéit.</span><span class="sxs-lookup"><span data-stu-id="a1d3c-116">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

## <span data-ttu-id="a1d3c-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a1d3c-117">PARAMETERS</span></span>

### <span data-ttu-id="a1d3c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1d3c-118">-AsJob</span></span>
<span data-ttu-id="a1d3c-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a1d3c-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1d3c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1d3c-120">-DefaultProfile</span></span>
<span data-ttu-id="a1d3c-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a1d3c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1d3c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1d3c-122">-InputObject</span></span>
<span data-ttu-id="a1d3c-123">A példány-gyűjtő bemeneti objektuma.</span><span class="sxs-lookup"><span data-stu-id="a1d3c-123">The instance pool input object.</span></span>

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

### <span data-ttu-id="a1d3c-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a1d3c-124">-LicenseType</span></span>
<span data-ttu-id="a1d3c-125">Meghatározza, hogy melyik licenc-típust szeretné használni.</span><span class="sxs-lookup"><span data-stu-id="a1d3c-125">Determines which License Type to use.</span></span>
<span data-ttu-id="a1d3c-126">A lehetséges értékek: BasePrice (AHB kedvezménnyel) és LicenseIncluded (AHB kedvezmény nélkül).</span><span class="sxs-lookup"><span data-stu-id="a1d3c-126">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="a1d3c-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a1d3c-127">-Name</span></span>
<span data-ttu-id="a1d3c-128">A példány-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="a1d3c-128">The name of the instance pool.</span></span>

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

### <span data-ttu-id="a1d3c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1d3c-129">-ResourceGroupName</span></span>
<span data-ttu-id="a1d3c-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a1d3c-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="a1d3c-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1d3c-131">-ResourceId</span></span>
<span data-ttu-id="a1d3c-132">A példány erőforráskészlet-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a1d3c-132">The instance pool resource identifier.</span></span>

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

### <span data-ttu-id="a1d3c-133">-Címke</span><span class="sxs-lookup"><span data-stu-id="a1d3c-133">-Tag</span></span>
<span data-ttu-id="a1d3c-134">A példánnyal társítani kívánt Címkék</span><span class="sxs-lookup"><span data-stu-id="a1d3c-134">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="a1d3c-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a1d3c-135">-Confirm</span></span>
<span data-ttu-id="a1d3c-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a1d3c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1d3c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1d3c-137">-WhatIf</span></span>
<span data-ttu-id="a1d3c-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a1d3c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1d3c-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a1d3c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1d3c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1d3c-140">CommonParameters</span></span>
<span data-ttu-id="a1d3c-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a1d3c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1d3c-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a1d3c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1d3c-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1d3c-143">INPUTS</span></span>

### <span data-ttu-id="a1d3c-144">Microsoft.Azure.Commands.Sql.Instance_Pools. Model. AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="a1d3c-144">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="a1d3c-145">System. String</span><span class="sxs-lookup"><span data-stu-id="a1d3c-145">System.String</span></span>

## <span data-ttu-id="a1d3c-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1d3c-146">OUTPUTS</span></span>

### <span data-ttu-id="a1d3c-147">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="a1d3c-147">System.Object</span></span>
## <span data-ttu-id="a1d3c-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a1d3c-148">NOTES</span></span>

## <span data-ttu-id="a1d3c-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1d3c-149">RELATED LINKS</span></span>
