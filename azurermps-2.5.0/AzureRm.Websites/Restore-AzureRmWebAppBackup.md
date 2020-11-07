---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappbackup
schema: 2.0.0
ms.openlocfilehash: 9c28d9235eefe6c4f33537115b548137c5bc6c88
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850202"
---
# <span data-ttu-id="fc730-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="fc730-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="fc730-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc730-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc730-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc730-103">SYNTAX</span></span>

### <span data-ttu-id="fc730-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="fc730-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="fc730-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="fc730-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="fc730-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc730-106">DESCRIPTION</span></span>
<span data-ttu-id="fc730-107">A **Restore-AzureRmWebAppBackup** parancsmag visszaállítja az Azure Web App biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="fc730-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="fc730-108">Példák</span><span class="sxs-lookup"><span data-stu-id="fc730-108">EXAMPLES</span></span>

### <span data-ttu-id="fc730-109">1:</span><span class="sxs-lookup"><span data-stu-id="fc730-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="fc730-110">A megadott app-ContosoWebApp biztonsági másolatának visszaállítása az erőforráscsoport alapértelmezett verziójában – web-WestUS a blob "myBlob"-on található https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="fc730-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="fc730-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc730-111">PARAMETERS</span></span>

### <span data-ttu-id="fc730-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fc730-112">-AppServicePlan</span></span>
<span data-ttu-id="fc730-113">A helyreállított alkalmazás alkalmazás-szolgáltatási tervének neve.</span><span class="sxs-lookup"><span data-stu-id="fc730-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="fc730-114">Ha a bal oldali üres, az alkalmazás a jelenlegi alkalmazás-szolgáltatási csomagot használja.</span><span class="sxs-lookup"><span data-stu-id="fc730-114">If left empty, the app's current App Service Plan is used.</span></span>
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

### <span data-ttu-id="fc730-115">-BlobName</span><span class="sxs-lookup"><span data-stu-id="fc730-115">-BlobName</span></span>
<span data-ttu-id="fc730-116">BLOB neve</span><span class="sxs-lookup"><span data-stu-id="fc730-116">Blob Name</span></span>

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

### <span data-ttu-id="fc730-117">-Adatbázisok</span><span class="sxs-lookup"><span data-stu-id="fc730-117">-Databases</span></span>
<span data-ttu-id="fc730-118">DatabaseBackupSetting típusú adatbázisok []</span><span class="sxs-lookup"><span data-stu-id="fc730-118">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="fc730-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc730-119">-DefaultProfile</span></span>
<span data-ttu-id="fc730-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc730-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc730-121">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="fc730-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="fc730-122">Ütköző állomásnevek mellőzése beállítás</span><span class="sxs-lookup"><span data-stu-id="fc730-122">Ignore Conflicting HostNames Option</span></span>

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

### <span data-ttu-id="fc730-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fc730-123">-Name</span></span>
<span data-ttu-id="fc730-124">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="fc730-124">WebApp Name</span></span>

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

### <span data-ttu-id="fc730-125">-Átír</span><span class="sxs-lookup"><span data-stu-id="fc730-125">-Overwrite</span></span>
<span data-ttu-id="fc730-126">Felülírási lehetőség</span><span class="sxs-lookup"><span data-stu-id="fc730-126">Overwrite Option</span></span>

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

### <span data-ttu-id="fc730-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc730-127">-ResourceGroupName</span></span>
<span data-ttu-id="fc730-128">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="fc730-128">Resource Group Name</span></span>

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

### <span data-ttu-id="fc730-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="fc730-129">-Slot</span></span>
<span data-ttu-id="fc730-130">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="fc730-130">WebApp Slot Name</span></span>

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

### <span data-ttu-id="fc730-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="fc730-131">-StorageAccountUrl</span></span>
<span data-ttu-id="fc730-132">A tárolási fiók URL-címe</span><span class="sxs-lookup"><span data-stu-id="fc730-132">Storage Account Url</span></span>

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

### <span data-ttu-id="fc730-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="fc730-133">-WebApp</span></span>
<span data-ttu-id="fc730-134">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="fc730-134">WebApp Object</span></span>

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

### <span data-ttu-id="fc730-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc730-135">CommonParameters</span></span>
<span data-ttu-id="fc730-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc730-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc730-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc730-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc730-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc730-138">INPUTS</span></span>

### <span data-ttu-id="fc730-139">Webhely</span><span class="sxs-lookup"><span data-stu-id="fc730-139">Site</span></span>
<span data-ttu-id="fc730-140">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="fc730-140">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="fc730-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc730-141">OUTPUTS</span></span>

## <span data-ttu-id="fc730-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc730-142">NOTES</span></span>

## <span data-ttu-id="fc730-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc730-143">RELATED LINKS</span></span>

