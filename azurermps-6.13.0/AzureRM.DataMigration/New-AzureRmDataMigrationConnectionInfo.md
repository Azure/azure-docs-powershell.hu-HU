---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
ms.openlocfilehash: 77559f5858c26d665d062f822a5c65258625bb14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672952"
---
# <span data-ttu-id="a4575-101">New-AzureRmDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="a4575-101">New-AzureRmDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="a4575-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4575-102">SYNOPSIS</span></span>
<span data-ttu-id="a4575-103">Új kapcsolati adatobjektumot hoz létre a kiszolgáló típusa és a kapcsolat neve mezőben.</span><span class="sxs-lookup"><span data-stu-id="a4575-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4575-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4575-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4575-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4575-105">DESCRIPTION</span></span>
<span data-ttu-id="a4575-106">A New-AzureRmDataMigrationConnectionInfo parancsmag létrehoz egy új kapcsolatot a kapcsolati adatok objektummal, amely a kapcsolat típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4575-106">The New-AzureRmDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 

## <span data-ttu-id="a4575-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a4575-107">EXAMPLES</span></span>

### <span data-ttu-id="a4575-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a4575-108">Example 1</span></span>
```
PS C:\> New-AzureRmDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

<span data-ttu-id="a4575-109">Az előző példa létrehoz egy új kapcsolati adatkapcsolatú objektumot, amely az SQL ServerType paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="a4575-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>

## <span data-ttu-id="a4575-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4575-110">PARAMETERS</span></span>

### <span data-ttu-id="a4575-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4575-111">-DefaultProfile</span></span>
<span data-ttu-id="a4575-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a4575-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4575-113">-ServerType</span><span class="sxs-lookup"><span data-stu-id="a4575-113">-ServerType</span></span>
<span data-ttu-id="a4575-114">A kiszolgálóhoz való csatlakozáshoz kapcsolódó Fájltípus leírása.</span><span class="sxs-lookup"><span data-stu-id="a4575-114">Enum that describes server type to connect to.</span></span> <span data-ttu-id="a4575-115">A jelenleg támogatott értékek az SQL Server, az Azure SQL-alapú SQL-példány és az Azure SQL-adatbázis.</span><span class="sxs-lookup"><span data-stu-id="a4575-115">Currently supported values are SQL for SQL Server, Azure SQL Managed Instance and Azure SQL Database.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ServerTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4575-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4575-116">CommonParameters</span></span>
<span data-ttu-id="a4575-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a4575-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4575-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4575-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4575-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4575-119">INPUTS</span></span>

### <span data-ttu-id="a4575-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="a4575-120">None</span></span>

## <span data-ttu-id="a4575-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4575-121">OUTPUTS</span></span>

### <span data-ttu-id="a4575-122">Microsoft. Azure. Management. DataMigration. models. ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="a4575-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>

## <span data-ttu-id="a4575-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4575-123">NOTES</span></span>

## <span data-ttu-id="a4575-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4575-124">RELATED LINKS</span></span>
