---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 15f26b611f90f8211e8f49c45c583d8953c028a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492375"
---
# <span data-ttu-id="a4692-101">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="a4692-101">New-AzureVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="a4692-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4692-102">SYNOPSIS</span></span>
<span data-ttu-id="a4692-103">Konfigurációs objektum létrehozása az SQL Server automatikus biztonsági mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="a4692-103">Creates a configuration object for SQL Server automatic backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4692-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4692-104">SYNTAX</span></span>

### <span data-ttu-id="a4692-105">StorageUriSqlServerAutoBackup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a4692-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a4692-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="a4692-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageContext] <AzureStorageContext>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="a4692-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4692-107">DESCRIPTION</span></span>
<span data-ttu-id="a4692-108">A **New-AzureVMSqlServerAutoBackupConfig** parancsmag létrehoz egy konfigurációs OBJEKTUMOT az SQL Server automatikus biztonsági mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="a4692-108">The **New-AzureVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="a4692-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a4692-109">EXAMPLES</span></span>

### <span data-ttu-id="a4692-110">Példa 1: automatikus biztonsági másolat létrehozása a tárolási URI és a fiók kulccsal</span><span class="sxs-lookup"><span data-stu-id="a4692-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="a4692-111">A parancs a tárterület-azonosító és a fiók kulcs megadásával automatikusan biztonsági másolatot készít a konfigurációs objektumról.</span><span class="sxs-lookup"><span data-stu-id="a4692-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="a4692-112">Az automatikus biztonsági mentés be van kapcsolva, és az automatikus biztonsági mentés 10 napig tart.</span><span class="sxs-lookup"><span data-stu-id="a4692-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="a4692-113">A parancs az eredményt a $AutoBackupConfig változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a4692-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="a4692-114">Ezt a konfigurációs elemet más parancsmagok, például az Set-AzureRmVMSqlServerExtension parancsmag esetében is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="a4692-114">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="a4692-115">2. példa: automatikus biztonságimásolat-konfiguráció létrehozása tárolási környezet használatával</span><span class="sxs-lookup"><span data-stu-id="a4692-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="a4692-116">Az első parancs létrehozza a tárolási környezetet, majd a $StorageContext változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a4692-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="a4692-117">További információt az új AzureStorageContext című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a4692-117">For more information, see New-AzureStorageContext.</span></span>

<span data-ttu-id="a4692-118">A második parancs az $StorageContext tárolási környezetének megadásával automatikusan biztonsági másolatot készít a konfigurációs objektumról.</span><span class="sxs-lookup"><span data-stu-id="a4692-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="a4692-119">Az automatikus biztonsági mentés be van kapcsolva, és az automatikus biztonsági mentés 10 napig tart.</span><span class="sxs-lookup"><span data-stu-id="a4692-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="a4692-120">3. példa: automatikus biztonsági másolat beállítása a tárolási környezettel a titkosítással és a jelszóval</span><span class="sxs-lookup"><span data-stu-id="a4692-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="a4692-121">Ezzel a paranccsal létrehozhatja és tárolhatja az automatikus biztonságimásolat-konfiguráció objektumát.</span><span class="sxs-lookup"><span data-stu-id="a4692-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="a4692-122">A parancs az előző példában létrehozott tárterület-környezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4692-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="a4692-123">A parancs engedélyezi a titkosítást a jelszóval.</span><span class="sxs-lookup"><span data-stu-id="a4692-123">The command enables encryption with password.</span></span>
<span data-ttu-id="a4692-124">A jelszó korábban biztonságos karakterláncként volt tárolva a $CertificatePassword változóban.</span><span class="sxs-lookup"><span data-stu-id="a4692-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="a4692-125">Ha biztonságos karakterláncot szeretne létrehozni, használja az ConvertTo-SecureString parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a4692-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="a4692-126">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4692-126">PARAMETERS</span></span>

### <span data-ttu-id="a4692-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="a4692-127">-BackupScheduleType</span></span>
<span data-ttu-id="a4692-128">Biztonságimásolat-ütemezés típusa, kézi vagy automatizált</span><span class="sxs-lookup"><span data-stu-id="a4692-128">Backup schedule type, manual or automated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Manual, Automated

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4692-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="a4692-129">-BackupSystemDbs</span></span>
<span data-ttu-id="a4692-130">Biztonsági másolat rendszeradatbázisai</span><span class="sxs-lookup"><span data-stu-id="a4692-130">Backup system databases</span></span>

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

