---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e7b6e8139f201a69684d4236a5e84e89f6607c5c
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93840131"
---
# <span data-ttu-id="876f4-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="876f4-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="876f4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="876f4-102">SYNOPSIS</span></span>
<span data-ttu-id="876f4-103">Állítsa be a biztonsági másolat konfigurációját a megadott helyre.</span><span class="sxs-lookup"><span data-stu-id="876f4-103">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="876f4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="876f4-104">SYNTAX</span></span>

### <span data-ttu-id="876f4-105">Update (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="876f4-105">Update (Default)</span></span>
```
Set-AzsBackupConfiguration [-ResourceGroupName <String>] [-Location <String>] [-Path <String>]
 [-Username <String>] [-Password <SecureString>] [-EncryptionKey <SecureString>]
 [-IsBackupSchedulerEnabled <Boolean>] [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>]
 [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="876f4-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="876f4-106">InputObject</span></span>
```
Set-AzsBackupConfiguration -InputObject <BackupLocation> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="876f4-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="876f4-107">ResourceId</span></span>
```
Set-AzsBackupConfiguration -ResourceId <String> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="876f4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="876f4-108">DESCRIPTION</span></span>
<span data-ttu-id="876f4-109">Állítsa be a biztonsági másolat konfigurációját a megadott helyre.</span><span class="sxs-lookup"><span data-stu-id="876f4-109">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="876f4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="876f4-110">EXAMPLES</span></span>

### <span data-ttu-id="876f4-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="876f4-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionKey $encryptionKey
```

<span data-ttu-id="876f4-112">Állítsa be az Azure-halom biztonsági mentése konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="876f4-112">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="876f4-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="876f4-113">PARAMETERS</span></span>

### <span data-ttu-id="876f4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="876f4-114">-AsJob</span></span>
<span data-ttu-id="876f4-115">Aszinkron módon futtathatja a feladatot, és visszaállíthatja a projekt objektumát.</span><span class="sxs-lookup"><span data-stu-id="876f4-115">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="876f4-116">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="876f4-116">-BackupFrequencyInHours</span></span>
<span data-ttu-id="876f4-117">A Feladatütemező által biztonsági másolatot tartalmazó gyakoriság intervalluma órákban.</span><span class="sxs-lookup"><span data-stu-id="876f4-117">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="876f4-118">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="876f4-118">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="876f4-119">Az adatmegőrzési időszak napokban, a tárolási hely biztonsági másolatai.</span><span class="sxs-lookup"><span data-stu-id="876f4-119">The retention period, in days, for backups in the storage location.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="876f4-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="876f4-120">-EncryptionKey</span></span>
<span data-ttu-id="876f4-121">A biztonsági másolatok titkosításához használt titkosítási kulcs.</span><span class="sxs-lookup"><span data-stu-id="876f4-121">Encryption key used to encrypt backups.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="876f4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="876f4-122">-InputObject</span></span>
<span data-ttu-id="876f4-123">A biztonságimásolat-hely konfigurációját a Get-AzsBackupConfiguration adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="876f4-123">Backup location configuration returned by Get-AzsBackupConfiguration.</span></span>

```yaml
Type: BackupLocation
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="876f4-124">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="876f4-124">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="876f4-125">Azt, hogy engedélyezve van-e a biztonsági másolat.</span><span class="sxs-lookup"><span data-stu-id="876f4-125">Whether the backup scheduler should be enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="876f4-126">-Hely</span><span class="sxs-lookup"><span data-stu-id="876f4-126">-Location</span></span>
<span data-ttu-id="876f4-127">A beállítandó hely.</span><span class="sxs-lookup"><span data-stu-id="876f4-127">Location to configure.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="876f4-128">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="876f4-128">-Password</span></span>
<span data-ttu-id="876f4-129">A biztonságimásolat-hely eléréséhez szükséges jelszó.</span><span class="sxs-lookup"><span data-stu-id="876f4-129">Password required to access backup location.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="876f4-130">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="876f4-130">-Path</span></span>
<span data-ttu-id="876f4-131">Az a hely, ahol a biztonsági másolatok lesznek tárolva.</span><span class="sxs-lookup"><span data-stu-id="876f4-131">Location where backups will be stored.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: BackupShare

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="876f4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="876f4-132">-ResourceGroupName</span></span>
<span data-ttu-id="876f4-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="876f4-133">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="876f4-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="876f4-134">-ResourceId</span></span>
<span data-ttu-id="876f4-135">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="876f4-135">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="876f4-136">-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="876f4-136">-Username</span></span>
<span data-ttu-id="876f4-137">A biztonságimásolat-hely eléréséhez szükséges Felhasználónév.</span><span class="sxs-lookup"><span data-stu-id="876f4-137">Username required to access backup location.</span></span>

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

### <span data-ttu-id="876f4-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="876f4-138">-Confirm</span></span>
<span data-ttu-id="876f4-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="876f4-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="876f4-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="876f4-140">-WhatIf</span></span>
<span data-ttu-id="876f4-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="876f4-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="876f4-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="876f4-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="876f4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="876f4-143">CommonParameters</span></span>
<span data-ttu-id="876f4-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="876f4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="876f4-145">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="876f4-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="876f4-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="876f4-146">INPUTS</span></span>

## <span data-ttu-id="876f4-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="876f4-147">OUTPUTS</span></span>

### <span data-ttu-id="876f4-148">Microsoft. AzureStack. Management. backup. admin. models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="876f4-148">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="876f4-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="876f4-149">NOTES</span></span>

## <span data-ttu-id="876f4-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="876f4-150">RELATED LINKS</span></span>

