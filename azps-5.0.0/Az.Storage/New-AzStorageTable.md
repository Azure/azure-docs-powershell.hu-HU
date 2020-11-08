---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
ms.openlocfilehash: 0f46570858368a821d176a5f4e0a907c8a56b49c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195056"
---
# <span data-ttu-id="9ac61-101">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="9ac61-101">New-AzStorageTable</span></span>

## <span data-ttu-id="9ac61-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9ac61-102">SYNOPSIS</span></span>
<span data-ttu-id="9ac61-103">Tároló táblát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9ac61-103">Creates a storage table.</span></span>

## <span data-ttu-id="9ac61-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9ac61-104">SYNTAX</span></span>

```
New-AzStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ac61-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9ac61-105">DESCRIPTION</span></span>
<span data-ttu-id="9ac61-106">A **New-AzStorageTable** parancsmag létrehoz egy tárterület-táblát az Azure-ban tárolt tárolási fiókhoz társítva.</span><span class="sxs-lookup"><span data-stu-id="9ac61-106">The **New-AzStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="9ac61-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9ac61-107">EXAMPLES</span></span>

### <span data-ttu-id="9ac61-108">1. példa: Azure Storage Table létrehozása</span><span class="sxs-lookup"><span data-stu-id="9ac61-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzStorageTable -Name "tableabc"
```

<span data-ttu-id="9ac61-109">A parancs létrehozza a tableabc nevű tárterület-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="9ac61-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="9ac61-110">2. példa: több Azure Storage-tábla létrehozása</span><span class="sxs-lookup"><span data-stu-id="9ac61-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzStorageTable
```

<span data-ttu-id="9ac61-111">A parancs több táblát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9ac61-111">This command creates multiple tables.</span></span>
<span data-ttu-id="9ac61-112">A .NET **String** osztály **felosztott** metódusát használja, és a neveket átadja a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="9ac61-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="9ac61-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9ac61-113">PARAMETERS</span></span>

### <span data-ttu-id="9ac61-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="9ac61-114">-Context</span></span>
<span data-ttu-id="9ac61-115">A tárolási környezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="9ac61-115">Specifies the storage context.</span></span>
<span data-ttu-id="9ac61-116">A létrehozáshoz használhatja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="9ac61-116">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="9ac61-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ac61-117">-DefaultProfile</span></span>
<span data-ttu-id="9ac61-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9ac61-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ac61-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9ac61-119">-Name</span></span>
<span data-ttu-id="9ac61-120">Az új tábla nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9ac61-120">Specifies a name for the new table.</span></span>

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

### <span data-ttu-id="9ac61-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ac61-121">CommonParameters</span></span>
<span data-ttu-id="9ac61-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9ac61-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ac61-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ac61-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ac61-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ac61-124">INPUTS</span></span>

### <span data-ttu-id="9ac61-125">System. String</span><span class="sxs-lookup"><span data-stu-id="9ac61-125">System.String</span></span>

### <span data-ttu-id="9ac61-126">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9ac61-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9ac61-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ac61-127">OUTPUTS</span></span>

### <span data-ttu-id="9ac61-128">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="9ac61-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="9ac61-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9ac61-129">NOTES</span></span>

## <span data-ttu-id="9ac61-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ac61-130">RELATED LINKS</span></span>

[<span data-ttu-id="9ac61-131">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="9ac61-131">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)

[<span data-ttu-id="9ac61-132">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="9ac61-132">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)

