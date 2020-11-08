---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 9AE41884-C39F-4AEB-8030-96167F98C8DD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6b46cc27b2e5380f3cb533a4355a94170e941cd8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016028"
---
# <span data-ttu-id="3d7ce-101">Start-AzureSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="3d7ce-101">Start-AzureSiteRecoveryTestFailoverJob</span></span>

## <span data-ttu-id="3d7ce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3d7ce-102">SYNOPSIS</span></span>
<span data-ttu-id="3d7ce-103">Teszteli a feladatátvételt a webhely-helyreállítási védelem entitásban.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-103">Starts a test failover for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="3d7ce-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3d7ce-104">SYNTAX</span></span>

### <span data-ttu-id="3d7ce-105">ByPEId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3d7ce-105">ByPEId (Default)</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d7ce-106">ByRPId</span><span class="sxs-lookup"><span data-stu-id="3d7ce-106">ByRPId</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3d7ce-107">ByRPIdWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="3d7ce-107">ByRPIdWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] -LogicalNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d7ce-108">ByRPIdWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="3d7ce-108">ByRPIdWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] -VmNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d7ce-109">ByRPIdWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="3d7ce-109">ByRPIdWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> -Network <ASRNetwork> [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3d7ce-110">ByPEObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="3d7ce-110">ByPEObjectWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3d7ce-111">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="3d7ce-111">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d7ce-112">ByPEIdWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="3d7ce-112">ByPEIdWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d7ce-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="3d7ce-113">ByRPObject</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d7ce-114">ByRPObjectWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="3d7ce-114">ByRPObjectWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3d7ce-115">ByRPObjectWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="3d7ce-115">ByRPObjectWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] -VmNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3d7ce-116">ByPEIdWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="3d7ce-116">ByPEIdWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3d7ce-117">ByPEIdWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="3d7ce-117">ByPEIdWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] -VmNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3d7ce-118">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="3d7ce-118">ByPEObject</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3d7ce-119">ByPEObjectWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="3d7ce-119">ByPEObjectWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3d7ce-120">ByPEObjectWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="3d7ce-120">ByPEObjectWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] -VmNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="3d7ce-121">Leírás</span><span class="sxs-lookup"><span data-stu-id="3d7ce-121">DESCRIPTION</span></span>
<span data-ttu-id="3d7ce-122">A **Start-AzureSiteRecoveryTestFailoverJob** parancsmag elindítja az Azure webhely-helyreállítási védelmi szervezet vagy helyreállítási terv feladatátvételét.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-122">The **Start-AzureSiteRecoveryTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="3d7ce-123">Ellenőrizheti, hogy a feladat sikeres volt-e a **Get-AzureRMSiteRecoveryJob** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-123">You can check whether the job succeeded by using the **Get-AzureRMSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="3d7ce-124">Példák</span><span class="sxs-lookup"><span data-stu-id="3d7ce-124">EXAMPLES</span></span>

### <span data-ttu-id="3d7ce-125">Példa 1: teszt-feladatátvétel indítása</span><span class="sxs-lookup"><span data-stu-id="3d7ce-125">Example 1: Start a test failover</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer
PS C:\> Start-AzureSiteRecoveryTestFailoverJob -ProtectionEntity $ProtectionEntity -Direction "PrimaryToRecovery"
ID               : c38eecdc-731c-405b-a61c-08db99aae2fe
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : {}
Name             : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="3d7ce-126">Az első parancs a **Get-AzureSiteRecoveryProtectionContainer** parancsmagot használja a védett tároló beszerzéséhez, majd a $ProtectionContainer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-126">The first command uses the **Get-AzureSiteRecoveryProtectionContainer** cmdlet to get a protected container, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="3d7ce-127">A második parancs a **Get-AzureSiteRecoveryProtectionEntity** parancsmag segítségével a védett tárolóhoz tartozó védett entitásokat kapja meg $ProtectionContainer.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-127">The second command gets the protected entities that belong to the protected container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="3d7ce-128">A parancs az eredményt a $ProtectionEntity változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-128">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="3d7ce-129">A végleges parancs elindítja a teszt-feladatátvételi műveletet az $ProtectionEntity tárolt védett entitások esetében, és a feladatátvétel irányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-129">The final command starts the test failover operation for the protected entities stored in $ProtectionEntity and specifies the direction of the failover.</span></span>

