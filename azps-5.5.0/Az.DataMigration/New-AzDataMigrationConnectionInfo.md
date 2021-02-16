---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
ms.openlocfilehash: e902785745ab22ab9bc1386fc2c6a2f9dd416b79
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144306"
---
# <span data-ttu-id="f3ebf-101">New-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="f3ebf-101">New-AzDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="f3ebf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3ebf-102">SYNOPSIS</span></span>
<span data-ttu-id="f3ebf-103">Létrehoz egy új Kapcsolat adatai objektumot, amely megadja a kapcsolat kiszolgálótípusát és nevét.</span><span class="sxs-lookup"><span data-stu-id="f3ebf-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

## <span data-ttu-id="f3ebf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f3ebf-104">SYNTAX</span></span>

```
New-AzDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3ebf-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f3ebf-105">DESCRIPTION</span></span>
<span data-ttu-id="f3ebf-106">A New-AzDataMigrationConnectionInfo parancsmag létrehoz egy új Kapcsolat adatai objektumot, amely megadja a kapcsolat kiszolgálótípusát.</span><span class="sxs-lookup"><span data-stu-id="f3ebf-106">The New-AzDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 

## <span data-ttu-id="f3ebf-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f3ebf-107">EXAMPLES</span></span>

### <span data-ttu-id="f3ebf-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="f3ebf-108">Example 1</span></span>
```
PS C:\> New-AzDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

<span data-ttu-id="f3ebf-109">Az előző példa létrehoz egy új Kapcsolat adatai objektumot, amely ServerType-paraméterként SQL-et ad meg.</span><span class="sxs-lookup"><span data-stu-id="f3ebf-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>

## <span data-ttu-id="f3ebf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3ebf-110">PARAMETERS</span></span>

### <span data-ttu-id="f3ebf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3ebf-111">-DefaultProfile</span></span>
<span data-ttu-id="f3ebf-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3ebf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3ebf-113">-ServerType</span><span class="sxs-lookup"><span data-stu-id="f3ebf-113">-ServerType</span></span>
<span data-ttu-id="f3ebf-114">Az a szám, amely leírja, hogy milyen kiszolgálótípushoz kell csatlakozni.</span><span class="sxs-lookup"><span data-stu-id="f3ebf-114">Enum that describes server type to connect to.</span></span> <span data-ttu-id="f3ebf-115">Jelenleg az SQL Serverhez, az Azure SQL Felügyelt példányhoz, a MongoDb, a NaplósDb és az Azure SQL-adatbázishoz támogatott értékek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="f3ebf-115">Currently supported values are SQL for SQL Server, Azure SQL Managed Instance, MongoDb, CosmosDb and Azure SQL Database.</span></span> 

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

### <span data-ttu-id="f3ebf-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3ebf-116">CommonParameters</span></span>
<span data-ttu-id="f3ebf-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3ebf-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3ebf-118">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3ebf-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3ebf-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3ebf-119">INPUTS</span></span>

### <span data-ttu-id="f3ebf-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="f3ebf-120">None</span></span>

## <span data-ttu-id="f3ebf-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3ebf-121">OUTPUTS</span></span>

### <span data-ttu-id="f3ebf-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="f3ebf-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>

## <span data-ttu-id="f3ebf-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f3ebf-123">NOTES</span></span>

## <span data-ttu-id="f3ebf-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3ebf-124">RELATED LINKS</span></span>
