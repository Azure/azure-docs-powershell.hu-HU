---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappdatabasebackupsetting
schema: 2.0.0
ms.openlocfilehash: f44b6f370b1431a5baf1a0686b4e893653327227
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850525"
---
# <span data-ttu-id="d9874-101">New-AzureRmWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="d9874-101">New-AzureRmWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="d9874-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d9874-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9874-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d9874-103">SYNTAX</span></span>

```
New-AzureRmWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9874-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="d9874-104">DESCRIPTION</span></span>
<span data-ttu-id="d9874-105">A **New-AzureRmWebAppDatabaseBackupSetting** parancsmag új Azure Web App biztonsági mentési beállítást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d9874-105">The **New-AzureRmWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="d9874-106">Példák</span><span class="sxs-lookup"><span data-stu-id="d9874-106">EXAMPLES</span></span>

### <span data-ttu-id="d9874-107">1:</span><span class="sxs-lookup"><span data-stu-id="d9874-107">1:</span></span>
```
PS C:\> New-AzureRmWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="d9874-108">Adatbázis biztonsági mentési beállítását (kapcsolati karakterláncát) hozza létre a megadott SqlAzure, amely az erőforráscsoport alapértelmezett ContosoWebApp (web-WestUS) tartozik.</span><span class="sxs-lookup"><span data-stu-id="d9874-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="d9874-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d9874-109">PARAMETERS</span></span>

### <span data-ttu-id="d9874-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="d9874-110">-ConnectionString</span></span>
<span data-ttu-id="d9874-111">Kapcsolati karakterlánc</span><span class="sxs-lookup"><span data-stu-id="d9874-111">Connection String</span></span>

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

### <span data-ttu-id="d9874-112">-ConnectionStringName</span><span class="sxs-lookup"><span data-stu-id="d9874-112">-ConnectionStringName</span></span>
<span data-ttu-id="d9874-113">Kapcsolati karakterlánc neve</span><span class="sxs-lookup"><span data-stu-id="d9874-113">Connection String Name</span></span>

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

### <span data-ttu-id="d9874-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="d9874-114">-DatabaseType</span></span>
<span data-ttu-id="d9874-115">Adatbázis típusa (például "SqlAzure" vagy "MySql")</span><span class="sxs-lookup"><span data-stu-id="d9874-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

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

### <span data-ttu-id="d9874-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9874-116">-DefaultProfile</span></span>
<span data-ttu-id="d9874-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d9874-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9874-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d9874-118">-Name</span></span>
<span data-ttu-id="d9874-119">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="d9874-119">WebApp Name</span></span>

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

### <span data-ttu-id="d9874-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9874-120">CommonParameters</span></span>
<span data-ttu-id="d9874-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d9874-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9874-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9874-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9874-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9874-123">INPUTS</span></span>

### <span data-ttu-id="d9874-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="d9874-124">None</span></span>
<span data-ttu-id="d9874-125">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="d9874-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d9874-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9874-126">OUTPUTS</span></span>

### <span data-ttu-id="d9874-127">Microsoft. Azure. Management. WebSites. models. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="d9874-127">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="d9874-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d9874-128">NOTES</span></span>

## <span data-ttu-id="d9874-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d9874-129">RELATED LINKS</span></span>

