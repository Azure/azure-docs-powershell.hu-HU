---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 4661C479-6E3B-425D-B9D2-B36D7A83130C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c55ebd22337a8078f3ae495b3901317f4201e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016294"
---
# <span data-ttu-id="77079-101">Get-AzureSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="77079-101">Get-AzureSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="77079-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="77079-102">SYNOPSIS</span></span>
<span data-ttu-id="77079-103">Az importálási vagy exportálási kérés állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="77079-103">Gets the status of an import or export request.</span></span>

## <span data-ttu-id="77079-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="77079-104">SYNTAX</span></span>

### <span data-ttu-id="77079-105">ByConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="77079-105">ByConnectionInfo</span></span>
```
Get-AzureSqlDatabaseImportExportStatus -Username <String> -Password <String> -ServerName <String>
 -RequestId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="77079-106">ByRequestObject</span><span class="sxs-lookup"><span data-stu-id="77079-106">ByRequestObject</span></span>
```
Get-AzureSqlDatabaseImportExportStatus -Request <ImportExportRequest> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="77079-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="77079-107">DESCRIPTION</span></span>
<span data-ttu-id="77079-108">A **Get-AzureSqlDatabaseImportExportStatus** parancsmag az importálási vagy exportálási kérés állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="77079-108">The **Get-AzureSqlDatabaseImportExportStatus** cmdlet gets the status of an import or export request.</span></span>
<span data-ttu-id="77079-109">A Start-AzureSqlDatabaseImport vagy Start-AzureSqlDatabaseExport parancsmag kezdeményezi a kéréseket.</span><span class="sxs-lookup"><span data-stu-id="77079-109">The Start-AzureSqlDatabaseImport or Start-AzureSqlDatabaseExport cmdlet initiates requests.</span></span>
<span data-ttu-id="77079-110">Megadhatja a Request objektumot a *Request* paraméterrel, vagy a *kérelemazonosító* paraméterrel, illetve a *Felhasználónév* , a *jelszó* és a *kiszolgálónév* paraméter használatával is megadhatja a kérést.</span><span class="sxs-lookup"><span data-stu-id="77079-110">You can specify the request object by using the *Request* parameter, or you can identify the request by using the *RequestId* parameter and the *Username* , *Password* , and *ServerName* parameters.</span></span>

## <span data-ttu-id="77079-111">Példák</span><span class="sxs-lookup"><span data-stu-id="77079-111">EXAMPLES</span></span>

### <span data-ttu-id="77079-112">Példa 1: exportálási kérés állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="77079-112">Example 1: Get the status of an export request</span></span>
```
PS C:\> $ExportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
PS C:\> Get-AzureSqlDatabaseImportExportStatus -Request $ExportRequest
```

<span data-ttu-id="77079-113">Az első parancs létrehoz egy exportálási kérést, majd a $ExportRequest változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="77079-113">The first command creates an export request, and then stores it in the $ExportRequest variable.</span></span>

<span data-ttu-id="77079-114">A második parancs a $ExportRequestban tárolt exportálási kérés állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="77079-114">The second command gets the status of the export request stored in $ExportRequest.</span></span>

## <span data-ttu-id="77079-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="77079-115">PARAMETERS</span></span>

### <span data-ttu-id="77079-116">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="77079-116">-Password</span></span>
<span data-ttu-id="77079-117">Az Azure SQL adatbázis-kiszolgálóhoz való csatlakozáshoz szükséges jelszót adja meg.</span><span class="sxs-lookup"><span data-stu-id="77079-117">Specifies the password that is required to connect to the Azure SQL Database server.</span></span>
<span data-ttu-id="77079-118">Ezt a paramétert akkor kell megadnia, ha a *kérelemazonosító* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="77079-118">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77079-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="77079-119">-Profile</span></span>
<span data-ttu-id="77079-120">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="77079-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="77079-121">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="77079-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="77079-122">-Request (kérés)</span><span class="sxs-lookup"><span data-stu-id="77079-122">-Request</span></span>
<span data-ttu-id="77079-123">Egy **ImportExportRequest** objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="77079-123">Specifies an **ImportExportRequest** object.</span></span>
<span data-ttu-id="77079-124">Importálási vagy exportálási kérési objektum beolvasásához használja a Start-AzureSqlDatabaseImport vagy Start-AzureSqlDatabaseExport parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="77079-124">To obtain an import or export request object, use the Start-AzureSqlDatabaseImport or Start-AzureSqlDatabaseExport cmdlet.</span></span>

