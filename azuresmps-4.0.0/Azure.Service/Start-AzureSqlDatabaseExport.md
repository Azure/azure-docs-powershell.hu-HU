---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 3005E411-9466-4602-8E07-F4EF8804AB2A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22bff485bf49e0ec5f482e1325af661862583605
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015752"
---
# <span data-ttu-id="fe6e6-101">Start-AzureSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="fe6e6-101">Start-AzureSqlDatabaseExport</span></span>

## <span data-ttu-id="fe6e6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fe6e6-102">SYNOPSIS</span></span>
<span data-ttu-id="fe6e6-103">Az exportálási műveletet egy Azure SQL-adatbázisból blob-tárolóba kezdi.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-103">Starts an export operation from an Azure SQL Database to Blob storage.</span></span>

## <span data-ttu-id="fe6e6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fe6e6-104">SYNTAX</span></span>

### <span data-ttu-id="fe6e6-105">ByContainerObject</span><span class="sxs-lookup"><span data-stu-id="fe6e6-105">ByContainerObject</span></span>
```
Start-AzureSqlDatabaseExport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContainer <AzureStorageContainer> -DatabaseName <String> -BlobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="fe6e6-106">ByContainerName</span><span class="sxs-lookup"><span data-stu-id="fe6e6-106">ByContainerName</span></span>
```
Start-AzureSqlDatabaseExport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContext <IStorageContext> -StorageContainerName <String> -DatabaseName <String> -BlobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fe6e6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fe6e6-107">DESCRIPTION</span></span>
<span data-ttu-id="fe6e6-108">A **Start-AzureSqlDatabaseExport** parancsmag az Azure SQL-adatbázisból blob-tárolóba kezdi az exportálási műveletet.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-108">The **Start-AzureSqlDatabaseExport** cmdlet starts an export operation from an Azure SQL Database to Blob storage.</span></span>
<span data-ttu-id="fe6e6-109">A művelethez adatbázis-kiszolgáló kapcsolati környezet szükséges.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-109">The operation requires a database server connection context.</span></span>
<span data-ttu-id="fe6e6-110">Az exportálási művelet állapotának lekérdezéséhez használja az Get-AzureSqlDatabaseImportExportStatus parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-110">Use the Get-AzureSqlDatabaseImportExportStatus cmdlet to get the status of the export operation.</span></span>

## <span data-ttu-id="fe6e6-111">Példák</span><span class="sxs-lookup"><span data-stu-id="fe6e6-111">EXAMPLES</span></span>

### <span data-ttu-id="fe6e6-112">1. példa: adatbázis exportálása</span><span class="sxs-lookup"><span data-stu-id="fe6e6-112">Example 1: Export a database</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> $SqlContext = New-AzureSqlDatabaseServerContext -ServerName $ServerName -Credential $Credential
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName $StorageName -StorageAccountKey $StorageKey
PS C:\> $Container = Get-AzureStorageContainer -Name $ContainerName -Context $StorageContext
PS C:\> $exportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
```

<span data-ttu-id="fe6e6-113">Ez a példa olyan exportálási folyamatot kezdeményez az Azure SQL-adatbázisból, amely a $DatabaseName változóban tárolt nevet tartalmazza a $BlobName változóban tárolt blob-tárolónak.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-113">This example initiates an export process from the Azure SQL Database that has the name stored in the $DatabaseName variable to the Blob storage stored in the $BlobName variable.</span></span>

## <span data-ttu-id="fe6e6-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fe6e6-114">PARAMETERS</span></span>

### <span data-ttu-id="fe6e6-115">-BlobName</span><span class="sxs-lookup"><span data-stu-id="fe6e6-115">-BlobName</span></span>
<span data-ttu-id="fe6e6-116">Annak az Azure Blob-tárolónak a nevét adja meg, amelyre a parancsmag az adatbázist exportálja.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-116">Specifies the name of the Azure Blob storage into which this cmdlet exports the database.</span></span>

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

### <span data-ttu-id="fe6e6-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fe6e6-117">-DatabaseName</span></span>
<span data-ttu-id="fe6e6-118">Annak az adatbázisnak a nevét adja meg, amelyből a parancsmag az adatot exportálja.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-118">Specifies the name of the database from which this cmdlet exports data.</span></span>

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

### <span data-ttu-id="fe6e6-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="fe6e6-119">-Profile</span></span>
<span data-ttu-id="fe6e6-120">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fe6e6-121">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fe6e6-122">-SqlConnectionContext</span><span class="sxs-lookup"><span data-stu-id="fe6e6-122">-SqlConnectionContext</span></span>
<span data-ttu-id="fe6e6-123">Az adatbázist tartalmazó kiszolgáló kapcsolati környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-123">Specifies the connection context of a server that contains the database.</span></span>

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

### <span data-ttu-id="fe6e6-124">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="fe6e6-124">-StorageContainer</span></span>
<span data-ttu-id="fe6e6-125">Annak a tárolónak a tárolóját adja meg, amely a parancsmagot tartalmazó blobot exportálja.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-125">Specifies the storage container that contains the Blob into which this cmdlet export a database.</span></span>

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

### <span data-ttu-id="fe6e6-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="fe6e6-126">-StorageContainerName</span></span>
<span data-ttu-id="fe6e6-127">Annak a tárolónak a nevét adja meg, amely a parancsmagot tartalmazó blobot exportálja.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-127">Specifies the name of the storage container that contains the Blob into which this cmdlet exports a database.</span></span>

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

### <span data-ttu-id="fe6e6-128">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="fe6e6-128">-StorageContext</span></span>
<span data-ttu-id="fe6e6-129">A blob-tároló tároló környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe6e6-129">Specifies the context of the Blob storage container.</span></span>

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

### <span data-ttu-id="fe6e6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe6e6-130">CommonParameters</span></span>
<span data-ttu-id="fe6e6-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fe6e6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe6e6-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe6e6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe6e6-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe6e6-133">INPUTS</span></span>

## <span data-ttu-id="fe6e6-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe6e6-134">OUTPUTS</span></span>

### <span data-ttu-id="fe6e6-135">Microsoft. WindowsAzure. Command. SqlDatabase. Services. ImportExportRequest</span><span class="sxs-lookup"><span data-stu-id="fe6e6-135">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExportRequest</span></span>

## <span data-ttu-id="fe6e6-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fe6e6-136">NOTES</span></span>

## <span data-ttu-id="fe6e6-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe6e6-137">RELATED LINKS</span></span>

[<span data-ttu-id="fe6e6-138">Azure SQL-adatbázis</span><span class="sxs-lookup"><span data-stu-id="fe6e6-138">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="fe6e6-139">Adatbázis exportálása</span><span class="sxs-lookup"><span data-stu-id="fe6e6-139">Export Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781282.aspx)

[<span data-ttu-id="fe6e6-140">Azure SQL-adatbázisok műveletei</span><span class="sxs-lookup"><span data-stu-id="fe6e6-140">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="fe6e6-141">Get-AzureSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="fe6e6-141">Get-AzureSqlDatabaseImportExportStatus</span></span>](./Get-AzureSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="fe6e6-142">Start-AzureSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="fe6e6-142">Start-AzureSqlDatabaseImport</span></span>](./Start-AzureSqlDatabaseImport.md)


