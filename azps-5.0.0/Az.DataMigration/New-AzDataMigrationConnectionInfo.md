---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
ms.openlocfilehash: e902785745ab22ab9bc1386fc2c6a2f9dd416b79
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297662"
---
# <span data-ttu-id="c4003-101">New-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="c4003-101">New-AzDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="c4003-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c4003-102">SYNOPSIS</span></span>
<span data-ttu-id="c4003-103">Új kapcsolati adatobjektumot hoz létre a kiszolgáló típusa és a kapcsolat neve mezőben.</span><span class="sxs-lookup"><span data-stu-id="c4003-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

## <span data-ttu-id="c4003-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c4003-104">SYNTAX</span></span>

```
New-AzDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4003-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c4003-105">DESCRIPTION</span></span>
<span data-ttu-id="c4003-106">A New-AzDataMigrationConnectionInfo parancsmag létrehoz egy új kapcsolatot a kapcsolati adatok objektummal, amely a kapcsolat típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c4003-106">The New-AzDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 

## <span data-ttu-id="c4003-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c4003-107">EXAMPLES</span></span>

### <span data-ttu-id="c4003-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c4003-108">Example 1</span></span>
```
PS C:\> New-AzDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

<span data-ttu-id="c4003-109">Az előző példa létrehoz egy új kapcsolati adatkapcsolatú objektumot, amely az SQL ServerType paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="c4003-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>

## <span data-ttu-id="c4003-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c4003-110">PARAMETERS</span></span>

### <span data-ttu-id="c4003-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4003-111">-DefaultProfile</span></span>
<span data-ttu-id="c4003-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c4003-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4003-113">-ServerType</span><span class="sxs-lookup"><span data-stu-id="c4003-113">-ServerType</span></span>
<span data-ttu-id="c4003-114">A kiszolgálóhoz való csatlakozáshoz kapcsolódó Fájltípus leírása.</span><span class="sxs-lookup"><span data-stu-id="c4003-114">Enum that describes server type to connect to.</span></span> <span data-ttu-id="c4003-115">Jelenleg támogatott értékek: SQL Server, Azure SQL-alapú, MongoDb, CosmosDb és Azure SQL-adatbázis.</span><span class="sxs-lookup"><span data-stu-id="c4003-115">Currently supported values are SQL for SQL Server, Azure SQL Managed Instance, MongoDb, CosmosDb and Azure SQL Database.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ServerTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: SQL, MongoDb, SQLMI

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4003-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4003-116">CommonParameters</span></span>
<span data-ttu-id="c4003-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c4003-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4003-118">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4003-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4003-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4003-119">INPUTS</span></span>

### <span data-ttu-id="c4003-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="c4003-120">None</span></span>

## <span data-ttu-id="c4003-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4003-121">OUTPUTS</span></span>

### <span data-ttu-id="c4003-122">Microsoft. Azure. Management. DataMigration. models. ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="c4003-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>

## <span data-ttu-id="c4003-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c4003-123">NOTES</span></span>

## <span data-ttu-id="c4003-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4003-124">RELATED LINKS</span></span>
