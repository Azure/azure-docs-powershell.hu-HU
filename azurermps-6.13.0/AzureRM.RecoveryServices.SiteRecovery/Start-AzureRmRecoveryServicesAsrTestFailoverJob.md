---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: f0350cfa9facfe8fc21e6c039c2fa5838bba8875
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495747"
---
# <span data-ttu-id="d39f3-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="d39f3-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="d39f3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d39f3-102">SYNOPSIS</span></span>
<span data-ttu-id="d39f3-103">Elindítja a teszt-feladatátvételi műveletet.</span><span class="sxs-lookup"><span data-stu-id="d39f3-103">Starts a test failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d39f3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d39f3-104">SYNTAX</span></span>

### <span data-ttu-id="d39f3-105">ByRPIObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d39f3-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d39f3-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="d39f3-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d39f3-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="d39f3-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d39f3-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="d39f3-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d39f3-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="d39f3-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d39f3-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="d39f3-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d39f3-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="d39f3-111">DESCRIPTION</span></span>
<span data-ttu-id="d39f3-112">A **Start-AzureRmRecoveryServicesAsrTestFailoverJob** parancsmag az Azure webhely-helyreállítási replikációs szolgáltatással védett elemek vagy helyreállítási terv feladatátvételének tesztelését indítja el.</span><span class="sxs-lookup"><span data-stu-id="d39f3-112">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="d39f3-113">Ellenőrizheti, hogy a feladat sikeres volt-e az Get-AzureRmRecoveryServicesAsrJob parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="d39f3-113">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="d39f3-114">Példák</span><span class="sxs-lookup"><span data-stu-id="d39f3-114">EXAMPLES</span></span>

### <span data-ttu-id="d39f3-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d39f3-115">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="d39f3-116">Elindítja a helyreállítási terv teszt-feladatátvételi műveletét a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="d39f3-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d39f3-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d39f3-117">PARAMETERS</span></span>

### <span data-ttu-id="d39f3-118">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="d39f3-118">-AzureVMNetworkId</span></span>
<span data-ttu-id="d39f3-119">Itt adhatja meg, hogy a teszt a virtuális gép (ek) ra való csatlakoztatáskor az Azure Virtual Network AZONOSÍTÓját adja-e meg.</span><span class="sxs-lookup"><span data-stu-id="d39f3-119">Specifies the Azure virtual network ID to connect the test fail over virtual machine(s) to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39f3-120">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="d39f3-120">-CloudServiceCreationOption</span></span>
<span data-ttu-id="d39f3-121">Megadja, hogy a tesztelési feladatátvételhez az új felhőalapú szolgáltatást kell-e létrehozni, vagy a VM szolgáltatáshoz konfigurált helyreállítási felhőben kell-e használni.</span><span class="sxs-lookup"><span data-stu-id="d39f3-121">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPIObject, ByRPObject, ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases:
Accepted values: UseRecoveryCloudService, AutoCreateCloudService

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39f3-122">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="d39f3-122">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="d39f3-123">Az elsődleges tanúsítvány fájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d39f3-123">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="d39f3-124">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="d39f3-124">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="d39f3-125">A másodlagos tanúsítvány fájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d39f3-125">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="d39f3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d39f3-126">-DefaultProfile</span></span>
<span data-ttu-id="d39f3-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d39f3-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d39f3-128">-Irány</span><span class="sxs-lookup"><span data-stu-id="d39f3-128">-Direction</span></span>
<span data-ttu-id="d39f3-129">A feladatátvétel irányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d39f3-129">Specifies the failover direction.</span></span>
<span data-ttu-id="d39f3-130">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d39f3-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d39f3-131">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="d39f3-131">PrimaryToRecovery</span></span>
- <span data-ttu-id="d39f3-132">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="d39f3-132">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="d39f3-133">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d39f3-133">-RecoveryPlan</span></span>
<span data-ttu-id="d39f3-134">Az ASR-helyreállítási terv objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d39f3-134">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d39f3-135">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="d39f3-135">-RecoveryPoint</span></span>
<span data-ttu-id="d39f3-136">Egyéni helyreállítási pont megadása a védett gép által végzett feladatátvétel teszteléséhez.</span><span class="sxs-lookup"><span data-stu-id="d39f3-136">Specifies a custom recovery point to test failover the protected machine to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39f3-137">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="d39f3-137">-RecoveryTag</span></span>
<span data-ttu-id="d39f3-138">Azt a helyreállítási címkét adja meg, amely teszteli a feladatátvételt</span><span class="sxs-lookup"><span data-stu-id="d39f3-138">Specifies the recovery tag to test failover to</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39f3-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d39f3-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="d39f3-140">Egy ASR-replikációs védelemmel ellátott elemet ad meg.</span><span class="sxs-lookup"><span data-stu-id="d39f3-140">Specifies an ASR replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d39f3-141">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="d39f3-141">-VMNetwork</span></span>
<span data-ttu-id="d39f3-142">A webhely-helyreállítási virtuális gép hálózata a teszt-feladatátvételi virtuális gép (ek) bekapcsolásához.</span><span class="sxs-lookup"><span data-stu-id="d39f3-142">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39f3-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d39f3-143">-Confirm</span></span>
<span data-ttu-id="d39f3-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d39f3-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d39f3-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d39f3-145">-WhatIf</span></span>
<span data-ttu-id="d39f3-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d39f3-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d39f3-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d39f3-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d39f3-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d39f3-148">CommonParameters</span></span>
<span data-ttu-id="d39f3-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d39f3-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d39f3-150">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d39f3-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d39f3-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d39f3-151">INPUTS</span></span>

### <span data-ttu-id="d39f3-152">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d39f3-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="d39f3-153">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d39f3-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="d39f3-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d39f3-154">OUTPUTS</span></span>

### <span data-ttu-id="d39f3-155">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d39f3-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d39f3-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d39f3-156">NOTES</span></span>

## <span data-ttu-id="d39f3-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d39f3-157">RELATED LINKS</span></span>

[<span data-ttu-id="d39f3-158">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="d39f3-158">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)
