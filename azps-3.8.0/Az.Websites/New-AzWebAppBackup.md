---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppBackup.md
ms.openlocfilehash: 36e8362551951dd068f8cafcd5430d069e8b5160
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010738"
---
# <span data-ttu-id="19307-101">New-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="19307-101">New-AzWebAppBackup</span></span>

## <span data-ttu-id="19307-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="19307-102">SYNOPSIS</span></span>

## <span data-ttu-id="19307-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="19307-103">SYNTAX</span></span>

### <span data-ttu-id="19307-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="19307-104">FromResourceName</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="19307-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="19307-105">FromWebApp</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="19307-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="19307-106">DESCRIPTION</span></span>
<span data-ttu-id="19307-107">A **New-AzWebAppBackup** parancsmag létrehoz egy Azure Web App biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="19307-107">The **New-AzWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="19307-108">Példák</span><span class="sxs-lookup"><span data-stu-id="19307-108">EXAMPLES</span></span>

### <span data-ttu-id="19307-109">1:</span><span class="sxs-lookup"><span data-stu-id="19307-109">1:</span></span>
```
PS C:\> New-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="19307-110">Biztonsági másolatot hoz létre a megadott app-ContosoWebApp, amely az erőforráscsoport alapértelmezett verziójában van – web-WestUS https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="19307-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="19307-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="19307-111">PARAMETERS</span></span>

### <span data-ttu-id="19307-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="19307-112">-BackupName</span></span>
<span data-ttu-id="19307-113">Biztonsági másolat neve</span><span class="sxs-lookup"><span data-stu-id="19307-113">Backup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19307-114">-Adatbázisok</span><span class="sxs-lookup"><span data-stu-id="19307-114">-Databases</span></span>
<span data-ttu-id="19307-115">DatabaseBackupSetting típusú adatbázisok []</span><span class="sxs-lookup"><span data-stu-id="19307-115">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19307-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19307-116">-DefaultProfile</span></span>
<span data-ttu-id="19307-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19307-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19307-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="19307-118">-Name</span></span>
<span data-ttu-id="19307-119">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="19307-119">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19307-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19307-120">-ResourceGroupName</span></span>
<span data-ttu-id="19307-121">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="19307-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19307-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="19307-122">-Slot</span></span>
<span data-ttu-id="19307-123">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="19307-123">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19307-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="19307-124">-StorageAccountUrl</span></span>
<span data-ttu-id="19307-125">A tárolási fiók URL-címe</span><span class="sxs-lookup"><span data-stu-id="19307-125">Storage Account Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19307-126">-WebApp</span><span class="sxs-lookup"><span data-stu-id="19307-126">-WebApp</span></span>
<span data-ttu-id="19307-127">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="19307-127">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19307-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19307-128">CommonParameters</span></span>
<span data-ttu-id="19307-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="19307-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19307-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19307-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19307-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="19307-131">INPUTS</span></span>

### <span data-ttu-id="19307-132">System. String</span><span class="sxs-lookup"><span data-stu-id="19307-132">System.String</span></span>

### <span data-ttu-id="19307-133">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="19307-133">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="19307-134">Microsoft. Azure. Management. WebSites. models. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="19307-134">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

## <span data-ttu-id="19307-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19307-135">OUTPUTS</span></span>

### <span data-ttu-id="19307-136">Microsoft. Azure. Command. WebApps. Parancsmags. WebApps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="19307-136">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="19307-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="19307-137">NOTES</span></span>

## <span data-ttu-id="19307-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19307-138">RELATED LINKS</span></span>
