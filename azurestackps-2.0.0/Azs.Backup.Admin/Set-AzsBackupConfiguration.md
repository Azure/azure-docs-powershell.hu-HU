---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/set-azsbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: c99e2c549cc865a5f7f9ad0d7c3252cbf6651e98
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844894"
---
# <span data-ttu-id="32a44-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="32a44-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="32a44-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="32a44-102">SYNOPSIS</span></span>
<span data-ttu-id="32a44-103">Biztonsági mentési hely frissítése</span><span class="sxs-lookup"><span data-stu-id="32a44-103">Update a backup location.</span></span>

## <span data-ttu-id="32a44-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="32a44-104">SYNTAX</span></span>

### <span data-ttu-id="32a44-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="32a44-105">UpdateExpanded (Default)</span></span>
```
Set-AzsBackupConfiguration [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-EncryptionCertPath <String>]
 [-IsBackupSchedulerEnabled] [-Password <SecureString>] [-Path <String>] [-Tag <Hashtable>]
 [-UserName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="32a44-106">Frissítés</span><span class="sxs-lookup"><span data-stu-id="32a44-106">Update</span></span>
```
Set-AzsBackupConfiguration -Backup <IBackupLocation> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="32a44-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="32a44-107">DESCRIPTION</span></span>
<span data-ttu-id="32a44-108">Biztonsági mentési hely frissítése</span><span class="sxs-lookup"><span data-stu-id="32a44-108">Update a backup location.</span></span>

## <span data-ttu-id="32a44-109">Példák</span><span class="sxs-lookup"><span data-stu-id="32a44-109">EXAMPLES</span></span>

### <span data-ttu-id="32a44-110">Példa 1: biztonsági másolat konfigurációjának beállítása</span><span class="sxs-lookup"><span data-stu-id="32a44-110">Example 1: Set backup configuration</span></span>
```powershell
PS C:\> Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionCertPath $encryptionCertPath

```

<span data-ttu-id="32a44-111">Állítsa be az Azure-halom biztonsági mentése konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="32a44-111">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="32a44-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="32a44-112">PARAMETERS</span></span>

### <span data-ttu-id="32a44-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32a44-113">-AsJob</span></span>
<span data-ttu-id="32a44-114">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="32a44-114">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="32a44-115">-Backup</span><span class="sxs-lookup"><span data-stu-id="32a44-115">-Backup</span></span>
<span data-ttu-id="32a44-116">Információ a biztonsági másolat helyéről.</span><span class="sxs-lookup"><span data-stu-id="32a44-116">Information about the backup location.</span></span>
<span data-ttu-id="32a44-117">A kivitelezéshez lásd: a megjegyzések szakasz a biztonsági mentési tulajdonságokhoz, és hozzon létre egy kivonatoló táblázatot.</span><span class="sxs-lookup"><span data-stu-id="32a44-117">To construct, see NOTES section for BACKUP properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="32a44-118">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="32a44-118">-BackupFrequencyInHours</span></span>
<span data-ttu-id="32a44-119">A Feladatütemező által biztonsági másolatot tartalmazó gyakoriság intervalluma órákban.</span><span class="sxs-lookup"><span data-stu-id="32a44-119">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="32a44-120">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="32a44-120">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="32a44-121">Az adatmegőrzési időszak napokban, a tárolási helyhez tartozó biztonsági másolatok esetében.</span><span class="sxs-lookup"><span data-stu-id="32a44-121">The retention period, in days, for backs in the storage location.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="32a44-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32a44-122">-DefaultProfile</span></span>
<span data-ttu-id="32a44-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="32a44-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="32a44-124">-EncryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="32a44-124">-EncryptionCertPath</span></span>
<span data-ttu-id="32a44-125">A titkosítási CERT-fájl elérési útja nyilvános kulccsal (. cer)</span><span class="sxs-lookup"><span data-stu-id="32a44-125">Path to the encryption cert file with public key (.cer).</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="32a44-126">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="32a44-126">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="32a44-127">True, ha a biztonságimásolat-készítő engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="32a44-127">True if the backup scheduler is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="32a44-128">-Hely</span><span class="sxs-lookup"><span data-stu-id="32a44-128">-Location</span></span>
<span data-ttu-id="32a44-129">A biztonsági másolat helyének neve.</span><span class="sxs-lookup"><span data-stu-id="32a44-129">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="32a44-130">-Várva</span><span class="sxs-lookup"><span data-stu-id="32a44-130">-NoWait</span></span>
<span data-ttu-id="32a44-131">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="32a44-131">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="32a44-132">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="32a44-132">-Password</span></span>
<span data-ttu-id="32a44-133">A hely eléréséhez használt jelszó.</span><span class="sxs-lookup"><span data-stu-id="32a44-133">Password to access the location.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="32a44-134">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="32a44-134">-Path</span></span>
<span data-ttu-id="32a44-135">A frissítési hely elérési útja</span><span class="sxs-lookup"><span data-stu-id="32a44-135">Path to the update location</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="32a44-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32a44-136">-ResourceGroupName</span></span>
<span data-ttu-id="32a44-137">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="32a44-137">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="32a44-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="32a44-138">-SubscriptionId</span></span>
<span data-ttu-id="32a44-139">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="32a44-139">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="32a44-140">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="32a44-140">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="32a44-141">-Címke</span><span class="sxs-lookup"><span data-stu-id="32a44-141">-Tag</span></span>
<span data-ttu-id="32a44-142">A kulcs érték párok listája</span><span class="sxs-lookup"><span data-stu-id="32a44-142">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="32a44-143">-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="32a44-143">-UserName</span></span>
<span data-ttu-id="32a44-144">A hely eléréséhez használt Felhasználónév.</span><span class="sxs-lookup"><span data-stu-id="32a44-144">Username to access the location.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="32a44-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="32a44-145">-Confirm</span></span>
<span data-ttu-id="32a44-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="32a44-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32a44-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32a44-147">-WhatIf</span></span>
<span data-ttu-id="32a44-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="32a44-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32a44-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="32a44-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32a44-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32a44-150">CommonParameters</span></span>
<span data-ttu-id="32a44-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="32a44-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32a44-152">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="32a44-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32a44-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="32a44-153">INPUTS</span></span>

