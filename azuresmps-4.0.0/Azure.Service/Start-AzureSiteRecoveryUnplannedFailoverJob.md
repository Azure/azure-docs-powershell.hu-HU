---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AC73119B-BB76-425B-AA44-44502028ECC4
online version: ''
schema: 2.0.0
ms.openlocfilehash: a74a02f219b5bb64957ab919168cb79ccf681869
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015806"
---
# <span data-ttu-id="b56b7-101">Start-AzureSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="b56b7-101">Start-AzureSiteRecoveryUnplannedFailoverJob</span></span>

## <span data-ttu-id="b56b7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b56b7-102">SYNOPSIS</span></span>
<span data-ttu-id="b56b7-103">Elindítja a nem tervezett feladatátvételt egy webhely-helyreállítási jogalanynál vagy helyreállítási tervben.</span><span class="sxs-lookup"><span data-stu-id="b56b7-103">Starts the unplanned failover for a Site Recovery protection entity or recovery plan.</span></span>

## <span data-ttu-id="b56b7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b56b7-104">SYNTAX</span></span>

### <span data-ttu-id="b56b7-105">ByRPId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b56b7-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -RPId <String> -Direction <String> [-PrimaryAction <Boolean>]
 [-PerformSourceSideActions] [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b56b7-106">ByPEId</span><span class="sxs-lookup"><span data-stu-id="b56b7-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-PerformSourceSiteOperations <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b56b7-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="b56b7-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PrimaryAction <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="b56b7-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="b56b7-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-PerformSourceSiteOperations <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b56b7-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="b56b7-109">DESCRIPTION</span></span>
<span data-ttu-id="b56b7-110">A **Start-AzureSiteRecoveryUnplannedFailoverJob** parancsmag az Azure webhely-helyreállítási védelem vagy helyreállítási terv nem tervezett feladatátvételét indítja el.</span><span class="sxs-lookup"><span data-stu-id="b56b7-110">The **Start-AzureSiteRecoveryUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="b56b7-111">Ellenőrizheti, hogy a feladat sikeres volt-e a **Get-AzureSiteRecoveryJob** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="b56b7-111">You can check whether the job succeeds by using the **Get-AzureSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="b56b7-112">Példák</span><span class="sxs-lookup"><span data-stu-id="b56b7-112">EXAMPLES</span></span>

### <span data-ttu-id="b56b7-113">Példa 1: nem tervezett feladatátvételi feladat indítása</span><span class="sxs-lookup"><span data-stu-id="b56b7-113">Example 1: Start an unplanned failover job</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer 
PS C:\> Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntity $ProtectionEntity -Direction "PrimaryToRecovery"
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

<span data-ttu-id="b56b7-114">Az első parancs a **Get-AzureSiteRecoveryProtectionContainer** parancsmag használatával kap védett tárolót, majd a $ProtectionContainer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b56b7-114">The first command gets a protected container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="b56b7-115">A második parancs a **Get-AzureSiteRecoveryProtectionEntity** parancsmag segítségével a védett tárolóhoz tartozó védett entitásokat kapja meg $ProtectionContainer.</span><span class="sxs-lookup"><span data-stu-id="b56b7-115">The second command gets the protected entities that belong to the protected container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="b56b7-116">A parancs az eredményt a $ProtectionEntity változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b56b7-116">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="b56b7-117">A végleges parancs elindítja a $ProtectionEntity tárolt védett entitások feladatátvételét, és a feladatátvétel irányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b56b7-117">The final command starts the failover for the protected entities stored in $ProtectionEntity and specifies the direction of the failover.</span></span>

## <span data-ttu-id="b56b7-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b56b7-118">PARAMETERS</span></span>

### <span data-ttu-id="b56b7-119">-Irány</span><span class="sxs-lookup"><span data-stu-id="b56b7-119">-Direction</span></span>
<span data-ttu-id="b56b7-120">A feladatátvétel irányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b56b7-120">Specifies the direction of the failover.</span></span>
<span data-ttu-id="b56b7-121">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b56b7-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b56b7-122">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="b56b7-122">PrimaryToRecovery</span></span>
- <span data-ttu-id="b56b7-123">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="b56b7-123">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="b56b7-124">-PerformSourceSideActions</span><span class="sxs-lookup"><span data-stu-id="b56b7-124">-PerformSourceSideActions</span></span>
<span data-ttu-id="b56b7-125">Azt jelzi, hogy a művelet a forrásként használható műveleteket is elvégezheti.</span><span class="sxs-lookup"><span data-stu-id="b56b7-125">Indicates that the action can perform source side actions.</span></span>

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

### <span data-ttu-id="b56b7-126">-PerformSourceSiteOperations</span><span class="sxs-lookup"><span data-stu-id="b56b7-126">-PerformSourceSiteOperations</span></span>
<span data-ttu-id="b56b7-127">Azt jelzi, hogy a forrás-webhely műveletei végrehajthatók.</span><span class="sxs-lookup"><span data-stu-id="b56b7-127">Indicates that source site operations can be performed.</span></span>

```yaml
Type: Boolean
Parameter Sets: ByPEId, ByPEObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b56b7-128">-PrimaryAction</span><span class="sxs-lookup"><span data-stu-id="b56b7-128">-PrimaryAction</span></span>
<span data-ttu-id="b56b7-129">Azt jelzi, hogy szükség van az elsődleges webhely műveleteire.</span><span class="sxs-lookup"><span data-stu-id="b56b7-129">Indicates that  primary site actions are required.</span></span>

```yaml
Type: Boolean
Parameter Sets: ByRPId, ByRPObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b56b7-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="b56b7-130">-Profile</span></span>
<span data-ttu-id="b56b7-131">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="b56b7-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b56b7-132">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="b56b7-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b56b7-133">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="b56b7-133">-ProtectionContainerId</span></span>
<span data-ttu-id="b56b7-134">Egy védett tároló AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b56b7-134">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="b56b7-135">Ez a parancsmag elindítja a feladatot egy olyan védett virtuális géphez, amely a parancsmag által megadott tárolóhoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="b56b7-135">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b56b7-136">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="b56b7-136">-ProtectionEntity</span></span>
<span data-ttu-id="b56b7-137">A webhely-helyreállítási védelem entitás objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b56b7-137">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b56b7-138">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="b56b7-138">-ProtectionEntityId</span></span>
<span data-ttu-id="b56b7-139">Annak a védett virtuális gépnek az AZONOSÍTÓját adja meg, amelyre a feladatot el szeretné indítani.</span><span class="sxs-lookup"><span data-stu-id="b56b7-139">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b56b7-140">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b56b7-140">-RecoveryPlan</span></span>
<span data-ttu-id="b56b7-141">A helyreállítási terv objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b56b7-141">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="b56b7-142">-RPId</span><span class="sxs-lookup"><span data-stu-id="b56b7-142">-RPId</span></span>
<span data-ttu-id="b56b7-143">Annak a helyreállítási tervnek az AZONOSÍTÓját adja meg, amelyre a feladatot el szeretné indítani.</span><span class="sxs-lookup"><span data-stu-id="b56b7-143">Specifies the ID of a recovery plan for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByRPId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b56b7-144">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="b56b7-144">-WaitForCompletion</span></span>
<span data-ttu-id="b56b7-145">Azt jelzi, hogy a parancsmag a művelet befejezéséhez vár, mielőtt a vezérlőt visszaadja a Windows PowerShell konzolnak.</span><span class="sxs-lookup"><span data-stu-id="b56b7-145">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="b56b7-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b56b7-146">CommonParameters</span></span>
<span data-ttu-id="b56b7-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b56b7-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b56b7-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b56b7-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b56b7-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b56b7-149">INPUTS</span></span>

## <span data-ttu-id="b56b7-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b56b7-150">OUTPUTS</span></span>

## <span data-ttu-id="b56b7-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b56b7-151">NOTES</span></span>

## <span data-ttu-id="b56b7-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b56b7-152">RELATED LINKS</span></span>

[<span data-ttu-id="b56b7-153">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="b56b7-153">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="b56b7-154">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b56b7-154">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="b56b7-155">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="b56b7-155">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="b56b7-156">Start-AzureSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="b56b7-156">Start-AzureSiteRecoveryTestFailoverJob</span></span>](./Start-AzureSiteRecoveryTestFailoverJob.md)


