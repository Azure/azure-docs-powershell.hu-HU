---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: DBB0E08F-63F4-4D61-A69E-3C16A35301EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
ms.openlocfilehash: e723aacbfbd1b782a91fdc6aa589bfe15df42cff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496831"
---
# <span data-ttu-id="7e04e-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="7e04e-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span></span>

## <span data-ttu-id="7e04e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7e04e-102">SYNOPSIS</span></span>
<span data-ttu-id="7e04e-103">A webhely-helyreállítási tervezett feladatátvételi művelet elindítása</span><span class="sxs-lookup"><span data-stu-id="7e04e-103">Starts a Site Recovery planned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e04e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7e04e-104">SYNTAX</span></span>

### <span data-ttu-id="7e04e-105">ByPEObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7e04e-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-Server <ASRServer>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e04e-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="7e04e-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e04e-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="7e04e-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e04e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7e04e-108">DESCRIPTION</span></span>
<span data-ttu-id="7e04e-109">A **Start-AzureRmSiteRecoveryPlannedFailoverJob** parancsmag tervezett feladatátvételt indít az Azure webhely-helyreállítási védelmi entitások vagy helyreállítási tervek számára.</span><span class="sxs-lookup"><span data-stu-id="7e04e-109">The **Start-AzureRmSiteRecoveryPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="7e04e-110">Ellenőrizheti, hogy a feladat sikeres volt-e az Get-AzureRmSiteRecoveryJob parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="7e04e-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="7e04e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="7e04e-111">EXAMPLES</span></span>

## <span data-ttu-id="7e04e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7e04e-112">PARAMETERS</span></span>

### <span data-ttu-id="7e04e-113">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="7e04e-113">-CreateVmIfNotFound</span></span>
<span data-ttu-id="7e04e-114">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7e04e-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7e04e-115">igen</span><span class="sxs-lookup"><span data-stu-id="7e04e-115">Yes</span></span>
- <span data-ttu-id="7e04e-116">nem</span><span class="sxs-lookup"><span data-stu-id="7e04e-116">No</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e04e-117">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="7e04e-117">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="7e04e-118">Az elsődleges tanúsítvány fájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7e04e-118">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="7e04e-119">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="7e04e-119">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="7e04e-120">A másodlagos tanúsítvány fájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7e04e-120">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="7e04e-121">-Irány</span><span class="sxs-lookup"><span data-stu-id="7e04e-121">-Direction</span></span>
<span data-ttu-id="7e04e-122">A feladatátvétel irányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7e04e-122">Specifies the direction of the failover.</span></span>
<span data-ttu-id="7e04e-123">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7e04e-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7e04e-124">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="7e04e-124">PrimaryToRecovery</span></span>
- <span data-ttu-id="7e04e-125">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="7e04e-125">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="7e04e-126">-Optimalizálás</span><span class="sxs-lookup"><span data-stu-id="7e04e-126">-Optimize</span></span>
<span data-ttu-id="7e04e-127">Itt adhatja meg, hogy mit szeretne optimalizálni.</span><span class="sxs-lookup"><span data-stu-id="7e04e-127">Specifies what to optimize for.</span></span>
<span data-ttu-id="7e04e-128">Ez a paraméter akkor érvényes, ha egy Azure-webhelyről olyan helyszíni webhelyre végez feladatátvételt, amely jelentős adatszinkronizálást követel meg.</span><span class="sxs-lookup"><span data-stu-id="7e04e-128">This parameter applies when failover is done from an Azure site to an on-premise site which requires a substantial data synchronization.</span></span>
<span data-ttu-id="7e04e-129">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="7e04e-129">Valid values are:</span></span>

- <span data-ttu-id="7e04e-130">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="7e04e-130">ForDowntime</span></span>
- <span data-ttu-id="7e04e-131">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="7e04e-131">ForSynchronization</span></span>

<span data-ttu-id="7e04e-132">Ha a **ForDowntime** meg van adva, ez azt jelzi, hogy az adatokat a program szinkronizálja a feladatátvétel minimalizálása előtt.</span><span class="sxs-lookup"><span data-stu-id="7e04e-132">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="7e04e-133">A szinkronizálás a virtuális gép leállítása nélkül végezhető el.</span><span class="sxs-lookup"><span data-stu-id="7e04e-133">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="7e04e-134">Miután befejeződött a szinkronizálás, a program felfüggeszti a feladatot.</span><span class="sxs-lookup"><span data-stu-id="7e04e-134">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="7e04e-135">Folytassa a feladatot, és végezze el a szinkronizálási műveletet, amely leállítja a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="7e04e-135">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="7e04e-136">Ha a **ForSynchronization** meg van adva, ez azt jelzi, hogy az adatok szinkronizálása a feladatátvétel során történik, így az adatok szinkronizálása kisméretű.</span><span class="sxs-lookup"><span data-stu-id="7e04e-136">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="7e04e-137">Ha engedélyezve van ez a beállítás, a virtuális gép azonnal leállt.</span><span class="sxs-lookup"><span data-stu-id="7e04e-137">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="7e04e-138">A szinkronizálás a leállítást követően kezdődik a feladatátvételi művelet befejezéséhez.</span><span class="sxs-lookup"><span data-stu-id="7e04e-138">Synchronization starts after shutdown to complete the failover operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: ForDownTime, ForSynchronization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e04e-139">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="7e04e-139">-ProtectionEntity</span></span>
<span data-ttu-id="7e04e-140">A webhely-helyreállítási védelem entitás objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7e04e-140">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e04e-141">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7e04e-141">-RecoveryPlan</span></span>
<span data-ttu-id="7e04e-142">A helyreállítási terv objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7e04e-142">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e04e-143">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7e04e-143">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e04e-144">-Server</span><span class="sxs-lookup"><span data-stu-id="7e04e-144">-Server</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: ByPEObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e04e-145">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="7e04e-145">-ServicesProvider</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e04e-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e04e-146">-DefaultProfile</span></span>
<span data-ttu-id="7e04e-147">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7e04e-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e04e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e04e-148">CommonParameters</span></span>
<span data-ttu-id="7e04e-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7e04e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e04e-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e04e-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e04e-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e04e-151">INPUTS</span></span>

### <span data-ttu-id="7e04e-152">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="7e04e-152">ASRProtectionEntity</span></span>
<span data-ttu-id="7e04e-153">A ' ProtectionEntity ' paraméter az "ASRProtectionEntity" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="7e04e-153">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="7e04e-154">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7e04e-154">ASRRecoveryPlan</span></span>
<span data-ttu-id="7e04e-155">A ' RecoveryPlan ' paraméter az "ASRRecoveryPlan" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="7e04e-155">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="7e04e-156">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7e04e-156">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="7e04e-157">A ' ReplicationProtectedItem ' paraméter az "ASRReplicationProtectedItem" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="7e04e-157">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="7e04e-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e04e-158">OUTPUTS</span></span>

### <span data-ttu-id="7e04e-159">Microsoft. Azure. Command. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7e04e-159">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7e04e-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7e04e-160">NOTES</span></span>

## <span data-ttu-id="7e04e-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e04e-161">RELATED LINKS</span></span>

