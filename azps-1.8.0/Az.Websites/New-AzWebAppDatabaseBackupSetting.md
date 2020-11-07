---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
ms.openlocfilehash: 29d85284261b5885c90bcd50b1d54a580b53e10d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668327"
---
# <span data-ttu-id="75e3a-101">New-AzWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="75e3a-101">New-AzWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="75e3a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="75e3a-102">SYNOPSIS</span></span>

## <span data-ttu-id="75e3a-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="75e3a-103">SYNTAX</span></span>

```
New-AzWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75e3a-104">Leírás</span><span class="sxs-lookup"><span data-stu-id="75e3a-104">DESCRIPTION</span></span>
<span data-ttu-id="75e3a-105">A **New-AzWebAppDatabaseBackupSetting** parancsmag új Azure Web App biztonsági mentési beállítást hoz létre.</span><span class="sxs-lookup"><span data-stu-id="75e3a-105">The **New-AzWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="75e3a-106">Példák</span><span class="sxs-lookup"><span data-stu-id="75e3a-106">EXAMPLES</span></span>

### <span data-ttu-id="75e3a-107">1:</span><span class="sxs-lookup"><span data-stu-id="75e3a-107">1:</span></span>
```
PS C:\> New-AzWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="75e3a-108">Adatbázis biztonsági mentési beállítását (kapcsolati karakterláncát) hozza létre a megadott SqlAzure, amely az erőforráscsoport alapértelmezett ContosoWebApp (web-WestUS) tartozik.</span><span class="sxs-lookup"><span data-stu-id="75e3a-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="75e3a-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="75e3a-109">PARAMETERS</span></span>

### <span data-ttu-id="75e3a-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="75e3a-110">-ConnectionString</span></span>
<span data-ttu-id="75e3a-111">Kapcsolati karakterlánc</span><span class="sxs-lookup"><span data-stu-id="75e3a-111">Connection String</span></span>

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

### <span data-ttu-id="75e3a-112">-ConnectionStringName</span><span class="sxs-lookup"><span data-stu-id="75e3a-112">-ConnectionStringName</span></span>
<span data-ttu-id="75e3a-113">Kapcsolati karakterlánc neve</span><span class="sxs-lookup"><span data-stu-id="75e3a-113">Connection String Name</span></span>

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

### <span data-ttu-id="75e3a-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="75e3a-114">-DatabaseType</span></span>
<span data-ttu-id="75e3a-115">Adatbázis típusa (például "SqlAzure" vagy "MySql")</span><span class="sxs-lookup"><span data-stu-id="75e3a-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

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

### <span data-ttu-id="75e3a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75e3a-116">-DefaultProfile</span></span>
<span data-ttu-id="75e3a-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="75e3a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75e3a-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="75e3a-118">-Name</span></span>
<span data-ttu-id="75e3a-119">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="75e3a-119">WebApp Name</span></span>

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

### <span data-ttu-id="75e3a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75e3a-120">CommonParameters</span></span>
<span data-ttu-id="75e3a-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="75e3a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75e3a-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75e3a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75e3a-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="75e3a-123">INPUTS</span></span>

### <span data-ttu-id="75e3a-124">System. String</span><span class="sxs-lookup"><span data-stu-id="75e3a-124">System.String</span></span>

## <span data-ttu-id="75e3a-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75e3a-125">OUTPUTS</span></span>

### <span data-ttu-id="75e3a-126">Microsoft. Azure. Management. WebSites. models. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="75e3a-126">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="75e3a-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="75e3a-127">NOTES</span></span>

## <span data-ttu-id="75e3a-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75e3a-128">RELATED LINKS</span></span>
