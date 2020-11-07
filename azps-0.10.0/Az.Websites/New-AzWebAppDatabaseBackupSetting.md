---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
ms.openlocfilehash: 7ea02fb05c64c751fc339c889098724b2822a8b8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842730"
---
# <span data-ttu-id="f318b-101">New-AzWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="f318b-101">New-AzWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="f318b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f318b-102">SYNOPSIS</span></span>

## <span data-ttu-id="f318b-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f318b-103">SYNTAX</span></span>

```
New-AzWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f318b-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="f318b-104">DESCRIPTION</span></span>
<span data-ttu-id="f318b-105">A **New-AzWebAppDatabaseBackupSetting** parancsmag új Azure Web App biztonsági mentési beállítást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f318b-105">The **New-AzWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="f318b-106">Példák</span><span class="sxs-lookup"><span data-stu-id="f318b-106">EXAMPLES</span></span>

### <span data-ttu-id="f318b-107">1:</span><span class="sxs-lookup"><span data-stu-id="f318b-107">1:</span></span>
```
PS C:\> New-AzWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="f318b-108">Adatbázis biztonsági mentési beállítását (kapcsolati karakterláncát) hozza létre a megadott SqlAzure, amely az erőforráscsoport alapértelmezett ContosoWebApp (web-WestUS) tartozik.</span><span class="sxs-lookup"><span data-stu-id="f318b-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="f318b-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f318b-109">PARAMETERS</span></span>

### <span data-ttu-id="f318b-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="f318b-110">-ConnectionString</span></span>
<span data-ttu-id="f318b-111">Kapcsolati karakterlánc</span><span class="sxs-lookup"><span data-stu-id="f318b-111">Connection String</span></span>

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

### <span data-ttu-id="f318b-112">-ConnectionStringName</span><span class="sxs-lookup"><span data-stu-id="f318b-112">-ConnectionStringName</span></span>
<span data-ttu-id="f318b-113">Kapcsolati karakterlánc neve</span><span class="sxs-lookup"><span data-stu-id="f318b-113">Connection String Name</span></span>

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

### <span data-ttu-id="f318b-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="f318b-114">-DatabaseType</span></span>
<span data-ttu-id="f318b-115">Adatbázis típusa (például "SqlAzure" vagy "MySql")</span><span class="sxs-lookup"><span data-stu-id="f318b-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

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

### <span data-ttu-id="f318b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f318b-116">-DefaultProfile</span></span>
<span data-ttu-id="f318b-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f318b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f318b-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f318b-118">-Name</span></span>
<span data-ttu-id="f318b-119">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="f318b-119">WebApp Name</span></span>

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

### <span data-ttu-id="f318b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f318b-120">CommonParameters</span></span>
<span data-ttu-id="f318b-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f318b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f318b-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f318b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f318b-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f318b-123">INPUTS</span></span>

### <span data-ttu-id="f318b-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="f318b-124">None</span></span>
<span data-ttu-id="f318b-125">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="f318b-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f318b-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f318b-126">OUTPUTS</span></span>

### <span data-ttu-id="f318b-127">Microsoft. Azure. Management. WebSites. models. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="f318b-127">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="f318b-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f318b-128">NOTES</span></span>

## <span data-ttu-id="f318b-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f318b-129">RELATED LINKS</span></span>

