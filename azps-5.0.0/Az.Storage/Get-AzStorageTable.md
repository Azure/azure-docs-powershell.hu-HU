---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: d501faaebcc5e381dc2a7270c8b55b148e2812b4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186621"
---
# <span data-ttu-id="e1f29-101">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="e1f29-101">Get-AzStorageTable</span></span>

## <span data-ttu-id="e1f29-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e1f29-102">SYNOPSIS</span></span>
<span data-ttu-id="e1f29-103">A tárolási táblák listája.</span><span class="sxs-lookup"><span data-stu-id="e1f29-103">Lists the storage tables.</span></span>

## <span data-ttu-id="e1f29-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e1f29-104">SYNTAX</span></span>

### <span data-ttu-id="e1f29-105">Táblanév (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e1f29-105">TableName (Default)</span></span>
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1f29-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="e1f29-106">TablePrefix</span></span>
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1f29-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e1f29-107">DESCRIPTION</span></span>
<span data-ttu-id="e1f29-108">A **Get-AzStorageTable** parancsmag az Azure-beli tárterület-fiókkal társított tárolási táblákat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="e1f29-108">The **Get-AzStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="e1f29-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e1f29-109">EXAMPLES</span></span>

### <span data-ttu-id="e1f29-110">1. példa: az összes Azure Storage Table listázása</span><span class="sxs-lookup"><span data-stu-id="e1f29-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzStorageTable
```

<span data-ttu-id="e1f29-111">Ez a parancs a tárterület-fiókok minden tárolási tábláját beilleszti.</span><span class="sxs-lookup"><span data-stu-id="e1f29-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="e1f29-112">2. példa: az Azure Storage Tables listázása helyettesítő karakterrel</span><span class="sxs-lookup"><span data-stu-id="e1f29-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzStorageTable -Name table*
```

<span data-ttu-id="e1f29-113">Ez a parancs egy helyettesítő karaktert használ az olyan tárolási táblák beszerzéséhez, amelyek neve táblázattal kezdődik.</span><span class="sxs-lookup"><span data-stu-id="e1f29-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="e1f29-114">3. példa: az Azure Storage Tables listázása táblanév előtaggal</span><span class="sxs-lookup"><span data-stu-id="e1f29-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

<span data-ttu-id="e1f29-115">Ez a parancs az *előtag* paraméterrel olyan tárolási táblákat kap, amelyeknek a neve táblázattal kezdődik.</span><span class="sxs-lookup"><span data-stu-id="e1f29-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="e1f29-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e1f29-116">PARAMETERS</span></span>

### <span data-ttu-id="e1f29-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e1f29-117">-Context</span></span>
<span data-ttu-id="e1f29-118">A tárolási környezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1f29-118">Specifies the storage context.</span></span>
<span data-ttu-id="e1f29-119">A létrehozáshoz használhatja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e1f29-119">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e1f29-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1f29-120">-DefaultProfile</span></span>
<span data-ttu-id="e1f29-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1f29-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1f29-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e1f29-122">-Name</span></span>
<span data-ttu-id="e1f29-123">A táblázat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1f29-123">Specifies the table name.</span></span>
<span data-ttu-id="e1f29-124">Ha a táblázat neve üres, a parancsmag felsorolja az összes táblázatot.</span><span class="sxs-lookup"><span data-stu-id="e1f29-124">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="e1f29-125">Ellenkező esetben az összes olyan táblát felsorolja, amely megfelel a megadott névnek vagy a normál név mintának.</span><span class="sxs-lookup"><span data-stu-id="e1f29-125">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1f29-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="e1f29-126">-Prefix</span></span>
<span data-ttu-id="e1f29-127">A bekapni kívánt tábla vagy táblák nevében használt előtagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1f29-127">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="e1f29-128">Ezzel az eszközzel megkeresheti az összes olyan táblát, amely ugyanazzal a karakterlánccal kezdődik, mint amilyen például a táblázat.</span><span class="sxs-lookup"><span data-stu-id="e1f29-128">You can use this to find all tables that start with the same string, such as table.</span></span>

```yaml
Type: System.String
Parameter Sets: TablePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f29-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1f29-129">CommonParameters</span></span>
<span data-ttu-id="e1f29-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e1f29-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1f29-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1f29-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1f29-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1f29-132">INPUTS</span></span>

### <span data-ttu-id="e1f29-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e1f29-133">System.String</span></span>

### <span data-ttu-id="e1f29-134">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e1f29-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e1f29-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1f29-135">OUTPUTS</span></span>

### <span data-ttu-id="e1f29-136">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="e1f29-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="e1f29-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e1f29-137">NOTES</span></span>

## <span data-ttu-id="e1f29-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1f29-138">RELATED LINKS</span></span>

[<span data-ttu-id="e1f29-139">Új – AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="e1f29-139">New-AzStorageTable</span></span>](./New-AzStorageTable.md)

[<span data-ttu-id="e1f29-140">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="e1f29-140">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)