### <span data-ttu-id="3d7ce-130">2. példa: teszt-feladatátvétel indítása helyreállítási csomag használatával</span><span class="sxs-lookup"><span data-stu-id="3d7ce-130">Example 2: Start a test failover using a recovery plan</span></span>
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan -Name "RecoveryPlan01"
Start-AzureSiteRecoveryTestFailoverJob -Direction PrimaryToRecovery -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="3d7ce-131">Ez a parancs a **Get-AzureSiteRecoveryRecoveryPlan** parancsmaggal megkapja a RecoveryPlan01 nevű helyreállítási tervet az aktuális Azure webhely-helyreállítási boltozathoz.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-131">This command gets the recovery plan named RecoveryPlan01 for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet.</span></span>
<span data-ttu-id="3d7ce-132">A parancs a csomagot a $RecoveryPlan változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-132">The command stores the plan in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="3d7ce-133">A második parancs elindítja a teszt-feladatátvételi műveletet az $RecoveryPlan tárolt helyreállítási tervhez, és a feladatátvétel irányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-133">The second command starts the test failover operation for the recovery plan stored in $RecoveryPlan and specifies the direction of the failover.</span></span>

## <span data-ttu-id="3d7ce-134">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3d7ce-134">PARAMETERS</span></span>

### <span data-ttu-id="3d7ce-135">-Irány</span><span class="sxs-lookup"><span data-stu-id="3d7ce-135">-Direction</span></span>
<span data-ttu-id="3d7ce-136">A feladatátvétel irányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-136">Specifies the failover direction.</span></span>
<span data-ttu-id="3d7ce-137">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3d7ce-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3d7ce-138">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="3d7ce-138">PrimaryToRecovery</span></span>
- <span data-ttu-id="3d7ce-139">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="3d7ce-139">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d7ce-140">-LogicalNetworkId</span><span class="sxs-lookup"><span data-stu-id="3d7ce-140">-LogicalNetworkId</span></span>
<span data-ttu-id="3d7ce-141">A logikai hálózat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-141">Specifies the ID of the logical network.</span></span>

