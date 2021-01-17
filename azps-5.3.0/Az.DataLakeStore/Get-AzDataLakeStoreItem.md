---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
ms.openlocfilehash: ad741d955399b355534074737741b153d8d48690
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465840"
---
# <span data-ttu-id="9dd7f-101">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9dd7f-101">Get-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="9dd7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dd7f-102">SYNOPSIS</span></span>
<span data-ttu-id="9dd7f-103">A Data Lake Store-ban található fájl vagy mappa részleteinek lekérte.</span><span class="sxs-lookup"><span data-stu-id="9dd7f-103">Gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="9dd7f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9dd7f-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9dd7f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9dd7f-105">DESCRIPTION</span></span>
<span data-ttu-id="9dd7f-106">A **Get-AzDataLakeStoreItem** parancsmag a Data Lake Store-ban található fájl vagy mappa részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9dd7f-106">The **Get-AzDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="9dd7f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9dd7f-107">EXAMPLES</span></span>

### <span data-ttu-id="9dd7f-108">1. példa: Fájl részleteinek megtekintése a Data Lake Store-ból</span><span class="sxs-lookup"><span data-stu-id="9dd7f-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="9dd7f-109">Ez a parancs a Data Lake StoreTest.csv ból kapja meg a fájl részleteit.</span><span class="sxs-lookup"><span data-stu-id="9dd7f-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="9dd7f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9dd7f-110">PARAMETERS</span></span>

### <span data-ttu-id="9dd7f-111">-Account</span><span class="sxs-lookup"><span data-stu-id="9dd7f-111">-Account</span></span>
<span data-ttu-id="9dd7f-112">A Data Lake Store-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9dd7f-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dd7f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dd7f-113">-DefaultProfile</span></span>
<span data-ttu-id="9dd7f-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9dd7f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd7f-115">-Path</span><span class="sxs-lookup"><span data-stu-id="9dd7f-115">-Path</span></span>
<span data-ttu-id="9dd7f-116">Azt az elérési utat adja meg a Data Lake Store-ban, amelyből a gyökérkönyvtártól (/) kezdve meg kell kapnia egy elem részleteit.</span><span class="sxs-lookup"><span data-stu-id="9dd7f-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dd7f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dd7f-117">CommonParameters</span></span>
<span data-ttu-id="9dd7f-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dd7f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dd7f-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dd7f-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dd7f-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9dd7f-120">INPUTS</span></span>

### <span data-ttu-id="9dd7f-121">System.String</span><span class="sxs-lookup"><span data-stu-id="9dd7f-121">System.String</span></span>

### <span data-ttu-id="9dd7f-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="9dd7f-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="9dd7f-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9dd7f-123">OUTPUTS</span></span>

### <span data-ttu-id="9dd7f-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9dd7f-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="9dd7f-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9dd7f-125">NOTES</span></span>

## <span data-ttu-id="9dd7f-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9dd7f-126">RELATED LINKS</span></span>

[<span data-ttu-id="9dd7f-127">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9dd7f-127">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="9dd7f-128">Get-AzDataLakeStoreDataItem</span><span class="sxs-lookup"><span data-stu-id="9dd7f-128">Get-AzDataLakeStoreChildItem</span></span>](./Get-AzDataLakeStoreChildItem.md)

[<span data-ttu-id="9dd7f-129">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9dd7f-129">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="9dd7f-130">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9dd7f-130">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="9dd7f-131">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9dd7f-131">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="9dd7f-132">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9dd7f-132">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="9dd7f-133">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9dd7f-133">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="9dd7f-134">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9dd7f-134">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


