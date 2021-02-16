---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 853D5585-2A92-4B65-BA8C-EC06BEE8C237
online version: ''
schema: 2.0.0
ms.openlocfilehash: d7681631d98f80def1076a04ab57f1774bad245c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403646"
---
# <span data-ttu-id="79b88-101">New-AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="79b88-101">New-AzureSiteRecoveryProtectionProfileObject</span></span>

## <span data-ttu-id="79b88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79b88-102">SYNOPSIS</span></span>
<span data-ttu-id="79b88-103">Létrehozza a Webhely-helyreállítás elleni védelem profilobjektumát.</span><span class="sxs-lookup"><span data-stu-id="79b88-103">Creates a Site Recovery protection profile object.</span></span>

## <span data-ttu-id="79b88-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="79b88-104">SYNTAX</span></span>

### <span data-ttu-id="79b88-105">EnterpriseToAzure (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="79b88-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 -RecoveryAzureSubscription <String> -RecoveryAzureStorageAccount <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="79b88-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="79b88-106">EnterpriseToEnterprise</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-CompressionEnabled] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-AllowReplicaDeletion] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="79b88-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="79b88-107">DESCRIPTION</span></span>
<span data-ttu-id="79b88-108">A **New-AzureSiteRecoveryProtectionProfileObject** parancsmag létrehoz egy Azure-webhely-helyreállítási profilobjektumot.</span><span class="sxs-lookup"><span data-stu-id="79b88-108">The **New-AzureSiteRecoveryProtectionProfileObject** cmdlet creates an Azure Site Recovery protection profile object.</span></span>
<span data-ttu-id="79b88-109">Ez a parancsmag létrehoz egy **ASRProtectionProfile** objektumot más parancsmagokkal való használatra.</span><span class="sxs-lookup"><span data-stu-id="79b88-109">This cmdlet creates an **ASRProtectionProfile** object to use with other cmdlets.</span></span>

## <span data-ttu-id="79b88-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="79b88-110">EXAMPLES</span></span>

### <span data-ttu-id="79b88-111">1. példa: Védelmi profil létrehozása</span><span class="sxs-lookup"><span data-stu-id="79b88-111">Example 1: Create a protection profile</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -ReplicationProvider "HyperVReplica" -AllowReplicaDeletion -ApplicationConsistentSnapshotFrequencyInHours 1 -CompressionEnabled -RecoveryPoints 2 -ReplicationFrequencyInSeconds 30 -ReplicationMethod "Online" -ReplicationPort 8085 -ReplicationStartTime 1
Name                                     : 
ID                                       : 
ReplicationProvider                      : HyperVReplica
HyperVReplicaProviderSettingsObject      : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaProviderSettings
HyperVReplicaAzureProviderSettingsObject :
```

<span data-ttu-id="79b88-112">Ez a parancs egy védelmi profilobjektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="79b88-112">This command creates a protection profile object.</span></span>

### <span data-ttu-id="79b88-113">2. példa: Védelmi profil létrehozása a HyperVReplicaAzure szolgáltatóhoz</span><span class="sxs-lookup"><span data-stu-id="79b88-113">Example 2: Create a protection profile for HyperVReplicaAzure provider</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -Name "ProtectionProfile" -ReplicationProvider "HyperVReplicaAzure" -RecoveryAzureSubscription "cb53d0c3-bd59-4721-89bc-06916a9147ef" -RecoveryAzureStorageAccount "Contoso01" -ReplicationFrequencyInSeconds 30 -RecoveryPoints 1 -Force
Name                                     : ProtectionProfile
ID                                       : 
ReplicationProvider                      : HyperVReplicaAzure
HyperVReplicaProviderSettingsObject      : 
HyperVReplicaAzureProviderSettingsObject : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaAzureProviderSettings
```

<span data-ttu-id="79b88-114">Ez a parancs egy védelmi profilt hoz létre a HyperVReplicaAzure szolgáltatóhoz.</span><span class="sxs-lookup"><span data-stu-id="79b88-114">This command creates a protection profile for a HyperVReplicaAzure provider.</span></span>

## <span data-ttu-id="79b88-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79b88-115">PARAMETERS</span></span>

### <span data-ttu-id="79b88-116">-AllowReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="79b88-116">-AllowReplicaDeletion</span></span>
<span data-ttu-id="79b88-117">Azt jelzi, hogy a védelmi profil lehetővé teszi a replika entitások törlését.</span><span class="sxs-lookup"><span data-stu-id="79b88-117">Indicates that the protection profile enables deletion of replica entities.</span></span>

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

### <span data-ttu-id="79b88-118">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="79b88-118">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="79b88-119">Az alkalmazás-konzisztens pillanatfelvételek gyakoriságát adja meg órákban.</span><span class="sxs-lookup"><span data-stu-id="79b88-119">Specifies the frequency, in hours, for application consistent snapshots.</span></span>

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

### <span data-ttu-id="79b88-120">-Authentication</span><span class="sxs-lookup"><span data-stu-id="79b88-120">-Authentication</span></span>
<span data-ttu-id="79b88-121">A használni használt hitelesítés típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="79b88-121">Specifies the type of authentication to use.</span></span>
<span data-ttu-id="79b88-122">A paraméter elfogadható értékei: Tanúsítvány és Kerberos.</span><span class="sxs-lookup"><span data-stu-id="79b88-122">The acceptable values for this parameter are: Certificate and Kerberos.</span></span>

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

### <span data-ttu-id="79b88-123">-CompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="79b88-123">-CompressionEnabled</span></span>
<span data-ttu-id="79b88-124">Azt jelzi, hogy a védelmi profil lehetővé teszi a tömörítést.</span><span class="sxs-lookup"><span data-stu-id="79b88-124">Indicates that the protection profile enables compression.</span></span>

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

