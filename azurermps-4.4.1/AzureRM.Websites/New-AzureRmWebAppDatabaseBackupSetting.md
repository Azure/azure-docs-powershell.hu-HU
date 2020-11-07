---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppDatabaseBackupSetting.md
ms.openlocfilehash: d8662f0a3f9ff10fccd9d38a2d5397bf32ea6b8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680455"
---
# <span data-ttu-id="f289b-101">New-AzureRmWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="f289b-101">New-AzureRmWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="f289b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f289b-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f289b-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f289b-103">SYNTAX</span></span>

```
New-AzureRmWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f289b-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="f289b-104">DESCRIPTION</span></span>
<span data-ttu-id="f289b-105">A **New-AzureRmWebAppDatabaseBackupSetting** parancsmag új Azure Web App biztonsági mentési beállítást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f289b-105">The **New-AzureRmWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="f289b-106">Példák</span><span class="sxs-lookup"><span data-stu-id="f289b-106">EXAMPLES</span></span>

### <span data-ttu-id="f289b-107">1:</span><span class="sxs-lookup"><span data-stu-id="f289b-107">1:</span></span>
```
PS C:\> New-AzureRmWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="f289b-108">Adatbázis biztonsági mentési beállítását (kapcsolati karakterláncát) hozza létre a megadott SqlAzure, amely az erőforráscsoport alapértelmezett ContosoWebApp (web-WestUS) tartozik.</span><span class="sxs-lookup"><span data-stu-id="f289b-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="f289b-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f289b-109">PARAMETERS</span></span>

### <span data-ttu-id="f289b-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="f289b-110">-ConnectionString</span></span>
<span data-ttu-id="f289b-111">Kapcsolati karakterlánc</span><span class="sxs-lookup"><span data-stu-id="f289b-111">Connection String</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f289b-112">-ConnectionStringName</span><span class="sxs-lookup"><span data-stu-id="f289b-112">-ConnectionStringName</span></span>
<span data-ttu-id="f289b-113">Kapcsolati karakterlánc neve</span><span class="sxs-lookup"><span data-stu-id="f289b-113">Connection String Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f289b-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="f289b-114">-DatabaseType</span></span>
<span data-ttu-id="f289b-115">Adatbázis típusa (például "SqlAzure" vagy "MySql")</span><span class="sxs-lookup"><span data-stu-id="f289b-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f289b-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f289b-116">-Name</span></span>
<span data-ttu-id="f289b-117">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="f289b-117">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f289b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f289b-118">-DefaultProfile</span></span>
<span data-ttu-id="f289b-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f289b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f289b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f289b-120">CommonParameters</span></span>
<span data-ttu-id="f289b-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f289b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f289b-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f289b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f289b-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f289b-123">INPUTS</span></span>

## <span data-ttu-id="f289b-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f289b-124">OUTPUTS</span></span>

### <span data-ttu-id="f289b-125">Microsoft. Azure. Management. WebSites. models. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="f289b-125">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="f289b-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f289b-126">NOTES</span></span>

## <span data-ttu-id="f289b-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f289b-127">RELATED LINKS</span></span>

