---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: da85c91aea3c47c2b3ba0e9ff19938980dbc80d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502207"
---
# <span data-ttu-id="46476-101">New-AzureRmVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="46476-101">New-AzureRmVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="46476-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="46476-102">SYNOPSIS</span></span>
<span data-ttu-id="46476-103">Konfigurációs objektum létrehozása az SQL Server automatikus biztonsági mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="46476-103">Creates a configuration object for SQL Server automatic backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46476-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="46476-104">SYNTAX</span></span>

### <span data-ttu-id="46476-105">StorageUriSqlServerAutoBackup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="46476-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzureRmVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46476-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="46476-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzureRmVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs]
 [-BackupScheduleType <String>] [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>]
 [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46476-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="46476-107">DESCRIPTION</span></span>
<span data-ttu-id="46476-108">A **New-AzureRmVMSqlServerAutoBackupConfig** parancsmag létrehoz egy konfigurációs OBJEKTUMOT az SQL Server automatikus biztonsági mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="46476-108">The **New-AzureRmVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="46476-109">Példák</span><span class="sxs-lookup"><span data-stu-id="46476-109">EXAMPLES</span></span>

### <span data-ttu-id="46476-110">Példa 1: automatikus biztonsági másolat létrehozása a tárolási URI és a fiók kulccsal</span><span class="sxs-lookup"><span data-stu-id="46476-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureRmVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="46476-111">A parancs a tárterület-azonosító és a fiók kulcs megadásával automatikusan biztonsági másolatot készít a konfigurációs objektumról.</span><span class="sxs-lookup"><span data-stu-id="46476-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="46476-112">Az automatikus biztonsági mentés be van kapcsolva, és az automatikus biztonsági mentés 10 napig tart.</span><span class="sxs-lookup"><span data-stu-id="46476-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="46476-113">A parancs az eredményt a $AutoBackupConfig változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="46476-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="46476-114">Ezt a konfigurációs elemet más parancsmagok, például az Set-AzureRmVMSqlServerExtension parancsmag esetében is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="46476-114">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="46476-115">2. példa: automatikus biztonságimásolat-konfiguráció létrehozása tárolási környezet használatával</span><span class="sxs-lookup"><span data-stu-id="46476-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzureRmVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="46476-116">Az első parancs létrehozza a tárolási környezetet, majd a $StorageContext változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="46476-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="46476-117">További információt az új AzureStorageContext című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="46476-117">For more information, see New-AzureStorageContext.</span></span>
<span data-ttu-id="46476-118">A második parancs az $StorageContext tárolási környezetének megadásával automatikusan biztonsági másolatot készít a konfigurációs objektumról.</span><span class="sxs-lookup"><span data-stu-id="46476-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="46476-119">Az automatikus biztonsági mentés be van kapcsolva, és az automatikus biztonsági mentés 10 napig tart.</span><span class="sxs-lookup"><span data-stu-id="46476-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="46476-120">3. példa: automatikus biztonsági másolat beállítása a tárolási környezettel a titkosítással és a jelszóval</span><span class="sxs-lookup"><span data-stu-id="46476-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzureRmVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="46476-121">Ezzel a paranccsal létrehozhatja és tárolhatja az automatikus biztonságimásolat-konfiguráció objektumát.</span><span class="sxs-lookup"><span data-stu-id="46476-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="46476-122">A parancs az előző példában létrehozott tárterület-környezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="46476-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="46476-123">A parancs engedélyezi a titkosítást a jelszóval.</span><span class="sxs-lookup"><span data-stu-id="46476-123">The command enables encryption with password.</span></span>
<span data-ttu-id="46476-124">A jelszó korábban biztonságos karakterláncként volt tárolva a $CertificatePassword változóban.</span><span class="sxs-lookup"><span data-stu-id="46476-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="46476-125">Ha biztonságos karakterláncot szeretne létrehozni, használja az ConvertTo-SecureString parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="46476-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="46476-126">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="46476-126">PARAMETERS</span></span>

### <span data-ttu-id="46476-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="46476-127">-BackupScheduleType</span></span>
<span data-ttu-id="46476-128">Biztonságimásolat-ütemezés típusa, kézi vagy automatizált</span><span class="sxs-lookup"><span data-stu-id="46476-128">Backup schedule type, manual or automated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Manual, Automated

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46476-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="46476-129">-BackupSystemDbs</span></span>
<span data-ttu-id="46476-130">Biztonsági másolat rendszeradatbázisai</span><span class="sxs-lookup"><span data-stu-id="46476-130">Backup system databases</span></span>

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

### <span data-ttu-id="46476-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="46476-131">-CertificatePassword</span></span>
<span data-ttu-id="46476-132">Megadja azt a jelszót, amellyel titkosítható az SQL Server titkosított biztonsági mentéseit szolgáló tanúsítvány.</span><span class="sxs-lookup"><span data-stu-id="46476-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46476-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46476-133">-DefaultProfile</span></span>
<span data-ttu-id="46476-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="46476-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46476-135">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="46476-135">-Enable</span></span>
<span data-ttu-id="46476-136">Azt jelzi, hogy az SQL Server virtuális gép automatikus biztonsági másolata engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="46476-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="46476-137">Ha ezt a paramétert adja meg, akkor az automatikus biztonsági mentés az összes aktuális és új adatbázis biztonsági ütemezését állítja be.</span><span class="sxs-lookup"><span data-stu-id="46476-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="46476-138">Ezzel frissíti a felügyelt biztonságimásolat-beállításokat az ütemezés követéséhez.</span><span class="sxs-lookup"><span data-stu-id="46476-138">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46476-139">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="46476-139">-EnableEncryption</span></span>
<span data-ttu-id="46476-140">Azt jelzi, hogy ez a parancsmag engedélyezi a titkosítást.</span><span class="sxs-lookup"><span data-stu-id="46476-140">Indicates that this cmdlet enables encryption.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46476-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="46476-141">-FullBackupFrequency</span></span>
<span data-ttu-id="46476-142">SQL Server – teljes biztonsági mentés gyakorisága, naponta vagy hetente</span><span class="sxs-lookup"><span data-stu-id="46476-142">Sql Server Full Backup frequency, daily or weekly</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Weekly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46476-143">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="46476-143">-FullBackupStartHour</span></span>
<span data-ttu-id="46476-144">A nap órája (0-23), amikor az SQL Server teljes biztonsági másolatát meg kell kezdeni</span><span class="sxs-lookup"><span data-stu-id="46476-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="46476-145">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="46476-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="46476-146">Az SQL Server teljes biztonsági másolat ablaka órában</span><span class="sxs-lookup"><span data-stu-id="46476-146">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="46476-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="46476-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="46476-148">SQL Server log Backup gyakorisága, 1-60 percenként</span><span class="sxs-lookup"><span data-stu-id="46476-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="46476-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46476-149">-ResourceGroupName</span></span>
<span data-ttu-id="46476-150">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="46476-150">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46476-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="46476-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="46476-152">Azt adja meg, hogy hány napig maradjon a biztonsági másolat.</span><span class="sxs-lookup"><span data-stu-id="46476-152">Specifies the number of days to retain a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46476-153">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="46476-153">-StorageContext</span></span>
<span data-ttu-id="46476-154">Azt a tárterületet adja meg, amelyet a biztonsági másolatok tárolására fog használni.</span><span class="sxs-lookup"><span data-stu-id="46476-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="46476-155">**AzureStorageContext** objektum beolvasásához használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="46476-155">To obtain an **AzureStorageContext** object, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="46476-156">Az alapértelmezett érték az SQL Server virtuális géphez társított tárolási fiók.</span><span class="sxs-lookup"><span data-stu-id="46476-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46476-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="46476-157">-StorageKey</span></span>
<span data-ttu-id="46476-158">A blob-tároló fiók tárolási kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="46476-158">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="46476-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="46476-159">-StorageUri</span></span>
<span data-ttu-id="46476-160">A blob-tároló fiók egységes erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="46476-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="46476-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46476-161">CommonParameters</span></span>
<span data-ttu-id="46476-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="46476-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46476-163">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46476-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46476-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="46476-164">INPUTS</span></span>

### <span data-ttu-id="46476-165">System. String</span><span class="sxs-lookup"><span data-stu-id="46476-165">System.String</span></span>

### <span data-ttu-id="46476-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="46476-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="46476-167">System. Int32</span><span class="sxs-lookup"><span data-stu-id="46476-167">System.Int32</span></span>

### <span data-ttu-id="46476-168">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="46476-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="46476-169">System. URI</span><span class="sxs-lookup"><span data-stu-id="46476-169">System.Uri</span></span>

### <span data-ttu-id="46476-170">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="46476-170">System.Security.SecureString</span></span>

### <span data-ttu-id="46476-171">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="46476-171">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="46476-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46476-172">OUTPUTS</span></span>

### <span data-ttu-id="46476-173">Microsoft. Azure. commands. kiszámítás. AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="46476-173">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="46476-174">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="46476-174">NOTES</span></span>

## <span data-ttu-id="46476-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46476-175">RELATED LINKS</span></span>

[<span data-ttu-id="46476-176">Új – AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="46476-176">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="46476-177">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="46476-177">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


