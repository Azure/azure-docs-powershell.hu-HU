---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: 97460caebc50fdb05fce542b3c8b6c0ea83202b7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156170"
---
# <span data-ttu-id="0e963-101">Get-AzSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="0e963-101">Get-AzSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="0e963-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e963-102">SYNOPSIS</span></span>
<span data-ttu-id="0e963-103">Szinkronizálási ügynök által csatolt SQL Server-adatbázisokkal kapcsolatos információkat ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="0e963-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="0e963-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0e963-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e963-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0e963-105">DESCRIPTION</span></span>
<span data-ttu-id="0e963-106">A **Get-AzSqlSyncAgentLinkedDatabase** parancsmag szinkronizálási ügynök által csatolt SQL Server-adatbázisokkal kapcsolatos információkat ad vissza.</span><span class="sxs-lookup"><span data-stu-id="0e963-106">The **Get-AzSqlSyncAgentLinkedDatabase** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="0e963-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0e963-107">EXAMPLES</span></span>

### <span data-ttu-id="0e963-108">1. példa: A csatolt SQL Server-adatbázisok lekérte egy Azure SQL-szinkronizálási ügynökhöz.</span><span class="sxs-lookup"><span data-stu-id="0e963-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>

<span data-ttu-id="0e963-109">Az alábbi példa az Azure SQL-szinkronizálási ügynök által csatolt csatolt SQL Server-adatbázisokat adja vissza.</span><span class="sxs-lookup"><span data-stu-id="0e963-109">The following example returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlSyncAgentLinkedDatabase -ResourceGroupName MyResourceGroup -ServerName s1 -SyncAgentName 'SyncAgent01'
```

## <span data-ttu-id="0e963-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e963-110">PARAMETERS</span></span>

### <span data-ttu-id="0e963-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e963-111">-DefaultProfile</span></span>
<span data-ttu-id="0e963-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0e963-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e963-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e963-113">-ResourceGroupName</span></span>
<span data-ttu-id="0e963-114">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0e963-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="0e963-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0e963-115">-ServerName</span></span>
<span data-ttu-id="0e963-116">Annak az Azure SQL Servernek a neve, amelyben a szinkronizálási ügynök található.</span><span class="sxs-lookup"><span data-stu-id="0e963-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="0e963-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="0e963-117">-SyncAgentName</span></span>
<span data-ttu-id="0e963-118">A szinkronizálási ügynök neve.</span><span class="sxs-lookup"><span data-stu-id="0e963-118">The sync agent name.</span></span>

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

### <span data-ttu-id="0e963-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e963-119">CommonParameters</span></span>
<span data-ttu-id="0e963-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e963-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e963-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e963-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e963-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0e963-122">INPUTS</span></span>

### <span data-ttu-id="0e963-123">System.String</span><span class="sxs-lookup"><span data-stu-id="0e963-123">System.String</span></span>

## <span data-ttu-id="0e963-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e963-124">OUTPUTS</span></span>

### <span data-ttu-id="0e963-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="0e963-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="0e963-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0e963-126">NOTES</span></span>

## <span data-ttu-id="0e963-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e963-127">RELATED LINKS</span></span>
