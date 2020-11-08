---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
ms.openlocfilehash: 480532e2fffcc2b03a57c7d0a63cc2737844f652
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010733"
---
# <span data-ttu-id="98b10-101">New-AzWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="98b10-101">New-AzWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="98b10-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="98b10-102">SYNOPSIS</span></span>

## <span data-ttu-id="98b10-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="98b10-103">SYNTAX</span></span>

```
New-AzWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98b10-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="98b10-104">DESCRIPTION</span></span>
<span data-ttu-id="98b10-105">A **New-AzWebAppDatabaseBackupSetting** parancsmag új Azure Web App biztonsági mentési beállítást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="98b10-105">The **New-AzWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="98b10-106">Példák</span><span class="sxs-lookup"><span data-stu-id="98b10-106">EXAMPLES</span></span>

### <span data-ttu-id="98b10-107">1:</span><span class="sxs-lookup"><span data-stu-id="98b10-107">1:</span></span>
```
PS C:\> New-AzWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="98b10-108">Adatbázis biztonsági mentési beállítását (kapcsolati karakterláncát) hozza létre a megadott SqlAzure, amely az erőforráscsoport alapértelmezett ContosoWebApp (web-WestUS) tartozik.</span><span class="sxs-lookup"><span data-stu-id="98b10-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="98b10-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="98b10-109">PARAMETERS</span></span>

### <span data-ttu-id="98b10-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="98b10-110">-ConnectionString</span></span>
<span data-ttu-id="98b10-111">Kapcsolati karakterlánc</span><span class="sxs-lookup"><span data-stu-id="98b10-111">Connection String</span></span>

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

### <span data-ttu-id="98b10-112">-ConnectionStringName</span><span class="sxs-lookup"><span data-stu-id="98b10-112">-ConnectionStringName</span></span>
<span data-ttu-id="98b10-113">Kapcsolati karakterlánc neve</span><span class="sxs-lookup"><span data-stu-id="98b10-113">Connection String Name</span></span>

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

### <span data-ttu-id="98b10-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="98b10-114">-DatabaseType</span></span>
<span data-ttu-id="98b10-115">Adatbázis típusa (például "SqlAzure" vagy "MySql")</span><span class="sxs-lookup"><span data-stu-id="98b10-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

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

### <span data-ttu-id="98b10-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98b10-116">-DefaultProfile</span></span>
<span data-ttu-id="98b10-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="98b10-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98b10-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="98b10-118">-Name</span></span>
<span data-ttu-id="98b10-119">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="98b10-119">WebApp Name</span></span>

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

### <span data-ttu-id="98b10-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98b10-120">CommonParameters</span></span>
<span data-ttu-id="98b10-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="98b10-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98b10-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98b10-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98b10-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="98b10-123">INPUTS</span></span>

### <span data-ttu-id="98b10-124">System. String</span><span class="sxs-lookup"><span data-stu-id="98b10-124">System.String</span></span>

## <span data-ttu-id="98b10-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98b10-125">OUTPUTS</span></span>

### <span data-ttu-id="98b10-126">Microsoft. Azure. Management. WebSites. models. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="98b10-126">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="98b10-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="98b10-127">NOTES</span></span>

## <span data-ttu-id="98b10-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98b10-128">RELATED LINKS</span></span>
