---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 853D5585-2A92-4B65-BA8C-EC06BEE8C237
online version: ''
schema: 2.0.0
ms.openlocfilehash: 63274c772c6085fc8c491557851673a38056aa77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015891"
---
# <span data-ttu-id="9376d-101">New-AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="9376d-101">New-AzureSiteRecoveryProtectionProfileObject</span></span>

## <span data-ttu-id="9376d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9376d-102">SYNOPSIS</span></span>
<span data-ttu-id="9376d-103">Webhely-helyreállítási védelmi profil objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="9376d-103">Creates a Site Recovery protection profile object.</span></span>

## <span data-ttu-id="9376d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9376d-104">SYNTAX</span></span>

### <span data-ttu-id="9376d-105">EnterpriseToAzure (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9376d-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 -RecoveryAzureSubscription <String> -RecoveryAzureStorageAccount <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9376d-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="9376d-106">EnterpriseToEnterprise</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-CompressionEnabled] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-AllowReplicaDeletion] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9376d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9376d-107">DESCRIPTION</span></span>
<span data-ttu-id="9376d-108">A **New-AzureSiteRecoveryProtectionProfileObject** parancsmag az Azure site Recovery Protection profil objektumát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="9376d-108">The **New-AzureSiteRecoveryProtectionProfileObject** cmdlet creates an Azure Site Recovery protection profile object.</span></span>
<span data-ttu-id="9376d-109">Ez a parancsmag létrehoz egy **ASRProtectionProfile** -objektumot, amelyet más parancsmagokkal használhat.</span><span class="sxs-lookup"><span data-stu-id="9376d-109">This cmdlet creates an **ASRProtectionProfile** object to use with other cmdlets.</span></span>

## <span data-ttu-id="9376d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9376d-110">EXAMPLES</span></span>

### <span data-ttu-id="9376d-111">Példa 1: védelmi profil létrehozása</span><span class="sxs-lookup"><span data-stu-id="9376d-111">Example 1: Create a protection profile</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -ReplicationProvider "HyperVReplica" -AllowReplicaDeletion -ApplicationConsistentSnapshotFrequencyInHours 1 -CompressionEnabled -RecoveryPoints 2 -ReplicationFrequencyInSeconds 30 -ReplicationMethod "Online" -ReplicationPort 8085 -ReplicationStartTime 1
Name                                     : 
ID                                       : 
ReplicationProvider                      : HyperVReplica
HyperVReplicaProviderSettingsObject      : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaProviderSettings
HyperVReplicaAzureProviderSettingsObject :
```

<span data-ttu-id="9376d-112">Ez a parancs egy védelmi profil objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9376d-112">This command creates a protection profile object.</span></span>

### <span data-ttu-id="9376d-113">2. példa: HyperVReplicaAzure-szolgáltató védelmi profiljának létrehozása</span><span class="sxs-lookup"><span data-stu-id="9376d-113">Example 2: Create a protection profile for HyperVReplicaAzure provider</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -Name "ProtectionProfile" -ReplicationProvider "HyperVReplicaAzure" -RecoveryAzureSubscription "cb53d0c3-bd59-4721-89bc-06916a9147ef" -RecoveryAzureStorageAccount "Contoso01" -ReplicationFrequencyInSeconds 30 -RecoveryPoints 1 -Force
Name                                     : ProtectionProfile
ID                                       : 
ReplicationProvider                      : HyperVReplicaAzure
HyperVReplicaProviderSettingsObject      : 
HyperVReplicaAzureProviderSettingsObject : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaAzureProviderSettings
```

<span data-ttu-id="9376d-114">Ez a parancs biztonsági profilt hoz létre egy HyperVReplicaAzure-szolgáltatónál.</span><span class="sxs-lookup"><span data-stu-id="9376d-114">This command creates a protection profile for a HyperVReplicaAzure provider.</span></span>

## <span data-ttu-id="9376d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9376d-115">PARAMETERS</span></span>

### <span data-ttu-id="9376d-116">-AllowReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="9376d-116">-AllowReplicaDeletion</span></span>
<span data-ttu-id="9376d-117">Azt jelzi, hogy a védelmi profil engedélyezi a replika entitások törlését.</span><span class="sxs-lookup"><span data-stu-id="9376d-117">Indicates that the protection profile enables deletion of replica entities.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9376d-118">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="9376d-118">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="9376d-119">Az alkalmazás konzisztens pillanatképei gyakoriságát adja meg órákban.</span><span class="sxs-lookup"><span data-stu-id="9376d-119">Specifies the frequency, in hours, for application consistent snapshots.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9376d-120">-Hitelesítés</span><span class="sxs-lookup"><span data-stu-id="9376d-120">-Authentication</span></span>
<span data-ttu-id="9376d-121">A használandó hitelesítés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9376d-121">Specifies the type of authentication to use.</span></span>
<span data-ttu-id="9376d-122">A paraméter elfogadható értékei a következők: tanúsítvány és Kerberos.</span><span class="sxs-lookup"><span data-stu-id="9376d-122">The acceptable values for this parameter are: Certificate and Kerberos.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9376d-123">-CompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="9376d-123">-CompressionEnabled</span></span>
<span data-ttu-id="9376d-124">Azt jelzi, hogy a védelmi profil lehetővé teszi a tömörítést.</span><span class="sxs-lookup"><span data-stu-id="9376d-124">Indicates that the protection profile enables compression.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9376d-125">-Force</span><span class="sxs-lookup"><span data-stu-id="9376d-125">-Force</span></span>
<span data-ttu-id="9376d-126">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="9376d-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9376d-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9376d-127">-Name</span></span>
<span data-ttu-id="9376d-128">A védelmi profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9376d-128">Specifies a name for the protection profile.</span></span>

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

