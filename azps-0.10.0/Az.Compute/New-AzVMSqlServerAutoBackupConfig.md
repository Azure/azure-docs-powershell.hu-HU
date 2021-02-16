---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: ecff02643dd6d0e017d56af01792a06dc7b8d998
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398274"
---
# <span data-ttu-id="c257f-101">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="c257f-101">New-AzVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="c257f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c257f-102">SYNOPSIS</span></span>
<span data-ttu-id="c257f-103">Konfigurációs objektumot hoz létre az SQL Server automatikus biztonsági mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="c257f-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="c257f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c257f-104">SYNTAX</span></span>

### <span data-ttu-id="c257f-105">StorageUriSqlServerAutoBackup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c257f-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c257f-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="c257f-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs]
 [-BackupScheduleType <String>] [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>]
 [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c257f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c257f-107">DESCRIPTION</span></span>
<span data-ttu-id="c257f-108">A **New-AzVMSqlServerAutoBackupConfig** parancsmag létrehoz egy konfigurációs objektumot az SQL Server automatikus biztonsági mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="c257f-108">The **New-AzVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="c257f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c257f-109">EXAMPLES</span></span>

### <span data-ttu-id="c257f-110">1. példa: Automatikus biztonságimásolat-konfiguráció létrehozása tárhely URI-jának és fiókkulcsának használatával</span><span class="sxs-lookup"><span data-stu-id="c257f-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="c257f-111">Ez a parancs a tárhely URI-jának és a fiókkulcsnak a megadásával létrehoz egy automatikus biztonságimásolat-konfigurációs objektumot.</span><span class="sxs-lookup"><span data-stu-id="c257f-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="c257f-112">Az automatikus biztonsági mentés engedélyezve van, az automatikus biztonsági mentések pedig 10 napig maradnak meg.</span><span class="sxs-lookup"><span data-stu-id="c257f-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="c257f-113">A parancs az eredményt a $AutoBackupConfig tárolja.</span><span class="sxs-lookup"><span data-stu-id="c257f-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="c257f-114">Ezt a konfigurációs elemet más parancsmagok, például a Set-AzVMSqlServerExtension is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="c257f-114">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="c257f-115">2. példa: Automatikus biztonsági mentés beállítása tárhelykörnyezet használatával</span><span class="sxs-lookup"><span data-stu-id="c257f-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="c257f-116">Az első parancs létrehoz egy tárolási környezetet, majd a helyi $StorageContext tárolja.</span><span class="sxs-lookup"><span data-stu-id="c257f-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="c257f-117">További információ: New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="c257f-117">For more information, see New-AzureStorageContext.</span></span>

<span data-ttu-id="c257f-118">A második parancs egy automatikus biztonságimásolat-konfigurációs objektumot hoz létre a tárterület környezetének $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="c257f-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="c257f-119">Az automatikus biztonsági mentés engedélyezve van, az automatikus biztonsági mentések pedig 10 napig maradnak meg.</span><span class="sxs-lookup"><span data-stu-id="c257f-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="c257f-120">3. példa: Automatikus biztonsági mentés beállítása titkosítással és jelszóval</span><span class="sxs-lookup"><span data-stu-id="c257f-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="c257f-121">Ez a parancs létrehoz és tárol egy automatikus biztonságimásolat-konfigurációs objektumot.</span><span class="sxs-lookup"><span data-stu-id="c257f-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="c257f-122">A parancs megadja az előző példában létrehozott tárterületkörnyezetet.</span><span class="sxs-lookup"><span data-stu-id="c257f-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="c257f-123">A parancs jelszóval való titkosítást tesz lehetővé.</span><span class="sxs-lookup"><span data-stu-id="c257f-123">The command enables encryption with password.</span></span>
<span data-ttu-id="c257f-124">A jelszót korábban biztonságos karakterláncként tárolta a $CertificatePassword változóban.</span><span class="sxs-lookup"><span data-stu-id="c257f-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="c257f-125">Biztonságos karakterlánc létrehozásához használja a ConvertTo-SecureString parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c257f-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="c257f-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c257f-126">PARAMETERS</span></span>

### <span data-ttu-id="c257f-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="c257f-127">-BackupScheduleType</span></span>
<span data-ttu-id="c257f-128">Biztonsági mentési ütemezés típusa, kézi vagy automatizált</span><span class="sxs-lookup"><span data-stu-id="c257f-128">Backup schedule type, manual or automated</span></span>

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

### <span data-ttu-id="c257f-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="c257f-129">-BackupSystemDbs</span></span>
<span data-ttu-id="c257f-130">Rendszer-adatbázisok biztonsági mentése</span><span class="sxs-lookup"><span data-stu-id="c257f-130">Backup system databases</span></span>

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

### <span data-ttu-id="c257f-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c257f-131">-CertificatePassword</span></span>
<span data-ttu-id="c257f-132">Megadja a jelszót az SQL Server által titkosított biztonsági másolatok végrehajtásához használt tanúsítvány titkosításához.</span><span class="sxs-lookup"><span data-stu-id="c257f-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

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

### <span data-ttu-id="c257f-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c257f-133">-DefaultProfile</span></span>
<span data-ttu-id="c257f-134">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c257f-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c257f-135">-Enable</span><span class="sxs-lookup"><span data-stu-id="c257f-135">-Enable</span></span>
<span data-ttu-id="c257f-136">Azt jelzi, hogy engedélyezve van az SQL Server virtuális gép automatikus biztonsági mentése.</span><span class="sxs-lookup"><span data-stu-id="c257f-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="c257f-137">Ha ezt a paramétert adja meg, az automatikus biztonsági mentés biztonsági mentési ütemezést állít be az összes jelenlegi és új adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="c257f-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="c257f-138">Ezzel frissíti a felügyelt biztonsági mentés beállításait, hogy kövessék ezt az ütemezést.</span><span class="sxs-lookup"><span data-stu-id="c257f-138">This updates your Managed Backup settings to follow this schedule.</span></span>

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

### <span data-ttu-id="c257f-139">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="c257f-139">-EnableEncryption</span></span>
<span data-ttu-id="c257f-140">Azt jelzi, hogy ez a parancsmag engedélyezi a titkosítást.</span><span class="sxs-lookup"><span data-stu-id="c257f-140">Indicates that this cmdlet enables encryption.</span></span>

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

### <span data-ttu-id="c257f-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="c257f-141">-FullBackupFrequency</span></span>
<span data-ttu-id="c257f-142">Sql Server Full Backup frequency, daily or weekly</span><span class="sxs-lookup"><span data-stu-id="c257f-142">Sql Server Full Backup frequency, daily or weekly</span></span>

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

### <span data-ttu-id="c257f-143">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="c257f-143">-FullBackupStartHour</span></span>
<span data-ttu-id="c257f-144">Az Sql Server teljes biztonsági mentésének indítási napja (0–23)</span><span class="sxs-lookup"><span data-stu-id="c257f-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="c257f-145">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="c257f-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="c257f-146">Sql Server Full Backup window in hours</span><span class="sxs-lookup"><span data-stu-id="c257f-146">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="c257f-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="c257f-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="c257f-148">Sql Server-napló biztonsági mentési gyakorisága, 1–60 percenként egyszer</span><span class="sxs-lookup"><span data-stu-id="c257f-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="c257f-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c257f-149">-ResourceGroupName</span></span>
<span data-ttu-id="c257f-150">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c257f-150">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c257f-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="c257f-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="c257f-152">Azt adja meg, hogy hány napig őrizze meg a biztonsági másolatokat.</span><span class="sxs-lookup"><span data-stu-id="c257f-152">Specifies the number of days to retain a backup.</span></span>

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

### <span data-ttu-id="c257f-153">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="c257f-153">-StorageContext</span></span>
<span data-ttu-id="c257f-154">Azt a tárfiókot adja meg, amely a biztonsági másolatok tárolására fog használni.</span><span class="sxs-lookup"><span data-stu-id="c257f-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="c257f-155">**AzureStorageContext-objektum** beszerzéséhez használja a New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c257f-155">To obtain an **AzureStorageContext** object, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="c257f-156">Az alapértelmezett érték az SQL Server virtuális géphez társított tárfiók.</span><span class="sxs-lookup"><span data-stu-id="c257f-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c257f-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="c257f-157">-StorageKey</span></span>
<span data-ttu-id="c257f-158">A blobtároló-fiók tárkulcsát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="c257f-158">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="c257f-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="c257f-159">-StorageUri</span></span>
<span data-ttu-id="c257f-160">A blobtároló fiók egységes erőforrás-azonosítóját (URI) adja meg.</span><span class="sxs-lookup"><span data-stu-id="c257f-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="c257f-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c257f-161">CommonParameters</span></span>
<span data-ttu-id="c257f-162">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c257f-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c257f-163">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c257f-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c257f-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c257f-164">INPUTS</span></span>

### <span data-ttu-id="c257f-165">Nincs</span><span class="sxs-lookup"><span data-stu-id="c257f-165">None</span></span>
<span data-ttu-id="c257f-166">Ez a parancsmag semmilyen bemenetet nem fogad el.</span><span class="sxs-lookup"><span data-stu-id="c257f-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c257f-167">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c257f-167">OUTPUTS</span></span>

### <span data-ttu-id="c257f-168">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="c257f-168">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="c257f-169">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c257f-169">NOTES</span></span>

## <span data-ttu-id="c257f-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c257f-170">RELATED LINKS</span></span>

[<span data-ttu-id="c257f-171">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="c257f-171">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="c257f-172">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="c257f-172">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


