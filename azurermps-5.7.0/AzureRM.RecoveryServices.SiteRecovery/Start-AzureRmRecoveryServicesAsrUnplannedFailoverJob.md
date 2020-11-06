---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: ba31be7094da4c4c17fa8c674728b8c32bfa2b8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492218"
---
# <span data-ttu-id="63dc7-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="63dc7-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="63dc7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="63dc7-102">SYNOPSIS</span></span>
<span data-ttu-id="63dc7-103">Nem tervezett feladatátvételi műveletet indít el.</span><span class="sxs-lookup"><span data-stu-id="63dc7-103">Starts a unplanned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63dc7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="63dc7-104">SYNTAX</span></span>

### <span data-ttu-id="63dc7-105">ByRPIObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="63dc7-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63dc7-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="63dc7-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63dc7-107">ByRPIObjectWithRecoveryTag</span><span class="sxs-lookup"><span data-stu-id="63dc7-107">ByRPIObjectWithRecoveryTag</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63dc7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="63dc7-108">DESCRIPTION</span></span>
<span data-ttu-id="63dc7-109">A **Start-AzureRmRecoveryServicesAsrTestFailoverJob** parancsmag az Azure webhely-helyreállítási replikációs szolgáltatással védett elemek vagy helyreállítási terv feladatátvételének tesztelését indítja el.</span><span class="sxs-lookup"><span data-stu-id="63dc7-109">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="63dc7-110">Ellenőrizheti, hogy a feladat sikeres volt-e az Get-AzureRmRecoveryServicesAsrJob parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="63dc7-110">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="63dc7-111">Példák</span><span class="sxs-lookup"><span data-stu-id="63dc7-111">EXAMPLES</span></span>

### <span data-ttu-id="63dc7-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="63dc7-112">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="63dc7-113">Elindítja a helyreállítási terv teszt-feladatátvételi műveletét a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="63dc7-113">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="63dc7-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="63dc7-114">PARAMETERS</span></span>

### <span data-ttu-id="63dc7-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="63dc7-115">-Confirm</span></span>
<span data-ttu-id="63dc7-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="63dc7-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63dc7-117">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="63dc7-117">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="63dc7-118">A védett elemek feladatátvételének adattitkosítási elsődleges elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="63dc7-118">Specifies the data encryption primary certificate file path for failover of Protected Item.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63dc7-119">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="63dc7-119">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="63dc7-120">Az adattitkosítás a másodlagos tanúsítvány fájl elérési útját adja meg a védett elemek feladatátvételéhez.</span><span class="sxs-lookup"><span data-stu-id="63dc7-120">Specifies the data encryption secondary certificate file path for failover of Protected Item.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63dc7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63dc7-121">-DefaultProfile</span></span>
<span data-ttu-id="63dc7-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="63dc7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="63dc7-123">-Irány</span><span class="sxs-lookup"><span data-stu-id="63dc7-123">-Direction</span></span>
<span data-ttu-id="63dc7-124">A feladatátvétel irányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="63dc7-124">Specifies the failover direction.</span></span>
<span data-ttu-id="63dc7-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="63dc7-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="63dc7-126">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="63dc7-126">PrimaryToRecovery</span></span>
- <span data-ttu-id="63dc7-127">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="63dc7-127">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63dc7-128">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="63dc7-128">-PerformSourceSideAction</span></span>
<span data-ttu-id="63dc7-129">Végezze el a műveletet a forrás oldalon, mielőtt megkezdené a nem tervezett feladatátvételt.</span><span class="sxs-lookup"><span data-stu-id="63dc7-129">Perform operation in source side before starting unplanned failover.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63dc7-130">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="63dc7-130">-RecoveryPlan</span></span>
<span data-ttu-id="63dc7-131">Az ASR-helyreállítási terv objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="63dc7-131">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63dc7-132">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="63dc7-132">-RecoveryPoint</span></span>
<span data-ttu-id="63dc7-133">Egyéni helyreállítási pont megadása a védett számítógép feladatátvételéhez.</span><span class="sxs-lookup"><span data-stu-id="63dc7-133">Specifies a custom recovery point to failover the protected machine to.</span></span>

```yaml
Type: ASRRecoveryPoint
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63dc7-134">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="63dc7-134">-RecoveryTag</span></span>
<span data-ttu-id="63dc7-135">Azt a helyreállítási címkét adja meg, amelyre a feladatátvétel vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="63dc7-135">Specifies the recovery tag to failover to.</span></span>

```yaml
Type: String
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
Type: String
Parameter Sets: ByRPIObjectWithRecoveryTag
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63dc7-136">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="63dc7-136">-ReplicationProtectedItem</span></span>
<span data-ttu-id="63dc7-137">Egy Azure-webhely-helyreállítási replikációs szolgáltatással védett elemet ad meg.</span><span class="sxs-lookup"><span data-stu-id="63dc7-137">Specifies an azure site recovery replication protected item.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithRecoveryTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63dc7-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63dc7-138">-WhatIf</span></span>
<span data-ttu-id="63dc7-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="63dc7-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63dc7-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="63dc7-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63dc7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63dc7-141">CommonParameters</span></span>
<span data-ttu-id="63dc7-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="63dc7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63dc7-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63dc7-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63dc7-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="63dc7-144">INPUTS</span></span>

### <span data-ttu-id="63dc7-145">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="63dc7-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="63dc7-146">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="63dc7-146">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="63dc7-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="63dc7-147">OUTPUTS</span></span>

### <span data-ttu-id="63dc7-148">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="63dc7-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="63dc7-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="63dc7-149">NOTES</span></span>

## <span data-ttu-id="63dc7-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="63dc7-150">RELATED LINKS</span></span>

[<span data-ttu-id="63dc7-151">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="63dc7-151">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)
