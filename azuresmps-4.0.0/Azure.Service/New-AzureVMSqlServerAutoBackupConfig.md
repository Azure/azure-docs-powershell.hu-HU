---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 55E097F4-1F49-4196-9A8B-949FD5D9108A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4035487fa0363e6a7802966d9bc6422429723d94
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016199"
---
# <span data-ttu-id="e1ab6-101">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="e1ab6-101">New-AzureVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="e1ab6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e1ab6-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ab6-103">Konfigurációs objektum létrehozása az SQL Server automatikus biztonsági mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="e1ab6-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="e1ab6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e1ab6-104">SYNTAX</span></span>

### <span data-ttu-id="e1ab6-105">StorageUriSqlServerAutoBackup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e1ab6-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>]
 [-BackupSystemDbs] [-BackupScheduleType <String>] [-FullBackupFrequency <String>]
 [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1ab6-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="e1ab6-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageContext] <AzureStorageContext>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e1ab6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e1ab6-107">DESCRIPTION</span></span>
<span data-ttu-id="e1ab6-108">A **New-AzureVMSqlServerAutoBackupConfig** parancsmag létrehoz egy konfigurációs OBJEKTUMOT az SQL Server automatikus biztonsági mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="e1ab6-108">The **New-AzureVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="e1ab6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e1ab6-109">EXAMPLES</span></span>

### <span data-ttu-id="e1ab6-110">Példa 1: automatikus biztonsági mentési konfiguráció létrehozása a tárolási URI és a fiók kulccsal</span><span class="sxs-lookup"><span data-stu-id="e1ab6-110">Example 1: Create an auto-backup configuration using storage URI and account key</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="e1ab6-111">Ez a parancs a tárterület URL-címének és a fiók kulcsának megadásával automatikus biztonsági másolatot hoz létre a konfigurációs objektumról.</span><span class="sxs-lookup"><span data-stu-id="e1ab6-111">This command creates an auto-backup configuration object by specifying storage URL and account key.</span></span>

### <span data-ttu-id="e1ab6-112">2. példa: automatikus biztonsági mentési konfiguráció létrehozása a tárolási környezettel</span><span class="sxs-lookup"><span data-stu-id="e1ab6-112">Example 2: Create an auto-backup configuration using storage context</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="e1ab6-113">A parancs a tárolási környezet megadásával automatikus biztonsági másolatot hoz létre a konfigurációs objektumról.</span><span class="sxs-lookup"><span data-stu-id="e1ab6-113">This command creates an auto-backup configuration object by specifying storage context.</span></span>

### <span data-ttu-id="e1ab6-114">3. példa: automatikus biztonsági mentési konfiguráció létrehozása tárolási környezettel a titkosítás és a jelszó használatával</span><span class="sxs-lookup"><span data-stu-id="e1ab6-114">Example 3: Create an auto-backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertPasswd
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="e1ab6-115">Ezzel a paranccsal automatikus biztonsági mentési objektumot hozhat létre a tárolási környezet megadásával és a titkosítás engedélyezésével a jelszó beállítással.</span><span class="sxs-lookup"><span data-stu-id="e1ab6-115">This command creates an auto-backup configuration object by specifying Storage context and enabling encryption option with password.</span></span>
<span data-ttu-id="e1ab6-116">A certificatepassword ist a $CertPasswd nevű változóban tárolják.</span><span class="sxs-lookup"><span data-stu-id="e1ab6-116">The certificatepassword ist stored in the variable named $CertPasswd.</span></span>

## <span data-ttu-id="e1ab6-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e1ab6-117">PARAMETERS</span></span>

### <span data-ttu-id="e1ab6-118">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="e1ab6-118">-BackupScheduleType</span></span>
<span data-ttu-id="e1ab6-119">Biztonságimásolat-ütemezés típusa, kézi vagy automatizált</span><span class="sxs-lookup"><span data-stu-id="e1ab6-119">Backup schedule type, manual or automated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ab6-120">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="e1ab6-120">-BackupSystemDbs</span></span>
<span data-ttu-id="e1ab6-121">Biztonsági másolat rendszeradatbázisai</span><span class="sxs-lookup"><span data-stu-id="e1ab6-121">Backup system databases</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ab6-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="e1ab6-122">-CertificatePassword</span></span>
<span data-ttu-id="e1ab6-123">Megadja azt a jelszót, amellyel titkosítható az SQL Server titkosított biztonsági mentéseit szolgáló tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="e1ab6-123">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ab6-124">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="e1ab6-124">-Enable</span></span>
<span data-ttu-id="e1ab6-125">Azt jelzi, hogy az SQL Server virtuális gép automatikus biztonsági másolata engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="e1ab6-125">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="e1ab6-126">Ha ezt a paramétert használja, az automatikus biztonsági mentés az összes aktuális és új adatbázis biztonsági ütemezését állítja be.</span><span class="sxs-lookup"><span data-stu-id="e1ab6-126">If you use this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="e1ab6-127">Ezzel frissíti a felügyelt biztonságimásolat-beállításokat az ütemezés követéséhez.</span><span class="sxs-lookup"><span data-stu-id="e1ab6-127">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ab6-128">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="e1ab6-128">-EnableEncryption</span></span>
<span data-ttu-id="e1ab6-129">Azt jelzi, hogy a titkosítás engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="e1ab6-129">Indicates that encryption is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ab6-130">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="e1ab6-130">-FullBackupFrequency</span></span>
<span data-ttu-id="e1ab6-131">SQL Server – teljes biztonsági másolat gyakorisága, naponta vagy hetente</span><span class="sxs-lookup"><span data-stu-id="e1ab6-131">Sql Server Full Backup frequency, daily or week</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ab6-132">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="e1ab6-132">-FullBackupStartHour</span></span>
<span data-ttu-id="e1ab6-133">A nap órája (0-23), amikor az SQL Server teljes biztonsági másolatát meg kell kezdeni</span><span class="sxs-lookup"><span data-stu-id="e1ab6-133">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ab6-134">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="e1ab6-134">-FullBackupWindowInHours</span></span>
<span data-ttu-id="e1ab6-135">Az SQL Server teljes biztonsági másolat ablaka órában</span><span class="sxs-lookup"><span data-stu-id="e1ab6-135">Sql Server Full Backup window in hours</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ab6-136">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e1ab6-136">-InformationAction</span></span>
<span data-ttu-id="e1ab6-137">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="e1ab6-137">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e1ab6-138">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e1ab6-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e1ab6-139">Folytassa</span><span class="sxs-lookup"><span data-stu-id="e1ab6-139">Continue</span></span>
- <span data-ttu-id="e1ab6-140">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="e1ab6-140">Ignore</span></span>
- <span data-ttu-id="e1ab6-141">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="e1ab6-141">Inquire</span></span>
- <span data-ttu-id="e1ab6-142">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e1ab6-142">SilentlyContinue</span></span>
- <span data-ttu-id="e1ab6-143">állj</span><span class="sxs-lookup"><span data-stu-id="e1ab6-143">Stop</span></span>
- <span data-ttu-id="e1ab6-144">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="e1ab6-144">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ab6-145">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e1ab6-145">-InformationVariable</span></span>
<span data-ttu-id="e1ab6-146">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="e1ab6-146">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ab6-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="e1ab6-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="e1ab6-148">SQL Server log Backup gyakorisága, 1-60 percenként</span><span class="sxs-lookup"><span data-stu-id="e1ab6-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ab6-149">-Profil</span><span class="sxs-lookup"><span data-stu-id="e1ab6-149">-Profile</span></span>
<span data-ttu-id="e1ab6-150">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="e1ab6-150">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e1ab6-151">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="e1ab6-151">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e1ab6-152">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="e1ab6-152">-RetentionPeriodInDays</span></span>
<span data-ttu-id="e1ab6-153">Az adatmegőrzési időszak hosszát adja meg napokban.</span><span class="sxs-lookup"><span data-stu-id="e1ab6-153">Specifies the length of the retention period in days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ab6-154">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="e1ab6-154">-StorageContext</span></span>
<span data-ttu-id="e1ab6-155">A biztonsági másolatok tárolásához használandó tárterületet adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1ab6-155">Specifies the storage account to be used to store backups.</span></span>
<span data-ttu-id="e1ab6-156">Az alapértelmezett érték az SQL Server virtuális géphez társított tárolási fiók.</span><span class="sxs-lookup"><span data-stu-id="e1ab6-156">Default is the storage account associated with the SQL Server virtual machine.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ab6-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="e1ab6-157">-StorageKey</span></span>
<span data-ttu-id="e1ab6-158">A blob-tároló fiók tárolási kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1ab6-158">Specifies the storage key of the blob storage account.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ab6-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="e1ab6-159">-StorageUri</span></span>
<span data-ttu-id="e1ab6-160">A blob-tároló fiók URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1ab6-160">Specifies a URI to the blob storage account.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ab6-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ab6-161">CommonParameters</span></span>
<span data-ttu-id="e1ab6-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e1ab6-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ab6-163">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1ab6-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ab6-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1ab6-164">INPUTS</span></span>

## <span data-ttu-id="e1ab6-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1ab6-165">OUTPUTS</span></span>

## <span data-ttu-id="e1ab6-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e1ab6-166">NOTES</span></span>

## <span data-ttu-id="e1ab6-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1ab6-167">RELATED LINKS</span></span>

[<span data-ttu-id="e1ab6-168">Új – AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="e1ab6-168">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)