```yaml
Type: ImportExportRequest
Parameter Sets: ByRequestObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77079-125">-Kérelemazonosító</span><span class="sxs-lookup"><span data-stu-id="77079-125">-RequestId</span></span>
<span data-ttu-id="77079-126">Annak az importálási vagy exportálási műveletnek az GUID-azonosítóját adja meg, amelyre a parancsmag állapota bekerül.</span><span class="sxs-lookup"><span data-stu-id="77079-126">Specifies the GUID of the import or export operation for which this cmdlet gets status.</span></span>
<span data-ttu-id="77079-127">Ha ezt a paramétert adja meg, meg kell adnia a *Felhasználónév* , a *jelszó* és a *kiszolgálónév* paramétert.</span><span class="sxs-lookup"><span data-stu-id="77079-127">If you specify this parameter, you must specify the *UserName* , *Password* , and *ServerName* parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77079-128">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="77079-128">-ServerName</span></span>
<span data-ttu-id="77079-129">Az Azure SQL adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="77079-129">Specifies the name of the Azure SQL Database server.</span></span>
<span data-ttu-id="77079-130">Ezt a paramétert akkor kell megadnia, ha a *kérelemazonosító* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="77079-130">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77079-131">-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="77079-131">-Username</span></span>
<span data-ttu-id="77079-132">Annak a felhasználónak a nevét adja meg, amely az Azure SQL adatbázis-kiszolgálóhoz való csatlakozáshoz szükséges.</span><span class="sxs-lookup"><span data-stu-id="77079-132">Specifies the user name required to connect to the Azure SQL Database server.</span></span>
<span data-ttu-id="77079-133">Ezt a paramétert akkor kell megadnia, ha a *kérelemazonosító* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="77079-133">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77079-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77079-134">CommonParameters</span></span>
<span data-ttu-id="77079-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="77079-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77079-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77079-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77079-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="77079-137">INPUTS</span></span>

## <span data-ttu-id="77079-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77079-138">OUTPUTS</span></span>

### <span data-ttu-id="77079-139">Microsoft. WindowsAzure. Command. SqlDatabase. Services. ImportExport. StatusInfo</span><span class="sxs-lookup"><span data-stu-id="77079-139">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExport.StatusInfo</span></span>

## <span data-ttu-id="77079-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="77079-140">NOTES</span></span>

## <span data-ttu-id="77079-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77079-141">RELATED LINKS</span></span>

[<span data-ttu-id="77079-142">Azure SQL-adatbázis</span><span class="sxs-lookup"><span data-stu-id="77079-142">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="77079-143">Importálás exportálása adatbázis-állapot</span><span class="sxs-lookup"><span data-stu-id="77079-143">Get Import Export Database Status</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781289.aspx)

[<span data-ttu-id="77079-144">Azure SQL-adatbázisok műveletei</span><span class="sxs-lookup"><span data-stu-id="77079-144">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="77079-145">Start-AzureSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="77079-145">Start-AzureSqlDatabaseExport</span></span>](./Start-AzureSqlDatabaseExport.md)

[<span data-ttu-id="77079-146">Start-AzureSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="77079-146">Start-AzureSqlDatabaseImport</span></span>](./Start-AzureSqlDatabaseImport.md)


