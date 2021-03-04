---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
ms.openlocfilehash: cfd8df9bc329ef252c28ef826b1ba68a1946bab4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925930"
---
# <span data-ttu-id="403ae-101">New-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="403ae-101">New-AzDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="403ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="403ae-102">SYNOPSIS</span></span>
<span data-ttu-id="403ae-103">Létrehoz egy új Kapcsolat adatai objektumot, amely megadja a kapcsolat kiszolgálótípusát és nevét.</span><span class="sxs-lookup"><span data-stu-id="403ae-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

## <span data-ttu-id="403ae-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="403ae-104">SYNTAX</span></span>

```
New-AzDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="403ae-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="403ae-105">DESCRIPTION</span></span>
<span data-ttu-id="403ae-106">A New-AzDataMigrationConnectionInfo parancsmag létrehoz egy új Kapcsolat adatai objektumot, amely megadja a kapcsolat kiszolgálótípusát.</span><span class="sxs-lookup"><span data-stu-id="403ae-106">The New-AzDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 

## <span data-ttu-id="403ae-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="403ae-107">EXAMPLES</span></span>

### <span data-ttu-id="403ae-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="403ae-108">Example 1</span></span>
```
PS C:\> New-AzDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

<span data-ttu-id="403ae-109">Az előző példa létrehoz egy új Kapcsolat adatai objektumot, amely ServerType-paraméterként SQL-et ad meg.</span><span class="sxs-lookup"><span data-stu-id="403ae-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>

## <span data-ttu-id="403ae-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="403ae-110">PARAMETERS</span></span>

### <span data-ttu-id="403ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="403ae-111">-DefaultProfile</span></span>
<span data-ttu-id="403ae-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="403ae-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="403ae-113">-ServerType</span><span class="sxs-lookup"><span data-stu-id="403ae-113">-ServerType</span></span>
<span data-ttu-id="403ae-114">Enum that describes server type to connect to.</span><span class="sxs-lookup"><span data-stu-id="403ae-114">Enum that describes server type to connect to.</span></span> <span data-ttu-id="403ae-115">Jelenleg az SQL Serverhez, az Azure SQL Felügyelt példányhoz, a MongoDb, a NaplósDb és az Azure SQL-adatbázishoz támogatott értékek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="403ae-115">Currently supported values are SQL for SQL Server, Azure SQL Managed Instance, MongoDb, CosmosDb and Azure SQL Database.</span></span> 

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

### <span data-ttu-id="403ae-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="403ae-116">CommonParameters</span></span>
<span data-ttu-id="403ae-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="403ae-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="403ae-118">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="403ae-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="403ae-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="403ae-119">INPUTS</span></span>

### <span data-ttu-id="403ae-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="403ae-120">None</span></span>

## <span data-ttu-id="403ae-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="403ae-121">OUTPUTS</span></span>

### <span data-ttu-id="403ae-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="403ae-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>

## <span data-ttu-id="403ae-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="403ae-123">NOTES</span></span>

## <span data-ttu-id="403ae-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="403ae-124">RELATED LINKS</span></span>
