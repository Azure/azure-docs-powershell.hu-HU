---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd5f27a942a33082b9488f74cac2779107f7371f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93840078"
---
# <span data-ttu-id="6e63e-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e63e-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="6e63e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6e63e-102">SYNOPSIS</span></span>
<span data-ttu-id="6e63e-103">Állítsa be a biztonsági másolat konfigurációját a megadott helyre.</span><span class="sxs-lookup"><span data-stu-id="6e63e-103">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="6e63e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6e63e-104">SYNTAX</span></span>

### <span data-ttu-id="6e63e-105">Update (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6e63e-105">Update (Default)</span></span>
```
Set-AzsBackupConfiguration [-ResourceGroupName <String>] [-Location <String>] [-Path <String>]
 [-Username <String>] [-Password <SecureString>] [-EncryptionCertPath <String>]
 [-IsBackupSchedulerEnabled <Boolean>] [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>]
 [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e63e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6e63e-106">InputObject</span></span>
```
Set-AzsBackupConfiguration -InputObject <BackupLocation> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionCertPath <String>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e63e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e63e-107">ResourceId</span></span>
```
Set-AzsBackupConfiguration -ResourceId <String> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionCertPath <String>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6e63e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6e63e-108">DESCRIPTION</span></span>
<span data-ttu-id="6e63e-109">Állítsa be a biztonsági másolat konfigurációját a megadott helyre.</span><span class="sxs-lookup"><span data-stu-id="6e63e-109">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="6e63e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6e63e-110">EXAMPLES</span></span>

### <span data-ttu-id="6e63e-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="6e63e-111">EXAMPLE 1</span></span>
```
Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionCertPath $encryptionCertPath
```

<span data-ttu-id="6e63e-112">Állítsa be az Azure-halom biztonsági mentése konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="6e63e-112">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="6e63e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6e63e-113">PARAMETERS</span></span>

### <span data-ttu-id="6e63e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e63e-114">-AsJob</span></span>
<span data-ttu-id="6e63e-115">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="6e63e-115">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e63e-116">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="6e63e-116">-BackupFrequencyInHours</span></span>
<span data-ttu-id="6e63e-117">A Feladatütemező által biztonsági másolatot tartalmazó gyakoriság intervalluma órákban.</span><span class="sxs-lookup"><span data-stu-id="6e63e-117">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e63e-118">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="6e63e-118">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="6e63e-119">Az adatmegőrzési időszak napokban, a tárolási hely biztonsági másolatai.</span><span class="sxs-lookup"><span data-stu-id="6e63e-119">The retention period, in days, for backups in the storage location.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e63e-120">-EncryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="6e63e-120">-EncryptionCertPath</span></span>
<span data-ttu-id="6e63e-121">A titkosítási CERT-fájl elérési útja nyilvános kulccsal (. cer)</span><span class="sxs-lookup"><span data-stu-id="6e63e-121">Path to the encryption cert file with public key (.cer).</span></span>

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

### <span data-ttu-id="6e63e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e63e-122">-InputObject</span></span>
<span data-ttu-id="6e63e-123">A biztonságimásolat-hely konfigurációját a Get-AzsBackupConfiguration adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="6e63e-123">Backup location configuration returned by Get-AzsBackupConfiguration.</span></span>

```yaml
Type: Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e63e-124">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="6e63e-124">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="6e63e-125">Azt, hogy engedélyezve van-e a biztonsági másolat.</span><span class="sxs-lookup"><span data-stu-id="6e63e-125">Whether the backup scheduler should be enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e63e-126">-Hely</span><span class="sxs-lookup"><span data-stu-id="6e63e-126">-Location</span></span>
<span data-ttu-id="6e63e-127">A beállítandó hely.</span><span class="sxs-lookup"><span data-stu-id="6e63e-127">Location to configure.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e63e-128">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="6e63e-128">-Password</span></span>
<span data-ttu-id="6e63e-129">A biztonságimásolat-hely eléréséhez szükséges jelszó.</span><span class="sxs-lookup"><span data-stu-id="6e63e-129">Password required to access backup location.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e63e-130">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="6e63e-130">-Path</span></span>
<span data-ttu-id="6e63e-131">Az a hely, ahol a biztonsági másolatok lesznek tárolva.</span><span class="sxs-lookup"><span data-stu-id="6e63e-131">Location where backups will be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupShare

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e63e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e63e-132">-ResourceGroupName</span></span>
<span data-ttu-id="6e63e-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6e63e-133">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e63e-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e63e-134">-ResourceId</span></span>
<span data-ttu-id="6e63e-135">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="6e63e-135">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e63e-136">-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="6e63e-136">-Username</span></span>
<span data-ttu-id="6e63e-137">A biztonságimásolat-hely eléréséhez szükséges Felhasználónév.</span><span class="sxs-lookup"><span data-stu-id="6e63e-137">Username required to access backup location.</span></span>

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

### <span data-ttu-id="6e63e-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6e63e-138">-Confirm</span></span>
<span data-ttu-id="6e63e-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6e63e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e63e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e63e-140">-WhatIf</span></span>
<span data-ttu-id="6e63e-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6e63e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e63e-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6e63e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e63e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e63e-143">CommonParameters</span></span>
<span data-ttu-id="6e63e-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6e63e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e63e-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e63e-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e63e-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e63e-146">INPUTS</span></span>

## <span data-ttu-id="6e63e-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e63e-147">OUTPUTS</span></span>

### <span data-ttu-id="6e63e-148">Microsoft. AzureStack. Management. backup. admin. models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="6e63e-148">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="6e63e-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6e63e-149">NOTES</span></span>

## <span data-ttu-id="6e63e-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e63e-150">RELATED LINKS</span></span>
