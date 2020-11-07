---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: 11c444e92c6377e0a0df5aaa324ee162647784a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679817"
---
# <span data-ttu-id="1cbf0-101">Get-AzureRmSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="1cbf0-101">Get-AzureRmSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="1cbf0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1cbf0-102">SYNOPSIS</span></span>
<span data-ttu-id="1cbf0-103">A Szinkronizáló ügynök által összekötött SQL Server-adatbázisokra vonatkozó információkat ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="1cbf0-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cbf0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1cbf0-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cbf0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1cbf0-105">DESCRIPTION</span></span>
<span data-ttu-id="1cbf0-106">A **Get-AzureRmSqlSyncAgentLinkedDatabases** parancsmag a Szinkronizáló ügynök által összekötött SQL Server-adatbázisokra vonatkozó adatokat ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="1cbf0-106">The **Get-AzureRmSqlSyncAgentLinkedDatabases** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="1cbf0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1cbf0-107">EXAMPLES</span></span>

### <span data-ttu-id="1cbf0-108">Példa 1: a kapcsolt SQL Server-adatbázisok beszerzése Azure SQL-szinkronizáló ügynökhöz.</span><span class="sxs-lookup"><span data-stu-id="1cbf0-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>
```
PS C:\> Get-AzureRmSqlSyncAgentLinkedDatabases -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01" | Format-List
SeverName                 : sever01
DatabaseId                : databaseId
DatabaseName              : database01
DatabaseType              : SQLServerDatabase
Description               : 
UserName                  : myAccount
```

<span data-ttu-id="1cbf0-109">Ez a parancs az Azure SQL Sync Agent által összekötött SQL Server-adatbázisokat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="1cbf0-109">This command returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

## <span data-ttu-id="1cbf0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1cbf0-110">PARAMETERS</span></span>

### <span data-ttu-id="1cbf0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cbf0-111">-DefaultProfile</span></span>
<span data-ttu-id="1cbf0-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1cbf0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1cbf0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cbf0-113">-ResourceGroupName</span></span>
<span data-ttu-id="1cbf0-114">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1cbf0-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="1cbf0-115">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="1cbf0-115">-ServerName</span></span>
<span data-ttu-id="1cbf0-116">Annak az Azure SQL Server-kiszolgálónak a neve, amelyen a Szinkronizáló ügynök be van jelentkezve.</span><span class="sxs-lookup"><span data-stu-id="1cbf0-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="1cbf0-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="1cbf0-117">-SyncAgentName</span></span>
<span data-ttu-id="1cbf0-118">A Szinkronizáló ügynök neve.</span><span class="sxs-lookup"><span data-stu-id="1cbf0-118">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cbf0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cbf0-119">CommonParameters</span></span>
<span data-ttu-id="1cbf0-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1cbf0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cbf0-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cbf0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cbf0-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1cbf0-122">INPUTS</span></span>

### <span data-ttu-id="1cbf0-123">System. String</span><span class="sxs-lookup"><span data-stu-id="1cbf0-123">System.String</span></span>

## <span data-ttu-id="1cbf0-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1cbf0-124">OUTPUTS</span></span>

### <span data-ttu-id="1cbf0-125">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncAgentLinkedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="1cbf0-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="1cbf0-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1cbf0-126">NOTES</span></span>

## <span data-ttu-id="1cbf0-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1cbf0-127">RELATED LINKS</span></span>