### <span data-ttu-id="79b88-125">-Force</span><span class="sxs-lookup"><span data-stu-id="79b88-125">-Force</span></span>
<span data-ttu-id="79b88-126">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="79b88-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="79b88-127">-Name</span><span class="sxs-lookup"><span data-stu-id="79b88-127">-Name</span></span>
<span data-ttu-id="79b88-128">Megadja a védelmi profil nevét.</span><span class="sxs-lookup"><span data-stu-id="79b88-128">Specifies a name for the protection profile.</span></span>

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

### <span data-ttu-id="79b88-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="79b88-129">-Profile</span></span>
<span data-ttu-id="79b88-130">Azt az Azure-profilt adja meg, amelyből a parancsmag olvas.</span><span class="sxs-lookup"><span data-stu-id="79b88-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="79b88-131">Ha nem ad meg profilt, ez a parancsmag a helyi alapértelmezett profilból olvassa be.</span><span class="sxs-lookup"><span data-stu-id="79b88-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="79b88-132">-RecoveryAzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="79b88-132">-RecoveryAzureStorageAccount</span></span>
<span data-ttu-id="79b88-133">Annak az Azure Storage-fióknak a nevét adja meg, amelyen tárolni kell az Azure replika-entitást.</span><span class="sxs-lookup"><span data-stu-id="79b88-133">Specifies the name of an Azure Storage account on which to store the Azure replica entity.</span></span>

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

### <span data-ttu-id="79b88-134">-RecoveryAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="79b88-134">-RecoveryAzureSubscription</span></span>
<span data-ttu-id="79b88-135">Egy tárfiók Azure-előfizetésének azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="79b88-135">Specifies the ID for an Azure Subscription for a storage account.</span></span>
<span data-ttu-id="79b88-136">Ez a paraméter arra a fiókra hivatkozik, amelyen tárolni kell az Azure replika-entitást.</span><span class="sxs-lookup"><span data-stu-id="79b88-136">This parameter refers to the account on which to store the Azure replica entity.</span></span>

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

### <span data-ttu-id="79b88-137">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="79b88-137">-RecoveryPoints</span></span>
<span data-ttu-id="79b88-138">Azt adja meg, hogy hány órát kell megőriznie a helyreállítási pontoknak.</span><span class="sxs-lookup"><span data-stu-id="79b88-138">Specifies the number of hours to retain recovery points.</span></span>

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

### <span data-ttu-id="79b88-139">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="79b88-139">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="79b88-140">A replikáció gyakoriságát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="79b88-140">Specifies the frequency interval, in seconds, for replication.</span></span> <span data-ttu-id="79b88-141">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="79b88-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="79b88-142">30</span><span class="sxs-lookup"><span data-stu-id="79b88-142">30</span></span> 
- <span data-ttu-id="79b88-143">300</span><span class="sxs-lookup"><span data-stu-id="79b88-143">300</span></span> 
- <span data-ttu-id="79b88-144">900</span><span class="sxs-lookup"><span data-stu-id="79b88-144">900</span></span>

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

### <span data-ttu-id="79b88-145">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="79b88-145">-ReplicationMethod</span></span>
<span data-ttu-id="79b88-146">A replikációs módszer megadása.</span><span class="sxs-lookup"><span data-stu-id="79b88-146">Specifies the replication method.</span></span> <span data-ttu-id="79b88-147">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="79b88-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="79b88-148">Online.</span><span class="sxs-lookup"><span data-stu-id="79b88-148">Online.</span></span>
<span data-ttu-id="79b88-149">Replikáció a hálózaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="79b88-149">Replication over the network.</span></span>
- <span data-ttu-id="79b88-150">Offline.</span><span class="sxs-lookup"><span data-stu-id="79b88-150">Offline.</span></span>

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

### <span data-ttu-id="79b88-151">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="79b88-151">-ReplicationPort</span></span>
<span data-ttu-id="79b88-152">Annak a portnak a számát adja meg, amelyen a replikáció történik.</span><span class="sxs-lookup"><span data-stu-id="79b88-152">Specifies the number of the port on which the replication occurs.</span></span>

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

### <span data-ttu-id="79b88-153">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="79b88-153">-ReplicationProvider</span></span>
<span data-ttu-id="79b88-154">A replikációs szolgáltató típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="79b88-154">Specifies the type of replication provider.</span></span> <span data-ttu-id="79b88-155">A paraméter elfogadható értékei: HyperVReplica és HyperVReplicaAzure.</span><span class="sxs-lookup"><span data-stu-id="79b88-155">The acceptable values for this parameter are: HyperVReplica and HyperVReplicaAzure.</span></span>

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

### <span data-ttu-id="79b88-156">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="79b88-156">-ReplicationStartTime</span></span>
<span data-ttu-id="79b88-157">A replikáció kezdési idejét adja meg.</span><span class="sxs-lookup"><span data-stu-id="79b88-157">Specifies the start time of the replication.</span></span>
<span data-ttu-id="79b88-158">A feladat kezdését követő 24 órán belül adjon meg egy időt.</span><span class="sxs-lookup"><span data-stu-id="79b88-158">Specify a time within 24 hours after you start the job.</span></span>

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

### <span data-ttu-id="79b88-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79b88-159">CommonParameters</span></span>
<span data-ttu-id="79b88-160">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79b88-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79b88-161">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79b88-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79b88-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79b88-162">INPUTS</span></span>

## <span data-ttu-id="79b88-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79b88-163">OUTPUTS</span></span>

## <span data-ttu-id="79b88-164">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="79b88-164">NOTES</span></span>

## <span data-ttu-id="79b88-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79b88-165">RELATED LINKS</span></span>




