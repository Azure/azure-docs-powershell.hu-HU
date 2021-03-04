---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 6d9047679f4286e0e2212ca8e599237825326dd7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930577"
---
# <span data-ttu-id="1b1bd-101">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="1b1bd-101">New-AzVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="1b1bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b1bd-102">SYNOPSIS</span></span>
<span data-ttu-id="1b1bd-103">Konfigurációs objektumot hoz létre az SQL Server automatikus biztonsági mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="1b1bd-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="1b1bd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1b1bd-104">SYNTAX</span></span>

### <span data-ttu-id="1b1bd-105">StorageUriSqlServerAutoBackup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1b1bd-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b1bd-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="1b1bd-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageContext] <IStorageContext>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b1bd-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1b1bd-107">DESCRIPTION</span></span>
<span data-ttu-id="1b1bd-108">A **New-AzVMSqlServerAutoBackupConfig** parancsmag létrehoz egy konfigurációs objektumot az SQL Server automatikus biztonsági mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="1b1bd-108">The **New-AzVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="1b1bd-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1b1bd-109">EXAMPLES</span></span>

### <span data-ttu-id="1b1bd-110">1. példa: Automatikus biztonságimásolat-konfiguráció létrehozása tárhely URI-jának és fiókkulcsának használatával</span><span class="sxs-lookup"><span data-stu-id="1b1bd-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="1b1bd-111">Ez a parancs a tárhely URI-jának és a fiókkulcsnak a megadásával létrehoz egy automatikus biztonságimásolat-konfigurációs objektumot.</span><span class="sxs-lookup"><span data-stu-id="1b1bd-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="1b1bd-112">Az automatikus biztonsági mentés engedélyezve van, az automatikus biztonsági mentések pedig 10 napig maradnak meg.</span><span class="sxs-lookup"><span data-stu-id="1b1bd-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="1b1bd-113">A parancs az eredményt a $AutoBackupConfig tárolja.</span><span class="sxs-lookup"><span data-stu-id="1b1bd-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="1b1bd-114">Ezt a konfigurációs elemet más parancsmagok, például a Set-AzVMSqlServerExtension is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="1b1bd-114">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="1b1bd-115">2. példa: Automatikus biztonsági mentés beállítása tárterületkörnyezet használatával</span><span class="sxs-lookup"><span data-stu-id="1b1bd-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="1b1bd-116">Az első parancs létrehoz egy tárterületkörnyezetet, majd a helyi $StorageContext tárolja.</span><span class="sxs-lookup"><span data-stu-id="1b1bd-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="1b1bd-117">További információ: New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="1b1bd-117">For more information, see New-AzStorageContext.</span></span>
<span data-ttu-id="1b1bd-118">A második parancs egy automatikus biztonságimásolat-konfigurációs objektumot hoz létre a tárterület környezetének $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="1b1bd-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="1b1bd-119">Az automatikus biztonsági mentés engedélyezve van, az automatikus biztonsági mentések pedig 10 napig maradnak meg.</span><span class="sxs-lookup"><span data-stu-id="1b1bd-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="1b1bd-120">3. példa: Automatikus biztonsági mentés beállítása titkosítással és jelszóval</span><span class="sxs-lookup"><span data-stu-id="1b1bd-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="1b1bd-121">Ez a parancs létrehoz és tárol egy automatikus biztonságimásolat-konfigurációs objektumot.</span><span class="sxs-lookup"><span data-stu-id="1b1bd-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="1b1bd-122">A parancs megadja az előző példában létrehozott tárterületkörnyezetet.</span><span class="sxs-lookup"><span data-stu-id="1b1bd-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="1b1bd-123">A parancs jelszóval való titkosítást tesz lehetővé.</span><span class="sxs-lookup"><span data-stu-id="1b1bd-123">The command enables encryption with password.</span></span>
<span data-ttu-id="1b1bd-124">A jelszót korábban biztonságos karakterláncként tárolta a $CertificatePassword változóban.</span><span class="sxs-lookup"><span data-stu-id="1b1bd-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="1b1bd-125">Biztonságos karakterlánc létrehozásához használja a ConvertTo-SecureString parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1b1bd-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="1b1bd-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b1bd-126">PARAMETERS</span></span>

### <span data-ttu-id="1b1bd-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="1b1bd-127">-BackupScheduleType</span></span>
<span data-ttu-id="1b1bd-128">Biztonsági mentési ütemezés típusa, kézi vagy automatizált</span><span class="sxs-lookup"><span data-stu-id="1b1bd-128">Backup schedule type, manual or automated</span></span>

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

### <span data-ttu-id="1b1bd-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="1b1bd-129">-BackupSystemDbs</span></span>
<span data-ttu-id="1b1bd-130">Rendszer-adatbázisok biztonsági mentése</span><span class="sxs-lookup"><span data-stu-id="1b1bd-130">Backup system databases</span></span>

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

### <span data-ttu-id="1b1bd-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="1b1bd-131">-CertificatePassword</span></span>
<span data-ttu-id="1b1bd-132">Megadja a jelszót az SQL Server által titkosított biztonsági másolatok végrehajtásához használt tanúsítvány titkosításához.</span><span class="sxs-lookup"><span data-stu-id="1b1bd-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

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

