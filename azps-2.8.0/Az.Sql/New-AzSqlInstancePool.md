---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
ms.openlocfilehash: d65e32992b113dfb587b68dd3fcdc1701b291ad4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839413"
---
# <span data-ttu-id="12cae-101">New-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="12cae-101">New-AzSqlInstancePool</span></span>

## <span data-ttu-id="12cae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="12cae-102">SYNOPSIS</span></span>
<span data-ttu-id="12cae-103">Azure SQL-kiszolgálópéldány-gyűjtőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="12cae-103">Creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="12cae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="12cae-104">SYNTAX</span></span>

```
New-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> -Location <String> -SubnetId <String>
 -VCore <Int32> -Edition <String> -ComputeGeneration <String> -LicenseType <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12cae-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="12cae-105">DESCRIPTION</span></span>
<span data-ttu-id="12cae-106">A **New-AzSqlInstancePool** parancsmag egy Azure SQL-példány készletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="12cae-106">The **New-AzSqlInstancePool** cmdlet creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="12cae-107">Példák</span><span class="sxs-lookup"><span data-stu-id="12cae-107">EXAMPLES</span></span>

### <span data-ttu-id="12cae-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="12cae-108">Example 1</span></span>
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

<span data-ttu-id="12cae-109">A parancs létrehoz egy új Azure SQL-példány-készletet.</span><span class="sxs-lookup"><span data-stu-id="12cae-109">This command creates a new Azure SQL Instance pool.</span></span>

## <span data-ttu-id="12cae-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="12cae-110">PARAMETERS</span></span>

### <span data-ttu-id="12cae-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12cae-111">-AsJob</span></span>
<span data-ttu-id="12cae-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="12cae-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="12cae-113">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="12cae-113">-ComputeGeneration</span></span>
<span data-ttu-id="12cae-114">A számítási generáció a példány-készletben.</span><span class="sxs-lookup"><span data-stu-id="12cae-114">The compute generation for the instance pool.</span></span>

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

### <span data-ttu-id="12cae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12cae-115">-DefaultProfile</span></span>
<span data-ttu-id="12cae-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="12cae-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12cae-117">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="12cae-117">-Edition</span></span>
<span data-ttu-id="12cae-118">A példány példányának kiadását.</span><span class="sxs-lookup"><span data-stu-id="12cae-118">The edition for the instance pool.</span></span>

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

### <span data-ttu-id="12cae-119">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="12cae-119">-LicenseType</span></span>
<span data-ttu-id="12cae-120">Meghatározza, hogy melyik licenc-típust szeretné használni.</span><span class="sxs-lookup"><span data-stu-id="12cae-120">Determines which License Type to use.</span></span>
<span data-ttu-id="12cae-121">A lehetséges értékek: BasePrice (AHB kedvezménnyel) és LicenseIncluded (AHB kedvezmény nélkül).</span><span class="sxs-lookup"><span data-stu-id="12cae-121">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="12cae-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="12cae-122">-Location</span></span>
<span data-ttu-id="12cae-123">A példány-készlet létrehozásának helye.</span><span class="sxs-lookup"><span data-stu-id="12cae-123">The location to create the instance pool.</span></span>

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

### <span data-ttu-id="12cae-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="12cae-124">-Name</span></span>
<span data-ttu-id="12cae-125">A példány-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="12cae-125">The name of the instance pool.</span></span>

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

### <span data-ttu-id="12cae-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12cae-126">-ResourceGroupName</span></span>
<span data-ttu-id="12cae-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="12cae-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="12cae-128">– NetI</span><span class="sxs-lookup"><span data-stu-id="12cae-128">-SubnetId</span></span>
<span data-ttu-id="12cae-129">Az alhálózati azonosító, amelyet például a készlet létrehozásakor kell használni.</span><span class="sxs-lookup"><span data-stu-id="12cae-129">The subnet id to use for instance pool creation.</span></span>

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

### <span data-ttu-id="12cae-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="12cae-130">-Tag</span></span>
<span data-ttu-id="12cae-131">A példánnyal társítani kívánt Címkék</span><span class="sxs-lookup"><span data-stu-id="12cae-131">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="12cae-132">-VCore</span><span class="sxs-lookup"><span data-stu-id="12cae-132">-VCore</span></span>
<span data-ttu-id="12cae-133">Meghatározza, hogy mennyi VCore társítson a példányhoz.</span><span class="sxs-lookup"><span data-stu-id="12cae-133">Determines how much VCore to associate with instance.</span></span>

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

### <span data-ttu-id="12cae-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="12cae-134">-Confirm</span></span>
<span data-ttu-id="12cae-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="12cae-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12cae-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12cae-136">-WhatIf</span></span>
<span data-ttu-id="12cae-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="12cae-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12cae-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="12cae-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12cae-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12cae-139">CommonParameters</span></span>
<span data-ttu-id="12cae-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="12cae-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12cae-141">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="12cae-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12cae-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="12cae-142">INPUTS</span></span>

### <span data-ttu-id="12cae-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="12cae-143">None</span></span>

## <span data-ttu-id="12cae-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12cae-144">OUTPUTS</span></span>

### <span data-ttu-id="12cae-145">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="12cae-145">System.Object</span></span>
## <span data-ttu-id="12cae-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="12cae-146">NOTES</span></span>

## <span data-ttu-id="12cae-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12cae-147">RELATED LINKS</span></span>
