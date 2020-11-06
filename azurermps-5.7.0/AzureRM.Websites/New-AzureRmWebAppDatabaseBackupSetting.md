---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppDatabaseBackupSetting.md
ms.openlocfilehash: 7eea25d4b82dc8a424fea0cbd3e361014c77c396
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500323"
---
# <span data-ttu-id="03267-101">New-AzureRmWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="03267-101">New-AzureRmWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="03267-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="03267-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03267-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="03267-103">SYNTAX</span></span>

```
New-AzureRmWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03267-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="03267-104">DESCRIPTION</span></span>
<span data-ttu-id="03267-105">A **New-AzureRmWebAppDatabaseBackupSetting** parancsmag új Azure Web App biztonsági mentési beállítást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="03267-105">The **New-AzureRmWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="03267-106">Példák</span><span class="sxs-lookup"><span data-stu-id="03267-106">EXAMPLES</span></span>

### <span data-ttu-id="03267-107">1:</span><span class="sxs-lookup"><span data-stu-id="03267-107">1:</span></span>
```
PS C:\> New-AzureRmWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="03267-108">Adatbázis biztonsági mentési beállítását (kapcsolati karakterláncát) hozza létre a megadott SqlAzure, amely az erőforráscsoport alapértelmezett ContosoWebApp (web-WestUS) tartozik.</span><span class="sxs-lookup"><span data-stu-id="03267-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="03267-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="03267-109">PARAMETERS</span></span>

### <span data-ttu-id="03267-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="03267-110">-ConnectionString</span></span>
<span data-ttu-id="03267-111">Kapcsolati karakterlánc</span><span class="sxs-lookup"><span data-stu-id="03267-111">Connection String</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03267-112">-ConnectionStringName</span><span class="sxs-lookup"><span data-stu-id="03267-112">-ConnectionStringName</span></span>
<span data-ttu-id="03267-113">Kapcsolati karakterlánc neve</span><span class="sxs-lookup"><span data-stu-id="03267-113">Connection String Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03267-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="03267-114">-DatabaseType</span></span>
<span data-ttu-id="03267-115">Adatbázis típusa (például "SqlAzure" vagy "MySql")</span><span class="sxs-lookup"><span data-stu-id="03267-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03267-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03267-116">-DefaultProfile</span></span>
<span data-ttu-id="03267-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03267-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03267-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="03267-118">-Name</span></span>
<span data-ttu-id="03267-119">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="03267-119">WebApp Name</span></span>

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

### <span data-ttu-id="03267-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03267-120">CommonParameters</span></span>
<span data-ttu-id="03267-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="03267-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03267-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03267-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03267-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="03267-123">INPUTS</span></span>

### <span data-ttu-id="03267-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="03267-124">None</span></span>
<span data-ttu-id="03267-125">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="03267-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="03267-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03267-126">OUTPUTS</span></span>

### <span data-ttu-id="03267-127">Microsoft. Azure. Management. WebSites. models. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="03267-127">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="03267-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="03267-128">NOTES</span></span>

## <span data-ttu-id="03267-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03267-129">RELATED LINKS</span></span>

