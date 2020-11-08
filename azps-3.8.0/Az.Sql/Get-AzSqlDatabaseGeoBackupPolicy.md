---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: d69d6c2976e71183fed07e2c18adc730d8ea6e61
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011546"
---
# <span data-ttu-id="44ed5-101">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="44ed5-101">Get-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="44ed5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="44ed5-102">SYNOPSIS</span></span>
<span data-ttu-id="44ed5-103">Egy adatbázis térinformatikai biztonsági házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="44ed5-103">Gets a database geo backup policy.</span></span>

## <span data-ttu-id="44ed5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="44ed5-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44ed5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="44ed5-105">DESCRIPTION</span></span>
<span data-ttu-id="44ed5-106">A **Get-AzSqlDatabaseGeoBackupPolicy** parancsmag az adatbázishoz regisztrált geo biztonsági házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="44ed5-106">The **Get-AzSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="44ed5-107">Ez egy olyan Azure Backup-erőforrás, amely a biztonságimásolat-tárolási házirend definiálására szolgál.</span><span class="sxs-lookup"><span data-stu-id="44ed5-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="44ed5-108">Példák</span><span class="sxs-lookup"><span data-stu-id="44ed5-108">EXAMPLES</span></span>

## <span data-ttu-id="44ed5-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="44ed5-109">PARAMETERS</span></span>

### <span data-ttu-id="44ed5-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="44ed5-110">-DatabaseName</span></span>
<span data-ttu-id="44ed5-111">Annak az adatbázisnak a neve, amelyhez a parancsmag a Geo biztonsági házirendet kapja.</span><span class="sxs-lookup"><span data-stu-id="44ed5-111">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

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

### <span data-ttu-id="44ed5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44ed5-112">-DefaultProfile</span></span>
<span data-ttu-id="44ed5-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="44ed5-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44ed5-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44ed5-114">-ResourceGroupName</span></span>
<span data-ttu-id="44ed5-115">Az adatbázist tartalmazó kiszolgáló erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="44ed5-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="44ed5-116">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="44ed5-116">-ServerName</span></span>
<span data-ttu-id="44ed5-117">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="44ed5-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="44ed5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44ed5-118">CommonParameters</span></span>
<span data-ttu-id="44ed5-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="44ed5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44ed5-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="44ed5-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44ed5-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="44ed5-121">INPUTS</span></span>

### <span data-ttu-id="44ed5-122">System. String</span><span class="sxs-lookup"><span data-stu-id="44ed5-122">System.String</span></span>

## <span data-ttu-id="44ed5-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44ed5-123">OUTPUTS</span></span>

### <span data-ttu-id="44ed5-124">Microsoft. Azure. Command. SQL. backup. Model. AzureSqlDatabaseGeoBackupPolicyModel</span><span class="sxs-lookup"><span data-stu-id="44ed5-124">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="44ed5-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="44ed5-125">NOTES</span></span>

## <span data-ttu-id="44ed5-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44ed5-126">RELATED LINKS</span></span>

[<span data-ttu-id="44ed5-127">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="44ed5-127">Set-AzSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="44ed5-128">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="44ed5-128">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