### <span data-ttu-id="1b1bd-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b1bd-133">-DefaultProfile</span></span>
<span data-ttu-id="1b1bd-134">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1b1bd-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b1bd-135">-Enable</span><span class="sxs-lookup"><span data-stu-id="1b1bd-135">-Enable</span></span>
<span data-ttu-id="1b1bd-136">Azt jelzi, hogy engedélyezve van az SQL Server virtuális gép automatikus biztonsági mentése.</span><span class="sxs-lookup"><span data-stu-id="1b1bd-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="1b1bd-137">Ha ezt a paramétert adja meg, az automatikus biztonsági mentés biztonsági mentési ütemezést állít be az összes aktuális és új adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="1b1bd-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="1b1bd-138">Ezzel frissíti a felügyelt biztonsági mentés beállításait, hogy kövessék ezt az ütemezést.</span><span class="sxs-lookup"><span data-stu-id="1b1bd-138">This updates your Managed Backup settings to follow this schedule.</span></span>

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

### <span data-ttu-id="1b1bd-139">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="1b1bd-139">-EnableEncryption</span></span>
<span data-ttu-id="1b1bd-140">Azt jelzi, hogy ez a parancsmag lehetővé teszi a titkosítást.</span><span class="sxs-lookup"><span data-stu-id="1b1bd-140">Indicates that this cmdlet enables encryption.</span></span>

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

### <span data-ttu-id="1b1bd-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="1b1bd-141">-FullBackupFrequency</span></span>
<span data-ttu-id="1b1bd-142">Sql Server Full Backup frequency, daily or weekly</span><span class="sxs-lookup"><span data-stu-id="1b1bd-142">Sql Server Full Backup frequency, daily or weekly</span></span>

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

### <span data-ttu-id="1b1bd-143">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="1b1bd-143">-FullBackupStartHour</span></span>
<span data-ttu-id="1b1bd-144">Az Sql Server teljes biztonsági mentésének indítási napja (0–23)</span><span class="sxs-lookup"><span data-stu-id="1b1bd-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="1b1bd-145">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="1b1bd-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="1b1bd-146">Sql Server Full Backup window in hours</span><span class="sxs-lookup"><span data-stu-id="1b1bd-146">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="1b1bd-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="1b1bd-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="1b1bd-148">Sql Server-napló biztonsági mentési gyakorisága, 1–60 percenként egyszer</span><span class="sxs-lookup"><span data-stu-id="1b1bd-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="1b1bd-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b1bd-149">-ResourceGroupName</span></span>
<span data-ttu-id="1b1bd-150">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b1bd-150">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1b1bd-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="1b1bd-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="1b1bd-152">Azt adja meg, hogy hány napig őrizze meg a biztonsági másolatokat.</span><span class="sxs-lookup"><span data-stu-id="1b1bd-152">Specifies the number of days to retain a backup.</span></span>

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

### <span data-ttu-id="1b1bd-153">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="1b1bd-153">-StorageContext</span></span>
<span data-ttu-id="1b1bd-154">Azt a tárfiókot adja meg, amely a biztonsági másolatok tárolására fog használni.</span><span class="sxs-lookup"><span data-stu-id="1b1bd-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="1b1bd-155">**AzureStorageContext-objektum** beszerzéséhez használja a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1b1bd-155">To obtain an **AzureStorageContext** object, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="1b1bd-156">Az alapértelmezett érték az SQL Server virtuális géphez társított tárfiók.</span><span class="sxs-lookup"><span data-stu-id="1b1bd-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

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

### <span data-ttu-id="1b1bd-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="1b1bd-157">-StorageKey</span></span>
<span data-ttu-id="1b1bd-158">A blobtároló-fiók tárkulcsát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="1b1bd-158">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="1b1bd-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="1b1bd-159">-StorageUri</span></span>
<span data-ttu-id="1b1bd-160">A blobtároló fiók egységes erőforrás-azonosítóját (URI) adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b1bd-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="1b1bd-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b1bd-161">CommonParameters</span></span>
<span data-ttu-id="1b1bd-162">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b1bd-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b1bd-163">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b1bd-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b1bd-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1b1bd-164">INPUTS</span></span>

### <span data-ttu-id="1b1bd-165">System.String</span><span class="sxs-lookup"><span data-stu-id="1b1bd-165">System.String</span></span>

### <span data-ttu-id="1b1bd-166">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1b1bd-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="1b1bd-167">System.Int32</span><span class="sxs-lookup"><span data-stu-id="1b1bd-167">System.Int32</span></span>

### <span data-ttu-id="1b1bd-168">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1b1bd-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="1b1bd-169">System.Uri</span><span class="sxs-lookup"><span data-stu-id="1b1bd-169">System.Uri</span></span>

### <span data-ttu-id="1b1bd-170">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="1b1bd-170">System.Security.SecureString</span></span>

### <span data-ttu-id="1b1bd-171">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1b1bd-171">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="1b1bd-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b1bd-172">OUTPUTS</span></span>

### <span data-ttu-id="1b1bd-173">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="1b1bd-173">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="1b1bd-174">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1b1bd-174">NOTES</span></span>

## <span data-ttu-id="1b1bd-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1b1bd-175">RELATED LINKS</span></span>

[<span data-ttu-id="1b1bd-176">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="1b1bd-176">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="1b1bd-177">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="1b1bd-177">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


