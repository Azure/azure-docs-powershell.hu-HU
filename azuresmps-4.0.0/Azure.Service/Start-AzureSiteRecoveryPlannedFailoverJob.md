---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2575F5C4-A276-49CE-AB0C-726F359DA6F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7f71138e47c851097fe36ca294784fc571b6369f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015751"
---
# <span data-ttu-id="2324f-101">Start-AzureSiteRecoveryPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="2324f-101">Start-AzureSiteRecoveryPlannedFailoverJob</span></span>

## <span data-ttu-id="2324f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2324f-102">SYNOPSIS</span></span>
<span data-ttu-id="2324f-103">A webhely-helyreállítási tervezett feladatátvételi művelet elindítása</span><span class="sxs-lookup"><span data-stu-id="2324f-103">Starts a Site Recovery planned failover operation.</span></span>

## <span data-ttu-id="2324f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2324f-104">SYNTAX</span></span>

### <span data-ttu-id="2324f-105">ByRPId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2324f-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -RPId <String> -Direction <String> [-WaitForCompletion]
 [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2324f-106">ByPEId</span><span class="sxs-lookup"><span data-stu-id="2324f-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2324f-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="2324f-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2324f-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="2324f-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2324f-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="2324f-109">DESCRIPTION</span></span>
<span data-ttu-id="2324f-110">A **Start-AzureSiteRecoveryPlannedFailoverJob** parancsmag tervezett feladatátvételt indít az Azure webhely-helyreállítási védelmi entitások vagy helyreállítási tervek számára.</span><span class="sxs-lookup"><span data-stu-id="2324f-110">The **Start-AzureSiteRecoveryPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="2324f-111">Ellenőrizheti, hogy a feladat sikeres volt-e a **Get-AzureSiteRecoveryJob** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="2324f-111">You can check whether the job succeeds by using the **Get-AzureSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="2324f-112">Példák</span><span class="sxs-lookup"><span data-stu-id="2324f-112">EXAMPLES</span></span>

### <span data-ttu-id="2324f-113">1. példa: tervezett feladatátvételi feladat indítása</span><span class="sxs-lookup"><span data-stu-id="2324f-113">Example 1: Start a planned failover job</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
PS C:\> Start-AzureSiteRecoveryPlannedFailoverJob -Direction PrimaryToRecovery -ProtectionEntity $Protected -Optimize ForDowntime
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

<span data-ttu-id="2324f-114">Az első parancs a **Get-AzureSiteRecoveryProtectionContainer** parancsmag segítségével az aktuális Azure-webhely helyreállítási tárolójában minden védett tárolót megkapja, majd a $Container változóban tárolja az eredményeket.</span><span class="sxs-lookup"><span data-stu-id="2324f-114">The first command gets all protected containers in the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores the results in the $Container variable.</span></span>
<span data-ttu-id="2324f-115">Ebben a példában egyetlen tároló található.</span><span class="sxs-lookup"><span data-stu-id="2324f-115">In this example, there is a single container.</span></span>

<span data-ttu-id="2324f-116">A második parancs a **Get-AzureSiteRecoveryProtectionEntity** parancsmaggal a $Container tárolt tárolóhoz tartozó védett virtuális gépeket kapja.</span><span class="sxs-lookup"><span data-stu-id="2324f-116">The second command gets the protected virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="2324f-117">A parancs az eredményt a $Protected változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2324f-117">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="2324f-118">A végleges parancs elindítja a feladatátvételi feladatot az $Protected-ban tárolt védett virtuális gépek iránya PrimaryToRecovery.</span><span class="sxs-lookup"><span data-stu-id="2324f-118">The final command starts the failover job in the direction PrimaryToRecovery for the protected virtual machines stored in $Protected.</span></span>

## <span data-ttu-id="2324f-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2324f-119">PARAMETERS</span></span>

### <span data-ttu-id="2324f-120">-Irány</span><span class="sxs-lookup"><span data-stu-id="2324f-120">-Direction</span></span>
<span data-ttu-id="2324f-121">A feladatátvétel irányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2324f-121">Specifies the direction of the failover.</span></span>
<span data-ttu-id="2324f-122">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2324f-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2324f-123">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="2324f-123">PrimaryToRecovery</span></span>
- <span data-ttu-id="2324f-124">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="2324f-124">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="2324f-125">-Optimalizálás</span><span class="sxs-lookup"><span data-stu-id="2324f-125">-Optimize</span></span>
<span data-ttu-id="2324f-126">Itt adhatja meg, hogy mit szeretne optimalizálni.</span><span class="sxs-lookup"><span data-stu-id="2324f-126">Specifies what to optimize for.</span></span>
<span data-ttu-id="2324f-127">Ez a paraméter egy Azure-webhelyről a helyszíni webhelyre való feladatátvételre vonatkozik, amely jelentős adatszinkronizálást követel meg.</span><span class="sxs-lookup"><span data-stu-id="2324f-127">This parameter applies for failover from an Azure site to an on-premise site which requires a significant data synchronization.</span></span>
<span data-ttu-id="2324f-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2324f-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2324f-129">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="2324f-129">ForDowntime</span></span>
- <span data-ttu-id="2324f-130">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="2324f-130">ForSynchronization</span></span>

<span data-ttu-id="2324f-131">Ha a **ForDowntime** meg van adva, ez azt jelzi, hogy az adatokat a program szinkronizálja a feladatátvétel minimalizálása előtt.</span><span class="sxs-lookup"><span data-stu-id="2324f-131">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="2324f-132">A szinkronizálás a virtuális gép leállítása nélkül végezhető el.</span><span class="sxs-lookup"><span data-stu-id="2324f-132">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="2324f-133">Miután befejeződött a szinkronizálás, a program felfüggeszti a feladatot.</span><span class="sxs-lookup"><span data-stu-id="2324f-133">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="2324f-134">Folytassa a feladatot, és végezze el a szinkronizálási műveletet, amely leállítja a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="2324f-134">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="2324f-135">Ha a **ForSynchronization** meg van adva, ez azt jelzi, hogy az adatok szinkronizálása a feladatátvétel során történik, így az adatok szinkronizálása kisméretű.</span><span class="sxs-lookup"><span data-stu-id="2324f-135">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="2324f-136">Mivel ez a beállítás engedélyezve van, a virtuális gép azonnal leállt.</span><span class="sxs-lookup"><span data-stu-id="2324f-136">Because this setting is enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="2324f-137">A szinkronizálás a leállítást követően kezdődik a feladatátvételi művelet befejezéséhez.</span><span class="sxs-lookup"><span data-stu-id="2324f-137">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="2324f-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="2324f-138">-Profile</span></span>
<span data-ttu-id="2324f-139">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="2324f-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2324f-140">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="2324f-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2324f-141">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="2324f-141">-ProtectionContainerId</span></span>
<span data-ttu-id="2324f-142">Annak a védett tárolónak az AZONOSÍTÓját adja meg, amelybe a feladatot el szeretné indítani.</span><span class="sxs-lookup"><span data-stu-id="2324f-142">Specifies the ID of the protected container for which to start the job.</span></span>

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

### <span data-ttu-id="2324f-143">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="2324f-143">-ProtectionEntity</span></span>
<span data-ttu-id="2324f-144">A webhely-helyreállítási védelem entitás objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2324f-144">Specifies the Site Recovery protection entity object.</span></span>

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

### <span data-ttu-id="2324f-145">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="2324f-145">-ProtectionEntityId</span></span>
<span data-ttu-id="2324f-146">Azt a **ASRProtectionEntity** -objektumot adja meg, amelybe a feladatot el szeretné kezdeni.</span><span class="sxs-lookup"><span data-stu-id="2324f-146">Specifies an **ASRProtectionEntity** object for which to start the job.</span></span>
<span data-ttu-id="2324f-147">Ha **ASRProtectionEntity** objektumot szeretne beolvasni, használja a **Get-AzureSiteRecoveryProtectionEntity** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2324f-147">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

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

### <span data-ttu-id="2324f-148">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2324f-148">-RecoveryPlan</span></span>
<span data-ttu-id="2324f-149">A helyreállítási terv objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2324f-149">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="2324f-150">-RPId</span><span class="sxs-lookup"><span data-stu-id="2324f-150">-RPId</span></span>
<span data-ttu-id="2324f-151">Annak a helyreállítási tervnek az AZONOSÍTÓját adja meg, amelyre a feladatot el szeretné indítani.</span><span class="sxs-lookup"><span data-stu-id="2324f-151">Specifies the ID of a recovery plan for which to start the job.</span></span>

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

### <span data-ttu-id="2324f-152">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="2324f-152">-WaitForCompletion</span></span>
<span data-ttu-id="2324f-153">Azt jelzi, hogy a parancsmag a művelet befejezéséhez vár, mielőtt a vezérlőt visszaadja a Windows PowerShell konzolnak.</span><span class="sxs-lookup"><span data-stu-id="2324f-153">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="2324f-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2324f-154">CommonParameters</span></span>
<span data-ttu-id="2324f-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2324f-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2324f-156">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2324f-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2324f-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2324f-157">INPUTS</span></span>

## <span data-ttu-id="2324f-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2324f-158">OUTPUTS</span></span>

## <span data-ttu-id="2324f-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2324f-159">NOTES</span></span>

## <span data-ttu-id="2324f-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2324f-160">RELATED LINKS</span></span>

[<span data-ttu-id="2324f-161">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="2324f-161">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="2324f-162">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="2324f-162">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


