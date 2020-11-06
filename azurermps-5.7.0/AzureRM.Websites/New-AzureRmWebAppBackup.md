---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppBackup.md
ms.openlocfilehash: 7784ea832faef9f73b46b04d6ad36bebe0e2f36d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500331"
---
# <span data-ttu-id="86ca9-101">New-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="86ca9-101">New-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="86ca9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86ca9-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86ca9-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86ca9-103">SYNTAX</span></span>

### <span data-ttu-id="86ca9-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="86ca9-104">FromResourceName</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="86ca9-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="86ca9-105">FromWebApp</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="86ca9-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="86ca9-106">DESCRIPTION</span></span>
<span data-ttu-id="86ca9-107">A **New-AzureRmWebAppBackup** parancsmag létrehoz egy Azure Web App biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="86ca9-107">The **New-AzureRmWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="86ca9-108">Példák</span><span class="sxs-lookup"><span data-stu-id="86ca9-108">EXAMPLES</span></span>

### <span data-ttu-id="86ca9-109">1:</span><span class="sxs-lookup"><span data-stu-id="86ca9-109">1:</span></span>
```
PS C:\> New-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="86ca9-110">Biztonsági másolatot hoz létre a megadott app-ContosoWebApp, amely az erőforráscsoport alapértelmezett verziójában van – web-WestUS https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="86ca9-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="86ca9-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86ca9-111">PARAMETERS</span></span>

### <span data-ttu-id="86ca9-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="86ca9-112">-BackupName</span></span>
<span data-ttu-id="86ca9-113">Biztonsági másolat neve</span><span class="sxs-lookup"><span data-stu-id="86ca9-113">Backup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86ca9-114">-Adatbázisok</span><span class="sxs-lookup"><span data-stu-id="86ca9-114">-Databases</span></span>
<span data-ttu-id="86ca9-115">DatabaseBackupSetting típusú adatbázisok []</span><span class="sxs-lookup"><span data-stu-id="86ca9-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="86ca9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86ca9-116">-DefaultProfile</span></span>
<span data-ttu-id="86ca9-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="86ca9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86ca9-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="86ca9-118">-Name</span></span>
<span data-ttu-id="86ca9-119">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="86ca9-119">WebApp Name</span></span>

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

### <span data-ttu-id="86ca9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86ca9-120">-ResourceGroupName</span></span>
<span data-ttu-id="86ca9-121">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="86ca9-121">Resource Group Name</span></span>

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

### <span data-ttu-id="86ca9-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="86ca9-122">-Slot</span></span>
<span data-ttu-id="86ca9-123">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="86ca9-123">WebApp Slot Name</span></span>

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

### <span data-ttu-id="86ca9-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="86ca9-124">-StorageAccountUrl</span></span>
<span data-ttu-id="86ca9-125">A tárolási fiók URL-címe</span><span class="sxs-lookup"><span data-stu-id="86ca9-125">Storage Account Url</span></span>

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

### <span data-ttu-id="86ca9-126">-WebApp</span><span class="sxs-lookup"><span data-stu-id="86ca9-126">-WebApp</span></span>
<span data-ttu-id="86ca9-127">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="86ca9-127">WebApp Object</span></span>

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

### <span data-ttu-id="86ca9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86ca9-128">CommonParameters</span></span>
<span data-ttu-id="86ca9-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86ca9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86ca9-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86ca9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86ca9-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86ca9-131">INPUTS</span></span>

### <span data-ttu-id="86ca9-132">Webhely</span><span class="sxs-lookup"><span data-stu-id="86ca9-132">Site</span></span>
<span data-ttu-id="86ca9-133">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="86ca9-133">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="86ca9-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86ca9-134">OUTPUTS</span></span>

### <span data-ttu-id="86ca9-135">Microsoft. Azure. Command. WebApps. Parancsmags. WebApps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="86ca9-135">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="86ca9-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86ca9-136">NOTES</span></span>

## <span data-ttu-id="86ca9-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86ca9-137">RELATED LINKS</span></span>

