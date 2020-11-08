---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5EE936CA-DD9A-4BC6-B835-E22AE633B46D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bc7c8f39f1bdbd35cfffeb59b3b4f184f30845e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015427"
---
# <span data-ttu-id="b198f-101">Start-AzureSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="b198f-101">Start-AzureSqlDatabaseImport</span></span>

## <span data-ttu-id="b198f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b198f-102">SYNOPSIS</span></span>
<span data-ttu-id="b198f-103">Az importálási művelet indítása blob-tárolóról Azure SQL-adatbázisba.</span><span class="sxs-lookup"><span data-stu-id="b198f-103">Starts an import operation from blob storage to an Azure SQL Database.</span></span>

## <span data-ttu-id="b198f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b198f-104">SYNTAX</span></span>

### <span data-ttu-id="b198f-105">ByContainerObject</span><span class="sxs-lookup"><span data-stu-id="b198f-105">ByContainerObject</span></span>
```
Start-AzureSqlDatabaseImport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContainer <AzureStorageContainer> -DatabaseName <String> -BlobName <String>
 [-Edition <DatabaseEdition>] [-DatabaseMaxSize <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b198f-106">ByContainerName</span><span class="sxs-lookup"><span data-stu-id="b198f-106">ByContainerName</span></span>
```
Start-AzureSqlDatabaseImport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContext <IStorageContext> -StorageContainerName <String> -DatabaseName <String> -BlobName <String>
 [-Edition <DatabaseEdition>] [-DatabaseMaxSize <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b198f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b198f-107">DESCRIPTION</span></span>
<span data-ttu-id="b198f-108">A **Start-AzureSqlDatabaseImport** parancsmag az Azure Blob-tárolóból egy Azure SQL-adatbázisba kezdi az importálási műveletet.</span><span class="sxs-lookup"><span data-stu-id="b198f-108">The **Start-AzureSqlDatabaseImport** cmdlet starts an import operation from Azure Blob storage to an Azure SQL Database.</span></span>
<span data-ttu-id="b198f-109">Ha az adatbázis nem létezik, akkor ez a parancsmag a megadott méret és kiadás értékekkel hozza létre azt.</span><span class="sxs-lookup"><span data-stu-id="b198f-109">If the database does not exist, this cmdlet creates it by using the size and edition values that you specify.</span></span>
<span data-ttu-id="b198f-110">A művelethez adatbázis-kiszolgáló kapcsolati környezet szükséges.</span><span class="sxs-lookup"><span data-stu-id="b198f-110">The operation requires a database server connection context.</span></span>
<span data-ttu-id="b198f-111">Az importálási művelet állapotának lekérdezéséhez használja az Get-AzureSqlDatabaseImportExportStatus parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b198f-111">Use the Get-AzureSqlDatabaseImportExportStatus cmdlet to get the status of the import operation.</span></span>

## <span data-ttu-id="b198f-112">Példák</span><span class="sxs-lookup"><span data-stu-id="b198f-112">EXAMPLES</span></span>

### <span data-ttu-id="b198f-113">1. példa: adatbázis importálása</span><span class="sxs-lookup"><span data-stu-id="b198f-113">Example 1: Import a database</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> $SqlContext = New-AzureSqlDatabaseServerContext -ServerName $ServerName -Credentials $Credential
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName $StorageName -StorageAccountKey $StorageKey
PS C:\> $Container = Get-AzureStorageContainer -Name $ContainerName -Context $StorageContext
PS C:\> $ImportRequest = Start-AzureSqlDatabaseImport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
```

<span data-ttu-id="b198f-114">Ez a példa egy importálási folyamatot kezdeményez a $BlobName változó blob-tárterületéről a DatabaseName nevű Azure SQL-adatbázisba.</span><span class="sxs-lookup"><span data-stu-id="b198f-114">This example initiates an import process from the Blob storage in the $BlobName variable into the Azure SQL Database named DatabaseName.</span></span>

## <span data-ttu-id="b198f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b198f-115">PARAMETERS</span></span>

### <span data-ttu-id="b198f-116">-BlobName</span><span class="sxs-lookup"><span data-stu-id="b198f-116">-BlobName</span></span>
<span data-ttu-id="b198f-117">Annak az Azure Blob-tárolónak a neve, amelyből a parancsmag az adatbázist importálja.</span><span class="sxs-lookup"><span data-stu-id="b198f-117">Specifies the name of the Azure Blob storage from which this cmdlet imports the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b198f-118">-DatabaseMaxSize</span><span class="sxs-lookup"><span data-stu-id="b198f-118">-DatabaseMaxSize</span></span>
<span data-ttu-id="b198f-119">Az adatbázis maximális méretét adja meg gigabájtban.</span><span class="sxs-lookup"><span data-stu-id="b198f-119">Specifies the maximum size, in gigabytes, for the database.</span></span>
<span data-ttu-id="b198f-120">Ha az adatbázis nem létezik, akkor ez a parancsmag a maximális méret alapján hozza létre.</span><span class="sxs-lookup"><span data-stu-id="b198f-120">If the database does not exist, this cmdlet creates it based on this maximum size.</span></span>
<span data-ttu-id="b198f-121">Az elfogadható értékek kiadás alapján eltérőek.</span><span class="sxs-lookup"><span data-stu-id="b198f-121">The acceptable values differ based on edition.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b198f-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b198f-122">-DatabaseName</span></span>
<span data-ttu-id="b198f-123">Az adatbázis nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b198f-123">Specifies a name for the database.</span></span>
<span data-ttu-id="b198f-124">Ha az adatbázis nem létezik, akkor ez a parancsmag hozza létre, és hozzárendeli a paraméter által megadott nevet.</span><span class="sxs-lookup"><span data-stu-id="b198f-124">If the database does not exist, this cmdlet creates it, and assigns the name that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b198f-125">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="b198f-125">-Edition</span></span>
<span data-ttu-id="b198f-126">Az adatbázis kiadását adja meg.</span><span class="sxs-lookup"><span data-stu-id="b198f-126">Specifies the edition of the database.</span></span>
<span data-ttu-id="b198f-127">Ha az adatbázis nem létezik, ez a parancsmag ezt a kiadást hozza létre.</span><span class="sxs-lookup"><span data-stu-id="b198f-127">If the database does not exist, this cmdlet creates it as this edition.</span></span>
<span data-ttu-id="b198f-128">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="b198f-128">Valid values are:</span></span> 

- <span data-ttu-id="b198f-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="b198f-129">None</span></span>
- <span data-ttu-id="b198f-130">Web</span><span class="sxs-lookup"><span data-stu-id="b198f-130">Web</span></span> 
- <span data-ttu-id="b198f-131">Vállalati verzió</span><span class="sxs-lookup"><span data-stu-id="b198f-131">Business</span></span> 
- <span data-ttu-id="b198f-132">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="b198f-132">Basic</span></span>
- <span data-ttu-id="b198f-133">Standard</span><span class="sxs-lookup"><span data-stu-id="b198f-133">Standard</span></span>
- <span data-ttu-id="b198f-134">Prémium verzió</span><span class="sxs-lookup"><span data-stu-id="b198f-134">Premium</span></span>

<span data-ttu-id="b198f-135">Az alapértelmezett a web.</span><span class="sxs-lookup"><span data-stu-id="b198f-135">The default is Web.</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b198f-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="b198f-136">-Profile</span></span>
<span data-ttu-id="b198f-137">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="b198f-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b198f-138">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="b198f-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b198f-139">-SqlConnectionContext</span><span class="sxs-lookup"><span data-stu-id="b198f-139">-SqlConnectionContext</span></span>
<span data-ttu-id="b198f-140">Az adatbázist tartalmazó kiszolgáló kapcsolati környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b198f-140">Specifies the connection context of a server that contains the database.</span></span>

```yaml
Type: ISqlServerConnectionInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b198f-141">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="b198f-141">-StorageContainer</span></span>
<span data-ttu-id="b198f-142">Annak a tárolónak a tárolóját adja meg, amelyből a parancsmag adatbázis-importálási lehetőséget tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="b198f-142">Specifies the storage container that contains the Blob from which this cmdlet imports a database.</span></span>

```yaml
Type: AzureStorageContainer
Parameter Sets: ByContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b198f-143">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="b198f-143">-StorageContainerName</span></span>
<span data-ttu-id="b198f-144">A blob-tároló tárolójának a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b198f-144">Specifies the name of the Blob storage container.</span></span>

```yaml
Type: String
Parameter Sets: ByContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b198f-145">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="b198f-145">-StorageContext</span></span>
<span data-ttu-id="b198f-146">A blob-tároló tároló környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b198f-146">Specifies the context of the Blob storage container.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ByContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b198f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b198f-147">CommonParameters</span></span>
<span data-ttu-id="b198f-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b198f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b198f-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b198f-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b198f-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b198f-150">INPUTS</span></span>

## <span data-ttu-id="b198f-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b198f-151">OUTPUTS</span></span>

### <span data-ttu-id="b198f-152">Microsoft. WindowsAzure. Command. SqlDatabase. Services. ImportExportRequest</span><span class="sxs-lookup"><span data-stu-id="b198f-152">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExportRequest</span></span>

## <span data-ttu-id="b198f-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b198f-153">NOTES</span></span>

## <span data-ttu-id="b198f-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b198f-154">RELATED LINKS</span></span>

[<span data-ttu-id="b198f-155">Azure SQL-adatbázis</span><span class="sxs-lookup"><span data-stu-id="b198f-155">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="b198f-156">Adatbázis importálása</span><span class="sxs-lookup"><span data-stu-id="b198f-156">Import Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781284.aspx)

[<span data-ttu-id="b198f-157">Azure SQL-adatbázisok műveletei</span><span class="sxs-lookup"><span data-stu-id="b198f-157">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="b198f-158">Get-AzureSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="b198f-158">Get-AzureSqlDatabaseImportExportStatus</span></span>](./Get-AzureSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="b198f-159">Start-AzureSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="b198f-159">Start-AzureSqlDatabaseExport</span></span>](./Start-AzureSqlDatabaseExport.md)


