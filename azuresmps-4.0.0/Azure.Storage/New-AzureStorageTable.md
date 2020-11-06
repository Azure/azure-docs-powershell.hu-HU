---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9a58f869d5308b176a68614cbb2fa2fec401fa14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491612"
---
# <span data-ttu-id="98275-101">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="98275-101">New-AzureStorageTable</span></span>

## <span data-ttu-id="98275-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="98275-102">SYNOPSIS</span></span>
<span data-ttu-id="98275-103">Tároló táblát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="98275-103">Creates a storage table.</span></span>

## <span data-ttu-id="98275-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="98275-104">SYNTAX</span></span>

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="98275-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="98275-105">DESCRIPTION</span></span>
<span data-ttu-id="98275-106">A **New-AzureStorageTable** parancsmag létrehoz egy tárterület-táblát az Azure-ban tárolt tárolási fiókhoz társítva.</span><span class="sxs-lookup"><span data-stu-id="98275-106">The **New-AzureStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="98275-107">Példák</span><span class="sxs-lookup"><span data-stu-id="98275-107">EXAMPLES</span></span>

### <span data-ttu-id="98275-108">1. példa: Azure Storage Table létrehozása</span><span class="sxs-lookup"><span data-stu-id="98275-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

<span data-ttu-id="98275-109">A parancs létrehozza a tableabc nevű tárterület-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="98275-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="98275-110">2. példa: több Azure Storage-tábla létrehozása</span><span class="sxs-lookup"><span data-stu-id="98275-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

<span data-ttu-id="98275-111">A parancs több táblát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="98275-111">This command creates multiple tables.</span></span>
<span data-ttu-id="98275-112">A .NET **String** osztály **felosztott** metódusát használja, és a neveket átadja a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="98275-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="98275-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="98275-113">PARAMETERS</span></span>

### <span data-ttu-id="98275-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="98275-114">-Context</span></span>
<span data-ttu-id="98275-115">A tárolási környezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="98275-115">Specifies the storage context.</span></span>
<span data-ttu-id="98275-116">A létrehozáshoz használhatja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="98275-116">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98275-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="98275-117">-Name</span></span>
<span data-ttu-id="98275-118">Az új tábla nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="98275-118">Specifies a name for the new table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98275-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98275-119">CommonParameters</span></span>
<span data-ttu-id="98275-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="98275-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98275-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98275-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98275-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="98275-122">INPUTS</span></span>

## <span data-ttu-id="98275-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98275-123">OUTPUTS</span></span>

## <span data-ttu-id="98275-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="98275-124">NOTES</span></span>

## <span data-ttu-id="98275-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98275-125">RELATED LINKS</span></span>

[<span data-ttu-id="98275-126">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="98275-126">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

[<span data-ttu-id="98275-127">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="98275-127">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


