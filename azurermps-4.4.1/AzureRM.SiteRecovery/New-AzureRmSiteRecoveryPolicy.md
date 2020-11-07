---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 85C543FE-BBC1-4A1B-9974-1D3BF520085C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: e876e1a7beeee19cd68ac629eb08d48356f98da8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680215"
---
# <span data-ttu-id="dc4fd-101">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="dc4fd-101">New-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="dc4fd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dc4fd-102">SYNOPSIS</span></span>
<span data-ttu-id="dc4fd-103">Webhely-helyreállítási replikációs házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="dc4fd-103">Creates a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc4fd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dc4fd-104">SYNTAX</span></span>

### <span data-ttu-id="dc4fd-105">EnterpriseToAzure (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dc4fd-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc4fd-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="dc4fd-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String> [-ReplicationMethod <String>]
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc4fd-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="dc4fd-107">DESCRIPTION</span></span>
<span data-ttu-id="dc4fd-108">A **New-AzureRmSiteRecoveryPolicy** parancsmag létrehoz egy Azure-webhely-helyreállítási replikációs házirendet.</span><span class="sxs-lookup"><span data-stu-id="dc4fd-108">The **New-AzureRmSiteRecoveryPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="dc4fd-109">A replikációs házirend segítségével megadhatja a replikációs beállításokat, például a replikációs gyakoriságot és a helyreállítási pontok számát.</span><span class="sxs-lookup"><span data-stu-id="dc4fd-109">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="dc4fd-110">Példák</span><span class="sxs-lookup"><span data-stu-id="dc4fd-110">EXAMPLES</span></span>

## <span data-ttu-id="dc4fd-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dc4fd-111">PARAMETERS</span></span>

### <span data-ttu-id="dc4fd-112">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="dc4fd-112">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="dc4fd-113">Az alkalmazás konzisztens pillanatképének gyakoriságát adja meg órákban.</span><span class="sxs-lookup"><span data-stu-id="dc4fd-113">Specifies the frequency of the application consistent snapshot in hours.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc4fd-114">-Hitelesítés</span><span class="sxs-lookup"><span data-stu-id="dc4fd-114">-Authentication</span></span>
<span data-ttu-id="dc4fd-115">A használt hitelesítés típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc4fd-115">Specifies the type of authentication used.</span></span>
<span data-ttu-id="dc4fd-116">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="dc4fd-116">Valid values are:</span></span>

- <span data-ttu-id="dc4fd-117">Tanúsítvány</span><span class="sxs-lookup"><span data-stu-id="dc4fd-117">Certificate</span></span>
-  <span data-ttu-id="dc4fd-118">Kerberos</span><span class="sxs-lookup"><span data-stu-id="dc4fd-118">Kerberos</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc4fd-119">-Tömörítés</span><span class="sxs-lookup"><span data-stu-id="dc4fd-119">-Compression</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc4fd-120">-Titkosítás</span><span class="sxs-lookup"><span data-stu-id="dc4fd-120">-Encryption</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc4fd-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dc4fd-121">-Name</span></span>
<span data-ttu-id="dc4fd-122">Rövid nevet ad meg, amely azonosítja a webhely-helyreállítási replikációs házirendet.</span><span class="sxs-lookup"><span data-stu-id="dc4fd-122">Specifies a friendly name which identifies the Site Recovery replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc4fd-123">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="dc4fd-123">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="dc4fd-124">A replikációs cél Azure Storage Account ID azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc4fd-124">Specifies the Azure storage account ID of the replication target.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc4fd-125">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="dc4fd-125">-RecoveryPoints</span></span>
<span data-ttu-id="dc4fd-126">Azt adja meg, hogy hány órát kell fenntartani a helyreállítási pontok számára.</span><span class="sxs-lookup"><span data-stu-id="dc4fd-126">Specifies the number of hours to retain recovery points.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc4fd-127">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="dc4fd-127">-ReplicaDeletion</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc4fd-128">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="dc4fd-128">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="dc4fd-129">A replikációs gyakoriság másodpercben megadott intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc4fd-129">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="dc4fd-130">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="dc4fd-130">Valid values are:</span></span>

- <span data-ttu-id="dc4fd-131">30</span><span class="sxs-lookup"><span data-stu-id="dc4fd-131">30</span></span>
- <span data-ttu-id="dc4fd-132">300</span><span class="sxs-lookup"><span data-stu-id="dc4fd-132">300</span></span>
- <span data-ttu-id="dc4fd-133">900</span><span class="sxs-lookup"><span data-stu-id="dc4fd-133">900</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc4fd-134">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="dc4fd-134">-ReplicationMethod</span></span>
<span data-ttu-id="dc4fd-135">A replikációs módszert adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc4fd-135">Specifies the replication method.</span></span>
<span data-ttu-id="dc4fd-136">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="dc4fd-136">Valid values are:</span></span>

- <span data-ttu-id="dc4fd-137">Online</span><span class="sxs-lookup"><span data-stu-id="dc4fd-137">Online</span></span>
- <span data-ttu-id="dc4fd-138">Offline</span><span class="sxs-lookup"><span data-stu-id="dc4fd-138">Offline</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc4fd-139">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="dc4fd-139">-ReplicationPort</span></span>
<span data-ttu-id="dc4fd-140">A replikációhoz használt portot adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc4fd-140">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc4fd-141">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="dc4fd-141">-ReplicationProvider</span></span>
<span data-ttu-id="dc4fd-142">A replikációs szolgáltatót adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc4fd-142">Specifies the replication provider.</span></span>
<span data-ttu-id="dc4fd-143">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="dc4fd-143">Valid values are:</span></span>

- <span data-ttu-id="dc4fd-144">HyperVReplica2012R2</span><span class="sxs-lookup"><span data-stu-id="dc4fd-144">HyperVReplica2012R2</span></span>
- <span data-ttu-id="dc4fd-145">HyperVReplica2012</span><span class="sxs-lookup"><span data-stu-id="dc4fd-145">HyperVReplica2012</span></span>
- <span data-ttu-id="dc4fd-146">HyperVReplicaAzure</span><span class="sxs-lookup"><span data-stu-id="dc4fd-146">HyperVReplicaAzure</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc4fd-147">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="dc4fd-147">-ReplicationStartTime</span></span>
<span data-ttu-id="dc4fd-148">A replikációs kezdési időpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc4fd-148">Specifies the replication start time.</span></span>
<span data-ttu-id="dc4fd-149">A feladat elejétől legkésőbb 24 óráig kell szerepelnie.</span><span class="sxs-lookup"><span data-stu-id="dc4fd-149">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc4fd-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc4fd-150">-DefaultProfile</span></span>
<span data-ttu-id="dc4fd-151">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dc4fd-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc4fd-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc4fd-152">CommonParameters</span></span>
<span data-ttu-id="dc4fd-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dc4fd-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc4fd-154">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc4fd-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc4fd-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc4fd-155">INPUTS</span></span>

## <span data-ttu-id="dc4fd-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc4fd-156">OUTPUTS</span></span>

## <span data-ttu-id="dc4fd-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dc4fd-157">NOTES</span></span>

## <span data-ttu-id="dc4fd-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dc4fd-158">RELATED LINKS</span></span>

[<span data-ttu-id="dc4fd-159">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="dc4fd-159">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="dc4fd-160">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="dc4fd-160">Remove-AzureRmSiteRecoveryPolicy</span></span>](./Remove-AzureRmSiteRecoveryPolicy.md)
