---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
ms.openlocfilehash: c68d9afb7c9498bbf734abcc376e6f123ebb8ac3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501284"
---
# <span data-ttu-id="31015-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="31015-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="31015-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="31015-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31015-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="31015-103">SYNTAX</span></span>

### <span data-ttu-id="31015-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="31015-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

### <span data-ttu-id="31015-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="31015-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String>
 [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="31015-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="31015-106">DESCRIPTION</span></span>
<span data-ttu-id="31015-107">A **Restore-AzureRmWebAppBackup** parancsmag visszaállítja az Azure Web App biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="31015-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="31015-108">Példák</span><span class="sxs-lookup"><span data-stu-id="31015-108">EXAMPLES</span></span>

### <span data-ttu-id="31015-109">1:</span><span class="sxs-lookup"><span data-stu-id="31015-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="31015-110">A megadott app-ContosoWebApp biztonsági másolatának visszaállítása az erőforráscsoport alapértelmezett verziójában – web-WestUS a blob "myBlob"-on található https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="31015-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="31015-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="31015-111">PARAMETERS</span></span>

### <span data-ttu-id="31015-112">-BlobName</span><span class="sxs-lookup"><span data-stu-id="31015-112">-BlobName</span></span>
<span data-ttu-id="31015-113">BLOB neve</span><span class="sxs-lookup"><span data-stu-id="31015-113">Blob Name</span></span>

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

### <span data-ttu-id="31015-114">-Adatbázisok</span><span class="sxs-lookup"><span data-stu-id="31015-114">-Databases</span></span>
<span data-ttu-id="31015-115">DatabaseBackupSetting típusú adatbázisok []</span><span class="sxs-lookup"><span data-stu-id="31015-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="31015-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31015-116">-DefaultProfile</span></span>
<span data-ttu-id="31015-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="31015-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31015-118">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="31015-118">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="31015-119">Ütköző állomásnevek mellőzése beállítás</span><span class="sxs-lookup"><span data-stu-id="31015-119">Ignore Conflicting HostNames Option</span></span>

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

### <span data-ttu-id="31015-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="31015-120">-Name</span></span>
<span data-ttu-id="31015-121">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="31015-121">WebApp Name</span></span>

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

### <span data-ttu-id="31015-122">-Átír</span><span class="sxs-lookup"><span data-stu-id="31015-122">-Overwrite</span></span>
<span data-ttu-id="31015-123">Felülírási lehetőség</span><span class="sxs-lookup"><span data-stu-id="31015-123">Overwrite Option</span></span>

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

### <span data-ttu-id="31015-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31015-124">-ResourceGroupName</span></span>
<span data-ttu-id="31015-125">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="31015-125">Resource Group Name</span></span>

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

### <span data-ttu-id="31015-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="31015-126">-Slot</span></span>
<span data-ttu-id="31015-127">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="31015-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="31015-128">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="31015-128">-StorageAccountUrl</span></span>
<span data-ttu-id="31015-129">A tárolási fiók URL-címe</span><span class="sxs-lookup"><span data-stu-id="31015-129">Storage Account Url</span></span>

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

### <span data-ttu-id="31015-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="31015-130">-WebApp</span></span>
<span data-ttu-id="31015-131">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="31015-131">WebApp Object</span></span>

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

### <span data-ttu-id="31015-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31015-132">CommonParameters</span></span>
<span data-ttu-id="31015-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="31015-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31015-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31015-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31015-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="31015-135">INPUTS</span></span>

### <span data-ttu-id="31015-136">Webhely</span><span class="sxs-lookup"><span data-stu-id="31015-136">Site</span></span>
<span data-ttu-id="31015-137">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="31015-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="31015-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31015-138">OUTPUTS</span></span>

## <span data-ttu-id="31015-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="31015-139">NOTES</span></span>

## <span data-ttu-id="31015-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31015-140">RELATED LINKS</span></span>

