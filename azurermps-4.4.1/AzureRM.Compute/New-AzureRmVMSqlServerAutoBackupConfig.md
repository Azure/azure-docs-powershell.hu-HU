---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
Module Name: Azure
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 2617ca54050f6a37fcc5714fe80e2f2d50e33e40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680608"
---
# <span data-ttu-id="4ad6a-101">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="4ad6a-101">New-AzureVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="4ad6a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4ad6a-102">SYNOPSIS</span></span>
<span data-ttu-id="4ad6a-103">Konfigurációs objektum létrehozása az SQL Server automatikus biztonsági mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-103">Creates a configuration object for SQL Server automatic backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ad6a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4ad6a-104">SYNTAX</span></span>

### <span data-ttu-id="4ad6a-105">StorageUriSqlServerAutoBackup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4ad6a-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>]
 [-BackupSystemDbs] [-BackupScheduleType <String>] [-FullBackupFrequency <String>]
 [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="4ad6a-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="4ad6a-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4ad6a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4ad6a-107">DESCRIPTION</span></span>
<span data-ttu-id="4ad6a-108">A **New-AzureVMSqlServerAutoBackupConfig** parancsmag létrehoz egy konfigurációs OBJEKTUMOT az SQL Server automatikus biztonsági mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-108">The **New-AzureVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="4ad6a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4ad6a-109">EXAMPLES</span></span>

### <span data-ttu-id="4ad6a-110">Példa 1: automatikus biztonsági másolat létrehozása a tárolási URI és a fiók kulccsal</span><span class="sxs-lookup"><span data-stu-id="4ad6a-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="4ad6a-111">A parancs a tárterület-azonosító és a fiók kulcs megadásával automatikusan biztonsági másolatot készít a konfigurációs objektumról.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="4ad6a-112">Az automatikus biztonsági mentés be van kapcsolva, és az automatikus biztonsági mentés 10 napig tart.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="4ad6a-113">A parancs az eredményt a $AutoBackupConfig változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="4ad6a-114">Ezt a konfigurációs elemet más parancsmagok, például az Set-AzureRmVMSqlServerExtension parancsmag esetében is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-114">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="4ad6a-115">2. példa: automatikus biztonságimásolat-konfiguráció létrehozása tárolási környezet használatával</span><span class="sxs-lookup"><span data-stu-id="4ad6a-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="4ad6a-116">Az első parancs létrehozza a tárolási környezetet, majd a $StorageContext változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="4ad6a-117">További információt az új AzureStorageContext című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-117">For more information, see New-AzureStorageContext.</span></span>

<span data-ttu-id="4ad6a-118">A második parancs az $StorageContext tárolási környezetének megadásával automatikusan biztonsági másolatot készít a konfigurációs objektumról.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="4ad6a-119">Az automatikus biztonsági mentés be van kapcsolva, és az automatikus biztonsági mentés 10 napig tart.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="4ad6a-120">3. példa: automatikus biztonsági másolat beállítása a tárolási környezettel a titkosítással és a jelszóval</span><span class="sxs-lookup"><span data-stu-id="4ad6a-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="4ad6a-121">Ezzel a paranccsal létrehozhatja és tárolhatja az automatikus biztonságimásolat-konfiguráció objektumát.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="4ad6a-122">A parancs az előző példában létrehozott tárterület-környezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="4ad6a-123">A parancs engedélyezi a titkosítást a jelszóval.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-123">The command enables encryption with password.</span></span>
<span data-ttu-id="4ad6a-124">A jelszó korábban biztonságos karakterláncként volt tárolva a $CertificatePassword változóban.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="4ad6a-125">Ha biztonságos karakterláncot szeretne létrehozni, használja az ConvertTo-SecureString parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="4ad6a-126">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4ad6a-126">PARAMETERS</span></span>

### <span data-ttu-id="4ad6a-127">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="4ad6a-127">-Enable</span></span>
<span data-ttu-id="4ad6a-128">Azt jelzi, hogy az SQL Server virtuális gép automatikus biztonsági másolata engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-128">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="4ad6a-129">Ha ezt a paramétert adja meg, akkor az automatikus biztonsági mentés az összes aktuális és új adatbázis biztonsági ütemezését állítja be.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-129">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="4ad6a-130">Ezzel frissíti a felügyelt biztonságimásolat-beállításokat az ütemezés követéséhez.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-130">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ad6a-131">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="4ad6a-131">-RetentionPeriodInDays</span></span>
<span data-ttu-id="4ad6a-132">Azt adja meg, hogy hány napig maradjon a biztonsági másolat.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-132">Specifies the number of days to retain a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ad6a-133">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="4ad6a-133">-EnableEncryption</span></span>
<span data-ttu-id="4ad6a-134">Azt jelzi, hogy ez a parancsmag engedélyezi a titkosítást.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-134">Indicates that this cmdlet enables encryption.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ad6a-135">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="4ad6a-135">-CertificatePassword</span></span>
<span data-ttu-id="4ad6a-136">Megadja azt a jelszót, amellyel titkosítható az SQL Server titkosított biztonsági mentéseit szolgáló tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-136">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ad6a-137">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="4ad6a-137">-StorageUri</span></span>
<span data-ttu-id="4ad6a-138">A blob-tároló fiók egységes erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-138">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ad6a-139">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="4ad6a-139">-StorageKey</span></span>
<span data-ttu-id="4ad6a-140">A blob-tároló fiók tárolási kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-140">Specifies the storage key of the blob storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ad6a-141">-Profil</span><span class="sxs-lookup"><span data-stu-id="4ad6a-141">-Profile</span></span>
<span data-ttu-id="4ad6a-142">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-142">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="4ad6a-143">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Utilities.Common.AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ad6a-144">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4ad6a-144">-InformationAction</span></span>
<span data-ttu-id="4ad6a-145">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="4ad6a-145">@{Text=}</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ad6a-146">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4ad6a-146">-InformationVariable</span></span>
<span data-ttu-id="4ad6a-147">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="4ad6a-147">@{Text=}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ad6a-148">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="4ad6a-148">-StorageContext</span></span>
<span data-ttu-id="4ad6a-149">Azt a tárterületet adja meg, amelyet a biztonsági másolatok tárolására fog használni.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-149">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="4ad6a-150">**AzureStorageContext** objektum beolvasásához használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-150">To obtain an **AzureStorageContext** object, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="4ad6a-151">Az alapértelmezett érték az SQL Server virtuális géphez társított tárolási fiók.</span><span class="sxs-lookup"><span data-stu-id="4ad6a-151">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ad6a-152">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="4ad6a-152">-BackupScheduleType</span></span>
<span data-ttu-id="4ad6a-153">Biztonságimásolat-ütemezés típusa, kézi vagy automatizált</span><span class="sxs-lookup"><span data-stu-id="4ad6a-153">Backup schedule type, manual or automated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ad6a-154">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="4ad6a-154">-BackupSystemDbs</span></span>
<span data-ttu-id="4ad6a-155">Biztonsági másolat rendszeradatbázisai</span><span class="sxs-lookup"><span data-stu-id="4ad6a-155">Backup system databases</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ad6a-156">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="4ad6a-156">-FullBackupFrequency</span></span>
<span data-ttu-id="4ad6a-157">SQL Server – teljes biztonsági másolat gyakorisága, naponta vagy hetente</span><span class="sxs-lookup"><span data-stu-id="4ad6a-157">Sql Server Full Backup frequency, daily or week</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ad6a-158">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="4ad6a-158">-FullBackupStartHour</span></span>
<span data-ttu-id="4ad6a-159">A nap órája (0-23), amikor az SQL Server teljes biztonsági másolatát meg kell kezdeni</span><span class="sxs-lookup"><span data-stu-id="4ad6a-159">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ad6a-160">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="4ad6a-160">-FullBackupWindowInHours</span></span>
<span data-ttu-id="4ad6a-161">Az SQL Server teljes biztonsági másolat ablaka órában</span><span class="sxs-lookup"><span data-stu-id="4ad6a-161">Sql Server Full Backup window in hours</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ad6a-162">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="4ad6a-162">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="4ad6a-163">SQL Server log Backup gyakorisága, 1-60 percenként</span><span class="sxs-lookup"><span data-stu-id="4ad6a-163">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ad6a-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ad6a-164">CommonParameters</span></span>
<span data-ttu-id="4ad6a-165">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4ad6a-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ad6a-166">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ad6a-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ad6a-167">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ad6a-167">INPUTS</span></span>

## <span data-ttu-id="4ad6a-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ad6a-168">OUTPUTS</span></span>

## <span data-ttu-id="4ad6a-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4ad6a-169">NOTES</span></span>

## <span data-ttu-id="4ad6a-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ad6a-170">RELATED LINKS</span></span>

[<span data-ttu-id="4ad6a-171">Új – AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="4ad6a-171">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="4ad6a-172">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="4ad6a-172">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