### <span data-ttu-id="a4692-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="a4692-131">-CertificatePassword</span></span>
<span data-ttu-id="a4692-132">Megadja azt a jelszót, amellyel titkosítható az SQL Server titkosított biztonsági mentéseit szolgáló tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="a4692-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4692-133">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="a4692-133">-Enable</span></span>
<span data-ttu-id="a4692-134">Azt jelzi, hogy az SQL Server virtuális gép automatikus biztonsági másolata engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="a4692-134">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="a4692-135">Ha ezt a paramétert adja meg, akkor az automatikus biztonsági mentés az összes aktuális és új adatbázis biztonsági ütemezését állítja be.</span><span class="sxs-lookup"><span data-stu-id="a4692-135">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="a4692-136">Ezzel frissíti a felügyelt biztonságimásolat-beállításokat az ütemezés követéséhez.</span><span class="sxs-lookup"><span data-stu-id="a4692-136">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4692-137">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="a4692-137">-EnableEncryption</span></span>
<span data-ttu-id="a4692-138">Azt jelzi, hogy ez a parancsmag engedélyezi a titkosítást.</span><span class="sxs-lookup"><span data-stu-id="a4692-138">Indicates that this cmdlet enables encryption.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4692-139">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="a4692-139">-FullBackupFrequency</span></span>
<span data-ttu-id="a4692-140">SQL Server – teljes biztonsági mentés gyakorisága, naponta vagy hetente</span><span class="sxs-lookup"><span data-stu-id="a4692-140">Sql Server Full Backup frequency, daily or weekly</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Daily, Weekly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4692-141">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="a4692-141">-FullBackupStartHour</span></span>
<span data-ttu-id="a4692-142">A nap órája (0-23), amikor az SQL Server teljes biztonsági másolatát meg kell kezdeni</span><span class="sxs-lookup"><span data-stu-id="a4692-142">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="a4692-143">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="a4692-143">-FullBackupWindowInHours</span></span>
<span data-ttu-id="a4692-144">Az SQL Server teljes biztonsági másolat ablaka órában</span><span class="sxs-lookup"><span data-stu-id="a4692-144">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="a4692-145">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="a4692-145">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="a4692-146">SQL Server log Backup gyakorisága, 1-60 percenként</span><span class="sxs-lookup"><span data-stu-id="a4692-146">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="a4692-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4692-147">-ResourceGroupName</span></span>
<span data-ttu-id="a4692-148">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4692-148">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4692-149">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="a4692-149">-RetentionPeriodInDays</span></span>
<span data-ttu-id="a4692-150">Azt adja meg, hogy hány napig maradjon a biztonsági másolat.</span><span class="sxs-lookup"><span data-stu-id="a4692-150">Specifies the number of days to retain a backup.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4692-151">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="a4692-151">-StorageContext</span></span>
<span data-ttu-id="a4692-152">Azt a tárterületet adja meg, amelyet a biztonsági másolatok tárolására fog használni.</span><span class="sxs-lookup"><span data-stu-id="a4692-152">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="a4692-153">**AzureStorageContext** objektum beolvasásához használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a4692-153">To obtain an **AzureStorageContext** object, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="a4692-154">Az alapértelmezett érték az SQL Server virtuális géphez társított tárolási fiók.</span><span class="sxs-lookup"><span data-stu-id="a4692-154">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4692-155">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="a4692-155">-StorageKey</span></span>
<span data-ttu-id="a4692-156">A blob-tároló fiók tárolási kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4692-156">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="a4692-157">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="a4692-157">-StorageUri</span></span>
<span data-ttu-id="a4692-158">A blob-tároló fiók egységes erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4692-158">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="a4692-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4692-159">CommonParameters</span></span>
<span data-ttu-id="a4692-160">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a4692-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4692-161">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4692-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4692-162">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4692-162">INPUTS</span></span>

### <span data-ttu-id="a4692-163">Nincs</span><span class="sxs-lookup"><span data-stu-id="a4692-163">None</span></span>
<span data-ttu-id="a4692-164">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="a4692-164">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a4692-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4692-165">OUTPUTS</span></span>

## <span data-ttu-id="a4692-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4692-166">NOTES</span></span>

## <span data-ttu-id="a4692-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4692-167">RELATED LINKS</span></span>

[<span data-ttu-id="a4692-168">Új – AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="a4692-168">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="a4692-169">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="a4692-169">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


