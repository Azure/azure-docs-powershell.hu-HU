---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 38e19e764e7a9d272db777a295f05016f0ef95af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839295"
---
# <span data-ttu-id="f0ca6-101">Set-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f0ca6-101">Set-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="f0ca6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f0ca6-102">SYNOPSIS</span></span>
<span data-ttu-id="f0ca6-103">Egy példány-feladatátvételi csoport konfigurációjának módosítása.</span><span class="sxs-lookup"><span data-stu-id="f0ca6-103">Modifies the configuration of an Instance Failover Group.</span></span>

## <span data-ttu-id="f0ca6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f0ca6-104">SYNTAX</span></span>

### <span data-ttu-id="f0ca6-105">SetIFGDefault (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f0ca6-105">SetIFGDefault (Default)</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0ca6-106">Példány-feladatátvételi csoport beállítása erőforrás-azonosítóból</span><span class="sxs-lookup"><span data-stu-id="f0ca6-106">Set a Instance Failover Group from Resource Id</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0ca6-107">Példány-feladatátvételi csoport beállítása AzureSqlInstanceFailoverGroupModel példány-definícióból</span><span class="sxs-lookup"><span data-stu-id="f0ca6-107">Set a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup -InputObject <AzureSqlInstanceFailoverGroupModel>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0ca6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f0ca6-108">DESCRIPTION</span></span>
<span data-ttu-id="f0ca6-109">Ez a parancs módosítja egy példány-feladatátvételi csoport konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="f0ca6-109">This command modifies the configuration of an Instance Failover Group.</span></span>

<span data-ttu-id="f0ca6-110">A példány feladatátvételi csoportjának elsődleges területét kell használni a parancs végrehajtásához.</span><span class="sxs-lookup"><span data-stu-id="f0ca6-110">The Instance Failover Group's primary region should be used to execute the command.</span></span>

<span data-ttu-id="f0ca6-111">A példány feladatátvételi csoportjai funkció előnézete során a '-GracePeriodWithDataLossHours ' paraméterben csak az 1 óránál nagyobb vagy azzal egyenlő értékek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="f0ca6-111">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="f0ca6-112">Példák</span><span class="sxs-lookup"><span data-stu-id="f0ca6-112">EXAMPLES</span></span>

### <span data-ttu-id="f0ca6-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f0ca6-113">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Set-AzSqlDatabaseFailoverGroup -FailoverPolicy Manual
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

<span data-ttu-id="f0ca6-114">A feladatátvételi csoport feladatátvételi házirendjét "kézi" értékre állítja a feladatátvétel csoportban.</span><span class="sxs-lookup"><span data-stu-id="f0ca6-114">Sets a Instance Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="f0ca6-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f0ca6-115">PARAMETERS</span></span>

### <span data-ttu-id="f0ca6-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="f0ca6-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="f0ca6-117">Azt, hogy a másodlagos kiszolgálón hány kiesést kell kezdeményezni, a csak olvasható végpont automatikus feladatátvételét kell elindítania.</span><span class="sxs-lookup"><span data-stu-id="f0ca6-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>
<span data-ttu-id="f0ca6-118">Ez a funkció még nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="f0ca6-118">This feature is not yet supported.</span></span>

```yaml
Type: AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ca6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0ca6-119">-DefaultProfile</span></span>
<span data-ttu-id="f0ca6-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f0ca6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0ca6-121">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="f0ca6-121">-FailoverPolicy</span></span>
<span data-ttu-id="f0ca6-122">A példány-feladatátvételi csoport feladatátvételi házirendje.</span><span class="sxs-lookup"><span data-stu-id="f0ca6-122">The failover policy of the Instance Failover Group.</span></span>

```yaml
Type: FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ca6-123">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="f0ca6-123">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="f0ca6-124">Az automatikus feladatátvétel kezdeményezésének gyakorisága, ha áramkimaradás történik az elsődleges kiszolgálón, és a feladatátvétel nem hajtható végre adatvesztés nélkül.</span><span class="sxs-lookup"><span data-stu-id="f0ca6-124">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ca6-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0ca6-125">-InputObject</span></span>
<span data-ttu-id="f0ca6-126">A megadni kívánt példány-feladatátvételi csoport objektuma</span><span class="sxs-lookup"><span data-stu-id="f0ca6-126">The Instance Failover Group object to set</span></span>

```yaml
Type: AzureSqlInstanceFailoverGroupModel
Parameter Sets: Set a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0ca6-127">-Hely</span><span class="sxs-lookup"><span data-stu-id="f0ca6-127">-Location</span></span>
<span data-ttu-id="f0ca6-128">Annak a helynek a neve, amelyből a példány feladatátvételi csoportját be szeretné olvasni.</span><span class="sxs-lookup"><span data-stu-id="f0ca6-128">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: SetIFGDefault, Set a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ca6-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f0ca6-129">-Name</span></span>
<span data-ttu-id="f0ca6-130">A példány-feladatátvételi csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f0ca6-130">The name of the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: SetIFGDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ca6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0ca6-131">-ResourceGroupName</span></span>
<span data-ttu-id="f0ca6-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f0ca6-132">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetIFGDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ca6-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0ca6-133">-ResourceId</span></span>
<span data-ttu-id="f0ca6-134">A beállítani kívánt példány-feladatátvételi csoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f0ca6-134">The Resource ID of the Instance Failover Group to set.</span></span>

```yaml
Type: String
Parameter Sets: Set a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0ca6-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f0ca6-135">-Confirm</span></span>
<span data-ttu-id="f0ca6-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f0ca6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0ca6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0ca6-137">-WhatIf</span></span>
<span data-ttu-id="f0ca6-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f0ca6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0ca6-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f0ca6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0ca6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0ca6-140">CommonParameters</span></span>
<span data-ttu-id="f0ca6-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f0ca6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0ca6-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0ca6-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0ca6-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0ca6-143">INPUTS</span></span>

### <span data-ttu-id="f0ca6-144">Microsoft. Azure. Command. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="f0ca6-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="f0ca6-145">System. String</span><span class="sxs-lookup"><span data-stu-id="f0ca6-145">System.String</span></span>

## <span data-ttu-id="f0ca6-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0ca6-146">OUTPUTS</span></span>

### <span data-ttu-id="f0ca6-147">Microsoft. Azure. Command. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="f0ca6-147">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="f0ca6-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f0ca6-148">NOTES</span></span>

## <span data-ttu-id="f0ca6-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f0ca6-149">RELATED LINKS</span></span>
