---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: 97460caebc50fdb05fce542b3c8b6c0ea83202b7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303278"
---
# <span data-ttu-id="3c9a0-101">Get-AzSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="3c9a0-101">Get-AzSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="3c9a0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3c9a0-102">SYNOPSIS</span></span>
<span data-ttu-id="3c9a0-103">A Szinkronizáló ügynök által összekötött SQL Server-adatbázisokra vonatkozó információkat ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="3c9a0-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="3c9a0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3c9a0-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c9a0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3c9a0-105">DESCRIPTION</span></span>
<span data-ttu-id="3c9a0-106">A **Get-AzSqlSyncAgentLinkedDatabase** parancsmag a Szinkronizáló ügynök által összekötött SQL Server-adatbázisokra vonatkozó adatokat ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="3c9a0-106">The **Get-AzSqlSyncAgentLinkedDatabase** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="3c9a0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3c9a0-107">EXAMPLES</span></span>

### <span data-ttu-id="3c9a0-108">Példa 1: a kapcsolt SQL Server-adatbázisok beszerzése Azure SQL-szinkronizáló ügynökhöz.</span><span class="sxs-lookup"><span data-stu-id="3c9a0-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>

<span data-ttu-id="3c9a0-109">Az alábbi példa az Azure SQL Sync Agent által létrehozott SQL Server-adatbázisokat számítja ki.</span><span class="sxs-lookup"><span data-stu-id="3c9a0-109">The following example returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlSyncAgentLinkedDatabase -ResourceGroupName MyResourceGroup -ServerName s1 -SyncAgentName 'SyncAgent01'
```

## <span data-ttu-id="3c9a0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3c9a0-110">PARAMETERS</span></span>

### <span data-ttu-id="3c9a0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c9a0-111">-DefaultProfile</span></span>
<span data-ttu-id="3c9a0-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3c9a0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c9a0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c9a0-113">-ResourceGroupName</span></span>
<span data-ttu-id="3c9a0-114">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3c9a0-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="3c9a0-115">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="3c9a0-115">-ServerName</span></span>
<span data-ttu-id="3c9a0-116">Annak az Azure SQL Server-kiszolgálónak a neve, amelyen a Szinkronizáló ügynök be van jelentkezve.</span><span class="sxs-lookup"><span data-stu-id="3c9a0-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="3c9a0-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="3c9a0-117">-SyncAgentName</span></span>
<span data-ttu-id="3c9a0-118">A Szinkronizáló ügynök neve.</span><span class="sxs-lookup"><span data-stu-id="3c9a0-118">The sync agent name.</span></span>

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

### <span data-ttu-id="3c9a0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c9a0-119">CommonParameters</span></span>
<span data-ttu-id="3c9a0-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3c9a0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c9a0-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3c9a0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c9a0-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c9a0-122">INPUTS</span></span>

### <span data-ttu-id="3c9a0-123">System. String</span><span class="sxs-lookup"><span data-stu-id="3c9a0-123">System.String</span></span>

## <span data-ttu-id="3c9a0-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c9a0-124">OUTPUTS</span></span>

### <span data-ttu-id="3c9a0-125">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncAgentLinkedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="3c9a0-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="3c9a0-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3c9a0-126">NOTES</span></span>

## <span data-ttu-id="3c9a0-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c9a0-127">RELATED LINKS</span></span>
