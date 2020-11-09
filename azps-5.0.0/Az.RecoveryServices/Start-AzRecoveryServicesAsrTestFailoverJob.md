---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: 11d254fbf43a05e4e58f0d51f5226a6a7065dd50
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302643"
---
# <span data-ttu-id="d4b35-101">Start-AzRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="d4b35-101">Start-AzRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="d4b35-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d4b35-102">SYNOPSIS</span></span>
<span data-ttu-id="d4b35-103">Elindítja a teszt-feladatátvételi műveletet.</span><span class="sxs-lookup"><span data-stu-id="d4b35-103">Starts a test failover operation.</span></span>

## <span data-ttu-id="d4b35-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d4b35-104">SYNTAX</span></span>

### <span data-ttu-id="d4b35-105">ByRPIObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d4b35-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4b35-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="d4b35-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4b35-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="d4b35-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4b35-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="d4b35-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4b35-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="d4b35-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4b35-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="d4b35-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4b35-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="d4b35-111">DESCRIPTION</span></span>
<span data-ttu-id="d4b35-112">A **Start-AzRecoveryServicesAsrTestFailoverJob** parancsmag az Azure webhely-helyreállítási replikációs szolgáltatással védett elemek vagy helyreállítási terv feladatátvételének tesztelését indítja el.</span><span class="sxs-lookup"><span data-stu-id="d4b35-112">The **Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="d4b35-113">Ellenőrizheti, hogy a feladat sikeres volt-e az Get-AzRecoveryServicesAsrJob parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="d4b35-113">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="d4b35-114">Példák</span><span class="sxs-lookup"><span data-stu-id="d4b35-114">EXAMPLES</span></span>

### <span data-ttu-id="d4b35-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d4b35-115">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="d4b35-116">Elindítja a helyreállítási terv teszt-feladatátvételi műveletét a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="d4b35-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="d4b35-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="d4b35-117">Example 2</span></span>

<span data-ttu-id="d4b35-118">Elindítja a teszt-feladatátvételi műveletet.</span><span class="sxs-lookup"><span data-stu-id="d4b35-118">Starts a test failover operation.</span></span> <span data-ttu-id="d4b35-119">autogenerated</span><span class="sxs-lookup"><span data-stu-id="d4b35-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrTestFailoverJob -AzureVMNetworkId <String> -Direction PrimaryToRecovery -RecoveryPlan $RP
```

## <span data-ttu-id="d4b35-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d4b35-120">PARAMETERS</span></span>

### <span data-ttu-id="d4b35-121">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="d4b35-121">-AzureVMNetworkId</span></span>
<span data-ttu-id="d4b35-122">A helyreállítási VM Azure VM hálózati azonosítóját adja meg a feladatátvétel után.</span><span class="sxs-lookup"><span data-stu-id="d4b35-122">Specifies the Azure vm network id for recovery VM after failover.</span></span>

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

### <span data-ttu-id="d4b35-123">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="d4b35-123">-CloudServiceCreationOption</span></span>
<span data-ttu-id="d4b35-124">Megadja, hogy a tesztelési feladatátvételhez az új felhőalapú szolgáltatást kell-e létrehozni, vagy a VM szolgáltatáshoz konfigurált helyreállítási felhőben kell-e használni.</span><span class="sxs-lookup"><span data-stu-id="d4b35-124">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

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

### <span data-ttu-id="d4b35-125">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="d4b35-125">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="d4b35-126">Az elsődleges tanúsítvány fájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4b35-126">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="d4b35-127">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="d4b35-127">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="d4b35-128">A másodlagos tanúsítvány fájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4b35-128">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="d4b35-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4b35-129">-DefaultProfile</span></span>
<span data-ttu-id="d4b35-130">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4b35-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d4b35-131">-Irány</span><span class="sxs-lookup"><span data-stu-id="d4b35-131">-Direction</span></span>
<span data-ttu-id="d4b35-132">A feladatátvétel irányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4b35-132">Specifies the failover direction.</span></span>
<span data-ttu-id="d4b35-133">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d4b35-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d4b35-134">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="d4b35-134">PrimaryToRecovery</span></span>
- <span data-ttu-id="d4b35-135">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="d4b35-135">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="d4b35-136">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d4b35-136">-RecoveryPlan</span></span>
<span data-ttu-id="d4b35-137">Az ASR-helyreállítási terv objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4b35-137">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="d4b35-138">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="d4b35-138">-RecoveryPoint</span></span>
<span data-ttu-id="d4b35-139">Egyéni helyreállítási pont megadása a védett gép által végzett feladatátvétel teszteléséhez.</span><span class="sxs-lookup"><span data-stu-id="d4b35-139">Specifies a custom recovery point to test failover the protected machine to.</span></span>

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

### <span data-ttu-id="d4b35-140">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="d4b35-140">-RecoveryTag</span></span>
<span data-ttu-id="d4b35-141">Azt a helyreállítási címkét adja meg, amely teszteli a feladatátvételt</span><span class="sxs-lookup"><span data-stu-id="d4b35-141">Specifies the recovery tag to test failover to</span></span>

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

### <span data-ttu-id="d4b35-142">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d4b35-142">-ReplicationProtectedItem</span></span>
<span data-ttu-id="d4b35-143">Egy ASR-replikációs védelemmel ellátott elemet ad meg.</span><span class="sxs-lookup"><span data-stu-id="d4b35-143">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="d4b35-144">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="d4b35-144">-VMNetwork</span></span>
<span data-ttu-id="d4b35-145">A webhely-helyreállítási virtuális gép hálózata a teszt-feladatátvételi virtuális gép (ek) bekapcsolásához.</span><span class="sxs-lookup"><span data-stu-id="d4b35-145">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

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

### <span data-ttu-id="d4b35-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d4b35-146">-Confirm</span></span>
<span data-ttu-id="d4b35-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d4b35-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4b35-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4b35-148">-WhatIf</span></span>
<span data-ttu-id="d4b35-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d4b35-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4b35-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d4b35-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4b35-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4b35-151">CommonParameters</span></span>
<span data-ttu-id="d4b35-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d4b35-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4b35-153">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d4b35-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4b35-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4b35-154">INPUTS</span></span>

### <span data-ttu-id="d4b35-155">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d4b35-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="d4b35-156">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d4b35-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="d4b35-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4b35-157">OUTPUTS</span></span>

### <span data-ttu-id="d4b35-158">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d4b35-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d4b35-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d4b35-159">NOTES</span></span>

## <span data-ttu-id="d4b35-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4b35-160">RELATED LINKS</span></span>

[<span data-ttu-id="d4b35-161">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="d4b35-161">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
