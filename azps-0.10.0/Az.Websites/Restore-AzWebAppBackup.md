---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/restore-Azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restore-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restore-AzWebAppBackup.md
ms.openlocfilehash: f93a173e79cb34c5603ce58fc3e03c92869a5d01
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842682"
---
# <span data-ttu-id="cafd9-101">Restore-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="cafd9-101">Restore-AzWebAppBackup</span></span>

## <span data-ttu-id="cafd9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cafd9-102">SYNOPSIS</span></span>

## <span data-ttu-id="cafd9-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cafd9-103">SYNTAX</span></span>

### <span data-ttu-id="cafd9-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="cafd9-104">FromResourceName</span></span>
```
Restore-AzWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="cafd9-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="cafd9-105">FromWebApp</span></span>
```
Restore-AzWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="cafd9-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="cafd9-106">DESCRIPTION</span></span>
<span data-ttu-id="cafd9-107">A **Restore-AzWebAppBackup** parancsmag visszaállítja az Azure Web App biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="cafd9-107">The **Restore-AzWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="cafd9-108">Példák</span><span class="sxs-lookup"><span data-stu-id="cafd9-108">EXAMPLES</span></span>

### <span data-ttu-id="cafd9-109">1:</span><span class="sxs-lookup"><span data-stu-id="cafd9-109">1:</span></span>
```
PS C:\> Restore-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="cafd9-110">A megadott app-ContosoWebApp biztonsági másolatának visszaállítása az erőforráscsoport alapértelmezett verziójában – web-WestUS a blob "myBlob"-on található https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="cafd9-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="cafd9-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cafd9-111">PARAMETERS</span></span>

### <span data-ttu-id="cafd9-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="cafd9-112">-AppServicePlan</span></span>
<span data-ttu-id="cafd9-113">A helyreállított alkalmazás alkalmazás-szolgáltatási tervének neve.</span><span class="sxs-lookup"><span data-stu-id="cafd9-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="cafd9-114">Ha a bal oldali üres, az alkalmazás a jelenlegi alkalmazás-szolgáltatási csomagot használja.</span><span class="sxs-lookup"><span data-stu-id="cafd9-114">If left empty, the app's current App Service Plan is used.</span></span>
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

### <span data-ttu-id="cafd9-115">-BlobName</span><span class="sxs-lookup"><span data-stu-id="cafd9-115">-BlobName</span></span>
<span data-ttu-id="cafd9-116">BLOB neve</span><span class="sxs-lookup"><span data-stu-id="cafd9-116">Blob Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cafd9-117">-Adatbázisok</span><span class="sxs-lookup"><span data-stu-id="cafd9-117">-Databases</span></span>
<span data-ttu-id="cafd9-118">DatabaseBackupSetting típusú adatbázisok []</span><span class="sxs-lookup"><span data-stu-id="cafd9-118">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cafd9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cafd9-119">-DefaultProfile</span></span>
<span data-ttu-id="cafd9-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cafd9-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cafd9-121">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="cafd9-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="cafd9-122">Ütköző állomásnevek mellőzése beállítás</span><span class="sxs-lookup"><span data-stu-id="cafd9-122">Ignore Conflicting HostNames Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cafd9-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cafd9-123">-Name</span></span>
<span data-ttu-id="cafd9-124">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="cafd9-124">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cafd9-125">-Átír</span><span class="sxs-lookup"><span data-stu-id="cafd9-125">-Overwrite</span></span>
<span data-ttu-id="cafd9-126">Felülírási lehetőség</span><span class="sxs-lookup"><span data-stu-id="cafd9-126">Overwrite Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cafd9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cafd9-127">-ResourceGroupName</span></span>
<span data-ttu-id="cafd9-128">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="cafd9-128">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cafd9-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="cafd9-129">-Slot</span></span>
<span data-ttu-id="cafd9-130">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="cafd9-130">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cafd9-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="cafd9-131">-StorageAccountUrl</span></span>
<span data-ttu-id="cafd9-132">A tárolási fiók URL-címe</span><span class="sxs-lookup"><span data-stu-id="cafd9-132">Storage Account Url</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cafd9-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="cafd9-133">-WebApp</span></span>
<span data-ttu-id="cafd9-134">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="cafd9-134">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cafd9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cafd9-135">CommonParameters</span></span>
<span data-ttu-id="cafd9-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cafd9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cafd9-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cafd9-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cafd9-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cafd9-138">INPUTS</span></span>

### <span data-ttu-id="cafd9-139">Webhely</span><span class="sxs-lookup"><span data-stu-id="cafd9-139">Site</span></span>
<span data-ttu-id="cafd9-140">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="cafd9-140">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="cafd9-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cafd9-141">OUTPUTS</span></span>

## <span data-ttu-id="cafd9-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cafd9-142">NOTES</span></span>

## <span data-ttu-id="cafd9-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cafd9-143">RELATED LINKS</span></span>

