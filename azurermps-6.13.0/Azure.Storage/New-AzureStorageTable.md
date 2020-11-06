---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
ms.openlocfilehash: 14f42ae951fe25f7594eb6e314ac65bb678e29c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492938"
---
# <span data-ttu-id="2f162-101">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="2f162-101">New-AzureStorageTable</span></span>

## <span data-ttu-id="2f162-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f162-102">SYNOPSIS</span></span>
<span data-ttu-id="2f162-103">Tároló táblát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2f162-103">Creates a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f162-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f162-104">SYNTAX</span></span>

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2f162-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f162-105">DESCRIPTION</span></span>
<span data-ttu-id="2f162-106">A **New-AzureStorageTable** parancsmag létrehoz egy tárterület-táblát az Azure-ban tárolt tárolási fiókhoz társítva.</span><span class="sxs-lookup"><span data-stu-id="2f162-106">The **New-AzureStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="2f162-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2f162-107">EXAMPLES</span></span>

### <span data-ttu-id="2f162-108">1. példa: Azure Storage Table létrehozása</span><span class="sxs-lookup"><span data-stu-id="2f162-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

<span data-ttu-id="2f162-109">A parancs létrehozza a tableabc nevű tárterület-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="2f162-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="2f162-110">2. példa: több Azure Storage-tábla létrehozása</span><span class="sxs-lookup"><span data-stu-id="2f162-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

<span data-ttu-id="2f162-111">A parancs több táblát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2f162-111">This command creates multiple tables.</span></span>
<span data-ttu-id="2f162-112">A .NET **String** osztály **felosztott** metódusát használja, és a neveket átadja a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="2f162-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="2f162-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f162-113">PARAMETERS</span></span>

### <span data-ttu-id="2f162-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="2f162-114">-Context</span></span>
<span data-ttu-id="2f162-115">A tárolási környezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f162-115">Specifies the storage context.</span></span>
<span data-ttu-id="2f162-116">A létrehozáshoz használhatja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2f162-116">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f162-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f162-117">-DefaultProfile</span></span>
<span data-ttu-id="2f162-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f162-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f162-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2f162-119">-Name</span></span>
<span data-ttu-id="2f162-120">Az új tábla nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f162-120">Specifies a name for the new table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f162-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f162-121">CommonParameters</span></span>
<span data-ttu-id="2f162-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f162-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f162-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f162-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f162-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f162-124">INPUTS</span></span>

### <span data-ttu-id="2f162-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2f162-125">System.String</span></span>

### <span data-ttu-id="2f162-126">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2f162-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2f162-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f162-127">OUTPUTS</span></span>

### <span data-ttu-id="2f162-128">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="2f162-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="2f162-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f162-129">NOTES</span></span>

## <span data-ttu-id="2f162-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f162-130">RELATED LINKS</span></span>

[<span data-ttu-id="2f162-131">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="2f162-131">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

[<span data-ttu-id="2f162-132">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="2f162-132">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


