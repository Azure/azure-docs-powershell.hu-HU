---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
ms.openlocfilehash: 53bb5f3a34cddf9e74bfb9d9c9f1bd1d109d8f6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496715"
---
# <span data-ttu-id="f3566-101">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="f3566-101">New-AzureStorageTable</span></span>

## <span data-ttu-id="f3566-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3566-102">SYNOPSIS</span></span>
<span data-ttu-id="f3566-103">Tároló táblát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f3566-103">Creates a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3566-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3566-104">SYNTAX</span></span>

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="f3566-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3566-105">DESCRIPTION</span></span>
<span data-ttu-id="f3566-106">A **New-AzureStorageTable** parancsmag létrehoz egy tárterület-táblát az Azure-ban tárolt tárolási fiókhoz társítva.</span><span class="sxs-lookup"><span data-stu-id="f3566-106">The **New-AzureStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="f3566-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f3566-107">EXAMPLES</span></span>

### <span data-ttu-id="f3566-108">1. példa: Azure Storage Table létrehozása</span><span class="sxs-lookup"><span data-stu-id="f3566-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

<span data-ttu-id="f3566-109">A parancs létrehozza a tableabc nevű tárterület-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="f3566-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="f3566-110">2. példa: több Azure Storage-tábla létrehozása</span><span class="sxs-lookup"><span data-stu-id="f3566-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

<span data-ttu-id="f3566-111">A parancs több táblát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f3566-111">This command creates multiple tables.</span></span>
<span data-ttu-id="f3566-112">A .NET **String** osztály **felosztott** metódusát használja, és a neveket átadja a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="f3566-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="f3566-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3566-113">PARAMETERS</span></span>

### <span data-ttu-id="f3566-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="f3566-114">-Context</span></span>
<span data-ttu-id="f3566-115">A tárolási környezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3566-115">Specifies the storage context.</span></span>
<span data-ttu-id="f3566-116">A létrehozáshoz használhatja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f3566-116">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f3566-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f3566-117">-Name</span></span>
<span data-ttu-id="f3566-118">Az új tábla nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3566-118">Specifies a name for the new table.</span></span>

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

### <span data-ttu-id="f3566-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3566-119">CommonParameters</span></span>
<span data-ttu-id="f3566-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f3566-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3566-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3566-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3566-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3566-122">INPUTS</span></span>

### <span data-ttu-id="f3566-123">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f3566-123">IStorageContext</span></span>

<span data-ttu-id="f3566-124">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f3566-124">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="f3566-125">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="f3566-125">String</span></span>

<span data-ttu-id="f3566-126">A "név" paraméter elfogadja a "string" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f3566-126">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="f3566-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3566-127">OUTPUTS</span></span>

### <span data-ttu-id="f3566-128">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="f3566-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="f3566-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3566-129">NOTES</span></span>

## <span data-ttu-id="f3566-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3566-130">RELATED LINKS</span></span>

[<span data-ttu-id="f3566-131">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="f3566-131">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

[<span data-ttu-id="f3566-132">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="f3566-132">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


