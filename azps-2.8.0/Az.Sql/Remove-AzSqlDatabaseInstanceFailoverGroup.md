---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 8027af33b9ea4f4184c10963da69e8be3b4e3961
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839395"
---
# <span data-ttu-id="7365a-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7365a-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="7365a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7365a-102">SYNOPSIS</span></span>
<span data-ttu-id="7365a-103">A példány-feladatátvételi csoport eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="7365a-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="7365a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7365a-104">SYNTAX</span></span>

### <span data-ttu-id="7365a-105">RemoveIFGDefault (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7365a-105">RemoveIFGDefault (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7365a-106">Példány-feladatátvételi csoport eltávolítása erőforrás-azonosítóból</span><span class="sxs-lookup"><span data-stu-id="7365a-106">Remove a Instance Failover Group from Resource Id</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7365a-107">Példány-feladatátvételi csoport eltávolítása a AzureSqlInstanceFailoverGroupModel-példány definícióból</span><span class="sxs-lookup"><span data-stu-id="7365a-107">Remove a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup -InputObject <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7365a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7365a-108">DESCRIPTION</span></span>
<span data-ttu-id="7365a-109">Ez a parancs eltávolítja a példány feladatátvételi csoportját a megadott névvel, így minden adatbázis érintetlen marad.</span><span class="sxs-lookup"><span data-stu-id="7365a-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="7365a-110">A figyelő végpontját a rendszer nem regisztrálja a DNS-ből.</span><span class="sxs-lookup"><span data-stu-id="7365a-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="7365a-111">A példány feladatátvételi csoportjának elsődleges területét kell használni a parancs végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="7365a-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="7365a-112">Példák</span><span class="sxs-lookup"><span data-stu-id="7365a-112">EXAMPLES</span></span>

### <span data-ttu-id="7365a-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7365a-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="7365a-114">Példány-feladatátvételi csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7365a-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="7365a-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7365a-115">PARAMETERS</span></span>

### <span data-ttu-id="7365a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7365a-116">-DefaultProfile</span></span>
<span data-ttu-id="7365a-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7365a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7365a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7365a-118">-Force</span></span>
<span data-ttu-id="7365a-119">A művelet elvégzésére vonatkozó megerősítési üzenet kihagyása.</span><span class="sxs-lookup"><span data-stu-id="7365a-119">Skip confirmation message for performing the action.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7365a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7365a-120">-InputObject</span></span>
<span data-ttu-id="7365a-121">A példány feladatátvételi csoportjának eltávolítandó objektuma</span><span class="sxs-lookup"><span data-stu-id="7365a-121">The Instance Failover Group object to remove</span></span>

```yaml
Type: AzureSqlInstanceFailoverGroupModel
Parameter Sets: Remove a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7365a-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="7365a-122">-Location</span></span>
<span data-ttu-id="7365a-123">Annak a helynek a neve, amelyből a példány feladatátvételi csoportját be szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="7365a-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault, Remove a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7365a-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7365a-124">-Name</span></span>
<span data-ttu-id="7365a-125">Az eltávolítandó példány-feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="7365a-125">The name of the Instance Failover Group to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7365a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7365a-126">-ResourceGroupName</span></span>
<span data-ttu-id="7365a-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7365a-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7365a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7365a-128">-ResourceId</span></span>
<span data-ttu-id="7365a-129">Az eltávolítandó példány-feladatátvételi csoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7365a-129">The Resource ID of the Instance Failover Group to remove.</span></span>

```yaml
Type: String
Parameter Sets: Remove a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7365a-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7365a-130">-Confirm</span></span>
<span data-ttu-id="7365a-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7365a-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7365a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7365a-132">-WhatIf</span></span>
<span data-ttu-id="7365a-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7365a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7365a-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7365a-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7365a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7365a-135">CommonParameters</span></span>
<span data-ttu-id="7365a-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7365a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7365a-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7365a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7365a-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7365a-138">INPUTS</span></span>

### <span data-ttu-id="7365a-139">Microsoft. Azure. Command. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="7365a-139">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="7365a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7365a-140">System.String</span></span>

## <span data-ttu-id="7365a-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7365a-141">OUTPUTS</span></span>

### <span data-ttu-id="7365a-142">Microsoft. Azure. Command. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="7365a-142">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="7365a-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7365a-143">NOTES</span></span>

## <span data-ttu-id="7365a-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7365a-144">RELATED LINKS</span></span>
