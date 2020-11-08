---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
ms.openlocfilehash: bf91d1948b4040a35ee77f2a1111861a03076783
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182865"
---
# <span data-ttu-id="6c97a-101">New-AzCosmosDBSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="6c97a-101">New-AzCosmosDBSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="6c97a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6c97a-102">SYNOPSIS</span></span>
<span data-ttu-id="6c97a-103">Új CosmosDB-SqlUniqueKeyPolicy objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6c97a-103">Creates a new CosmosDB SqlUniqueKeyPolicy object.</span></span>

## <span data-ttu-id="6c97a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6c97a-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6c97a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6c97a-105">DESCRIPTION</span></span>
<span data-ttu-id="6c97a-106">A **New-AzCosmosDBSqlUniqueKeyPolicy** parancsmag új, PSSqlUniqueKeyPolicy típusú objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6c97a-106">The **New-AzCosmosDBSqlUniqueKeyPolicy** cmdlet creates a new object of type PSSqlUniqueKeyPolicy.</span></span>

## <span data-ttu-id="6c97a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6c97a-107">EXAMPLES</span></span>

### <span data-ttu-id="6c97a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6c97a-108">Example 1</span></span>
```powershell
PS C:\>New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey {psUniqueKey1, psUniqueKey2}

UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="6c97a-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6c97a-109">PARAMETERS</span></span>

### <span data-ttu-id="6c97a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c97a-110">-DefaultProfile</span></span>
<span data-ttu-id="6c97a-111">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6c97a-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c97a-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="6c97a-112">-UniqueKey</span></span>
<span data-ttu-id="6c97a-113">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="6c97a-113">Database name.</span></span>

```yaml
Type: PSSqlUniqueKey[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c97a-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c97a-114">CommonParameters</span></span>
<span data-ttu-id="6c97a-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6c97a-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c97a-116">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6c97a-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c97a-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c97a-117">INPUTS</span></span>

### <span data-ttu-id="6c97a-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="6c97a-118">None</span></span>

## <span data-ttu-id="6c97a-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c97a-119">OUTPUTS</span></span>

### <span data-ttu-id="6c97a-120">Microsoft. Azure. Command. CosmosDB. models. PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="6c97a-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="6c97a-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6c97a-121">NOTES</span></span>

## <span data-ttu-id="6c97a-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6c97a-122">RELATED LINKS</span></span>