### <span data-ttu-id="9376d-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="9376d-129">-Profile</span></span>
<span data-ttu-id="9376d-130">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="9376d-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9376d-131">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="9376d-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9376d-132">-RecoveryAzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9376d-132">-RecoveryAzureStorageAccount</span></span>
<span data-ttu-id="9376d-133">Annak az Azure-tárterület-fióknak a nevét adja meg, amelybe az Azure Replica entitást tárolni szeretné.</span><span class="sxs-lookup"><span data-stu-id="9376d-133">Specifies the name of an Azure Storage account on which to store the Azure replica entity.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9376d-134">-RecoveryAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="9376d-134">-RecoveryAzureSubscription</span></span>
<span data-ttu-id="9376d-135">A tárolási fiók Azure-előfizetésének AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9376d-135">Specifies the ID for an Azure Subscription for a storage account.</span></span>
<span data-ttu-id="9376d-136">Ez a paraméter arra a fiókra hivatkozik, amelyen az Azure Replica Entity áruházat tárolják.</span><span class="sxs-lookup"><span data-stu-id="9376d-136">This parameter refers to the account on which to store the Azure replica entity.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9376d-137">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="9376d-137">-RecoveryPoints</span></span>
<span data-ttu-id="9376d-138">Azt adja meg, hogy hány órát kell fenntartani a helyreállítási pontok számára.</span><span class="sxs-lookup"><span data-stu-id="9376d-138">Specifies the number of hours to retain recovery points.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9376d-139">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="9376d-139">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="9376d-140">A replikálás gyakorisági intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="9376d-140">Specifies the frequency interval, in seconds, for replication.</span></span> <span data-ttu-id="9376d-141">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="9376d-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9376d-142">30</span><span class="sxs-lookup"><span data-stu-id="9376d-142">30</span></span> 
- <span data-ttu-id="9376d-143">300</span><span class="sxs-lookup"><span data-stu-id="9376d-143">300</span></span> 
- <span data-ttu-id="9376d-144">900</span><span class="sxs-lookup"><span data-stu-id="9376d-144">900</span></span>

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

### <span data-ttu-id="9376d-145">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="9376d-145">-ReplicationMethod</span></span>
<span data-ttu-id="9376d-146">A replikációs módszert adja meg.</span><span class="sxs-lookup"><span data-stu-id="9376d-146">Specifies the replication method.</span></span> <span data-ttu-id="9376d-147">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="9376d-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9376d-148">Online.</span><span class="sxs-lookup"><span data-stu-id="9376d-148">Online.</span></span>
<span data-ttu-id="9376d-149">Hálózaton keresztüli replikáció</span><span class="sxs-lookup"><span data-stu-id="9376d-149">Replication over the network.</span></span>
- <span data-ttu-id="9376d-150">Offline.</span><span class="sxs-lookup"><span data-stu-id="9376d-150">Offline.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9376d-151">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="9376d-151">-ReplicationPort</span></span>
<span data-ttu-id="9376d-152">Annak a portnak a száma, amelyen a replikáció történik.</span><span class="sxs-lookup"><span data-stu-id="9376d-152">Specifies the number of the port on which the replication occurs.</span></span>

```yaml
Type: UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9376d-153">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="9376d-153">-ReplicationProvider</span></span>
<span data-ttu-id="9376d-154">A replikációs szolgáltató típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9376d-154">Specifies the type of replication provider.</span></span> <span data-ttu-id="9376d-155">A paraméter elfogadható értékei a következők: HyperVReplica és HyperVReplicaAzure.</span><span class="sxs-lookup"><span data-stu-id="9376d-155">The acceptable values for this parameter are: HyperVReplica and HyperVReplicaAzure.</span></span>

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

### <span data-ttu-id="9376d-156">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="9376d-156">-ReplicationStartTime</span></span>
<span data-ttu-id="9376d-157">A replikáció kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9376d-157">Specifies the start time of the replication.</span></span>
<span data-ttu-id="9376d-158">A feladat elkezdése után 24 órán belül adjon meg egy időpontot.</span><span class="sxs-lookup"><span data-stu-id="9376d-158">Specify a time within 24 hours after you start the job.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9376d-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9376d-159">CommonParameters</span></span>
<span data-ttu-id="9376d-160">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9376d-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9376d-161">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9376d-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9376d-162">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9376d-162">INPUTS</span></span>

## <span data-ttu-id="9376d-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9376d-163">OUTPUTS</span></span>

## <span data-ttu-id="9376d-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9376d-164">NOTES</span></span>

## <span data-ttu-id="9376d-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9376d-165">RELATED LINKS</span></span>

[<span data-ttu-id="9376d-166">Azure site Recovery Services-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="9376d-166">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


