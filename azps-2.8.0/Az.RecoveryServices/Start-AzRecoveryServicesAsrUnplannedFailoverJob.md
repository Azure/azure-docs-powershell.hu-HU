---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: 2339ae9dbeb2806acd7701fe3a9733c0eaa31503
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839014"
---
# <span data-ttu-id="324ed-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="324ed-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="324ed-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="324ed-102">SYNOPSIS</span></span>
<span data-ttu-id="324ed-103">Nem tervezett feladatátvételi műveletet indít el.</span><span class="sxs-lookup"><span data-stu-id="324ed-103">Starts an unplanned failover operation.</span></span>

## <span data-ttu-id="324ed-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="324ed-104">SYNTAX</span></span>

### <span data-ttu-id="324ed-105">ByRPIObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="324ed-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="324ed-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="324ed-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="324ed-107">ByRPIObjectWithRecoveryTag</span><span class="sxs-lookup"><span data-stu-id="324ed-107">ByRPIObjectWithRecoveryTag</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="324ed-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="324ed-108">DESCRIPTION</span></span>
<span data-ttu-id="324ed-109">A **Start-AzRecoveryServicesAsrUnplannedFailoverJob** parancsmag nem tervezett feladatátvételt indít az Azure webhely-helyreállítási replikációs szolgáltatással védett elemekkel vagy helyreállítási tervekkel.</span><span class="sxs-lookup"><span data-stu-id="324ed-109">The **Start-AzRecoveryServicesAsrUnplannedFailoverJob** cmdlet starts unplanned failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="324ed-110">Ellenőrizheti, hogy a feladat sikeres volt-e az Get-AzRecoveryServicesAsrJob parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="324ed-110">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="324ed-111">Példák</span><span class="sxs-lookup"><span data-stu-id="324ed-111">EXAMPLES</span></span>

### <span data-ttu-id="324ed-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="324ed-112">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $RecoveryNetwork
```

<span data-ttu-id="324ed-113">Elindítja a helyreállítási terv nem tervezett feladatátvételi műveletét a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="324ed-113">Starts the unplanned failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="324ed-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="324ed-114">PARAMETERS</span></span>

### <span data-ttu-id="324ed-115">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="324ed-115">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="324ed-116">A védett elemek feladatátvételének adattitkosítási elsődleges elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="324ed-116">Specifies the data encryption primary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="324ed-117">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="324ed-117">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="324ed-118">Az adattitkosítás a másodlagos tanúsítvány fájl elérési útját adja meg a védett elemek feladatátvételéhez.</span><span class="sxs-lookup"><span data-stu-id="324ed-118">Specifies the data encryption secondary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="324ed-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="324ed-119">-DefaultProfile</span></span>
<span data-ttu-id="324ed-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="324ed-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="324ed-121">-Irány</span><span class="sxs-lookup"><span data-stu-id="324ed-121">-Direction</span></span>
<span data-ttu-id="324ed-122">A feladatátvétel irányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="324ed-122">Specifies the failover direction.</span></span>
<span data-ttu-id="324ed-123">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="324ed-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="324ed-124">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="324ed-124">PrimaryToRecovery</span></span>
- <span data-ttu-id="324ed-125">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="324ed-125">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="324ed-126">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="324ed-126">-PerformSourceSideAction</span></span>
<span data-ttu-id="324ed-127">Végezze el a műveletet a forrás oldalon, mielőtt megkezdené a nem tervezett feladatátvételt.</span><span class="sxs-lookup"><span data-stu-id="324ed-127">Perform operation in source side before starting unplanned failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="324ed-128">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="324ed-128">-RecoveryPlan</span></span>
<span data-ttu-id="324ed-129">Az ASR-helyreállítási terv objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="324ed-129">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="324ed-130">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="324ed-130">-RecoveryPoint</span></span>
<span data-ttu-id="324ed-131">Egyéni helyreállítási pont megadása a védett számítógép feladatátvételéhez.</span><span class="sxs-lookup"><span data-stu-id="324ed-131">Specifies a custom recovery point to failover the protected machine to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="324ed-132">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="324ed-132">-RecoveryTag</span></span>
<span data-ttu-id="324ed-133">Azt a helyreállítási címkét adja meg, amelyre a feladatátvétel vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="324ed-133">Specifies the recovery tag to failover to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObject
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByRPIObjectWithRecoveryTag
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="324ed-134">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="324ed-134">-ReplicationProtectedItem</span></span>
<span data-ttu-id="324ed-135">Egy Azure-webhely-helyreállítási replikációs szolgáltatással védett elemet ad meg.</span><span class="sxs-lookup"><span data-stu-id="324ed-135">Specifies an azure site recovery replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithRecoveryTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="324ed-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="324ed-136">-Confirm</span></span>
<span data-ttu-id="324ed-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="324ed-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="324ed-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="324ed-138">-WhatIf</span></span>
<span data-ttu-id="324ed-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="324ed-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="324ed-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="324ed-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="324ed-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="324ed-141">CommonParameters</span></span>
<span data-ttu-id="324ed-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="324ed-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="324ed-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="324ed-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="324ed-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="324ed-144">INPUTS</span></span>

### <span data-ttu-id="324ed-145">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="324ed-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="324ed-146">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="324ed-146">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="324ed-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="324ed-147">OUTPUTS</span></span>

### <span data-ttu-id="324ed-148">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="324ed-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="324ed-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="324ed-149">NOTES</span></span>

## <span data-ttu-id="324ed-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="324ed-150">RELATED LINKS</span></span>

[<span data-ttu-id="324ed-151">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="324ed-151">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