### <span data-ttu-id="32a44-154">Microsoft. Azure. PowerShell. parancsmagok. BackupAdmin. modellek. Api20180901. IBackupLocation</span><span class="sxs-lookup"><span data-stu-id="32a44-154">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>

## <span data-ttu-id="32a44-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="32a44-155">OUTPUTS</span></span>

### <span data-ttu-id="32a44-156">Microsoft. Azure. PowerShell. parancsmagok. BackupAdmin. modellek. Api20180901. IBackupLocation</span><span class="sxs-lookup"><span data-stu-id="32a44-156">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>



## <span data-ttu-id="32a44-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="32a44-157">NOTES</span></span>

<span data-ttu-id="32a44-158">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="32a44-158">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="32a44-159">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="32a44-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="32a44-160">Biztonsági másolat <IBackupLocation> : információ a biztonsági másolat helyéről.</span><span class="sxs-lookup"><span data-stu-id="32a44-160">BACKUP <IBackupLocation>: Information about the backup location.</span></span>
  - <span data-ttu-id="32a44-161">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="32a44-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="32a44-162">`[Tag <IResourceTags>]`: A kulcsok érték párok listája.</span><span class="sxs-lookup"><span data-stu-id="32a44-162">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="32a44-163">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="32a44-163">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="32a44-164">`[BackupFrequencyInHours <Int32?>]`: A Feladatütemező által biztonsági másolatot tartalmazó gyakoriság (óra) intervalluma.</span><span class="sxs-lookup"><span data-stu-id="32a44-164">`[BackupFrequencyInHours <Int32?>]`: The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>
  - <span data-ttu-id="32a44-165">`[BackupRetentionPeriodInDays <Int32?>]`: Az adatmegőrzési időszak napokban, a tárolási helyről.</span><span class="sxs-lookup"><span data-stu-id="32a44-165">`[BackupRetentionPeriodInDays <Int32?>]`: The retention period, in days, for backs in the storage location.</span></span>
  - <span data-ttu-id="32a44-166">`[EncryptionCertBase64 <String>]`: A biztonsági másolat titkosítási tanúsítványának Base64 RAW-adatainak beállítása.</span><span class="sxs-lookup"><span data-stu-id="32a44-166">`[EncryptionCertBase64 <String>]`: The base64 raw data for the backup encryption certificate.</span></span>
  - <span data-ttu-id="32a44-167">`[IsBackupSchedulerEnabled <Boolean?>]`: Igaz, ha engedélyezve van a biztonsági másolat.</span><span class="sxs-lookup"><span data-stu-id="32a44-167">`[IsBackupSchedulerEnabled <Boolean?>]`: True if the backup scheduler is enabled.</span></span>
  - <span data-ttu-id="32a44-168">`[Password <String>]`: Jelszó a hely eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="32a44-168">`[Password <String>]`: Password to access the location.</span></span>
  - <span data-ttu-id="32a44-169">`[Path <String>]`: A frissítési hely elérési útja</span><span class="sxs-lookup"><span data-stu-id="32a44-169">`[Path <String>]`: Path to the update location</span></span>
  - <span data-ttu-id="32a44-170">`[UserName <String>]`: Felhasználónév a hely eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="32a44-170">`[UserName <String>]`: Username to access the location.</span></span>

## <span data-ttu-id="32a44-171">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="32a44-171">RELATED LINKS</span></span>

