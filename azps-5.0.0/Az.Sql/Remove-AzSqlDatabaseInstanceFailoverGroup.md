---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 12bc26177a249995f748a879a9ae8d2f73900c99
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186634"
---
# <span data-ttu-id="e0912-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e0912-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="e0912-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e0912-102">SYNOPSIS</span></span>
<span data-ttu-id="e0912-103">A példány-feladatátvételi csoport eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="e0912-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="e0912-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e0912-104">SYNTAX</span></span>

### <span data-ttu-id="e0912-105">RemoveIFGDefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e0912-105">RemoveIFGDefaultSet (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0912-106">RemoveInstanceFailoverGroupByResourceId</span><span class="sxs-lookup"><span data-stu-id="e0912-106">RemoveInstanceFailoverGroupByResourceId</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0912-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="e0912-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0912-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e0912-108">DESCRIPTION</span></span>
<span data-ttu-id="e0912-109">Ez a parancs eltávolítja a példány feladatátvételi csoportját a megadott névvel, így minden adatbázis érintetlen marad.</span><span class="sxs-lookup"><span data-stu-id="e0912-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="e0912-110">A figyelő végpontját a rendszer nem regisztrálja a DNS-ből.</span><span class="sxs-lookup"><span data-stu-id="e0912-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="e0912-111">A példány feladatátvételi csoportjának elsődleges területét kell használni a parancs végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="e0912-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="e0912-112">Példák</span><span class="sxs-lookup"><span data-stu-id="e0912-112">EXAMPLES</span></span>

### <span data-ttu-id="e0912-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e0912-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="e0912-114">Példány-feladatátvételi csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e0912-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="e0912-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e0912-115">PARAMETERS</span></span>

### <span data-ttu-id="e0912-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0912-116">-DefaultProfile</span></span>
<span data-ttu-id="e0912-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0912-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0912-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e0912-118">-Force</span></span>
<span data-ttu-id="e0912-119">A művelet elvégzésére vonatkozó megerősítési üzenet kihagyása.</span><span class="sxs-lookup"><span data-stu-id="e0912-119">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="e0912-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0912-120">-InputObject</span></span>
<span data-ttu-id="e0912-121">A példány feladatátvételi csoportjának eltávolítandó objektuma</span><span class="sxs-lookup"><span data-stu-id="e0912-121">The Instance Failover Group object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0912-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="e0912-122">-Location</span></span>
<span data-ttu-id="e0912-123">Annak a helynek a neve, amelyből a példány feladatátvételi csoportját be szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="e0912-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet, RemoveInstanceFailoverGroupByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0912-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e0912-124">-Name</span></span>
<span data-ttu-id="e0912-125">Az eltávolítandó példány-feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e0912-125">The name of the Instance Failover Group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0912-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0912-126">-PassThru</span></span>
<span data-ttu-id="e0912-127">Megadja, hogy át kell-e adni a parancsmag végrehajtási kimenetét.</span><span class="sxs-lookup"><span data-stu-id="e0912-127">Specifies whether to pass through cmdlet execution output.</span></span>

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

### <span data-ttu-id="e0912-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0912-128">-ResourceGroupName</span></span>
<span data-ttu-id="e0912-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e0912-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0912-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0912-130">-ResourceId</span></span>
<span data-ttu-id="e0912-131">Az eltávolítandó példány-feladatátvételi csoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e0912-131">The Resource ID of the Instance Failover Group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFailoverGroupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0912-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e0912-132">-Confirm</span></span>
<span data-ttu-id="e0912-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e0912-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0912-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0912-134">-WhatIf</span></span>
<span data-ttu-id="e0912-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e0912-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0912-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e0912-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0912-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0912-137">CommonParameters</span></span>
<span data-ttu-id="e0912-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e0912-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0912-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e0912-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0912-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0912-140">INPUTS</span></span>

### <span data-ttu-id="e0912-141">Microsoft. Azure. Command. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="e0912-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="e0912-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e0912-142">System.String</span></span>

## <span data-ttu-id="e0912-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0912-143">OUTPUTS</span></span>

### <span data-ttu-id="e0912-144">Microsoft. Azure. Command. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="e0912-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="e0912-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e0912-145">NOTES</span></span>

## <span data-ttu-id="e0912-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0912-146">RELATED LINKS</span></span>