```yaml
Type: String
Parameter Sets: ByRPIdWithLogicalNetworkID, ByRPObjectWithLogicalNetworkID, ByPEIdWithLogicalNetworkID, ByPEObjectWithLogicalNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d7ce-142">– Hálózat</span><span class="sxs-lookup"><span data-stu-id="3d7ce-142">-Network</span></span>
<span data-ttu-id="3d7ce-143">Annak a hálózati objektumnak a meghatározása, amelyet a feladatátvétel teszteléséhez használni kell.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-143">Specifies the network object to use for test failover.</span></span>
<span data-ttu-id="3d7ce-144">Ha hálózatba szeretne hozzájutni, használja a **Get-AzureSiteRecoveryNetwork** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-144">To obtain a network, use the **Get-AzureSiteRecoveryNetwork** cmdlet.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByPEId, ByRPId, ByRPIdWithLogicalNetworkID, ByRPIdWithVMNetworkID, ByRPObject, ByRPObjectWithLogicalNetworkID, ByRPObjectWithVMNetworkID, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID, ByPEObject, ByPEObjectWithLogicalNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRNetwork
Parameter Sets: ByRPIdWithVMNetwork, ByPEObjectWithVMNetwork, ByRPObjectWithVMNetwork, ByPEIdWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d7ce-145">-NetworkType</span><span class="sxs-lookup"><span data-stu-id="3d7ce-145">-NetworkType</span></span>
<span data-ttu-id="3d7ce-146">A feladatátvétel teszteléséhez használandó hálózati típust adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-146">Specifies the network type to use for test failover.</span></span>
<span data-ttu-id="3d7ce-147">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3d7ce-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3d7ce-148">Nincs</span><span class="sxs-lookup"><span data-stu-id="3d7ce-148">None</span></span>
- <span data-ttu-id="3d7ce-149">Új</span><span class="sxs-lookup"><span data-stu-id="3d7ce-149">New</span></span>
- <span data-ttu-id="3d7ce-150">Meglévő</span><span class="sxs-lookup"><span data-stu-id="3d7ce-150">Existing</span></span>

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

### <span data-ttu-id="3d7ce-151">-Profil</span><span class="sxs-lookup"><span data-stu-id="3d7ce-151">-Profile</span></span>
<span data-ttu-id="3d7ce-152">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-152">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3d7ce-153">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-153">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d7ce-154">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="3d7ce-154">-ProtectionContainerId</span></span>
<span data-ttu-id="3d7ce-155">Egy védett tároló AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-155">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="3d7ce-156">Ez a parancsmag elindítja a feladatot egy olyan védett virtuális géphez, amely a parancsmag által megadott tárolóhoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-156">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId, ByPEIdWithVMNetwork, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d7ce-157">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="3d7ce-157">-ProtectionEntity</span></span>
<span data-ttu-id="3d7ce-158">A webhely-helyreállítási védelem entitás objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-158">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObjectWithVMNetwork, ByPEObjectWithLogicalNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d7ce-159">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="3d7ce-159">-ProtectionEntityId</span></span>
<span data-ttu-id="3d7ce-160">Annak a védett virtuális gépnek az AZONOSÍTÓját adja meg, amelyre a feladatot el szeretné indítani.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-160">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId, ByPEIdWithVMNetwork, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d7ce-161">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3d7ce-161">-RecoveryPlan</span></span>
<span data-ttu-id="3d7ce-162">Azt a helyreállítási tervet adja meg, amelyre a feladatot el szeretné indítani.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-162">Specifies a recovery plan for which to start the job.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObjectWithVMNetwork, ByRPObjectWithLogicalNetworkID, ByRPObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d7ce-163">-RpId</span><span class="sxs-lookup"><span data-stu-id="3d7ce-163">-RpId</span></span>
<span data-ttu-id="3d7ce-164">Annak a helyreállítási tervnek az AZONOSÍTÓját adja meg, amelyre a feladatot el szeretné indítani.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-164">Specifies the ID of a recovery plan for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByRPId, ByRPIdWithLogicalNetworkID, ByRPIdWithVMNetworkID, ByRPIdWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d7ce-165">-VmNetworkId</span><span class="sxs-lookup"><span data-stu-id="3d7ce-165">-VmNetworkId</span></span>
<span data-ttu-id="3d7ce-166">A virtuálisgép-hálózat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-166">Specifies the ID of the virtual machine network.</span></span>

```yaml
Type: String
Parameter Sets: ByRPIdWithVMNetworkID, ByRPObjectWithVMNetworkID, ByPEIdWithVMNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d7ce-167">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="3d7ce-167">-WaitForCompletion</span></span>
<span data-ttu-id="3d7ce-168">Azt jelzi, hogy a parancsmag a művelet befejezéséhez vár, mielőtt a vezérlőt visszaadja a Windows PowerShell konzolnak.</span><span class="sxs-lookup"><span data-stu-id="3d7ce-168">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d7ce-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d7ce-169">CommonParameters</span></span>
<span data-ttu-id="3d7ce-170">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3d7ce-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d7ce-171">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d7ce-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d7ce-172">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d7ce-172">INPUTS</span></span>

## <span data-ttu-id="3d7ce-173">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d7ce-173">OUTPUTS</span></span>

## <span data-ttu-id="3d7ce-174">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3d7ce-174">NOTES</span></span>

## <span data-ttu-id="3d7ce-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d7ce-175">RELATED LINKS</span></span>

[<span data-ttu-id="3d7ce-176">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="3d7ce-176">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="3d7ce-177">Get-AzureSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="3d7ce-177">Get-AzureSiteRecoveryNetwork</span></span>](./Get-AzureSiteRecoveryNetwork.md)

[<span data-ttu-id="3d7ce-178">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="3d7ce-178">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="3d7ce-179">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3d7ce-179">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="3d7ce-180">Start-AzureSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="3d7ce-180">Start-AzureSiteRecoveryUnplannedFailoverJob</span></span>](./Start-AzureSiteRecoveryUnplannedFailoverJob.md)


