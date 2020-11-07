---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppBackup.md
ms.openlocfilehash: a01c49ac6591cfec7d8087d664ba61ddd825ac5e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842750"
---
# <span data-ttu-id="c16e8-101">New-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="c16e8-101">New-AzWebAppBackup</span></span>

## <span data-ttu-id="c16e8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c16e8-102">SYNOPSIS</span></span>

## <span data-ttu-id="c16e8-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c16e8-103">SYNTAX</span></span>

### <span data-ttu-id="c16e8-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="c16e8-104">FromResourceName</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="c16e8-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="c16e8-105">FromWebApp</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="c16e8-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="c16e8-106">DESCRIPTION</span></span>
<span data-ttu-id="c16e8-107">A **New-AzWebAppBackup** parancsmag létrehoz egy Azure Web App biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="c16e8-107">The **New-AzWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="c16e8-108">Példák</span><span class="sxs-lookup"><span data-stu-id="c16e8-108">EXAMPLES</span></span>

### <span data-ttu-id="c16e8-109">1:</span><span class="sxs-lookup"><span data-stu-id="c16e8-109">1:</span></span>
```
PS C:\> New-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="c16e8-110">Biztonsági másolatot hoz létre a megadott app-ContosoWebApp, amely az erőforráscsoport alapértelmezett verziójában van – web-WestUS https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="c16e8-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="c16e8-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c16e8-111">PARAMETERS</span></span>

### <span data-ttu-id="c16e8-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="c16e8-112">-BackupName</span></span>
<span data-ttu-id="c16e8-113">Biztonsági másolat neve</span><span class="sxs-lookup"><span data-stu-id="c16e8-113">Backup Name</span></span>

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

### <span data-ttu-id="c16e8-114">-Adatbázisok</span><span class="sxs-lookup"><span data-stu-id="c16e8-114">-Databases</span></span>
<span data-ttu-id="c16e8-115">DatabaseBackupSetting típusú adatbázisok []</span><span class="sxs-lookup"><span data-stu-id="c16e8-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="c16e8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c16e8-116">-DefaultProfile</span></span>
<span data-ttu-id="c16e8-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c16e8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c16e8-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c16e8-118">-Name</span></span>
<span data-ttu-id="c16e8-119">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="c16e8-119">WebApp Name</span></span>

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

### <span data-ttu-id="c16e8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c16e8-120">-ResourceGroupName</span></span>
<span data-ttu-id="c16e8-121">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="c16e8-121">Resource Group Name</span></span>

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

### <span data-ttu-id="c16e8-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="c16e8-122">-Slot</span></span>
<span data-ttu-id="c16e8-123">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="c16e8-123">WebApp Slot Name</span></span>

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

### <span data-ttu-id="c16e8-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="c16e8-124">-StorageAccountUrl</span></span>
<span data-ttu-id="c16e8-125">A tárolási fiók URL-címe</span><span class="sxs-lookup"><span data-stu-id="c16e8-125">Storage Account Url</span></span>

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

### <span data-ttu-id="c16e8-126">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c16e8-126">-WebApp</span></span>
<span data-ttu-id="c16e8-127">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="c16e8-127">WebApp Object</span></span>

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

### <span data-ttu-id="c16e8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c16e8-128">CommonParameters</span></span>
<span data-ttu-id="c16e8-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c16e8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c16e8-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c16e8-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c16e8-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c16e8-131">INPUTS</span></span>

### <span data-ttu-id="c16e8-132">Webhely</span><span class="sxs-lookup"><span data-stu-id="c16e8-132">Site</span></span>
<span data-ttu-id="c16e8-133">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="c16e8-133">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="c16e8-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c16e8-134">OUTPUTS</span></span>

### <span data-ttu-id="c16e8-135">Microsoft. Azure. Command. WebApps. Parancsmags. WebApps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="c16e8-135">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="c16e8-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c16e8-136">NOTES</span></span>

## <span data-ttu-id="c16e8-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c16e8-137">RELATED LINKS</span></span>

