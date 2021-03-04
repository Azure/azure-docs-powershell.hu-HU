---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: d4296acd16b29640fa8925d8482cca012be27b73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940754"
---
# <span data-ttu-id="70d65-101">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="70d65-101">Get-AzStorageTable</span></span>

## <span data-ttu-id="70d65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70d65-102">SYNOPSIS</span></span>
<span data-ttu-id="70d65-103">A tárolótáblák listája.</span><span class="sxs-lookup"><span data-stu-id="70d65-103">Lists the storage tables.</span></span>

## <span data-ttu-id="70d65-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="70d65-104">SYNTAX</span></span>

### <span data-ttu-id="70d65-105">TableName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="70d65-105">TableName (Default)</span></span>
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="70d65-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="70d65-106">TablePrefix</span></span>
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="70d65-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="70d65-107">DESCRIPTION</span></span>
<span data-ttu-id="70d65-108">A **Get-AzStorageTable** parancsmag felsorolja az Azure-beli tárfiókhoz társított tártáblákat.</span><span class="sxs-lookup"><span data-stu-id="70d65-108">The **Get-AzStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="70d65-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="70d65-109">EXAMPLES</span></span>

### <span data-ttu-id="70d65-110">1. példa: Az összes Azure Storage-tábla felsorolása</span><span class="sxs-lookup"><span data-stu-id="70d65-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzStorageTable
```

<span data-ttu-id="70d65-111">Ez a parancs a Tárfiók összes tártábláját beveszi.</span><span class="sxs-lookup"><span data-stu-id="70d65-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="70d65-112">2. példa: Azure Storage-táblák felsorolása helyettesítő karakterrel</span><span class="sxs-lookup"><span data-stu-id="70d65-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzStorageTable -Name table*
```

<span data-ttu-id="70d65-113">Ez a parancs egy helyettesítő karaktert használ a táblával kezdődik nevű tárolótáblák be szerezze be.</span><span class="sxs-lookup"><span data-stu-id="70d65-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="70d65-114">3. példa: Azure Storage-táblák felsorolása táblanév előtaggal</span><span class="sxs-lookup"><span data-stu-id="70d65-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

<span data-ttu-id="70d65-115">Ez a parancs az *Előtag paraméter* segítségével beveszi a táblával kezdődik nevű tárolótáblákat.</span><span class="sxs-lookup"><span data-stu-id="70d65-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="70d65-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70d65-116">PARAMETERS</span></span>

### <span data-ttu-id="70d65-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="70d65-117">-Context</span></span>
<span data-ttu-id="70d65-118">A tárterület környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="70d65-118">Specifies the storage context.</span></span>
<span data-ttu-id="70d65-119">A létrehozásához használhatja a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="70d65-119">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="70d65-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70d65-120">-DefaultProfile</span></span>
<span data-ttu-id="70d65-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="70d65-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70d65-122">-Name</span><span class="sxs-lookup"><span data-stu-id="70d65-122">-Name</span></span>
<span data-ttu-id="70d65-123">A tábla nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="70d65-123">Specifies the table name.</span></span>
<span data-ttu-id="70d65-124">Ha a tábla neve üres, a parancsmag felsorolja az összes táblát.</span><span class="sxs-lookup"><span data-stu-id="70d65-124">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="70d65-125">Ellenkező esetben felsorolja az összes olyan táblát, amely megfelel a megadott névnek vagy a normál név mintának.</span><span class="sxs-lookup"><span data-stu-id="70d65-125">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

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

### <span data-ttu-id="70d65-126">-Előtag</span><span class="sxs-lookup"><span data-stu-id="70d65-126">-Prefix</span></span>
<span data-ttu-id="70d65-127">Megadja a lekért tábla vagy táblák nevében használt előtagot.</span><span class="sxs-lookup"><span data-stu-id="70d65-127">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="70d65-128">Ezzel a segítségével megkeresheti az összes olyan táblát, amely ugyanannak a karakterláncnak (például a táblának) az elején áll.</span><span class="sxs-lookup"><span data-stu-id="70d65-128">You can use this to find all tables that start with the same string, such as table.</span></span>

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

### <span data-ttu-id="70d65-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70d65-129">CommonParameters</span></span>
<span data-ttu-id="70d65-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70d65-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70d65-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70d65-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70d65-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="70d65-132">INPUTS</span></span>

### <span data-ttu-id="70d65-133">System.String</span><span class="sxs-lookup"><span data-stu-id="70d65-133">System.String</span></span>

### <span data-ttu-id="70d65-134">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="70d65-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="70d65-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70d65-135">OUTPUTS</span></span>

### <span data-ttu-id="70d65-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="70d65-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="70d65-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="70d65-137">NOTES</span></span>

## <span data-ttu-id="70d65-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70d65-138">RELATED LINKS</span></span>

[<span data-ttu-id="70d65-139">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="70d65-139">New-AzStorageTable</span></span>](./New-AzStorageTable.md)

[<span data-ttu-id="70d65-140">Remove-AzstorageTable</span><span class="sxs-lookup"><span data-stu-id="70d65-140">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)


