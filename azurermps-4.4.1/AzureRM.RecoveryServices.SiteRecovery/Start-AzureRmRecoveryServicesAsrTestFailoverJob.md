---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: d547de0af8d4f7b4f98a572d95dcc023d975fc2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501672"
---
# <span data-ttu-id="8e9a7-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="8e9a7-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="8e9a7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8e9a7-102">SYNOPSIS</span></span>
<span data-ttu-id="8e9a7-103">Elindítja a teszt-feladatátvételi műveletet.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-103">Starts a test failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e9a7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8e9a7-104">SYNTAX</span></span>

### <span data-ttu-id="8e9a7-105">ByRPIObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8e9a7-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e9a7-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="8e9a7-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e9a7-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="8e9a7-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e9a7-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="8e9a7-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e9a7-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="8e9a7-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e9a7-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="8e9a7-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e9a7-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e9a7-111">DESCRIPTION</span></span>
<span data-ttu-id="8e9a7-112">A **Start-AzureRmRecoveryServicesAsrTestFailoverJob** parancsmag az Azure webhely-helyreállítási replikációs szolgáltatással védett elemek vagy helyreállítási terv feladatátvételének tesztelését indítja el.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-112">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="8e9a7-113">Ellenőrizheti, hogy a feladat sikeres volt-e az Get-AzureRmRecoveryServicesAsrJob parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-113">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="8e9a7-114">Példák</span><span class="sxs-lookup"><span data-stu-id="8e9a7-114">EXAMPLES</span></span>

### <span data-ttu-id="8e9a7-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8e9a7-115">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="8e9a7-116">Elindítja a helyreállítási terv teszt-feladatátvételi műveletét a megadott paraméterekkel, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8e9a7-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8e9a7-117">PARAMETERS</span></span>

### <span data-ttu-id="8e9a7-118">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="8e9a7-118">-AzureVMNetworkId</span></span>
<span data-ttu-id="8e9a7-119">Itt adhatja meg, hogy a teszt a virtuális gép (ek) ra való csatlakoztatáskor az Azure Virtual Network AZONOSÍTÓját adja-e meg.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-119">Specifies the Azure virtual network ID to connect the test fail over virtual machine(s) to.</span></span>

```yaml
Type: String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e9a7-120">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="8e9a7-120">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="8e9a7-121">Az elsődleges tanúsítvány fájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-121">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="8e9a7-122">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="8e9a7-122">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="8e9a7-123">A másodlagos tanúsítvány fájlját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-123">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="8e9a7-124">-Irány</span><span class="sxs-lookup"><span data-stu-id="8e9a7-124">-Direction</span></span>
<span data-ttu-id="8e9a7-125">A feladatátvétel irányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-125">Specifies the failover direction.</span></span>
<span data-ttu-id="8e9a7-126">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8e9a7-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8e9a7-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="8e9a7-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="8e9a7-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="8e9a7-128">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="8e9a7-129">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8e9a7-129">-RecoveryPlan</span></span>
<span data-ttu-id="8e9a7-130">Az ASR-helyreállítási terv objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-130">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e9a7-131">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8e9a7-131">-ReplicationProtectedItem</span></span>
<span data-ttu-id="8e9a7-132">Egy ASR-replikációs védelemmel ellátott elemet ad meg.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-132">Specifies an ASR replication protected item.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e9a7-133">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="8e9a7-133">-VMNetwork</span></span>
<span data-ttu-id="8e9a7-134">A webhely-helyreállítási virtuális gép hálózata a teszt-feladatátvételi virtuális gép (ek) bekapcsolásához.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-134">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e9a7-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8e9a7-135">-Confirm</span></span>
<span data-ttu-id="8e9a7-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e9a7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e9a7-137">-WhatIf</span></span>
<span data-ttu-id="8e9a7-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e9a7-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e9a7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e9a7-140">CommonParameters</span></span>
<span data-ttu-id="8e9a7-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8e9a7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e9a7-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e9a7-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e9a7-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e9a7-143">INPUTS</span></span>

### <span data-ttu-id="8e9a7-144">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8e9a7-144">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="8e9a7-145">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8e9a7-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="8e9a7-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e9a7-146">OUTPUTS</span></span>

### <span data-ttu-id="8e9a7-147">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8e9a7-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8e9a7-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8e9a7-148">NOTES</span></span>

## <span data-ttu-id="8e9a7-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e9a7-149">RELATED LINKS</span></span>

[<span data-ttu-id="8e9a7-150">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="8e9a7-150">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)
