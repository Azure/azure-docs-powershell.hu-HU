---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
ms.openlocfilehash: ac25103ed8a933af4e118087371511842044b6a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496744"
---
# <span data-ttu-id="5e3b7-101">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="5e3b7-101">Get-AzureStorageTable</span></span>

## <span data-ttu-id="5e3b7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5e3b7-102">SYNOPSIS</span></span>
<span data-ttu-id="5e3b7-103">A tárolási táblák listája.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-103">Lists the storage tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e3b7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5e3b7-104">SYNTAX</span></span>

### <span data-ttu-id="5e3b7-105">Táblanév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5e3b7-105">TableName (Default)</span></span>
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="5e3b7-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="5e3b7-106">TablePrefix</span></span>
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="5e3b7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5e3b7-107">DESCRIPTION</span></span>
<span data-ttu-id="5e3b7-108">A **Get-AzureStorageTable** parancsmag az Azure-beli tárterület-fiókkal társított tárolási táblákat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-108">The **Get-AzureStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="5e3b7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5e3b7-109">EXAMPLES</span></span>

### <span data-ttu-id="5e3b7-110">1. példa: az összes Azure Storage Table listázása</span><span class="sxs-lookup"><span data-stu-id="5e3b7-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzureStorageTable
```

<span data-ttu-id="5e3b7-111">Ez a parancs a tárterület-fiókok minden tárolási tábláját beilleszti.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="5e3b7-112">2. példa: az Azure Storage Tables listázása helyettesítő karakterrel</span><span class="sxs-lookup"><span data-stu-id="5e3b7-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageTable -Name table*
```

<span data-ttu-id="5e3b7-113">Ez a parancs egy helyettesítő karaktert használ az olyan tárolási táblák beszerzéséhez, amelyek neve táblázattal kezdődik.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="5e3b7-114">3. példa: az Azure Storage Tables listázása táblanév előtaggal</span><span class="sxs-lookup"><span data-stu-id="5e3b7-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

<span data-ttu-id="5e3b7-115">Ez a parancs az *előtag* paraméterrel olyan tárolási táblákat kap, amelyeknek a neve táblázattal kezdődik.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="5e3b7-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5e3b7-116">PARAMETERS</span></span>

### <span data-ttu-id="5e3b7-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="5e3b7-117">-Context</span></span>
<span data-ttu-id="5e3b7-118">A tárolási környezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-118">Specifies the storage context.</span></span>
<span data-ttu-id="5e3b7-119">A létrehozáshoz használhatja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-119">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5e3b7-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5e3b7-120">-Name</span></span>
<span data-ttu-id="5e3b7-121">A táblázat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-121">Specifies the table name.</span></span>
<span data-ttu-id="5e3b7-122">Ha a táblázat neve üres, a parancsmag felsorolja az összes táblázatot.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-122">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="5e3b7-123">Ellenkező esetben az összes olyan táblát felsorolja, amely megfelel a megadott névnek vagy a normál név mintának.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-123">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

```yaml
Type: String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="5e3b7-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="5e3b7-124">-Prefix</span></span>
<span data-ttu-id="5e3b7-125">A bekapni kívánt tábla vagy táblák nevében használt előtagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-125">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="5e3b7-126">Ezzel az eszközzel megkeresheti az összes olyan táblát, amely ugyanazzal a karakterlánccal kezdődik, mint amilyen például a táblázat.</span><span class="sxs-lookup"><span data-stu-id="5e3b7-126">You can use this to find all tables that start with the same string, such as table.</span></span>

```yaml
Type: String
Parameter Sets: TablePrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e3b7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e3b7-127">CommonParameters</span></span>
<span data-ttu-id="5e3b7-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5e3b7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e3b7-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e3b7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e3b7-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e3b7-130">INPUTS</span></span>

### <span data-ttu-id="5e3b7-131">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5e3b7-131">IStorageContext</span></span>

<span data-ttu-id="5e3b7-132">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="5e3b7-132">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="5e3b7-133">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="5e3b7-133">String</span></span>

<span data-ttu-id="5e3b7-134">A "név" paraméter elfogadja a "string" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="5e3b7-134">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="5e3b7-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e3b7-135">OUTPUTS</span></span>

### <span data-ttu-id="5e3b7-136">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="5e3b7-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="5e3b7-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5e3b7-137">NOTES</span></span>

## <span data-ttu-id="5e3b7-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e3b7-138">RELATED LINKS</span></span>

[<span data-ttu-id="5e3b7-139">Új – AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="5e3b7-139">New-AzureStorageTable</span></span>](./New-AzureStorageTable.md)

[<span data-ttu-id="5e3b7-140">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="5e3b7-140">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


