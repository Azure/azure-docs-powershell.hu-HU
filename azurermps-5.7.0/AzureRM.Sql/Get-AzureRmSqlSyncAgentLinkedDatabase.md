---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: 8fceaa92f14c6218d723b7fa7153970f118855a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679656"
---
# <span data-ttu-id="c7ef6-101">Get-AzureRmSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="c7ef6-101">Get-AzureRmSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="c7ef6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c7ef6-102">SYNOPSIS</span></span>
<span data-ttu-id="c7ef6-103">A Szinkronizáló ügynök által összekötött SQL Server-adatbázisokra vonatkozó információkat ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="c7ef6-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7ef6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c7ef6-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7ef6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c7ef6-105">DESCRIPTION</span></span>
<span data-ttu-id="c7ef6-106">A **Get-AzureRmSqlSyncAgentLinkedDatabases** parancsmag a Szinkronizáló ügynök által összekötött SQL Server-adatbázisokra vonatkozó adatokat ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="c7ef6-106">The **Get-AzureRmSqlSyncAgentLinkedDatabases** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="c7ef6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c7ef6-107">EXAMPLES</span></span>

### <span data-ttu-id="c7ef6-108">Példa 1: a kapcsolt SQL Server-adatbázisok beszerzése Azure SQL-szinkronizáló ügynökhöz.</span><span class="sxs-lookup"><span data-stu-id="c7ef6-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>
```
PS C:\> Get-AzureRmSqlSyncAgentLinkedDatabases -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01" | Format-List
SeverName                 : sever01
DatabaseId                : databaseId
DatabaseName              : database01
DatabaseType              : SQLServerDatabase
Description               : 
UserName                  : myAccount
```

<span data-ttu-id="c7ef6-109">Ez a parancs az Azure SQL Sync Agent által összekötött SQL Server-adatbázisokat jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="c7ef6-109">This command returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

## <span data-ttu-id="c7ef6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c7ef6-110">PARAMETERS</span></span>

### <span data-ttu-id="c7ef6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7ef6-111">-DefaultProfile</span></span>
<span data-ttu-id="c7ef6-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c7ef6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ef6-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7ef6-113">-ResourceGroupName</span></span>
<span data-ttu-id="c7ef6-114">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c7ef6-114">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ef6-115">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="c7ef6-115">-ServerName</span></span>
<span data-ttu-id="c7ef6-116">Annak az Azure SQL Server-kiszolgálónak a neve, amelyen a Szinkronizáló ügynök be van jelentkezve.</span><span class="sxs-lookup"><span data-stu-id="c7ef6-116">The name of the Azure SQL Server the sync agent is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ef6-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="c7ef6-117">-SyncAgentName</span></span>
<span data-ttu-id="c7ef6-118">A Szinkronizáló ügynök neve.</span><span class="sxs-lookup"><span data-stu-id="c7ef6-118">The sync agent name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ef6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7ef6-119">CommonParameters</span></span>
<span data-ttu-id="c7ef6-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c7ef6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7ef6-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7ef6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7ef6-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7ef6-122">INPUTS</span></span>

### <span data-ttu-id="c7ef6-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="c7ef6-123">None</span></span>
<span data-ttu-id="c7ef6-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="c7ef6-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c7ef6-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7ef6-125">OUTPUTS</span></span>

### <span data-ttu-id="c7ef6-126">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncAgentLinkedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="c7ef6-126">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="c7ef6-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c7ef6-127">NOTES</span></span>

## <span data-ttu-id="c7ef6-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7ef6-128">RELATED LINKS</span></span>
