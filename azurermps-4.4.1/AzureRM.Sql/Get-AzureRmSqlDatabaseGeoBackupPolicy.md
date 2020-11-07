---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: b8f7d04a709ebb14ed6a7a76cffab556c13d26ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680471"
---
# <span data-ttu-id="6c39d-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="6c39d-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="6c39d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6c39d-102">SYNOPSIS</span></span>
<span data-ttu-id="6c39d-103">Egy adatbázis térinformatikai biztonsági házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6c39d-103">Gets a database geo backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c39d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6c39d-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c39d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6c39d-105">DESCRIPTION</span></span>
<span data-ttu-id="6c39d-106">A **Get-AzureRmSqlDatabaseGeoBackupPolicy** parancsmag az adatbázishoz regisztrált geo biztonsági házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6c39d-106">The **Get-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="6c39d-107">Ez egy olyan Azure Backup-erőforrás, amely a biztonságimásolat-tárolási házirend definiálására szolgál.</span><span class="sxs-lookup"><span data-stu-id="6c39d-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="6c39d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="6c39d-108">EXAMPLES</span></span>

## <span data-ttu-id="6c39d-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6c39d-109">PARAMETERS</span></span>

### <span data-ttu-id="6c39d-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6c39d-110">-DatabaseName</span></span>
<span data-ttu-id="6c39d-111">Annak az adatbázisnak a neve, amelyhez a parancsmag a Geo biztonsági házirendet kapja.</span><span class="sxs-lookup"><span data-stu-id="6c39d-111">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

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

### <span data-ttu-id="6c39d-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c39d-112">-ResourceGroupName</span></span>
<span data-ttu-id="6c39d-113">Az adatbázist tartalmazó kiszolgáló erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c39d-113">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="6c39d-114">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="6c39d-114">-ServerName</span></span>
<span data-ttu-id="6c39d-115">Az adatbázist tároló kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c39d-115">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="6c39d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c39d-116">-DefaultProfile</span></span>
<span data-ttu-id="6c39d-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6c39d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c39d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c39d-118">CommonParameters</span></span>
<span data-ttu-id="6c39d-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6c39d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c39d-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c39d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c39d-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c39d-121">INPUTS</span></span>

## <span data-ttu-id="6c39d-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c39d-122">OUTPUTS</span></span>

## <span data-ttu-id="6c39d-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6c39d-123">NOTES</span></span>

## <span data-ttu-id="6c39d-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6c39d-124">RELATED LINKS</span></span>

[<span data-ttu-id="6c39d-125">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="6c39d-125">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzureRmSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="6c39d-126">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="6c39d-126">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
