---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 12bc26177a249995f748a879a9ae8d2f73900c99
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343001"
---
# <span data-ttu-id="52416-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="52416-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="52416-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52416-102">SYNOPSIS</span></span>
<span data-ttu-id="52416-103">Egy példány feladatátvételi csoportjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="52416-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="52416-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="52416-104">SYNTAX</span></span>

### <span data-ttu-id="52416-105">RemoveIFGDefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="52416-105">RemoveIFGDefaultSet (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52416-106">RemoveInstanceFailoverGroupByResourceId</span><span class="sxs-lookup"><span data-stu-id="52416-106">RemoveInstanceFailoverGroupByResourceId</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52416-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="52416-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52416-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="52416-108">DESCRIPTION</span></span>
<span data-ttu-id="52416-109">Ez a parancs eltávolítja a megadott nevű Példány feladatátvételi csoportot, és az összes adatbázis érintetlen marad.</span><span class="sxs-lookup"><span data-stu-id="52416-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="52416-110">A figyelő végpont nem lesz regisztrálva a DNS-ről.</span><span class="sxs-lookup"><span data-stu-id="52416-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="52416-111">A parancs végrehajtásához a Példány feladatátvétele csoport elsődleges régióját kell használni.</span><span class="sxs-lookup"><span data-stu-id="52416-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="52416-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="52416-112">EXAMPLES</span></span>

### <span data-ttu-id="52416-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="52416-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="52416-114">Példány feladatátvételi csoportjának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="52416-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="52416-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52416-115">PARAMETERS</span></span>

### <span data-ttu-id="52416-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52416-116">-DefaultProfile</span></span>
<span data-ttu-id="52416-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="52416-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52416-118">-Force</span><span class="sxs-lookup"><span data-stu-id="52416-118">-Force</span></span>
<span data-ttu-id="52416-119">Hagyja ki a művelet végrehajtásához szükséges megerősítő üzenetet.</span><span class="sxs-lookup"><span data-stu-id="52416-119">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="52416-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52416-120">-InputObject</span></span>
<span data-ttu-id="52416-121">The Instance Failover Group object to remove</span><span class="sxs-lookup"><span data-stu-id="52416-121">The Instance Failover Group object to remove</span></span>

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

### <span data-ttu-id="52416-122">-Location</span><span class="sxs-lookup"><span data-stu-id="52416-122">-Location</span></span>
<span data-ttu-id="52416-123">Annak a helyi régiónak a neve, amelyből lekéri a példány feladatátvételi csoportját.</span><span class="sxs-lookup"><span data-stu-id="52416-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="52416-124">-Name</span><span class="sxs-lookup"><span data-stu-id="52416-124">-Name</span></span>
<span data-ttu-id="52416-125">Az eltávolítható Példány feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="52416-125">The name of the Instance Failover Group to remove.</span></span>

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

### <span data-ttu-id="52416-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52416-126">-PassThru</span></span>
<span data-ttu-id="52416-127">Megadja, hogy áthaladjon-e a parancsmag végrehajtási kimeneten.</span><span class="sxs-lookup"><span data-stu-id="52416-127">Specifies whether to pass through cmdlet execution output.</span></span>

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

### <span data-ttu-id="52416-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52416-128">-ResourceGroupName</span></span>
<span data-ttu-id="52416-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="52416-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="52416-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52416-130">-ResourceId</span></span>
<span data-ttu-id="52416-131">Az eltávolítható példány feladatátvételi csoportjának erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="52416-131">The Resource ID of the Instance Failover Group to remove.</span></span>

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

### <span data-ttu-id="52416-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52416-132">-Confirm</span></span>
<span data-ttu-id="52416-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="52416-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52416-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52416-134">-WhatIf</span></span>
<span data-ttu-id="52416-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="52416-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52416-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="52416-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52416-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52416-137">CommonParameters</span></span>
<span data-ttu-id="52416-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52416-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52416-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52416-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52416-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="52416-140">INPUTS</span></span>

### <span data-ttu-id="52416-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="52416-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="52416-142">System.String</span><span class="sxs-lookup"><span data-stu-id="52416-142">System.String</span></span>

## <span data-ttu-id="52416-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="52416-143">OUTPUTS</span></span>

### <span data-ttu-id="52416-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="52416-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="52416-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="52416-145">NOTES</span></span>

## <span data-ttu-id="52416-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="52416-146">RELATED LINKS</span></span>
