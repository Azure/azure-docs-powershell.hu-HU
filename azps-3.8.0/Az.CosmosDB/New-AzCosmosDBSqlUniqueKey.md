---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
ms.openlocfilehash: e3c96cfd4051a186e0584d810088bc06a57ad862
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013633"
---
# <span data-ttu-id="fcb76-101">New-AzCosmosDBSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="fcb76-101">New-AzCosmosDBSqlUniqueKey</span></span>

## <span data-ttu-id="fcb76-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fcb76-102">SYNOPSIS</span></span>
<span data-ttu-id="fcb76-103">Új CosmosDB SQL-UniqueKey objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="fcb76-103">Creates a new CosmosDB Sql UniqueKey object.</span></span>

## <span data-ttu-id="fcb76-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fcb76-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcb76-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fcb76-105">DESCRIPTION</span></span>
<span data-ttu-id="fcb76-106">A **New-AzCosmosDBSqlUniqueKey** parancsmag új, PSUniqueKey típusú objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fcb76-106">The **New-AzCosmosDBSqlUniqueKey** cmdlet creates a new object of type PSUniqueKey.</span></span>

## <span data-ttu-id="fcb76-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fcb76-107">EXAMPLES</span></span>

### <span data-ttu-id="fcb76-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fcb76-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUniqueKey -Path {path}

Path
----
{path}
```

## <span data-ttu-id="fcb76-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fcb76-109">PARAMETERS</span></span>

### <span data-ttu-id="fcb76-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcb76-110">-DefaultProfile</span></span>
<span data-ttu-id="fcb76-111">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fcb76-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcb76-112">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="fcb76-112">-Path</span></span>
<span data-ttu-id="fcb76-113">Az elérésiút-értékek karakterláncának tömbje</span><span class="sxs-lookup"><span data-stu-id="fcb76-113">Array of string of path values</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcb76-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcb76-114">CommonParameters</span></span>
<span data-ttu-id="fcb76-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fcb76-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcb76-116">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fcb76-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcb76-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fcb76-117">INPUTS</span></span>

### <span data-ttu-id="fcb76-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="fcb76-118">None</span></span>

## <span data-ttu-id="fcb76-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fcb76-119">OUTPUTS</span></span>

### <span data-ttu-id="fcb76-120">Microsoft. Azure. Command. CosmosDB. models. PSSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="fcb76-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey</span></span>

## <span data-ttu-id="fcb76-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fcb76-121">NOTES</span></span>

## <span data-ttu-id="fcb76-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fcb76-122">RELATED LINKS</span></span>
