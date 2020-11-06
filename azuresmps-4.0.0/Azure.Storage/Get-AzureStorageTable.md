---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f2bccab190fc27b5e97ecf3af502d3488f28998
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491715"
---
# <span data-ttu-id="28e70-101">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="28e70-101">Get-AzureStorageTable</span></span>

## <span data-ttu-id="28e70-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="28e70-102">SYNOPSIS</span></span>
<span data-ttu-id="28e70-103">A tárolási táblák listája.</span><span class="sxs-lookup"><span data-stu-id="28e70-103">Lists the storage tables.</span></span>

## <span data-ttu-id="28e70-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="28e70-104">SYNTAX</span></span>

### <span data-ttu-id="28e70-105">Táblanév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="28e70-105">TableName (Default)</span></span>
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="28e70-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="28e70-106">TablePrefix</span></span>
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="28e70-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="28e70-107">DESCRIPTION</span></span>
<span data-ttu-id="28e70-108">A **Get-AzureStorageTable** parancsmag az Azure-beli tárterület-fiókkal társított tárolási táblákat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="28e70-108">The **Get-AzureStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="28e70-109">Példák</span><span class="sxs-lookup"><span data-stu-id="28e70-109">EXAMPLES</span></span>

### <span data-ttu-id="28e70-110">1. példa: az összes Azure Storage Table listázása</span><span class="sxs-lookup"><span data-stu-id="28e70-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzureStorageTable
```

<span data-ttu-id="28e70-111">Ez a parancs a tárterület-fiókok minden tárolási tábláját beilleszti.</span><span class="sxs-lookup"><span data-stu-id="28e70-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="28e70-112">2. példa: az Azure Storage Tables listázása helyettesítő karakterrel</span><span class="sxs-lookup"><span data-stu-id="28e70-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageTable -Name table*
```

<span data-ttu-id="28e70-113">Ez a parancs egy helyettesítő karaktert használ az olyan tárolási táblák beszerzéséhez, amelyek neve táblázattal kezdődik.</span><span class="sxs-lookup"><span data-stu-id="28e70-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="28e70-114">3. példa: az Azure Storage Tables listázása táblanév előtaggal</span><span class="sxs-lookup"><span data-stu-id="28e70-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

<span data-ttu-id="28e70-115">Ez a parancs az *előtag* paraméterrel olyan tárolási táblákat kap, amelyeknek a neve táblázattal kezdődik.</span><span class="sxs-lookup"><span data-stu-id="28e70-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="28e70-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="28e70-116">PARAMETERS</span></span>

### <span data-ttu-id="28e70-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="28e70-117">-Context</span></span>
<span data-ttu-id="28e70-118">A tárolási környezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="28e70-118">Specifies the storage context.</span></span>
<span data-ttu-id="28e70-119">A létrehozáshoz használhatja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="28e70-119">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="28e70-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="28e70-120">-Name</span></span>
<span data-ttu-id="28e70-121">A táblázat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="28e70-121">Specifies the table name.</span></span>
<span data-ttu-id="28e70-122">Ha a táblázat neve üres, a parancsmag felsorolja az összes táblázatot.</span><span class="sxs-lookup"><span data-stu-id="28e70-122">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="28e70-123">Ellenkező esetben az összes olyan táblát felsorolja, amely megfelel a megadott névnek vagy a normál név mintának.</span><span class="sxs-lookup"><span data-stu-id="28e70-123">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

```yaml
Type: String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28e70-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="28e70-124">-Prefix</span></span>
<span data-ttu-id="28e70-125">A bekapni kívánt tábla vagy táblák nevében használt előtagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="28e70-125">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="28e70-126">Ezzel az eszközzel megkeresheti az összes olyan táblát, amely ugyanazzal a karakterlánccal kezdődik, mint amilyen például a táblázat.</span><span class="sxs-lookup"><span data-stu-id="28e70-126">You can use this to find all tables that start with the same string, such as table.</span></span>

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

### <span data-ttu-id="28e70-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28e70-127">CommonParameters</span></span>
<span data-ttu-id="28e70-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="28e70-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28e70-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28e70-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28e70-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="28e70-130">INPUTS</span></span>

## <span data-ttu-id="28e70-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="28e70-131">OUTPUTS</span></span>

## <span data-ttu-id="28e70-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="28e70-132">NOTES</span></span>

## <span data-ttu-id="28e70-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="28e70-133">RELATED LINKS</span></span>

[<span data-ttu-id="28e70-134">Új – AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="28e70-134">New-AzureStorageTable</span></span>](./New-AzureStorageTable.md)

[<span data-ttu-id="28e70-135">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="28e70-135">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


