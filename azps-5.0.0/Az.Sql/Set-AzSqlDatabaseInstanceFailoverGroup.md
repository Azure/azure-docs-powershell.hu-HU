---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 79d7482d51ffc7c03703dbf62e00fd9230f9976d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195490"
---
# <span data-ttu-id="8fdc2-101">Set-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8fdc2-101">Set-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="8fdc2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8fdc2-102">SYNOPSIS</span></span>
<span data-ttu-id="8fdc2-103">Egy példány-feladatátvételi csoport konfigurációjának módosítása.</span><span class="sxs-lookup"><span data-stu-id="8fdc2-103">Modifies the configuration of an Instance Failover Group.</span></span>

## <span data-ttu-id="8fdc2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8fdc2-104">SYNTAX</span></span>

### <span data-ttu-id="8fdc2-105">SetInstanceFailoverGroupDefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8fdc2-105">SetInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fdc2-106">SetInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8fdc2-106">SetInstanceFailoverGroupByResourceIdSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-FailoverPolicy <String>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fdc2-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="8fdc2-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fdc2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8fdc2-108">DESCRIPTION</span></span>
<span data-ttu-id="8fdc2-109">Ez a parancs módosítja egy példány-feladatátvételi csoport konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="8fdc2-109">This command modifies the configuration of an Instance Failover Group.</span></span>

<span data-ttu-id="8fdc2-110">A példány feladatátvételi csoportjának elsődleges területét kell használni a parancs végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="8fdc2-110">The Instance Failover Group's primary region should be used to execute the command.</span></span>

<span data-ttu-id="8fdc2-111">A példány feladatátvételi csoportjai funkció előnézete során a '-GracePeriodWithDataLossHours ' paraméterben csak az 1 óránál nagyobb vagy azzal egyenlő értékek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="8fdc2-111">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="8fdc2-112">Példák</span><span class="sxs-lookup"><span data-stu-id="8fdc2-112">EXAMPLES</span></span>

### <span data-ttu-id="8fdc2-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8fdc2-113">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Set-AzSqlDatabaseInstanceFailoverGroup -FailoverPolicy Manual
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Manual
FailoverWithDataLossGracePeriodHours  : 
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="8fdc2-114">A feladatátvételi csoport feladatátvételi házirendjét "kézi" értékre állítja a feladatátvétel csoportban.</span><span class="sxs-lookup"><span data-stu-id="8fdc2-114">Sets a Instance Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="8fdc2-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8fdc2-115">PARAMETERS</span></span>

### <span data-ttu-id="8fdc2-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="8fdc2-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="8fdc2-117">Azt, hogy a másodlagos kiszolgálón hány kiesést kell kezdeményezni, a csak olvasható végpont automatikus feladatátvételét kell elindítania.</span><span class="sxs-lookup"><span data-stu-id="8fdc2-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>
<span data-ttu-id="8fdc2-118">Ez a funkció még nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="8fdc2-118">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="8fdc2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fdc2-119">-DefaultProfile</span></span>
<span data-ttu-id="8fdc2-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8fdc2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fdc2-121">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="8fdc2-121">-FailoverPolicy</span></span>
<span data-ttu-id="8fdc2-122">A példány-feladatátvételi csoport feladatátvételi házirendje.</span><span class="sxs-lookup"><span data-stu-id="8fdc2-122">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="8fdc2-123">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="8fdc2-123">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="8fdc2-124">Az automatikus feladatátvétel kezdeményezésének gyakorisága, ha áramkimaradás történik az elsődleges kiszolgálón, és a feladatátvétel nem hajtható végre adatvesztés nélkül.</span><span class="sxs-lookup"><span data-stu-id="8fdc2-124">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fdc2-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8fdc2-125">-InputObject</span></span>
<span data-ttu-id="8fdc2-126">A megadni kívánt példány-feladatátvételi csoport objektuma</span><span class="sxs-lookup"><span data-stu-id="8fdc2-126">The Instance Failover Group object to set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8fdc2-127">-Hely</span><span class="sxs-lookup"><span data-stu-id="8fdc2-127">-Location</span></span>
<span data-ttu-id="8fdc2-128">Annak a helynek a neve, amelyből a példány feladatátvételi csoportját be szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="8fdc2-128">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet, SetInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fdc2-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8fdc2-129">-Name</span></span>
<span data-ttu-id="8fdc2-130">A példány-feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="8fdc2-130">The name of the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fdc2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fdc2-131">-ResourceGroupName</span></span>
<span data-ttu-id="8fdc2-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8fdc2-132">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fdc2-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fdc2-133">-ResourceId</span></span>
<span data-ttu-id="8fdc2-134">A beállítani kívánt példány-feladatátvételi csoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8fdc2-134">The Resource ID of the Instance Failover Group to set.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fdc2-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8fdc2-135">-Confirm</span></span>
<span data-ttu-id="8fdc2-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8fdc2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fdc2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fdc2-137">-WhatIf</span></span>
<span data-ttu-id="8fdc2-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8fdc2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fdc2-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8fdc2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fdc2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fdc2-140">CommonParameters</span></span>
<span data-ttu-id="8fdc2-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8fdc2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fdc2-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8fdc2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fdc2-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fdc2-143">INPUTS</span></span>

### <span data-ttu-id="8fdc2-144">Microsoft. Azure. Command. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="8fdc2-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="8fdc2-145">System. String</span><span class="sxs-lookup"><span data-stu-id="8fdc2-145">System.String</span></span>

## <span data-ttu-id="8fdc2-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fdc2-146">OUTPUTS</span></span>

### <span data-ttu-id="8fdc2-147">Microsoft. Azure. Command. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="8fdc2-147">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="8fdc2-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8fdc2-148">NOTES</span></span>

## <span data-ttu-id="8fdc2-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8fdc2-149">RELATED LINKS</span></span>
