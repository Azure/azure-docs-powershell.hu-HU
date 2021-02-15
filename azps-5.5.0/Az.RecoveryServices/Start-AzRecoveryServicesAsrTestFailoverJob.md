---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: 11d254fbf43a05e4e58f0d51f5226a6a7065dd50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160058"
---
# <span data-ttu-id="fb7d4-101">Start-AzRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="fb7d4-101">Start-AzRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="fb7d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb7d4-102">SYNOPSIS</span></span>
<span data-ttu-id="fb7d4-103">Teszt feladatátvételi műveletet kezd.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-103">Starts a test failover operation.</span></span>

## <span data-ttu-id="fb7d4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fb7d4-104">SYNTAX</span></span>

### <span data-ttu-id="fb7d4-105">ByRPIObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fb7d4-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb7d4-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="fb7d4-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb7d4-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="fb7d4-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb7d4-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="fb7d4-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb7d4-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="fb7d4-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb7d4-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="fb7d4-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fb7d4-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fb7d4-111">DESCRIPTION</span></span>
<span data-ttu-id="fb7d4-112">A **Start-AzRecoveryServicesAsrTestFailover Parancsfájl** parancsmag elindítja egy Azure-webhely-helyreállítási replikációval védett elem vagy helyreállítási terv feladatátvételét.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-112">The **Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="fb7d4-113">A feladat sikeres voltának ellenőrzéséhez használja a Get-AzRecoveryServicesAsrJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-113">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="fb7d4-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fb7d4-114">EXAMPLES</span></span>

### <span data-ttu-id="fb7d4-115">1. példa</span><span class="sxs-lookup"><span data-stu-id="fb7d4-115">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="fb7d4-116">Elindítja a helyreállítási terv feladatátvételi tesztműveletét a megadott paraméterekkel, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="fb7d4-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="fb7d4-117">Example 2</span></span>

<span data-ttu-id="fb7d4-118">Teszt feladatátvételi műveletet kezd.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-118">Starts a test failover operation.</span></span> <span data-ttu-id="fb7d4-119">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="fb7d4-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrTestFailoverJob -AzureVMNetworkId <String> -Direction PrimaryToRecovery -RecoveryPlan $RP
```

## <span data-ttu-id="fb7d4-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb7d4-120">PARAMETERS</span></span>

### <span data-ttu-id="fb7d4-121">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="fb7d4-121">-AzureVMNetworkId</span></span>
<span data-ttu-id="fb7d4-122">Megadja a helyreállítási VIRTUÁLIS GÉP azure-hálózati azonosítóját a feladatátvétel után.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-122">Specifies the Azure vm network id for recovery VM after failover.</span></span>

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

### <span data-ttu-id="fb7d4-123">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="fb7d4-123">-CloudServiceCreationOption</span></span>
<span data-ttu-id="fb7d4-124">Azt adja meg, hogy új felhőszolgáltatást kell-e létrehozni, vagy a virtuális géphez konfigurált helyreállítási felhőszolgáltatást kell használni a teszt feladatátvételhez.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-124">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

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

### <span data-ttu-id="fb7d4-125">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="fb7d4-125">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="fb7d4-126">Az elsődleges tanúsítványfájlt adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-126">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="fb7d4-127">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="fb7d4-127">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="fb7d4-128">A másodlagos tanúsítványfájlt adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-128">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="fb7d4-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb7d4-129">-DefaultProfile</span></span>
<span data-ttu-id="fb7d4-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="fb7d4-131">-Irány</span><span class="sxs-lookup"><span data-stu-id="fb7d4-131">-Direction</span></span>
<span data-ttu-id="fb7d4-132">A feladatátvétel irányát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-132">Specifies the failover direction.</span></span>
<span data-ttu-id="fb7d4-133">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="fb7d4-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fb7d4-134">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="fb7d4-134">PrimaryToRecovery</span></span>
- <span data-ttu-id="fb7d4-135">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="fb7d4-135">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="fb7d4-136">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fb7d4-136">-RecoveryPlan</span></span>
<span data-ttu-id="fb7d4-137">Egy ASR helyreállítási tervobjektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-137">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="fb7d4-138">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="fb7d4-138">-RecoveryPoint</span></span>
<span data-ttu-id="fb7d4-139">Megad egy egyéni helyreállítási pontot, amely teszteli a védett számítógép feladatátvételét.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-139">Specifies a custom recovery point to test failover the protected machine to.</span></span>

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

### <span data-ttu-id="fb7d4-140">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="fb7d4-140">-RecoveryTag</span></span>
<span data-ttu-id="fb7d4-141">Annak a helyreállítási címkének a megadása, amelynek tesztelni kell a feladatátvételt</span><span class="sxs-lookup"><span data-stu-id="fb7d4-141">Specifies the recovery tag to test failover to</span></span>

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

### <span data-ttu-id="fb7d4-142">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fb7d4-142">-ReplicationProtectedItem</span></span>
<span data-ttu-id="fb7d4-143">AsR-replikációval védett elemet ad meg.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-143">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="fb7d4-144">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="fb7d4-144">-VMNetwork</span></span>
<span data-ttu-id="fb7d4-145">Megadja a webhely-helyreállítás virtuális gép hálózatát, amely(k)hez csatlakoztatni kell a teszt feladatátvételi virtuális gép(eket).</span><span class="sxs-lookup"><span data-stu-id="fb7d4-145">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

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

### <span data-ttu-id="fb7d4-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb7d4-146">-Confirm</span></span>
<span data-ttu-id="fb7d4-147">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb7d4-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb7d4-148">-WhatIf</span></span>
<span data-ttu-id="fb7d4-149">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb7d4-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb7d4-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb7d4-151">CommonParameters</span></span>
<span data-ttu-id="fb7d4-152">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb7d4-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb7d4-153">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb7d4-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb7d4-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fb7d4-154">INPUTS</span></span>

### <span data-ttu-id="fb7d4-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fb7d4-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="fb7d4-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fb7d4-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="fb7d4-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb7d4-157">OUTPUTS</span></span>

### <span data-ttu-id="fb7d4-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="fb7d4-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fb7d4-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fb7d4-159">NOTES</span></span>

## <span data-ttu-id="fb7d4-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb7d4-160">RELATED LINKS</span></span>

[<span data-ttu-id="fb7d4-161">Get-AzRecoveryServicesAsrService</span><span class="sxs-lookup"><span data-stu-id="fb7d4-161">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
