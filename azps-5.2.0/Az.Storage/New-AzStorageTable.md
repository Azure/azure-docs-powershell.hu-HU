---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
ms.openlocfilehash: 0f46570858368a821d176a5f4e0a907c8a56b49c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324655"
---
# <span data-ttu-id="0a1f7-101">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="0a1f7-101">New-AzStorageTable</span></span>

## <span data-ttu-id="0a1f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a1f7-102">SYNOPSIS</span></span>
<span data-ttu-id="0a1f7-103">Tárolótáblát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0a1f7-103">Creates a storage table.</span></span>

## <span data-ttu-id="0a1f7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0a1f7-104">SYNTAX</span></span>

```
New-AzStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0a1f7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0a1f7-105">DESCRIPTION</span></span>
<span data-ttu-id="0a1f7-106">A **New-AzStorageTable** parancsmag létrehoz egy tártáblát, amely az Azure-beli tárfiókhoz van társítva.</span><span class="sxs-lookup"><span data-stu-id="0a1f7-106">The **New-AzStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="0a1f7-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0a1f7-107">EXAMPLES</span></span>

### <span data-ttu-id="0a1f7-108">1. példa: Azure-tártábla létrehozása</span><span class="sxs-lookup"><span data-stu-id="0a1f7-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzStorageTable -Name "tableabc"
```

<span data-ttu-id="0a1f7-109">Ez a parancs létrehoz egy tárolótáblát a tableabc nevével.</span><span class="sxs-lookup"><span data-stu-id="0a1f7-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="0a1f7-110">2. példa: Több Azure-tárterülettáblák létrehozása</span><span class="sxs-lookup"><span data-stu-id="0a1f7-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzStorageTable
```

<span data-ttu-id="0a1f7-111">Ez a parancs több táblát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0a1f7-111">This command creates multiple tables.</span></span>
<span data-ttu-id="0a1f7-112">A  **.NET-karakterláncosztály Felosztás** metódusát használja, majd átadja a neveket a folyamatnak.</span><span class="sxs-lookup"><span data-stu-id="0a1f7-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="0a1f7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a1f7-113">PARAMETERS</span></span>

### <span data-ttu-id="0a1f7-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0a1f7-114">-Context</span></span>
<span data-ttu-id="0a1f7-115">A tárterület környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="0a1f7-115">Specifies the storage context.</span></span>
<span data-ttu-id="0a1f7-116">A létrehozásához használhatja a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0a1f7-116">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0a1f7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a1f7-117">-DefaultProfile</span></span>
<span data-ttu-id="0a1f7-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0a1f7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a1f7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0a1f7-119">-Name</span></span>
<span data-ttu-id="0a1f7-120">Az új tábla nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a1f7-120">Specifies a name for the new table.</span></span>

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

### <span data-ttu-id="0a1f7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a1f7-121">CommonParameters</span></span>
<span data-ttu-id="0a1f7-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a1f7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a1f7-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a1f7-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a1f7-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a1f7-124">INPUTS</span></span>

### <span data-ttu-id="0a1f7-125">System.String</span><span class="sxs-lookup"><span data-stu-id="0a1f7-125">System.String</span></span>

### <span data-ttu-id="0a1f7-126">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0a1f7-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0a1f7-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a1f7-127">OUTPUTS</span></span>

### <span data-ttu-id="0a1f7-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="0a1f7-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="0a1f7-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0a1f7-129">NOTES</span></span>

## <span data-ttu-id="0a1f7-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a1f7-130">RELATED LINKS</span></span>

[<span data-ttu-id="0a1f7-131">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="0a1f7-131">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)

[<span data-ttu-id="0a1f7-132">Remove-AzstorageTable</span><span class="sxs-lookup"><span data-stu-id="0a1f7-132">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)


